**Technická analýza a implementácia autonómneho bezpilotného systému na platforme GEPRC Mark4-8 so sprievodným počítačom Raspberry Pi 5 a riadiacim stackom PX4**  
**Systémová architektúra a technologický základ osempalcovej platformy**  
Návrh a konštrukcia moderného bezpilotného prostriedku (UAV) určeného na autonómne misie vyžaduje hĺbkovú integráciu mechanických, elektronických a softvérových subsystémov. Výber komponentov pre túto konkrétnu zostavu reflektuje prechod od klasických pretekárskych FPV dronov k pokročilým robotickým systémom. Základom celého stroja je rám GEPRC Mark4-8, ktorý je v komunite dronov uznávaný pre svoju odolnosť a optimalizovanú geometriu pre dlhé ramená.\[1, 2\] Použitie osempalcových vrtúľ HQprop LR8X4.2X3 v kombinácii s motormi iFlight XING2 2809 s hodnotou 1250Kv naznačuje zameranie na vysokú efektivitu pri stredne ťažkom zaťažení a schopnosť stabilného letu v náročnejších poveternostných podmienkach.\[3\]  
Elektronické jadro systému pozostáva zo stacku Skystars H7 Dual Gyro a regulátora AM60. Flight controller (FC) postavený na procesore STM32H743 disponuje frekvenciou 480*MHz*, čo poskytuje dostatočný výpočtový výkon pre beh real-time operačného systému NuttX, na ktorom je založený stack PX4.\[4, 5\] Unikátnou vlastnosťou tohto FC je implementácia dvoch gyroskopov BMI270, ktoré sú voči sebe fyzicky pootočené o 90 stupňov. Táto konfigurácia umožňuje algoritmu Extended Kalman Filter (EKF2) v PX4 efektívnejšie potláčať vibračné šumy, čo je pri osempalcových ramenách náchylných na nízkofrekvenčné oscilácie kritické.\[4, 5, 6\]  
Doplnenie systému o sprievodný počítač Raspberry Pi 5 (8GB RAM) transformuje platformu na autonómny uzol schopný spracovávať úlohy počítačového videnia a AI v reálnom čase.\[7, 8\] Komunikácia medzi Raspberry Pi a Skystars H7 prebieha prostredníctvom protokolu MAVLink cez vysokorýchlostné sériové rozhranie (UART), čo umožňuje off-board riadenie a pokročilé plánovanie misií.\[9, 10\]  
**Technická špecifikácia hlavných komponentov**  
V nasledujúcej tabuľke sú zhrnuté kľúčové technické parametre pohonného a riadiaceho systému, ktoré priamo ovplyvňujú letovú dynamiku a energetickú náročnosť.

| Komponent | Parameter | Hodnota / Typ |
| ----- | ----- | ----- |
| Rám | Materiál | Karbónové vlákna (T700) |
| Motory | Staton / Kv | 2809 / 1250Kv \[3\] |
| ESC | Firmware | AM32 (32-bit ARM) \[5, 11\] |
| FC MCU | Procesor | STM32H743VIT6 (480*MHz*) \[4\] |
| IMU | Senzory | 2x BMI270 (Dual Gyro) \[4\] |
| Napájanie | Batéria | 6S LiPo (22.2*V* nominálne) \[5\] |
| Kapacita | Batéria | 5500*mAh* 70C |
| AI Počítač | CPU / RAM | Broadcom BCM2712 / 8GB LPDDR4X |

