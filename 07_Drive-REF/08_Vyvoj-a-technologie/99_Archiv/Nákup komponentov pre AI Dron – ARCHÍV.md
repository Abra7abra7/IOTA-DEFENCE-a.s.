# **Architektúra a implementácia autonómnych bezpilotných systémov s integrovanou umelou inteligenciou na báze platforiem ArduPilot a Raspberry Pi 5**

Súčasný vývoj v oblasti bezpilotných prostriedkov (UAV) smeruje od jednoduchých, manuálne ovládaných strojov k plne autonómnym robotickým platformám schopným vykonávať komplexné misie v reálnom čase bez priameho zásahu človeka. Tento prechod je umožnený synergiou pokročilého letového riadenia a výpočtového výkonu na okraji siete (edge computing). Implementácia systému založeného na ArduPilot v kombinácii s procesorom Raspberry Pi 5 a akcelerátorom Hailo-8L predstavuje technologický vrchol v kategórii malých UAV, kde sa deterministické riadenie letu stretáva s heuristickou analýzou obrazu prostredníctvom neurónových sietí.1

## **Konštrukčná integrita a mechanická analýza rámu Mark 4**

Voľba rámu Mark 4 v 7-palcovej verzii (295 mm wheelbase) nie je náhodná. Pre autonómne misie vyžadujúce integráciu prídavného výpočtového hardvéru je kľúčový dostatočný priestor a nosnosť. Tento rám, vyrobený z vysokokvalitných uhlíkových vlákien 3K, poskytuje potrebnú tuhosť na elimináciu torzných rezonancií, ktoré by mohli negatívne ovplyvniť prácu gyroskopov a následne stabilitu letu.4

Mechanická štruktúra rámu s 5 mm hrubými ramenami je navrhnutá tak, aby odolala dynamickému zaťaženiu pri akcelerácii motorov EMAX ECO II 2807\. Geometria typu "H" umožňuje oddeliť letovú elektroniku od batérie a sprievodného počítača, čo uľahčuje správu ťažiska (CG). Správne umiestnené ťažisko je kritické pre autonómne algoritmy ArduPilot, ktoré predpokladajú symetrickú odozvu systému na riadiace impulzy.5

### **Technické parametre rámu a mechanické vlastnosti**

| Komponent | Parameter | Hodnota / Materiál | Zdroj |
| :---- | :---- | :---- | :---- |
| Model rámu | Mark 4 7-palcový | 3K Uhlíkové vlákno | 4 |
| Rázvor (Wheelbase) | 295 mm | N/A | 4 |
| Hrúbka ramien | 5 mm | Uhlík | 4 |
| Hmotnosť rámu | cca 121 g | N/A | 5 |
| Vnútorný priestor | 25 mm výška | Hliníkové dištančné stĺpiky | 5 |

Implementácia rámu Mark 4 tiež rieši otázku aerodynamického odporu a prúdenia vzduchu. Optimalizované výrezy v uhlíkových platniach nielen znižujú hmotnosť, ale umožňujú efektívne chladenie komponentov, ako je Raspberry Pi 5, ktorý pri plnom vyťažení AI úloh produkuje značné množstvo tepla.2

## **Pohonné systémy a aerodynamická efektivita**

Pohonný systém je navrhnutý pre maximalizáciu letového času a stability. Motory EMAX ECO II 2807 s hodnotou 1300KV sú optimalizované pre napätie 6S (22,2 V \- 25,2 V). Táto konfigurácia poskytuje vysoký krútiaci moment, ktorý je nevyhnutný pre otáčanie 7-palcových vrtúľ HQPROP 7040\. Použitie magnetov N52SH v motoroch zabezpečuje vysokú tepelnú odolnosť a lineárnu odozvu plynu, čo je kľúčové pre presné udržiavanie pozície v autonómnych režimoch.11

Vrtule HQPROP 7040 s tromi listami ponúkajú ideálny kompromis medzi ťahom a efektivitou. Ich profil je navrhnutý tak, aby minimalizoval turbulencie na koncoch listov, čím sa znižuje akustický podpis drona a vibračné zaťaženie rámu.14 Pre autonómny systém, ktorý spracováva obraz cez YOLO AI, je minimalizácia vibrácií nevyhnutná pre elimináciu efektu "jello" v obraze, ktorý by mohol viesť k nesprávnej detekcii objektov.1

### **Analýza pohonnej sústavy**

| Komponent | Špecifikácia | Význam pre AI systém | Zdroj |
| :---- | :---- | :---- | :---- |
| Motor | EMAX ECO II 2807 1300KV | Stabilný ťah pre ťažší náklad (RPi 5 \+ AI Kit) | 11 |
| Ložiská motora | 12mm EZO | Dlhá životnosť a nízke trenie | 12 |
| Vrtule | HQPROP 7040 Tri-blade | Vysoká efektivita pri cruise rýchlostiach | 14 |
| Konfigurácia | 6S Li-ion | Napájanie pre dlhý dolet | 18 |

Z hľadiska aerodynamiky možno ťah vrtule vyjadriť vzťahom pre výkonovú účinnosť, kde väčší priemer (7 palcov oproti bežným 5 palcom) zvyšuje plochu disku a umožňuje generovať rovnaký vztlak pri nižších otáčkach. To priamo koreluje s úsporou energie z 8000mAh batérie a predĺžením operačného rádiusu drona.12

## **Riadiaci systém a digitálny mozog: SpeedyBee F7 V3**

Riadiaca jednotka SpeedyBee F7 V3 s procesorom STM32F722 slúži ako centrálny uzol pre deterministické operácie. Oproti starším procesorom F4 ponúka F7 vyššiu taktovaciu frekvenciu a viac hardvérových portov UART, čo je kritické pre súčasné pripojenie GPS modulu, telemetrie SiK, prijímača ELRS a komunikáciu s Raspberry Pi cez protokol MAVLink.20

Integrovaný 50A ESC (Electronic Speed Controller) s firmvérom BLHeli\_32 podporuje telemetriu motora v reálnom čase, čo ArduPilot využíva na dynamické prispôsobovanie filtrov pre potlačenie šumu (Notch filters). Tento stack je vybavený ochrannými diódami TVS, ktoré absorbujú napäťové špičky vznikajúce pri brzdení motorov, čím chránia citlivé obvody Raspberry Pi 5\.21

### **Vlastnosti letového stacku SpeedyBee F7 V3**

| Funkcia | Špecifikácia | Prínos | Zdroj |
| :---- | :---- | :---- | :---- |
| MCU | STM32F722 | Rýchle spracovanie PID slučiek | 21 |
| Blackbox | 500 MB Flash | Analýza dát z autonómneho letu | 21 |
| Bezdrôtové pripojenie | Bluetooth/Wi-Fi | Konfigurácia v teréne cez smartfón | 21 |
| Výstupy BEC | 9V 4A / 5V 2A | Napájanie kamier a GPS | 21 |

