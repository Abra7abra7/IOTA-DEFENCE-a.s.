Stavba drona s umelou inteligenciou, ktorý kombinuje FPV komponenty (ako Skystars H7) s Raspberry Pi a systémom PX4, je fantastický a ambiciózny projekt. Vyžaduje si to však trpezlivosť a presnosť.

Keďže používaš **PX4 a QGroundControl (QGC)** na klasickom FPV "stacku" (riadiaca jednotka \+ ESC), postup sa mierne líši od bežných FPV stavieb s Betaflightom. Tu je presný krok-za-krokom postup a zoznam vecí, na ktoré si dať najväčší pozor.

---

### **🛠️ Fáza 1: Mechanická stavba a príprava rámu**

1. **Príprava karbónu:** Hrany karbónového rámu (GEPRC Mark4-8) je dobré jemne prebehnúť pilníkom pod tečúcou vodou a zaliať sekundovým lepidlom. Zabráni to štiepeniu pri náraze a chráni káble pred predratím.  
2. **Zloženie rámu:** Zlož rám podľa manuálu. Skrutky, ktoré spájajú ramená so spodným plátom, zatiahnite pevne.  
3. **Montáž motorov:** Pripevni motory (iFlight XING2) na konce ramien.  
   * ⚠️ **NA ČO SI DAŤ POZOR:** Použi **zaisťovač závitov (KAVAN)** na skrutky motorov\! Kvapni malú kvapku na závit. Pred dotiahnutím sa **vizuálne uisti, že skrutka zospodu nedotýka vinutia (medených drôtikov) vo vnútri motora.** Ak by sa dotkla, motor by po zapnutí okamžite zhorel.

### **⚡ Fáza 2: Spájkovanie a napájanie (Power System)**

Tvoja spájkovačka Sequre a cín s tavidlom (Flux) budú tvoji najlepší priatelia. Pri 6S napájaní pretekajú systémom obrovské prúdy, takže spoje musia byť dokonalé.

1. **Príprava ESC:** Na kontakty pre batériu na ESC (elektronický regulátor otáčok) nanes dostatok cínu.  
2. **Napájací kábel a Kondenzátor:** Pripoj hlavný XT60 kábel (použi hrubý červený a čierny 18AWG, ideálne ešte hrubší ak bol k ESC) k ESC. **Nezabudni pripájať kondenzátor (1000uF 50V)** priamo na tieto plôšky (dlhšia nožička je \+, kratšia s pásikom je \-). Chráni elektroniku pred napäťovými špičkami.  
3. **Motory k ESC:** Skráť káble z motorov na potrebnú dĺžku a prispájkuj ich na 3 plôšky na ESC pre každý motor. Na poradí káblov nezáleží (smer otáčania neskôr nastavíme v softvéri).  
   * ⚠️ **NA ČO SI DAŤ POZOR:** Zamedz vzniku "studených spojov" (matný, hrboľatý cín). Spoj musí byť lesklý a cín musí byť dobre rozliaty po plôške aj kábli. Používaj veľa tavidla (Flux)\!

### **🧠 Fáza 3: Elektronika a Periférie**

Teraz namontuješ riadiacu jednotku (FC \- Skystars H7) nad ESC pomocou gumených dištančných stĺpikov. Prepoj ich priloženým konektorom.

1. **Prijímač (ELRS):** Prispájkuj na voľný UART port na FC (5V, GND, TX na RX, RX na TX).  
2. **GPS a Kompas:** Pripoj na ďalší UART (GPS) a I2C zbernicu (Kompas \- SCL, SDA).  
   * ⚠️ **NA ČO SI DAŤ POZOR:** GPS modul má na sebe šípku. Musí smerovať **presne dopredu** v smere letu drona a nemalo by nad ním byť nič kovové alebo karbónové.  
3. **Video (VTX a Kamera):** Zapoj Caddx Ratel kameru a Axisflying VTX podľa schémy tvojej FC. VTX potrebuje dobré chladenie, umiestni ho dozadu. Nezapínaj ho bez naskrutkovanej antény\!

