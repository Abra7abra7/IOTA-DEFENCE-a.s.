**Konštrukcia autonómneho FPV drona pre doručovanie nákladu**  
Podľa poskytnutých zdrojov sa kniha primárne zameriava na zostrojenie autonómneho FPV drona určeného na doručovanie nákladu. Tu je presný a logicky zoradený zoznam všetkých potrebných komponentov na jeho stavbu:  
**1\. Rám a pohon (Základ drona)**

* **Karbónový rám:** Na stavbu kostry drona je odporúčaný 7-palcový karbónový rám Mark 4 7" (295 mm), ideálne originál od výrobcu Readytosky \[1\]. K nemu je potrebné dokúpiť alebo na 3D tlačiarni vytlačiť držiaky pre FPV a rádiové antény \[2\].  
* **Motory:** O pohon sa starajú štyri motory EMAX ECO II 2807 6S 1300KV \[3\]. Pre ich bezpečné zapojenie a ochranu káblov sa odporúča prikúpiť aj ochranné opletenie a zmršťovacie bužírky \[4, 5\].  
* **Vrtule:** Vhodnými vrtuľami pre túto zostavu sú trojlistové vrtule HQPROP 7040 (rozmer 7x4x3) \[6\].

**2\. Riadenie a komunikácia (Mozog drona)**

* **Riadiaca jednotka a ESC:** Srdcom drona je "stack" Aocoda F460 (60A), ktorý kombinuje riadiacu jednotku (Flight Controller) Aocoda F405 v2 a elektronický regulátor otáčok (ESC) s výkonom 60A \[7, 8\].  
* **Rádiový prijímač:** Na prijímanie signálov z ovládača operátora slúži modul ExpressLRS 2.4 GHz Nano s T-anténou \[9\].  
* **Zhadzovací systém (Drop system):** Súčasťou zostavy je aj 3D vytlačený modulárny zhadzovací systém ovládaný servomotorom, ktorý je určený na uchytenie a doručenie zásielky (napr. fľaše s vodou) \[10\].

**3\. FPV a video systém (Prenos obrazu)**

* **FPV Kamera:** Ako hlavná letová kamera pre operátora slúži analógová kamera Jinjiean B19 s rozlíšením 1500TVL \[11\].  
* **Video vysielač (VTX):** Prenos obrazu zabezpečuje výkonný video vysielač AKK Race Ranger 1.6W VTX \[12\]. K tomuto vysielaču je nutné dokúpiť dlhší 20 cm kábel JST-SH 1.0mm a MMCX/SMA F-kábel pre prepojenie s anténou \[13\].  
* **FPV Anténa:** Na video vysielač sa pripája anténa s kruhovou polarizáciou Lollipop 4 V4 SMA \[14\].  
* **Video prijímač:** Na prijímanie videa z drona sa namiesto okuliarov používa duálny prijímač Skydroid 5.8 GHz 150 CH, ktorý sa pomocou UVC OTG kábla pripája priamo k Android smartfónu \[15\].

**4\. Autopilot a umelá inteligencia (Počítačové videnie)**

* **Palubný počítač:** Ako takzvaný "companion computer", na ktorom beží softvér autopilota a AI modely, slúži Raspberry Pi 5 s 8GB RAM \[16\].  
* **Kamera pre Raspberry Pi:** Keďže autopilot nemá priamy prístup ku hlavnej kamere drona, Raspberry Pi využíva na sledovanie cieľa vlastnú kameru Waveshare 1165 (Full HD) pripojenú priamo cez CSI port \[17, 18\].

**5\. Napájanie a ovládanie**

* **Batéria pre drona:** Hlavným zdrojom energie pre celý systém je 6-článková dlhodoletová Li-ion batéria v konfigurácii 6S2P 90A s kapacitou 8400 mAh \[19\].  
* **Napájacie meniče a redukcie:** Pre správne a bezpečné napájanie Raspberry Pi (ktoré potrebuje 5V) z hlavnej batérie drona (ktorá operuje až do 26V) je potrebný rozbočovací kábel XT60 (1 samec na 2 samice) a samostatný DC-DC menič napätia z 6-26V na 5V/5A \[20, 21\].  
* **Rádiový ovládač:** Dron sa manuálne ovláda pomocou rádiového ovládača RadioMaster Pocket ELRS 2.4 GHz \[22\]. Tento ovládač si na svoje fungovanie vyžaduje dve batérie typu 18650 Li-ion \[22, 23\].

**6\. Nástroje a príslušenstvo**

* **Základné náradie:** Na zostavenie a spájkovanie budete potrebovať spájkovačku, cín, tavidlo (flux), sadu skrutkovačov, kliešte, spájkovaciu podložku a multimeter pre meranie napätia \[24, 25\].  
* **Nabíjačka batérií:** Na bezpečné nabíjanie hlavnej 6S Li-Ion batérie je určená výkonná nabíjačka ToolkitRC M7 spoločne s adaptérom ADP100 \[25\].