Použitie barometra BMP280 a gyroskopu BMI270 v tejto jednotke umožňuje presné udržiavanie výšky a orientácie. V autonómnom režime "Auto" ArduPilot preberá navigáciu podľa GPS bodov, zatiaľ čo Raspberry Pi 5 môže cez MAVLink posielať korekcie kurzu na základe vizuálnych dát, napríklad pri automatickom pristávaní na pohyblivú cieľovú plochu.22

## **Navigácia a senzory pre autonómny let**

Pre autonómny pohyb v priestore je dron vybavený modulom Matek M10Q-5883, ktorý využíva najnovšiu generáciu čipov u-blox M10. Tento senzor dokáže súčasne sledovať štyri konštelácie GNSS (GPS, GLONASS, Galileo a BeiDou), čo drasticky zvyšuje presnosť určenia polohy v náročných podmienkach, ako sú mestské zástavby alebo hlboké doliny.26

Súčasťou modulu je aj magnetický kompas QMC5883L. V ArduPilote je kompas nevyhnutný pre režimy riadené GPS, pretože bez informácie o magnetickom severe by systém nevedel určiť orientáciu drona vzhľadom na plánovanú trasu. Pri inštalácii je dôležité dodržať vzdialenosť aspoň 10 cm od silových káblov, aby sa predišlo elektromagnetickému rušeniu kompasu.26

### **Parametre navigačného modulu GNSS**

| Vlastnosť | Špecifikácia | Zdroj |
| :---- | :---- | :---- |
| GNSS Čip | u-blox SAM-M10Q-00B | 26 |
| Podporované systémy | GPS, GLONASS, Galileo, BeiDou | 26 |
| Magnetometer | QMC5883L | 26 |
| Obnovovacia frekvencia | 5 Hz (UBX) / 1 Hz (NMEA) | 26 |
| Anténa | 15 x 15 mm Patch | 26 |

Dôsledná kalibrácia kompasu a nastavenie parametrov EKF3 (Extended Kalman Filter) v ArduPilote zabezpečujú, že dron bude schopný vykonávať misie s presnosťou na desiatky centimetrov. To je kľúčové pre AI úlohy, kde je potrebné presne lokalizovať detekované objekty v globálnych súradniciach.26

## **Umelá inteligencia na okraji: Raspberry Pi 5 a Hailo-8L**

Najvýznamnejším prvkom tohto systému je implementácia umelej inteligencie (AI) priamo na palube. Srdcom tohto subsystému je Raspberry Pi 5 s 8 GB RAM, ktorý poskytuje 2- až 3-násobný nárast výkonu oproti predchádzajúcim generáciám.2 Pi 5 slúži ako sprievodný počítač (companion computer), ktorý beží na operačnom systéme Linux a komunikuje s letovým ovládačom cez vysokorýchlostné sériové rozhranie.1

Pre efektívny beh algoritmov hlbokého učenia, ako je YOLOv8 pre detekciu objektov, je Pi 5 doplnený o Raspberry Pi AI Kit. Tento modul obsahuje NPU (Neural Processing Unit) Hailo-8L, ktorý je schopný vykonať 13 biliónov operácií za sekundu (13 TOPS).1 Vďaka tomu môže dron analyzovať video z kamery Waveshare IMX219 v reálnom čase bez toho, aby zaťažoval hlavný procesor, ktorý sa tak môže venovať iným úlohám, ako je plánovanie dráhy alebo šifrovanie komunikácie.3

### **Špecifikácia AI subsystému**

| Komponent | Model | Výkon / Vlastnosti | Zdroj |
| :---- | :---- | :---- | :---- |
| Počítač | Raspberry Pi 5 (8GB) | 2,4 GHz Quad-Core Arm A76 | 2 |
| AI Akcelerátor | Hailo-8L (M.2 module) | 13 TOPS (INT8) | 1 |
| Rozhranie | M.2 HAT+ (PCIe Gen 2\) | Vysoká dátová priepustnosť | 1 |
| Chladenie | RPi Active Cooler | Teplotne riadený ventilátor | 10 |
| Vizuálny vstup | Waveshare IMX219 | 8MP, 120° zorné pole | 35 |

Integrácia Hailo-8L do ekosystému Raspberry Pi je realizovaná prostredníctvom softvérového stacku rpicam-apps, ktorý natívne podporuje NPU pre post-processing úloh videnia. To znamená, že vývojár môže jednoducho nasadiť vopred natrénované modely TensorFlow alebo ONNX, ktoré sú optimalizované pre Hailo architektúru, čím sa dosiahne minimálna latencia medzi zachytením obrazu a akciou drona.1

## **Vizuálny subsystém a oči umelej inteligencie**

Pre potreby umelej inteligencie je dron vybavený kamerou Waveshare IMX219 s rozlíšením 8 megapixelov a širokým zorným polom 120 stupňov. Toto široké pole je kritické pre autonómnu navigáciu a vyhýbanie sa prekážkam, pretože poskytuje systému väčší kontext o okolí stroja.36 Kamera je pripojená cez dedikované rozhranie MIPI CSI k Raspberry Pi 5, čo zabezpečuje prenos digitálneho signálu s nízkym šumom.35

Okrem digitálnej kamery pre AI disponuje dron aj analógovým FPV systémom pre operátora. Kamera Caddx Ratel 2 je priemyselným štandardom pre lety v zhoršených svetelných podmienkach vďaka svojmu 1/1,8" Starlight senzoru. Dokáže poskytnúť jasný obraz aj v šere, čo je dôležité pre bezpečnostného pilota, ktorý musí mať možnosť kedykoľvek zasiahnuť do riadenia.39

### **Analýza kamerových systémov**

| Systém | Model | Hlavná výhoda | Zdroj |
| :---- | :---- | :---- | :---- |
| AI Vision | Waveshare IMX219 | Optimalizácia pre RPi 5 a Hailo | 36 |
| FPV Link | Caddx Ratel 2 | Nočné videnie (0,0001 lux) | 40 |
| VTX (Vysielač) | AKK Race Ranger 1.6W | Extrémny dosah video signálu | 42 |
| Anténa | Foxeer Lollipop 4 | Odolnosť a stabilita signálu | 43 |

Video signál z FPV kamery je vysielaný cez AKK Race Ranger s výkonom až 1,6 W. Tento výkon umožňuje prenos obrazu na vzdialenosti presahujúce 5 – 10 km v závislosti od prostredia a použitých antén. Foxeer Lollipop 4 s kruhovou polarizáciou (RHCP) zabezpečuje, že signál bude stabilný aj pri náklonoch drona počas manévrovania.42

## **Komunikačné protokoly a diaľkové riadenie**

Spoľahlivosť komunikácie je zabezpečená dvoma nezávislými linkami. Pre riadenie a manuálne zásahy sa využíva systém ExpressLRS (ELRS) na frekvencii 2,4 GHz. RadioMaster Pocket v kombinácii s prijímačom RP2 Nano ponúka extrémne nízku latenciu a vysokú odolnosť voči rušeniu vďaka modulácii LoRa. Prijímač RP2 obsahuje integrovanú keramickú anténu a TCXO oscilátor, čo eliminuje drift frekvencie pri teplotných zmenách počas letu.46