### **🤖 Fáza 4: Integrácia Raspberry Pi (AI Počítač)**

1. **Napájanie RPi:** K hlavným napájacím plôškam na ESC prispájkuj káble vedúce do **BEC modulu**. BEC nastav/zapoj tak, aby dával presne 5V (ideálne 5.1V). Výstup z BECu pôjde cez tvoj USB-C pigtail priamo do Raspberry Pi.  
2. **Komunikácia (MAVLink):** Prepoj Raspberry Pi (GPIO piny pre UART) s voľným UART portom na riadiacej jednotke (FC). Cez toto spojenie bude prúdiť telemetria a príkazy medzi RPi a PX4.

### **💻 Fáza 5: Softvér \- PX4 a QGroundControl**

*💡 Dôležitá poznámka k realite: FC Skystars H7 je primárne navrhnutá pre Betaflight/INAV. Podpora pre PX4 na FPV doskách existuje, ale môžeš naraziť na nutnosť kompilovať vlastný "target" (firmvér), ak doska nie je priamo podporovaná v QGC. Predpokladajme, že máš správny firmvér.*

1. **Flashovanie PX4:** Pripoj riadiacu jednotku cez USB do PC. Otvor QGroundControl. Choď do *Vehicle Setup (ikona ozubeného kolesa) \-\> Firmware*. Nahraj PX4 Pro.  
2. **Výber Airframu:** V záložke *Airframe* vyber **Generic 4" \- 8" Quadcopter**. Dron sa reštartuje.  
3. **Kalibrácia Senzorov:** Choď do záložky *Sensors*. Postupne podľa obrázkov na obrazovke skalibruj Kompas (budeš musieť dronom točiť do všetkých strán), Akcelerometer a Gyroskop. Dron musí byť pri tom na rovnej ploche.  
4. **Nastavenie Rádia:** Zapni ovládač (RadioMaster Pocket). V záložke *Radio* ho skalibruj (hýb páčkami do extrémov). Priraď prepínače pre letové režimy (odporúčam: *Position*, *Altitude*, *Return to Launch*) a samostatný prepínač na *Arm/Disarm* (odblokovanie motorov).  
5. **Napájanie (Power):** Nastav parametre batérie: 6S (počet článkov), kapacita 5500mAh.

### **🛡️ Fáza 6: Oživenie a prvá skúška (Smoketest)**

1. **Ochrana proti skratu:** Kým zapojíš batériu, **VŽDY pripoj VIFLY ShortSaver\!** Ak je niekde na doske skrat, ShortSaver okamžite odpojí prúd a zachráni ti elektroniku za stovky eur. Ak zasvieti na zeleno, si v bezpečí.  
2. **Smer otáčania motorov:** **VRTULE SÚ ZATIAĽ ZLOŽENÉ\!** V QGC choď do záložky *Motors*. Roztoč každý motor na minimum a prstom skontroluj smer otáčania. Musia sa točiť podľa schémy v QGC (zvyčajne "In" \- predné dozadu/dovnútra, zadné dopredu/dovnútra). Ak sa nejaký točí naopak, prepoj sa do AM32 konfigurátora a zmeň jeho smer tam.

### **🚀 Zhrnutie najkritickejších chýb, ktorým sa vyhnúť:**

* **Nikdy nemaj nasadené vrtule, keď dron nastavuješ cez USB na stole.**  
* **Nikdy nezapájaj batériu prvýkrát bez ShortSaveru.**  
* **Nikdy nezapínaj dron (ani na stole), ak na VTX (video vysielači) nie je namontovaná anténa. VTX sa do pár sekúnd upečie a zničí.**  
* **Skrutky v motoroch nesmú byť príliš dlhé.**

Máš už ujasnené, ako prepojíš Raspberry Pi a riadiacu jednotku (aké konkrétne piny použiješ pre MAVLink komunikáciu)? Ak chceš, môžeme sa v ďalšom kroku zamerať čisto na toto prepojenie a nastavenie portov v PX4\!