**Mechanická montáž a štrukturálna optimalizácia rámu**  
Proces fyzickej stavby začína zostavením rámu GEPRC Mark4-8. Pri osempalcovej verzii je nevyhnutné venovať zvýšenú pozornosť tuhosti ramien. Akékoľvek mikropohyby v mieste uchytenia ramien k stredovým platniam môžu generovať mechanický hluk, ktorý zmätie gyroskopy a spôsobí prehrievanie motorov v dôsledku nadmernej korekcie PID regulátora.\[12, 13\]  
**Inštalácia pohonnej sústavy**  
Motory iFlight XING2 2809 sa montujú na konce ramien pomocou M3 skrutiek s použitím stredne pevného zaisťovača závitov (KAVAN). Pri osempalcových motoroch je dôležité dbať na to, aby skrutky nezasahovali do vinutia statora, čo by pri napätí 6S viedlo k okamžitému zničeniu elektroniky.\[12\] Káble od motorov by mali byť chránené pred ostrými hranami karbónu buď plastovými chráničmi, alebo dostatočnou vrstvou textilnej pásky.  
Pre efektívny manažment vibrácií sa odporúča namontovať riadiacu jednotku na silikónové silentbloky (grommets), ktoré sú súčasťou balenia Skystars H7.\[5, 14\] Celý stack (ESC \+ FC) musí byť umiestnený v ťažisku stroja, aby sa minimalizovala asymetria v momente zotrvačnosti, čo zjednodušuje prácu algoritmov PX4 pre kontrolu polohy.\[12, 13\]  
**Strategické umiestnenie periférií**  
GPS modul FlyfishRC M10QMC-5883L obsahuje nielen prijímač satelitného signálu, ale aj citlivý magnetometer (kompas).\[15, 16\] Ten musí byť umiestnený na vyvýšenom stĺpiku, čo najďalej od vysokoprúdových káblov a motorov, ktoré počas letu generujú silné elektromagnetické polia schopné vychýliť meranie svetových strán.\[7, 15\] Anténa Foxeer Lollipop 4 Plus pre video prenos by mala byť vyvedená v zadnej časti rámu pod uhlom, ktorý zabezpečí optimálne vyžarovanie aj pri náklone drona počas dopredného letu.\[17\]  
**Elektrotechnická integrácia a manažment energie**  
Napájanie osempalcového drona s AI počítačom vyžaduje robustnú elektrickú architektúru. Hlavná batéria 6S (22.2*V* \- 25.2*V*) napája priamo regulátor motorov (ESC), zatiaľ čo ostatné komponenty vyžadujú regulované napätie.\[4, 5\]  
**Implementácia Skystars AM60 a filtrácia šumu**  
Regulátor Skystars AM60 využíva moderný firmware AM32, ktorý poskytuje plynulejšiu odozvu na plyn a podporuje telemetriu motorov cez dedikovaný UART.\[5, 11, 18\] Na hlavné napájacie pady ESC musí byť pripájkaný kondenzátor 1000uF 50V. Jeho úlohou je absorbovať napäťové špičky vznikajúce pri regeneratívnom brzdení motorov, čím chráni nielen ESC, ale aj citlivú 3.3V logiku na riadiacej jednotke a Raspberry Pi.\[5, 19\]  
Pri spájkovaní hlavného XT60 konektora je nutné použiť kábel 18AWG (alebo hrubší), aby sa minimalizoval odpor a tepelné straty pri prúdoch, ktoré môžu v špičkách presiahnuť 100A.\[5\] Všetky spoje musia byť realizované vysokokvalitným cínom s tavidlom pri teplote spájkovačky približne 350  
∘  
*C* až 400  
∘  
*C*, aby sa zabezpečil dokonalý "wetting" na veľkých medených plochách.\[19\]  
**Napájací subsystém pre Raspberry Pi 5**  
Raspberry Pi 5 má v porovnaní s predchodcami výrazne vyššie nároky na stabilitu a prúdovú kapacitu zdroja. Oficiálne špecifikácie uvádzajú potrebu 5V 5A (25W) pre plnohodnotnú prevádzku bez obmedzovania výkonu periférií.\[20, 21\] V tejto zostave sa používa externý BEC 2-13S 5V 5A, ktorý sa pripája priamo na Vbat (napätie batérie) na vstupných padoch ESC.\[8, 22\]  
Výstup z BECu je vedený do USB-C pigtail kábla, ktorý sa pripája k Raspberry Pi 5\. Je dôležité si uvedomiť, že Pi 5 pri detekcii zdroja, ktorý nedokáže komunikovať cez Power Delivery (PD) protokol, môže štandardne obmedziť prúd pre USB porty na 600*mA*.\[21, 22\] Toto obmedzenie je možné v operačnom systéme obísť zápisom parametra `usb_max_current_enable=1` do súboru `config.txt`, čím sa zabezpečí dostatok energie pre pripojenú RPi Cameru 3 a prípadné ďalšie senzory.\[22\]  
**Komplexná kabeláž a mapovanie UART rozhraní**  
Riadiaca jednotka Skystars H7 disponuje ôsmimi UART portami, čo umožňuje paralelné pripojenie telemetrie, GPS, prijímača, video vysielača a sprievodného počítača.\[4, 23\] Pre stack PX4 je odporúčané nasledujúce mapovanie:

| Port | Periféria | Protokol | Poznámka |
| ----- | ----- | ----- | ----- |
| UART1 (R1/T1) | Radiomaster XR1 | CRSF | RC control a telemetria \[4, 24\] |
| UART2 (R2/T2) | Raspberry Pi 5 | MAVLink | Companion computer link \[9, 25\] |
| UART3 (R3) | ESC Telemetry | DShot/AM32 | Sledovanie otáčok a teploty ESC \[4, 23\] |
| UART4 (R4/T4) | FlyfishRC GPS | GNSS | Navigačné dáta \[4, 15\] |
| UART6 (T6) | Smurfs VTX | IRC Tramp | Ovládanie výkonu a kanálu VTX \[17, 23\] |
| I2C (SDA/SCL) | FlyfishRC Compass | I2C | Orientácia voči mag. pólu \[4, 15\] |

**Zapojenie ELRS prijímača a GPS**  
Prijímač Radiomaster XR1 Nano vyžaduje obojsmerné prepojenie. TX prijímača ide na RX1 (R1) flight controllera a RX prijímača na TX1 (T1). Napájanie prijímača sa realizuje z 4.5V alebo 5V padu, ktorý je pod napätím aj pri napájaní FC iba cez USB, čo uľahčuje konfiguráciu na stole bez batérie.\[24, 26\]  
GPS modul vyžaduje štyri káble pre základnú funkciu a dva ďalšie pre kompas. Pri zapojení I2C zbernice (SDA a SCL) nesmie dôjsť k zámene káblov, inak PX4 nahlási chybu `Compass not found`.\[4, 15\] FlyfishRC M10QMC využíva protokol u-blox, ktorý PX4 automaticky rozpozná po nastavení príslušného UART portu.\[15, 27\]  
**Integrácia Raspberry Pi 5 a konfigurácia MAVLink**  
Kľúčovým prvkom tejto zostavy je prepojenie medzi Skystars H7 a Raspberry Pi 5\. Raspberry Pi funguje ako "Companion Computer", ktorý spracováva dáta z kamery a posiela príkazy do flight controllera cez MAVLink.\[7, 28\]  
**Hardvérové prepojenie UART**  
Komunikácia prebieha cez GPIO piny na Raspberry Pi a UART2 port na FC.

* **RPi GPIO 14 (TX, Pin 8\)** sa pripojí na **R2 (UART2 RX)** na FC.  
* **RPi GPIO 15 (RX, Pin 10\)** sa pripojí na **T2 (UART2 TX)** na FC.  
* **RPi GND (Pin 6\)** sa musí prepojiť s **GND** na FC pre zabezpečenie spoločnej signálovej zeme.\[9, 25\]

Je dôležité si uvedomiť, že logika Skystars H7 pracuje s napätím 3.3*V*, čo je plne kompatibilné s Raspberry Pi, takže nie je potrebný prevodník úrovní.\[10\] Vzdialenosť medzi FC a RPi by mala byť čo najmenšia, aby sa predišlo elektromagnetickému rušeniu na sériovej linke, prípadne je vhodné použiť tienené káble.  
**Softvérová príprava Raspberry Pi (Linux)**  
Na oficiálnu 64GB SD kartu sa nainštaluje najnovší Raspberry Pi OS (vydanie Bookworm). Prvým krokom po inštalácii je vypnutie sériovej konzoly, ktorá štandardne beží na UART pinoch a blokovala by dáta z MAVLinku.\[25\]  
V termináli Raspberry Pi sa vykonajú tieto kroky:

1. Otvorenie konfiguračného nástroja: `sudo raspi-config`.  
2. Prechod do `Interface Options` \-\> `Serial Port`.  
3. Na otázku "Would you like a login shell to be accessible over serial?" odpovedzte **No**.  
4. Na otázku "Would you like the serial port hardware to be enabled?" odpovedzte **Yes**.  
5. Reštartujte systém príkazom `sudo reboot`.\[25\]

Následne je potrebné nainštalovať `mavlink-router` alebo `MAVProxy`, ktoré slúžia na distribúciu správ medzi fyzickým sériovým portom a UDP portami, cez ktoré môžu k dronu pristupovať ďalšie aplikácie (napr. Python skripty využívajúce MAVSDK alebo ROS 2).\[25, 29, 30\]  
**Konfigurácia softvéru PX4 cez QGroundControl**  
Používanie stacku PX4 na "racing-style" doskách ako Skystars H7 vyžaduje špecifický prístup k nahrávaniu firmware a konfigurácii parametrov.  
**Nahrávanie Firmware**  
Na počítači so systémom Windows sa spustí QGroundControl. Po pripojení Skystars H7 cez USB-C v záložke `Firmware` vyberieme inštaláciu PX4.\[31, 32\] Keďže Skystars H7 je postavená na architektúre Kakute H7 alebo FMUv6x, QGC by mal automaticky ponúknuť správny cieľ. Ak nie, je možné nahrať vlastný súbor `px4_fmu-v6x_default.px4`.\[6, 14\] Po úspešnom nahratí je nevyhnutný reštart jednotky.  
**Výber Airframe a základná kalibrácia**  
V menu `Airframe` je potrebné vybrať kategóriu `Generic Quadcopter` a následne model, ktorý najviac zodpovedá osempalcovej platforme, napríklad `Holybro S500` alebo `Generic 250 Racer`, a manuálne ho upraviť.\[32, 33\] Tento krok nastaví predvolené PID hodnoty a konfiguráciu motorových výstupov.  
Kalibrácia senzorov v QGC prebieha nasledovne:

1. **Akcelerometer:** Dron sa postupne umiestňuje do šiestich polôh (hore, dole, boky, predok, zadok). Je nutné, aby bol dron počas merania v každej polohe absolútne nehybný.\[12, 34\]  
2. **Kompas:** Vyžaduje rotáciu drona vo všetkých osiach. Prítomnosť Raspberry Pi a kovových skrutiek v blízkosti GPS modulu môže kalibráciu sťažiť, preto sa odporúča vykonávať ju v otvorenom priestore.\[7, 12\]  
3. **Radio:** Nastavenie rozsahov kanálov pre RadioMaster Pocket. ELRS prijímač musí byť vopred spárovaný s vysielačom pomocou binding phrase alebo tlačidla.\[24, 27\]

**Nastavenie aktuátorov a zhadzovací systém (Servo MG90S)**  
V moderných verziách PX4 (1.14 a novšie) sa konfigurácia motorov a serv vykonáva v záložke `Actuators`.\[35\]

* Motory 1-4 sa priradia k príslušným PWM výstupom podľa schémy Quad X.  
* Servo MG90S pre zhadzovací systém sa pripojí na voľný PWM výstup (napr. M5 alebo M6).\[4, 36\]  
* V záložke `Actuators` sa výstupu pre servo priradí funkcia `Generic Actuator 1`. Frekvencia tohto výstupu musí byť nastavená na 50*Hz* (štandard pre analógové servá), zatiaľ čo motory môžu bežať na 400*Hz* alebo v protokole DShot.\[35\]  
* Pomocou posuvníkov v QGC sa overia krajné polohy serva, ktoré zabezpečia otvorenie a zatvorenie mechanizmu.

**Dynamika letu a ladenie PID regulátora pre 8-palcové vrtule**  
Ladenie osempalcového drona je zásadne odlišné od ladenia malých pretekárskych kvadrokoptér. Väčšie vrtule majú vyšší moment zotrvačnosti, čo znamená, že motory iFlight 2809 potrebujú viac času na zmenu otáčok.\[37, 38\]  
**Teória PID v kontexte PX4**  
PX4 využíva kaskádový systém regulácie:

1. **Rate Controller:** Najrýchlejšia slučka, ktorá koriguje uhlovú rýchlosť (deg/*s*).  
2. **Attitude Controller:** Riadi uhol náklonu drona.  
3. **Velocity/Position Controller:** Najpomalšia slučka využívajúca GPS a barometer pre udržanie polohy.\[13, 39\]

Pre osempalcovú platformu sú predvolené hodnoty `P` (proportional) zvyčajne príliš vysoké, čo môže spôsobiť agresívne oscilácie hneď po štarte.\[37\] Odporúča sa znížiť `MC_ROLLRATE_P` a `MC_PITCHRATE_P` o 20-30% pred prvým letom a následne ich postupne zvyšovať.\[13, 40\]  
**Implementácia funkcie Autotune**  
PX4 disponuje pokročilým algoritmom pre automatické ladenie. Postup je nasledovný:

1. Vzlietnite v režime `Altitude` alebo `Position` do výšky minimálne 5 metrov.  
2. V QGroundControl v menu `PID Tuning` povoľte `Autotune`.\[41\]  
3. Aktivujte proces. Dron začne vykonávať rýchle impulzy v osiach roll, pitch a yaw. Počas tohto procesu dron analyzuje odozvu a ukladá optimálne hodnoty `P`, `I` a `D`.\[41\]  
4. Po dokončení (cca 40-60 sekúnd) pristaňte a potvrďte uloženie parametrov.

Pri ladení je dôležité sledovať teplotu motorov. Ak sú motory po krátkom lete horúce na dotyk, hodnota `D` (derivative) je príliš vysoká a zosilňuje vysokofrekvenčný šum z motorov, čo vedie k energetickým stratám.\[13, 40\]  
**Pokročilé funkcie AI a počítačového videnia**  
S procesorom Raspberry Pi 5 a kamerou RPi Camera 3 sa dron stáva autonómnym robotom. Spracovanie obrazu prebieha lokálne na Pi, ktoré následne posiela príkazy do PX4.\[7, 8\]  
**Inštalácia RPi Camera 3 a aktívneho chladenia**  
Kamera sa pripája k RPi 5 pomocou MIPI kábla (verzia pre Pi 5 má iný konektor ako predchádzajúce modely). Vzhľadom na vysoký tepelný výkon Broadcom procesora je inštalácia Raspberry Pi 5 Active Cooler nevyhnutná.\[20\] Bez adekvátneho chladenia dôjde k poklesu frekvencie procesora (thermal throttling), čo spôsobí lagy v AI spracovaní a môže viesť k nestabilite autonómnej misie.\[20, 21\]  
**Príklady využitia Companion Computer**

1. **Precision Landing:** Pomocou knižnice OpenCV a detekcie ArUco markerov môže Raspberry Pi naviesť drona na presné miesto pristátia s odchýlkou len niekoľkých centimetrov.\[8\]  
2. **Obstacle Avoidance:** Hoci táto zostava nemá hĺbkovú kameru, Pi 5 dokáže pomocou monokulárneho videnia a AI modelov (napr. TensorFlow Lite) identifikovať prekážky ako stromy alebo budovy a vyslať príkaz na zastavenie alebo obletenie prekážky cez MAVLink správu `OBSTACLE_DISTANCE`.\[8\]  
3. **Zhadzovací systém riadený AI:** Raspberry Pi môže automaticky aktivovať servo MG90S, keď kamera rozpozná špecifický cieľ, čím sa eliminuje potreba manuálneho ovládania operátorom.\[7, 42\]

**Prevádzková bezpečnosť a predletové protokoly**  
Prevádzka osempalcového drona s celkovou hmotnosťou presahujúcou 1 kg (v závislosti od nákladu) nesie so sebou značné riziká. PX4 poskytuje rozsiahle mechanizmy pre zabezpečenie letu.\[27\]  
**Konfigurácia Failsafe mechanizmov**  
V QGroundControl je nevyhnutné nastaviť správanie drona pri kritických situáciách:

* **RC Loss:** Ak dron stratí signál z RadioMaster Pocket, PX4 by mal byť nastavený na `Return mode` (návrat na miesto vzletu) alebo `Land`.\[27\]  
* **Battery Failsafe:** Pri poklese napätia pod 21.0*V* (pre 6S) by mal dron upozorniť pilota, a pri kritickej hodnote (20.4*V*) automaticky pristáť.\[27\]  
* **MAVLink Timeout:** Ak prestane komunikovať Raspberry Pi, flight controller môže byť nastavený tak, aby prešiel do bezpečného manuálneho režimu alebo aktivoval RTL, čím sa zabráni "odleteniu" drona v dôsledku chyby v AI kóde.\[10\]

**Kontrola pred štartom (Pre-flight checklist)**

1. Overenie pevnosti všetkých M3 a M2 skrutiek na ráme GEPRC Mark4-8.  
2. Kontrola integrity vrtúľ HQprop a smeru ich rotácie (CW/CCW).  
3. Overenie sily signálu ELRS a kvality analógového videa v Skyzone Cobra X okuliaroch.  
4. Kontrola GPS fixu (minimálne 10 satelitov pre bezpečný autonómny let).\[15, 27\]  
5. Overenie funkčnosti Active Cooler na Raspberry Pi.

**Integrácia pozemnej stanice a telemetrie**  
Ovládanie drona zo zeme zabezpečuje RadioMaster Pocket v kombinácii s Windows notebookom bežiacim QGroundControl.  
**RadioMaster Pocket a ExpressLRS**  
Vysielač RadioMaster Pocket s modulom ELRS 2.4GHz poskytuje extrémne stabilné spojenie aj v zarušenom prostredí. Vďaka telemetrii prenášanej cez ELRS môže pilot priamo na displeji ovládača sledovať napätie batérie a GPS súradnice, čo je kľúčové v prípade núdzového pristátia v teréne.\[26, 43, 44\]  
**Analógový video prenos**  
Okuliare Skyzone Cobra X V4 so vstavaným prijímačom SteadyView kombinujú signál z dvoch antén Foxeer Lollipop, čím minimalizujú výpadky obrazu (tzv. static) pri lete za prekážkami. Hoci je systém analógový, nízka latencia je neoceniteľná pri manuálnych korekciách letu v blízkosti prekážok, kde by digitálny prenos mohol mať nepredvídateľné oneskorenie.\[17, 45\]  
**Energetická bilancia a letový čas**  
Pri kapacite batérie 5500*mAh* a konfigurácii motorov 2809 možno očakávať letové časy v rozmedzí 15 až 25 minút, v závislosti od agresivity letu a hmotnosti nákladu. Raspberry Pi 5 so svojím odberom približne 2−3*A* pri 5V predstavuje len zlomok celkového odberu (približne 15*W* oproti stovkám wattov odoberaných motormi), avšak jeho vplyv na vybíjanie batérie pri dlhom čakaní na zemi nie je zanedbateľný.\[20, 21\]  
Je dôležité kalibrovať prúdový senzor na Skystars H7 v QGroundControl, aby údaje o spotrebovanej kapacite (*mAh*) zodpovedali realite. Presné nastavenie parametra `BATT_AMP_PERVLT` umožní PX4 presne odhadnúť zostávajúci čas letu a včas aktivovať návrat domov.\[4, 23\]  
**Záverečné technické zhodnotenie systému**  
Kombinácia rámu GEPRC Mark4-8, výkonnej riadiacej jednotky Skystars H7 a sprievodného počítača Raspberry Pi 5 vytvára vysoko kompetentnú platformu pre modernú robotiku. Úspešná implementácia vyžaduje nielen precíznu mechanickú prácu a spájkovanie, ale aj hlboké porozumenie softvérovým stackom PX4 a Linuxu.  
Vďaka využitiu open-source riešení (PX4, MAVLink, AM32) je tento systém plne rozšíriteľný. Budúci vývoj môže zahŕňať pridanie RTK GPS pre centimetrovú presnosť polohovania alebo integráciu LIDAR senzorov pre pokročilé mapovanie terénu. Pre profesionálne využitie v rámci Windows ekosystému poskytuje QGroundControl najstabilnejšie prostredie pre správu misií a detailnú diagnostiku celého UAV systému. Pri dodržaní všetkých technických postupov a bezpečnostných protokolov predstavuje táto zostava spoľahlivý nástroj pre autonómny prieskum a transportné úlohy.  