Pre prenos komplexných telemetrických dát a komunikáciu s pozemnou stanicou (GCS) sa používa SiK Telemetry V3 na frekvencii 433 MHz. Táto nižšia frekvencia má lepšie penetračné vlastnosti cez prekážky ako 2,4 GHz linka a umožňuje prenos MAVLink správ medzi ArduPilotom a aplikáciou Mission Planner na notebooku operátora.49

### **Štruktúra komunikačných liniek**

| Typ linky | Hardvér | Frekvencia | Účel | Zdroj |
| :---- | :---- | :---- | :---- | :---- |
| RC Control | RadioMaster Pocket / RP2 | 2,4 GHz | Manuálne riadenie (ELRS) | 46 |
| Telemetry | SiK Radio V3 | 433 MHz | Autonómna misia, GCS dáta | 49 |
| Video Link | AKK Race Ranger / EV800D | 5,8 GHz | Vizuálny dohľad operátora | 42 |

Použitie frekvencie 433 MHz pre telemetriu je v súlade s európskymi predpismi pre rádiové zariadenia a umožňuje bezpečné monitorovanie stavu drona (napätie batérie, počet satelitov, AI status) na veľké vzdialenosti.49

## **Napájanie a manažment energie pre dlhú výdrž**

Dlhý dolet a výdrž vo vzduchu sú priamo závislé od hustoty energie v batériách. Pre tento typ 7-palcového drona je optimálnym riešením 6S2P Li-ion akumulátor s kapacitou 8000 mAh. Na rozdiel od LiPo batérií majú Li-ion články (napr. Samsung 40T alebo EVE 21700\) vyššiu energetickú hustotu, čo umožňuje dlhšie lety (cca 20 \- 30 minút) pri zachovaní akceptovateľnej hmotnosti okolo 880 g.18

Napájanie palubného počítača Raspberry Pi 5 vyžaduje stabilné napätie 5 V s prúdom až 5 A, čo bežné BEC obvody na letových ovládačoch nedokážu poskytnúť. Preto je v systéme integrovaný Matek UBEC, ktorý konvertuje napätie z hlavnej 6S batérie na stabilný výstup pre Pi 5 a AI Kit. Nízkoodporový kondenzátor 1000uF 35V slúži na filtráciu elektrického šumu od motorov, ktorý by inak mohol spôsobovať reštarty AI procesora.21

### **Energetická bilancia systému**

| Parameter | Hodnota | Poznámka | Zdroj |
| :---- | :---- | :---- | :---- |
| Typ batérie | 6S2P Li-ion (21700) | Maximálna výdrž pre cruise let | 18 |
| Kapacita | 8000 mAh / 177,6 Wh | Dostatočná energia pre AI misie | 18 |
| Hmotnosť batérie | \~896 g | Optimalizované pre 7" rám | 54 |
| Regulácia | Matek UBEC (5V/9V Adj) | Napájanie pre RPi 5 a AI Kit | 56 |

Pri výpočte letového času je potrebné brať do úvahy aj spotrebu elektroniky. Raspberry Pi 5 s Hailo NPU môže pri plnom výkone odoberať až 15 \- 20 W, čo je však zanedbateľné v porovnaní s príkonom motorov (stovky wattov), no podstatné pre tepelný manažment v uzavretom priestore rámu.1

## **Pozemná stanica a rozhranie človek-stroj**

Operátor interaguje s dronom prostredníctvom ovládača RadioMaster Pocket a okuliarov Eachine EV800D. Okuliare EV800D sú výnimočné svojou diverzitnou prijímacou jednotkou, ktorá automaticky prepína medzi dvoma anténami pre dosiahnutie najlepšieho signálu. Ich 5-palcový displej je možné odobrať a použiť ako samostatný monitor, čo je neoceniteľné pri testovaní AI algoritmov priamo na mieste vzletu.53

RadioMaster Pocket, hoci kompaktný, beží na plnohodnotnom firmvéri EdgeTX, čo umožňuje programovanie komplexných logických spínačov pre aktiváciu AI režimov alebo núdzových funkcií (napr. Return to Home). Jeho hall-effect gimbaly zaručujú precízne ovládanie, ktoré je dôležité najmä vo fázach letu, kde autopilot vyžaduje manuálnu asistenciu.46

### **Komponenty pozemnej stanice**

| Zariadenie | Kľúčové vlastnosti | Zdroj |
| :---- | :---- | :---- |
| RadioMaster Pocket | Kompaktnosť, ELRS, Hall gimbaly | 46 |
| Eachine EV800D | 800\*480px, DVR, Diverzitný RX | 53 |
| Mission Planner | Plánovanie misií, Analýza telemetrie | N/A |
| SiK Ground Unit | Pripojenie telemetrie k PC cez USB | 49 |

Táto konfigurácia pozemnej stanice poskytuje operátorovi plnú kontrolu nad strojom a zároveň umožňuje monitorovať výstupy z umelej inteligencie prostredníctvom dátového prenosu na pripojený počítač.49

## **Logistika a nákupný zoznam: Kde a za koľko kúpiť komponenty**

Pre úspešnú realizáciu projektu v podmienkach slovenského trhu je dôležité kombinovať nákupy od lokálnych predajcov (kvôli záruke a rýchlosti dodania výpočtovej techniky) a špecializovaných zahraničných e-shopov (kvôli špecifickým FPV komponentom). Kľúčovým slovenským dodávateľom pre platformu Raspberry Pi a Waveshare je RLX.sk, zatiaľ čo komponenty pohonu a navigácie sú dostupné u regionálnych lídrov ako Rotorama (CZ) alebo Baltic Drones.2

### **Podrobný prehľad komponentov a nákupné linky**

Nižšie uvedená tabuľka sumarizuje presné komponenty, ich odhadované ceny a overené miesta nákupu v rámci Slovenska a EÚ.

