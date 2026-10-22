Podľa knihy je na zostrojenie plne funkčného autonómneho FPV dronu s umelou inteligenciou potrebné zaobstarať špecifický zoznam komponentov. Rozdelil som ich do logických kategórií spolu s vysvetlením ich účelu:

### 1\. Základné komponenty drona (Hardvér a pohon)

* **Karbónový rám (Mark 4 7" \- 295 mm):** Slúži ako základná kostra drona, ktorá drží všetky komponenty pohromade. Odporúča sa originálny rám od Readytosky pre jeho odolnosť a dobré rozloženie váhy 1\. Bude tiež potrebné dokúpiť alebo na 3D tlačiarni vytlačiť držiaky pre antény 2\.  
* **Motory EMAX ECO II 2807 6S 1300KV (4 kusy):** Zabezpečujú samotný pohyb a ťah drona. Tento model ponúka skvelý pomer výkonu a efektivity pre 7-palcové rámy a dokáže plynule fungovať na 6S batériách 3\.  
* **Vrtule HQPROP 7040 (7x4x3):** Sú to 7-palcové trojlistové vrtule so 4-palcovým stúpaním. Poskytujú silný ťah a výbornú odozvu, čo je ideálne pre dynamické lety, pričom je dôležité dbať na to, aby do seba a do iných komponentov nenarážali 4\.  
* **Riadiaca jednotka a ESC (Aocoda F460 Stack 60A):** Ide o "mozog" drona. Skladá sa z dvoch častí: *Flight Controller (F4)* spracúva dáta zo senzorov a pokyny z autopilota/ovládača a stabilizuje let 5\. *ESC (Electronic Speed Controller \- 60A)* sa stará o distribúciu prúdu do motorov 5, 6\.

### 2\. Počítačové videnie a umelá inteligencia (Autopilot)

* **Palubný počítač Raspberry Pi 5 (8GB RAM):** Tento minipočítač beží súbežne s riadiacou jednotkou. Spúšťa sa na ňom skript autopilota a modely umelej inteligencie (počítačové videnie YOLO), vďaka ktorým dron dokáže rozoznávať objekty a autonómne sa k nim navigovať 7\.  
* **Kamera pre Raspberry Pi (Waveshare s CSI portom):** Keďže autopilot nemá priamy prístup k obrazu z hlavnej FPV kamery drona, Raspberry Pi potrebuje vlastnú kameru s Full HD rozlíšením, ktorá slúži výhradne na úlohy počítačového videnia a sledovania cieľa 8, 9\.  
* **Napájacia redukcia a menič napätia pre RPi:** Na napájanie Raspberry Pi z hlavnej batérie drona budete potrebovať **rozbočovací kábel XT60** (1 samec na 2 samice) a **DC menič (6-26V na 5V/5A)**. Dron totiž operuje na vyššom napätí (až 26V), kým Raspberry Pi vyžaduje presne 5V 10-12.

### 3\. FPV Video systém (Prenos obrazu operátorovi)

* **Analógová FPV kamera (Jinjiean B19):** Hlavná letová kamera, ktorá sníma okolie pre operátora (vysielač). Je kompaktná a poskytuje dobrú kvalitu obrazu (1500TVL) s vynikajúcim výkonom aj v horších svetelných podmienkach 13\.  
* **Video vysielač (AKK Race Ranger 1.6W VTX):** Zodpovedá za odosielanie video signálu z kamery drona do vašich okuliarov alebo monitora. Vďaka vysokému výkonu dokáže prenášať obraz až na vzdialenosť 3000 metrov 14\. (Bude k nemu potrebné dokúpiť aj predlžovacie káble – napr. dlhší JST-SH 1.0mm a MMCX/SMA F-kábel 15).  
* **Video anténa (Lollipop 4 V4 SMA):** Pripája sa na video vysielač. Jej kruhová polarizácia pomáha minimalizovať rušenie signálu a zabezpečuje čistý obrazový prenos aj v náročnom prostredí 16\.  
* **Video prijímač (Skydroid 5.8 GHz 150 CH):** Prijímač s dvoma anténami, ktorý sa pomocou UVC OTG kábla pripája priamo k Android smartfónu. Slúži ako alternatíva k drahým FPV okuliarom a umožňuje sledovať let priamo na displeji mobilu 17\.

### 4\. Komunikácia, napájanie a iné systémy

* **Prijímač ExpressLRS 2.4 GHz Nano s T-anténou:** Modul, ktorý prijíma príkazy priamo z vášho rádiového ovládača. Využíva sa tu verzia 2.4 GHz, nakoľko dron letí väčšinou autonómne a na štart stačí štandardný dosah 18\.  
* **Rádiový ovládač (RadioMaster Pocket ELRS 2.4 GHz):** Cenovo dostupný joystick (ovládač), ktorým drona zapínate, prepínate mu letové módy, ovládate zhadzovací systém a v prípade potreby preberáte manuálnu kontrolu. Vyžaduje dve Li-ion batérie typu 18650 19\.  
* **Li-ion Batéria (BANDERA AKB 6s2p 90A \- 8400 mAh):** Obrovský zdroj energie pre celý systém. Je schopná poskytovať stabilný a silný prúd (až 60A pre ESC a 30A rezervu pre počítačové vybavenie a kamery), čo z nej robí ideálnu voľbu pre lety na dlhé vzdialenosti 10, 20\.  
* **Zhadzovací systém (Drop system):** Modul ovládaný servomotorom, ktorý sa dá vytlačiť na 3D tlačiarni alebo kúpiť hotový. Slúži na uchytenie a uvoľnenie nákladu (napr. fľaše s vodou), hneď ako mu to autopilot alebo operátor prikáže 21\.

### 5\. Nástroje na stavbu (Náradie)

Aby ste to celé dali dokopy, kniha odporúča aj špecifické vybavenie 22-24:

* **Spájkovačka, cín a tavidlo** (nevyhnutné pre elektrické spoje).  
* **Multimeter** (na meranie prúdu, napätia a kontrolu skratov pred prvým zapojením).  
* **Sada skrutkovačov, kliešte a izolačné materiály** (zmršťovacie bužírky, ochranné opletenia na káble k motorom).  
* **Nabíjačka ToolkitRC M7 s adaptérom ADP100:** Výkonná nabíjačka potrebná na správne a bezpečné nabíjanie zakúpenej 6S Li-Ion batérie 23, 24\.