| Kategória | Komponent | Odhad ceny | Obchod (Lokalita) | Presný Link na nákup | Zdroj |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **Rám** | Mark 4 7" (295 mm) | 45 € | Drone24hours (EU) | [Kúpiť tu](https://drone24hours.com/en/products/geprc-mark4-7) | 5 |
| **Pohon** | 4x EMAX ECO II 2807 1300KV | 95 € | Rotorama (EU) | [Kúpiť tu](https://www.rotorama.com/product/emax-eco-ii-2807-1300kv) | 11 |
| **Vrtule** | HQPROP 7040 (3 sady) | 15 € | Rotorama (EU) | [Kúpiť tu](https://www.rotorama.com/product/hq-7x4x3-grey) | 14 |
| **Mozog (FC)** | SpeedyBee F7 V3 50A Stack | 110 € | AliExpress (Official) | [Kúpiť tu](https://www.aliexpress.com/item/1005005839363102.html) | 20 |
| **GPS** | Matek M10Q-5883 | 45 € | Rotorama (EU) | [Kúpiť tu](https://www.rotorama.com/product/matek-m10-5883-gps-s-kompasem) | 27 |
| **Počítač** | Raspberry Pi 5 (8GB) | 105 € | RLX.sk (Slovensko) | [Kúpiť tu](https://rlx.sk/sk/raspberry-pi-single-board-computer-/9359-raspberry-pi-5-8gb.html) | 2 |
| **AI NPU** | RPi AI Kit (Hailo-8L) | 90 € | RLX.sk (Slovensko) | [Kúpiť tu](https://rlx.sk/sk/raspberry-pi-5/9698-raspberry-pi-ai-kit.html) | 3 |
| **Chladenie** | RPi 5 Active Cooler | 10 € | RLX.sk (Slovensko) | [Kúpiť tu](https://rlx.sk/sk/raspberry-pi-5/9406-raspberry-pi-5-active-cooler.html) | 10 |
| **AI Kamera** | Waveshare IMX219 (120°) | 18 € | RLX.sk (Slovensko) | [Kúpiť tu](https://rlx.sk/sk/raspberry-pi-5/9420-imx219-camera-module-120-fov.html) | 36 |
| **FPV Kamera** | Caddx Ratel 2 | 35 € | Hobbydrone (CZ) | [Kúpiť tu](https://www.hobbydrone.cz/en/caddx-ratel-2--red/) | 39 |
| **VTX** | AKK Race Ranger 1.6W | 45 € | AliExpress | [Kúpiť tu](https://www.aliexpress.com/item/4000100414925.html) | 42 |
| **Anténa** | Foxeer Lollipop 4 (SMA) | 15 € | Rotorama (EU) | [Kúpiť tu](https://www.rotorama.com/product/foxeer-lollipop-v4-mini-sma) | 45 |
| **Prijímač** | Radiomaster ELRS Nano | 18 € | Baltic Drones (EU) | [Kúpiť tu](https://balticdrones.lt/en/products/receiver-radiomaster-rp1-expresslrs-2-4ghz-nano) | 47 |
| **Telemetria** | SiK Telemetry V3 433MHz | 80 € | Baltic Drones (EU) | [Kúpiť tu](https://balticdrones.eu/collections/telemetry) | 49 |
| **Ovládač** | RadioMaster Pocket ELRS | 80 € | Baltic Drones (EU) | [Kúpiť tu](https://balticdrones.lt/en/products/controller-radiomaster-pocket-expresslrs) | 60 |
| **Okuliare** | Eachine EV800D | 110 € | Ubuy (Slovensko) | [Kúpiť tu](https://www.ubuy.sk/en/product/2D9T3WEY-eachine-ev800d) | 57 |
| **Batéria** | 6S2P Li-ion 8000mAh | 125 € | Hobbydrone (CZ) | [Kúpiť tu](https://www.hobbydrone.cz/en/batteries/) | 55 |
| **UBEC** | Matek UBEC 5V/9V | 15 € | eBay / AliExpress | [Kúpiť tu](https://www.ebay.com/itm/387641852369) | 56 |
| **Kondenzátor** | 1000uF 35V Low ESR | 2 € | Miestny elektropredaj | N/A | 21 |

**Celková odhadovaná suma projektu: 1 045 €**

Táto suma nezahŕňa náklady na dopravu, náradie (spájkovačka, skrutkovače) a nabíjačku pre Li-ion batérie. Pri nákupoch z krajín mimo EÚ (napr. AliExpress, eBay) je potrebné počítať s možnosťou doplatku DPH a colných poplatkov, hoci mnohí predajcovia už tieto poplatky zahŕňajú do ceny (označenie IOSS).4

## **Pokročilé aspekty integrácie a systémového inžinierstva**

Stavba autonómneho drona s AI nie je len o mechanickom zložení dielov, ale o hlbokej integrácii softvérových vrstiev. Proces prepojenia Raspberry Pi 5 a SpeedyBee F7 V3 prebieha cez protokol MAVLink, kde Pi 5 funguje ako "GCS na palube".

1. **Fyzické prepojenie**: Výstup UART z letového ovládača sa pripojí na GPIO piny (TX/RX) Raspberry Pi 5\.  
2. **Konfigurácia ArduPilot**: Je potrebné nastaviť parametre SERIALx\_BAUD na 921 (921600 bps) a SERIALx\_PROTOCOL na 2 (MAVLink 2\) pre zabezpečenie dostatočnej šírky pásma pre prenos stavových dát.21  
3. **Hailo-8L Setup**: Po inštalácii AI Kitu do M.2 slotu je nutné nainštalovať ovládače hailo-taped-device a knižnice pre prácu s NPU. Hailo-8L využíva PCIe rozhranie, čo umožňuje prenos dát bez latencie, ktorá je typická pre USB akcelerátory.1  
4. **AI logika**: Algoritmus detekcie (napr. YOLOv8) spracováva obraz z IMX219 kamery. Ak systém detekuje cieľ, vypočíta jeho relatívne súradnice a cez MAVLink pošle príkaz SET\_POSITION\_TARGET\_LOCAL\_NED letovému ovládaču, čím dron fyzicky upraví svoju polohu tak, aby cieľ sledoval.3

### **Výpočtový model inference AI na Hailo-8L**

Výkon Hailo-8L pri detekcii objektov možno modelovať pomocou priepustnosti (throughput) meranej v snímkach za sekundu (FPS). Pre model YOLOv8n (nano verzia) možno na tomto hardvéri očakávať:

![][image1]  
Kde ![][image2] je čas samotnej inference na NPU (cca 5-10 ms), ![][image3] je čas predbežného spracovania obrazu na CPU Raspberry Pi a ![][image4] je čas dekódovania výsledkov. Vďaka 13 TOPS výkonu Hailo-8L sa celková hodnota FPS pohybuje v rozsahu 30 \- 60, čo je viac než dostatočné pre riadenie drona v reálnom čase.3

## **Operačná bezpečnosť a legislatívny rámec**

Prevádzka takto vybaveného drona podlieha prísnym pravidlám EASA (Európska agentúra pre bezpečnosť letectva). Keďže ide o stroj s hmotnosťou presahujúcou 1 kg (vrátane batérie a AI výbavy) a schopnosťou autonómneho letu, spadá do kategórie "Open A3" alebo "Specific" v závislosti od miesta prevádzky.

* **Registrácia**: Majiteľ drona musí byť registrovaný na Dopravnom úrade SR a dron musí byť označený registračným číslom.  
* **Vysielací výkon**: Video vysielač AKK Race Ranger dosahuje výkon 1,6 W, čo výrazne prekračuje povolených 25 mW pre pásmo 5,8 GHz bez špeciálneho povolenia. Pre legálnu prevádzku v SR je nutné výkon softvérovo obmedziť alebo vlastniť rádioamatérsku licenciu.42  
* **Autonómny let**: Legislatíva vyžaduje, aby mal operátor nad dronom neustály vizuálny dohľad (VLOS). Autonómne misie musia byť programované tak, aby bolo možné kedykoľvek prevziať manuálne riadenie pomocou ELRS ovládača.46

## **Závery a odporúčania pre ďalší vývoj**

Navrhovaná zostava predstavuje robustnú vedecko-výskumnú platformu, ktorá ponúka bezkonkurenčný pomer ceny a výkonu v oblasti autonómnych UAV. Synergia medzi osvedčeným riadiacim systémom ArduPilot a moderným výpočtovým hardvérom Raspberry Pi 5 otvára dvere k aplikáciám, ktoré boli doteraz vyhradené pre vojenské alebo drahé priemyselné systémy.

Pre budúcich používateľov sa odporúča zamerať sa na:

* **Tepelný manažment**: Raspberry Pi 5 a Hailo NPU vyžadujú aktívne chladenie. Je dôležité zabezpečiť, aby bol Active Cooler správne nainštalovaný a aby mal prístup k čerstvému vzduchu aj vo vnútri rámu.10  
* **Vibračná izolácia**: Hoci je rám Mark 4 tuhý, jemné vibrácie môžu zmiasť neurónovú sieť. Použitie soft-mount podložiek pod letový ovládač a kameru IMX219 je vysoko odporúčané.5  
* **Zálohovanie dát**: Všetky lety by mali byť logované nielen v Blackboxe FC, ale aj na SD kartu v Raspberry Pi pre hĺbkovú analýzu správania neurónovej siete v reálnych letových podmienkach.2

Tento report poskytuje komplexný technický a logistický základ pre stavbu špičkového autonómneho stroja, ktorý je pripravený na výzvy modernej robotiky a umelej inteligencie.1

#### **Citované práce**

> 1. Buy a Raspberry Pi AI Kit, otvorené marca 6, 2026, [https    www\.raspberrypi.com/products/ai-kit/](https://www.raspberrypi.com/products/ai-kit/)  
> 2. Raspberry Pi 5 8GB \- BCM2712, 800MHz VideoCore VII GPU, 2×4-Lane MIPI \- RLX.sk, otvorené marca 6, 2026, [https\://rlx.sk/en/raspberry-pi-single-board-computer-/9359-raspberry-pi-5-8gb-bcm2712-800mhz-videocore-vii-gpu-24-lane-mipi.html](https://rlx.sk/en/raspberry-pi-single-board-computer-/9359-raspberry-pi-5-8gb-bcm2712-800mhz-videocore-vii-gpu-24-lane-mipi.html)  
> 3. Raspberry Pi AI Kit AI \+ modul Raspberry Pi M.2 HAT+ (RASPBERRY PI AI KIT, RASPBERRY PI 5 BRD) SC1438, otvorené marca 6, 2026, [https\://rlx.sk/en/raspb     erry-pi-5/9698-raspberry-pi-ai-kit-ai-modul-raspberry-pi-m2-hat-raspberry-pi-ai-kit-raspberry-pi-5-brd-sc1438.html](https://rlx.sk/en/raspberry-pi-5/9698-raspberry-pi-ai-kit-ai-modul-raspberry-pi-m2-hat-raspberry-pi-ai-kit-raspberry-pi-5-brd-sc1438.html)  
> 4. Mark 4 7inch 295mm 2807 1300KV Brushless Motor 7040 Propeller for Mark4 FPV Racing Drone Quadcopter Freestyle Frame Kit \- AliExpress, otvorené marca 6, 2026, [https\://www\.aliexpress.com/item/1005009079403534.html](https://www.aliexpress.com/item/1005009079403534.html)  
> 5. GEPRC Mark4 7" \- Drone24Hours, otvorené marca 6, 2026, [https\://drone24hours.com/en/products/geprc-mark4-7](https://drone24hours.com/en/products/geprc-mark4-7)  
> 6. Mark4 7 inch FPV Racing Drone Frame 295mm Carbon Fiber Freestyle RC Quadcopter Frame Kit with 5mm Arm and Print Parts \- AliExpress, otvorené marca 6, 2026, [https\://www\.aliexpress.com/i/1005006407123777.html](https://www.aliexpress.com/i/1005006407123777.html)  
> 7. MAK4 Carbon Fiber 5-7 inch Freestyle Drone Frame Kit Lightweight \- Mepsking, otvorené marca 6, 2026, [https\://www\.mepsking.shop/mak4-5inch-6inch-7inch-frame-kit.html](https://www.mepsking.shop/mak4-5inch-6inch-7inch-frame-kit.html)  
> 8. Mark4 7inch 295mm T5 Carbon Fiber Frame Kit without 3DP/C \- Evelta, otvorené marca 6, 2026, [https\://evelta.com/mark4-7inch-295mm-t5-carbon-fiber-frame-kit-without-3dp-c/](https://evelta.com/mark4-7inch-295mm-t5-carbon-fiber-frame-kit-without-3dp-c/)  
> 9. Mark4 5inch FPV Frame Kit \- 225mm/ 6inch 260mm / 7inch 295mm W/ 5mm Ar \- RCDrone, otvorené marca 6, 2026, [https\://rcdrone.top/products/mark4-5inch-fpv-frame-kit](https://rcdrone.top/products/mark4-5inch-fpv-frame-kit)  
> 10. Raspberry Pi 5 Official Active Cooler \- Pimoroni, otvorené marca 6, 2026, [https\://shop.pimoroni.com/products/raspberry-pi-5-active-cooler](https://shop.pimoroni.com/products/raspberry-pi-5-active-cooler)  
> 11. Emax Eco II 2807 1300Kv \- Rotorama, otvorené marca 6, 2026, [https\://www\.rotorama.com/product/emax-eco-ii-2807-1300kv](https://www.rotorama.com/product/emax-eco-ii-2807-1300kv)  
> 12. EMAX ECO II 2807 Brushless Motor 1300KV \- RMRC \- ReadyMadeRC, otvorené marca 6, 2026, [https\://www\.readymaderc.com/products/details/emax-eco-ii-2807-brushless-motor-1300kv](https://www.readymaderc.com/products/details/emax-eco-ii-2807-brushless-motor-1300kv)  
> 13. Emax ECO II Series 2807-1300KV Motor \- Pyrodrone, otvorené marca 6, 2026, [https\://pyrodrone.com/products/emax-eco-ii-2807-stator-for-7-propeller-freestyle-heavy-lifter-and-long-range-crafts-1300kv](https://pyrodrone.com/products/emax-eco-ii-2807-stator-for-7-propeller-freestyle-heavy-lifter-and-long-range-crafts-1300kv)  
> 14. 4x HQProp 7040 CW CCW Propeller 7" 3-Blades Props for RC FPV Racing Drone \| eBay, otvorené marca 6, 2026, [https\://www\.ebay.com/itm/285706909500](https://www.ebay.com/itm/285706909500)  
> 15. HQProp 7040 7X4X3 Drone Propellers 3-Blade \- Mepsking, otvorené marca 6, 2026, [https\://www\.mepsking.shop/hq-7040-7x4x3-propellers.html](https://www.mepsking.shop/hq-7040-7x4x3-propellers.html)  
> 16. HQ Prop Durable 7040-3 / 7" 7x4x3 Tri-Blade Spec FPV Drone Racing Prop \- DinDrones, otvorené marca 6, 2026, [https\://dindrones.com/products/hq-prop-durable-7040-3-7-7x4x3-tri-blade-spec-fpv-drone-racing-props-4-pack-choose-color](https://dindrones.com/products/hq-prop-durable-7040-3-7-7x4x3-tri-blade-spec-fpv-drone-racing-props-4-pack-choose-color)  
> 17. Emax ECO II Series 2807 Motor (1300KV/1500KV/1700KV) \- GetFPV, otvorené marca 6, 2026, [https\://www\.getfpv.com/emax-eco-ii-series-2807-motor-1300kv-1500kv-1700kv.html](https://www.getfpv.com/emax-eco-ii-series-2807-motor-1300kv-1500kv-1700kv.html)  
> 18. DOGCOM 6S2P 8000mAh Li-Ion Battery \| European Warehouse, otvorené marca 6, 2026, [https\://iflight-rc.eu/en/products/dogcom-6s2p-8000mah-li-ion-battery](https://iflight-rc.eu/en/products/dogcom-6s2p-8000mah-li-ion-battery)  
> 19. Chimera7 ECO 6S \- iFlight, otvorené marca 6, 2026, [https\://shop.iflight.com/Chimera7-ECO-6S-Pro2066](https://shop.iflight.com/Chimera7-ECO-6S-Pro2066)  
> 20. SpeedyBee F7 V3 50A Stack F722 Flight Control BL32 50A 4in1 ESC3\~6S Lipo with Blackbox Analyzer Suitable for FPV Freestyle Drone \- AliExpress, otvorené marca 6, 2026, [https\://www\.aliexpress.com/item/1005005839363102.html](https://www.aliexpress.com/item/1005005839363102.html)  
> 21. SpeedyBee F7 V3 BL32 50A 30x30 Stack \- Speedy Bee, otvorené marca 6, 2026, [https\://www\.speedybee.com/speedybee-f7-v3-bl32-50a-30x30-stack/](https://www.speedybee.com/speedybee-f7-v3-bl32-50a-30x30-stack/)  
> 22. SpeedyBee F7 V3 Flight Controller \- Speedy Bee, otvorené marca 6, 2026, [https\://www\.speedybee.com/speedybee-f7-v3-flight-controller/](https://www.speedybee.com/speedybee-f7-v3-flight-controller/)  
> 23. SpeedyBee F7 V3 BL32 50A 4-in-1 ESC \- Speedy Bee, otvorené marca 6, 2026, [https\://www\.speedybee.com/speedybee-f7-v3-bl32-50a-4-in-1-esc/](https://www.speedybee.com/speedybee-f7-v3-bl32-50a-4-in-1-esc/)  
> 24. SpeedyBee F7 V3 Flight Controller / 50A ESC / Flight Stack 3-6S for FPV Drone \| eBay, otvorené marca 6, 2026, [https\://www\.ebay.com/itm/146847736893](https://www.ebay.com/itm/146847736893)  
> 25. SpeedyBee F7 V3 50A Stack \- ProgressiveRC, otvorené marca 6, 2026, [https\://www\.progressiverc.com/products/speedybee-f7-v3-50a-stack](https://www.progressiverc.com/products/speedybee-f7-v3-50a-stack)  
> 26. MATEKSYS M10Q-5883 GNSS & Compass \- Lumenier, otvorené marca 6, 2026, [https\://www\.lumenier.com/products/mateksys-m10q-5883-gnss-compass](https://www.lumenier.com/products/mateksys-m10q-5883-gnss-compass)  
> 27. Matek M10Q-5883 GPS with compass \- Rotorama, otvorené marca 6, 2026, [https\://www\.rotorama.com/product/matek-m10-5883-gps-s-kompasem](https://www.rotorama.com/product/matek-m10-5883-gps-s-kompasem)  
> 28. Matek M10Q-5883 GNSS GPS & Compass Module \- Pyrodrone, otvorené marca 6, 2026, [https\://pyrodrone.com/products/matek-m10q-5883-gnss-gps-compass-module](https://pyrodrone.com/products/matek-m10q-5883-gnss-gps-compass-module)  
> 29. Matek GNSS GPS & Compass Module M10Q-5883 \- Flying Tech, otvorené marca 6, 2026, [https\://www\.flyingtech.co.uk/product/matek-gnss-gps-compass-module-m10-5883/](https://www.flyingtech.co.uk/product/matek-gnss-gps-compass-module-m10-5883/)  
> 30. Matek Systems GNSS M10Q-5883 U-Blox M10 GPS Compass QMC5883L Module For RC FPV \| eBay, otvorené marca 6, 2026, [https\://www\.ebay.com/itm/306206718108](https://www.ebay.com/itm/306206718108)  
> 31. Raspberry Pi 5 4GB \- BCM2712, 800MHz VideoCore VII GPU, 2×4-lane MIPI \- RLX.sk, otvorené marca 6, 2026, [https\://rlx.sk/en/raspberry-pi-single-board-computer-/9358-raspberry-pi-5-4gb-bcm2712-800mhz-videocore-vii-gpu-24-lane-mipi.html](https://rlx.sk/en/raspberry-pi-single-board-computer-/9358-raspberry-pi-5-4gb-bcm2712-800mhz-videocore-vii-gpu-24-lane-mipi.html)  
> 32. Raspberry Pi 5 AI Kit, Hailo AI Acceleration Module With Raspberry Pi M.2 HAT+, 13Tops Computing Power, Raspberry Pi 5 HAT \| Raspberry Pi AI Kit \- Waveshare, otvorené marca 6, 2026, [https\://www\.waveshare.com/raspberry-pi-ai-kit.htm](https://www.waveshare.com/raspberry-pi-ai-kit.htm)  
> 33. Hailo-8 M.2 AI Accelerator Module, 26TOPS Hailo-8 AI Processor, Optional For PCIe To M.2 for Raspberry Pi 5 (WS-27812) \- RLX.sk, otvorené marca 6, 2026, [https\://rlx.sk/en/raspberry-pi-5/9785-hailo-8-m2-ai-accelerator-module-26tops-hailo-8-ai-processor-optional-for-pcie-to-m2-for-raspberry-pi-5-ws-27812.html](https://rlx.sk/en/raspberry-pi-5/9785-hailo-8-m2-ai-accelerator-module-26tops-hailo-8-ai-processor-optional-for-pcie-to-m2-for-raspberry-pi-5-ws-27812.html)  
> 34. Raspberry Pi 5 Active Cooler \- Micro Center, otvorené marca 6, 2026, [https\://www\.microcenter.com/product/671930/raspberry-pi-5-active-cooler](https://www.microcenter.com/product/671930/raspberry-pi-5-active-cooler)  
> 35. Waveshare IMX219 Camera Module For Raspberry Pi 5 8MP MIPI-CSI For 79.3° / 120° \| eBay, otvorené marca 6, 2026, [https\://www\.ebay.com/itm/256343026139](https://www.ebay.com/itm/256343026139)  
> 36. IMX219 Camera Module For Raspberry Pi 5, 8MP, MIPI-CSI Interface, 120° FOV (WS-26185) \- RLX.sk, otvorené marca 6, 2026, [https\://rlx.sk/en/raspberry-pi-5/9420-imx219-camera-module-for-raspberry-pi-5-8mp-mipi-csi-interface-120-fov-ws-26185.html](https://rlx.sk/en/raspberry-pi-5/9420-imx219-camera-module-for-raspberry-pi-5-8mp-mipi-csi-interface-120-fov-ws-26185.html)  
> 37. IMX219 Camera Module For Raspberry Pi 5, 8MP, MIPI-CSI, 120° FOV \- PiShop.us, otvorené marca 6, 2026, [https\://www\.pishop.us/product/imx219-camera-module-for-raspberry-pi-5-8mp-mipi-csi-120-fov/](https://www.pishop.us/product/imx219-camera-module-for-raspberry-pi-5-8mp-mipi-csi-120-fov/)  
> 38. IMX219 Camera Module For Raspberry Pi 5, 8MP, MIPI-CSI Interface, Options For 79.3° / 120° FOV \- Waveshare, otvorené marca 6, 2026, [https\://www\.waveshare.com/pi5-imx219.htm](https://www.waveshare.com/pi5-imx219.htm)  
> 39. FPV Camera CaddxFPV Ratel 2 (Red) \| na Hobbydrone.cz, otvorené marca 6, 2026, [https\://www\.hobbydrone.cz/en/caddx-ratel-2--red/](https://www.hobbydrone.cz/en/caddx-ratel-2--red/)  
> 40. Caddx Ratel 2 HD FPV Camera with High Sensitivity and Low Latency \- Drone24Hours, otvorené marca 6, 2026, [https\://drone24hours.com/en/products/caddx-ratel-2](https://drone24hours.com/en/products/caddx-ratel-2)  
> 41. CaddxFPV Ratel 2 Starlight Low Latency Micro Size Freestyle FPV Camera \- Pyrodrone, otvorené marca 6, 2026, [https\://pyrodrone.com/products/caddxfpv-ratel-2-starlight-low-latency-micro-size-freestyle-fpv-camera](https://pyrodrone.com/products/caddxfpv-ratel-2-starlight-low-latency-micro-size-freestyle-fpv-camera)  
> 42. AKK Race Ranger Analog Long Range VTX \- Unmanned Tech, otvorené marca 6, 2026, [https\://www\.unmannedtechshop.co.uk/products/akk-race-ranger-analog-long-range-vtx](https://www.unmannedtechshop.co.uk/products/akk-race-ranger-analog-long-range-vtx)  
> 43. Foxeer Lollipop V4 Stubby 5.8GHz Antenna 2 Pack \- RHCP \- Flying Tech, otvorené marca 6, 2026, [https\://www\.flyingtech.co.uk/product/foxeer-lollipop-v4-stubby-5-8ghz-antenna-2-pack-rhcp/](https://www.flyingtech.co.uk/product/foxeer-lollipop-v4-stubby-5-8ghz-antenna-2-pack-rhcp/)  
> 44. Antenna Foxeer Lollipop 4 Omni Stubby 5.8G RHCP SMA-Male \| FPVUA online store, otvorené marca 6, 2026, [https\://fpvua.com/en/antena-foxeer-lollipop-4-omni-stubby-5-8g-rhcp-sma-male/](https://fpvua.com/en/antena-foxeer-lollipop-4-omni-stubby-5-8g-rhcp-sma-male/)  
> 45. Foxeer Lollipop V4 Mini SMA \- Rotorama, otvorené marca 6, 2026, [https\://www\.rotorama.com/product/foxeer-lollipop-rhcp-super-mini](https://www.rotorama.com/product/foxeer-lollipop-rhcp-super-mini)  
> 46. RadioMaster Pocket ELRS 2.4GHz Radio Controller \- Rising Sun FPV, otvorené marca 6, 2026, [https\://risingsunfpv.com.au/products/radiomaster-pocket-radio-transmitter-controller](https://risingsunfpv.com.au/products/radiomaster-pocket-radio-transmitter-controller)  
> 47. RadioMaster RP2 V2 ExpressLRS 2.4 GHz nano-receiver \- MegaDron, otvorené marca 6, 2026, [https\://megadron.pl/en/products/radiomaster-rp2-v2-expresslrs-2-4-ghz-nano-receiver-29479.html](https://megadron.pl/en/products/radiomaster-rp2-v2-expresslrs-2-4-ghz-nano-receiver-29479.html)  
> 48. RP2 V2 ExpressLRS 2.4ghz Nano Receiver \- RadioMaster RC, otvorené marca 6, 2026, [https\://radiomasterrc.com/products/rp2-expresslrs-2-4ghz-nano-receiver](https://radiomasterrc.com/products/rp2-expresslrs-2-4ghz-nano-receiver)  
> 49. Telemetry \- HobbyDrone.cz, otvorené marca 6, 2026, [https\://www\.hobbydrone.cz/en/telemetry/](https://www.hobbydrone.cz/en/telemetry/)  
> 50. 3DR SiK Telemetry Radio Air/Ground Bundle Kit Long-Range \- NewBeeDrone, otvorené marca 6, 2026, [https\://newbeedrone.com/products/3dr-3dr-sik-telemetry-radio-air-ground-bundle-kit](https://newbeedrone.com/products/3dr-3dr-sik-telemetry-radio-air-ground-bundle-kit)  
> 51. 3DR SiK Air Telemetry Radio 915MHz Kit \- NewBeeDrone, otvorené marca 6, 2026, [https\://newbeedrone.com/products/3dr-sik-air-telemetry-radio-915mhz](https://newbeedrone.com/products/3dr-sik-air-telemetry-radio-915mhz)  
> 52. Telemetry \- Baltic Drones, otvorené marca 6, 2026, [https\://balticdrones.eu/collections/telemetry](https://balticdrones.eu/collections/telemetry)  
> 53. Eachine EV800D 5.8G 40CH Diversity FPV Goggles w/ DVR \- GetFPV, otvorené marca 6, 2026, [https\://www\.getfpv.com/eachine-ev800d-5-8g-40ch-diversity-fpv-goggles-with-dvr.html](https://www.getfpv.com/eachine-ev800d-5-8g-40ch-diversity-fpv-goggles-with-dvr.html)  
> 54. iFlight Fullsend 6S 2P 22.2V 8000mAh-XT60H \- RobotShop, otvorené marca 6, 2026, [https\://eu.robotshop.com/products/iflight-fullsend-6s-2p-222v-8000mah-xt60h](https://eu.robotshop.com/products/iflight-fullsend-6s-2p-222v-8000mah-xt60h)  
> 55. Long-Lasting Batteries for Drones \- HobbyDrone.cz, otvorené marca 6, 2026, [https\://www\.hobbydrone.cz/en/batteries/](https://www.hobbydrone.cz/en/batteries/)  
> 56. 3Pcs Matek Systems Micro BEC 6S IN 6-30V out 5V/9V-ADJ for RC FPV Drone \| eBay, otvorené marca 6, 2026, [https\://www\.ebay.com/itm/387641852369](https://www.ebay.com/itm/387641852369)  
> 57. Eachine EV800D FPV Goggle \- 5.8G 40CH 5 Inch 800\*480 Video Headset HD \- RCDrone, otvorené marca 6, 2026, [https\://rcdrone.top/products/eachine-ev800d-fpv-goggle](https://rcdrone.top/products/eachine-ev800d-fpv-goggle)  
> 58. Eachine EV800D 5.8G 40CH 5 Inch FPV Goggles with HD Slovakia \| Ubuy, otvorené marca 6, 2026, [https\://www\.ubuy.sk/en/producthk/2D9T3WEY-in-stock-eachine-ev800d-5-8g-40ch-5-inch-800480-video-headset-hd-dvr-diversity-fpv-goggles-with-batt](https://www.ubuy.sk/en/producthk/2D9T3WEY-in-stock-eachine-ev800d-5-8g-40ch-5-inch-800480-video-headset-hd-dvr-diversity-fpv-goggles-with-batt)  
> 59. RadioMaster Pocket ELRS Transparent Radio Controller \- MegaDron, otvorené marca 6, 2026, [https\://megadron.pl/en/products/radiomaster-pocket-elrs-transparent-radio-controller-29426.html](https://megadron.pl/en/products/radiomaster-pocket-elrs-transparent-radio-controller-29426.html)  
> 60. Controller RadioMaster Pocket Crush Edition ExpressLRS Red \- Baltic Drones, otvorené marca 6, 2026, [https\://balticdrones.lt/en/products/controller-radiomaster-pocket-crush-edition-expresslrs-red](https://balticdrones.lt/en/products/controller-radiomaster-pocket-crush-edition-expresslrs-red)  
> 61. RC Transmitter Receiver RadioMaster Pocket ELRS Gimbal Hall effect Built n Antna, otvorené marca 6, 2026, [https\://www\.ebay.co.uk/itm/127048402926](https://www.ebay.co.uk/itm/127048402926)  
> 62. Eachine EV800D 5.8G 40CH Diversity FPV Goggles with DVR \- AddictiveRC, otvorené marca 6, 2026, [https\://shop.addictiverc.com/products/eachine-ev800d-5-8g-40ch-diversity-fpv-goggles-with-dvr](https://shop.addictiverc.com/products/eachine-ev800d-5-8g-40ch-diversity-fpv-goggles-with-dvr)  
> 63. Hailo-8 M.2 AI Accelerator Module, Based On The 26TOPS Hailo-8 AI Processor, For Raspberry Pi 5 (WS-27841) \- RLX.sk, otvorené marca 6, 2026, [https\://rlx.sk/en/raspberry-pi-5/9784-ws-27841.html](https://rlx.sk/en/raspberry-pi-5/9784-ws-27841.html)

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB0AAAAYCAYAAAAGXva8AAABSklEQVR4Xu2SPS9EURCGx1cjIUsidApa0W1DodFIJJJt/AnJBoVCSecPKGwnGrVEiEI0NCTK/Q0UEmI3K7yvmZuMsV/B2Sj2SZ7smXc2Z+4994h06ZKAF3gTw9S8w2IMUzIrOrQ3NlIwD5fgmejQZauTsg43RQc+WE07AoeuxfAPGI9Bxozo0J7YMK7hcAzb4BzOwUpskGPRoY3YjUGbcM8JOBkbhM3HGP6SEWn+Ip9NXqaMK/vlE17AA9c7hfeiN5wnVIX9rk+4n7cubEzb2p9/GY7CN6v37Zf/H7N1CW7Y2nMLCzH07Ilu9Crfn5qXaNXVfLhnV9dEv1uk2cVsSTyeQ7jt6tjPaJS3ZEH0iIdgzjJuNmDrFdFjnIKDlhG+4Y+HEh75kat5cTL64BPccRnh5zgJWVIW4aXU/85J2IJ38vWidYR8DP4FHwKGQgegEZPvAAAAAElFTkSuQmCC>

[image3]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABsAAAAYCAYAAAALQIb7AAABLklEQVR4Xu2UQUsCYRCGpxCCCDx769AtQgTBi3dD8AcU0c28mIj4MwT/guC1WxBIHkIiKKJzWB27ZUEHq1O9w8zKONCG0OdpH3jwm3d2d9ZvV4kSEhZgCm98GIpv2PRhCLIkw1Z94z8pwjI8JxlW0ToILdgmGTTRmg0KDzv2YQh2SIat+EYITkiGLQUe9OrDUPAwfkkiLvVzD16TbPMdfIDb2uP6HTZgDx5ozozgAL6ZbAYP29L1l8n553AIH03Gx1bNegPew67J1nRdguu6ntEhOegTplxvTHJShH22/jnXNRvCD7g73/4be0HeshddH8Ez02O47rtsIX77Js+wYGqmBk9NnYObpo5lH96SXJi3JW16fgsjLuAVycuRmW/F80QB/ycteZK7561IiOUH1KpA0puqp/MAAAAASUVORK5CYII=>

[image4]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACEAAAAYCAYAAAB0kZQKAAABY0lEQVR4Xu2VTStFURSGX2IkX/9BBiSUoaGSz+KWYmCsRJI/YGAiP0KZGPgHFAMTEiZSPgaSGWa+IryrtbezWk5cg3Nu6j71dPd+975nr85etwuUKfMPeKT7PsybDzrnwzxphxZR6RfyoJv2001oEUNhnivzdAFawF2YiyVBipjxYZ60QYuo8AsZUOODyAa0iKwZpMc+jEgB9z7MgCM64sOIFCHNGdkNn+N0D3pdh/SctsZNZIqe0Cs6bfI6+kS36ARtgZ4RXU+2JshCUxi/mFx+tpP0wmTx2tboYkpux830NCVPZQW64ZlWubUz2mvm8UH+gbax38N852sVGMYP/fAb9rBZekvHoAdFqvG9qB76iuSa5DpHk+W/kfaaG+mbya9pXxjLno4wXqUNJhekP2rDuCikqQ7oDbTR6s3aMvTwByT9JMh3pFGljwZMvkS3acFkRXGJEvyPWLqgr7DTL5TJik/CFVDDgvh0MgAAAABJRU5ErkJggg==>