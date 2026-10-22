**Logovanie, monitoring a kybernetická prevádzka**

*Delta Defence a.s. · štandard logovania, MFA, PAM, záplat, zraniteľností, SIEM a väzby na incidenty a NIS2*

Delta Defence a.s. · Verzia 1.0 · Dátum: 6\. 10\. 2026 · Vypracoval: Márian Stančík · Klasifikácia: Interné – Dôverné · Stav: NÁVRH

| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. Štandard logovania, monitoringu a kybernetickej prevádzky. Retencie, SLA záplat, časy reakcie a prahy sú \[DOPLNIŤ\] – určí CISO na základe analýzy rizík a Legal/DPO podľa právnych požiadaviek. Lehoty hlásení podľa zákona č. 69/2018 Z. z. v znení zákona č. 366/2024 Z. z. sa uvádzajú orientačne a pred schválením ich overí Legal podľa aktuálneho znenia. |
| :---- |

 

# **1\. Účel, rozsah, roly**

| Položka | Obsah |
| :---- | :---- |
| Účel | Zabezpečiť detekciu, vyšetrenie a preukázanie bezpečnostných udalostí; definovať minimálne kybernetické kontroly (MFA, záplaty, zraniteľnosti, privilegované prístupy) a väzbu na reakciu na incidenty (schéma 08\) a BCP/DR (dokument 08). |
| Rozsah | Bežné IT a SaaS, sieť, koncové zariadenia, ERP a platby, register partnerov, fyzický prístup, OT/výroba (v rozsahu technických možností). Utajované prostredie – len podľa bezpečnostnej dokumentácie NBÚ (kap. 11). |
| Vlastník (A) | CISO – štandard, use-cases, dohľad, revízia |
| Výkon (R) | IT prevádzka / externý správca / SOC (ak bude zmluvne zabezpečený) – konfigurácia, zber, prvotné vyhodnotenie (U-06) |
| Konzultovaní (C) | Legal a DPO – zákonnosť monitoringu zamestnancov; Bezpečnostný manažér – rozhranie k utajovanému prostrediu |

 

# **2\. Čo sa loguje – minimálne zdroje**

| Zdroj | Udalosti (minimum) | Vlastník zdroja | Retencia | Revízia |
| :---- | :---- | :---- | :---- | :---- |
| Identita (IdP – Google / Entra ID) | Prihlásenia úspešné/neúspešné, MFA udalosti, zmeny MFA, nové zariadenia, zmeny rolí, vytvorenie/zmazanie účtu | IT prevádzka | \[DOPLNIŤ\] | automaticky \+ týždenne |
| Administrácia tenantu / cloudu | Admin aktivity, zmeny politík, zdieľanie navonok, API/aplikácie s prístupom k dátam | IT prevádzka | \[DOPLNIŤ\] | týždenne |
| E-mail | Pravidlá presmerovania, prístupy do schránok, delegácie, phishing hlásenia, DLP udalosti | IT prevádzka | \[DOPLNIŤ\] | týždenne |
| Koncové zariadenia (EDR, MDM) | Detekcie, vypnutie ochrany, inštalácia SW, USB média, šifrovanie disku | IT prevádzka | \[DOPLNIŤ\] | denne (alerty) |
| Sieť (firewall, VPN, DNS, Wi-Fi) | Spojenia, blokácie, VPN prihlásenia, zmeny konfigurácie | IT prevádzka | \[DOPLNIŤ\] | týždenne |
| Servery a databázy | Prihlásenia, privilegované príkazy, zmeny konfigurácie, zálohy | IT prevádzka | \[DOPLNIŤ\] | týždenne |
| ERP a internetbanking | Schválenia platieb, **zmeny IBAN a kmeňových dát dodávateľov**, zmeny limitov, nové užívateľské práva | Financie | \[DOPLNIŤ\] | denne pri platbách, mesačne revízia |
| Register partnerov / CRM | Zmeny stavu DD, schválenia CCO, STOP, prístupy k Dôverným záznamom | CCO | \[DOPLNIŤ\] | mesačne |
| Súborové úložiská (zóna Dôverné) | Prístupy, hromadné sťahovanie, externé zdieľanie, zmeny oprávnení | Vlastníci dát | \[DOPLNIŤ\] | mesačne |
| Privilegované relácie (PAM) | Začiatok/koniec, účet, cieľ, schválenie JIT, záznam relácie (ak je zavedený) | CISO | \[DOPLNIŤ\] | každé použitie break-glass; mesačne |
| Fyzický prístup | Vstupy do areálu, chránených priestorov, serverovne; návštevy | Bezp. manažér / Správa budov | \[DOPLNIŤ\] | mesačne |
| Zálohovací systém | Úspešnosť úloh, zmeny retencie, mazanie, obnovy | IT prevádzka | \[DOPLNIŤ\] | denne |
| OT / výroba | Vzdialené prístupy dodávateľov, zmeny programov/konfigurácií | Výroba | \[DOPLNIŤ\] | pri každom prístupe |

 

## **2.1 Požiadavky na logy**

> * **Synchronizácia času:** všetky systémy z jedného spoľahlivého zdroja (NTP), časová zóna v záznamoch jednoznačná.  
> * **Integrita:** logy sa ukladajú centrálne (SIEM / log úložisko) s ochranou proti zmene a zmazaniu (nemenné úložisko); administrátor nesmie mazať logy o vlastnej činnosti.  
> * **Prístup k logom:** len CISO, poverení analytici IT prevádzky / SOC, interný audit na požiadanie; prístup k logom sa sám loguje.  
> * **Obsah:** neukladať heslá, tokeny ani obsah komunikácie, ak to nie je nevyhnutné; minimalizácia osobných údajov.  
> * **Retencia:** \[DOPLNIŤ pre každý zdroj\] – zohľadniť potrebu vyšetrovania, požiadavky zákona č. 69/2018 Z. z. (ak v pôsobnosti), GDPR (primeranosť) a zmluvné požiadavky konzorcií.  
> * **Výpadok zberu:** zastavenie zberu logov z kritického zdroja je alert P2.

## **2.2 Monitoring zamestnancov – právne podmienky**

| Monitoring činnosti zamestnancov (logy, e-mail, DLP, kamery) je prípustný len v súlade so Zákonníkom práce (§ 13 ods. 4 – vážne dôvody spočívajúce v osobitnej povahe činností, rozsah a spôsob kontroly, prerokovanie so zástupcami zamestnancov, ak pôsobia, a vopred informovanie zamestnancov) a s GDPR (právny základ, posúdenie primeranosti, prípadne DPIA, informačná povinnosť). Pred zapnutím use-cases týkajúcich sa správania jednotlivcov (napr. hromadné sťahovanie, DLP) Legal a DPO vydajú písomné posúdenie a HR zabezpečí informovanie zamestnancov. Freelanceri sa informujú zmluvne. |
| :---- |

 

# **3\. Viacfaktorová autentifikácia (MFA)**

| Skupina účtov | Požiadavka | Výnimky |
| :---- | :---- | :---- |
| Všetci zamestnanci a freelanceri | MFA vynútené politikou podmieneného prístupu; prednostne aplikácia s overením čísla alebo FIDO2; SMS len dočasne s výnimkou | Len písomne, s dobou platnosti, register výnimiek |
| Privilegované a administrátorské účty | FIDO2 / hardvérový kľúč, oddelený admin účet bez e-mailu | Žiadne |
| Break-glass účty | FIDO2, uložené v trezore, monitorované, použitie \= alert P1 | — |
| Servisné účty | Bez interaktívneho prihlásenia; obmedzenie IP/rozsahu; rotácia tajomstiev \[DOPLNIŤ\] | Register servisných účtov |
| Externý správca / dodávateľ | MFA \+ JIT prístup schválený CISO, záznam relácie | — |
| Internetbanking | Podľa banky; autorizácia platby oddelená od prípravy (4-eyes) | — |

 

**Kontrola:** mesačný report pokrytia MFA (KPI CISO), zoznam účtov bez MFA \= nápravné opatrenie s termínom.

# **4\. Privilegované prístupy (PAM) – minimum**

> * Oddelené administrátorské účty; žiadna administrácia z bežného účtu ani z neriadeného zariadenia.  
> * Zoznam privilegovaných účtov (register) s vlastníkom, schvaľovateľom a dôvodom; recertifikácia štvrťročne.  
> * Just-in-time pridelenie práv s maximálnou dobou \[DOPLNIŤ\]; trvalé globálne admin práva len pre \[DOPLNIŤ počet\] break-glass účtov.  
> * Logovanie všetkých privilegovaných relácií; záznam relácií externého správcu (cieľovo).  
> * CISO nemá trvalé privilegované práva v produkčných systémoch (U-06); prístup len na čítanie logov a konfigurácií.  
> * Odobratie privilegovaných práv v deň zmeny funkcie / odchodu (Onboarding – offboarding časová os).

# **5\. Správa záplat (patch management)**

| Kritickosť zraniteľnosti | Príklad | SLA nasadenia | Výnimka schvaľuje |
| :---- | :---- | :---- | :---- |
| Kritická / aktívne zneužívaná | Zraniteľnosť v katalógu aktívne zneužívaných (napr. CISA KEV), externe dostupný systém | \[DOPLNIŤ\] | CISO \+ vlastník systému, kompenzačné opatrenie |
| Vysoká | CVSS vysoká na internom systéme | \[DOPLNIŤ\] | CISO |
| Stredná | — | \[DOPLNIŤ\] | IT prevádzka |
| Nízka | — | \[DOPLNIŤ\] | IT prevádzka |

 

> * Rozsah: OS, prehliadače, kancelárske aplikácie, firmvér sieťových prvkov a firewallov, VPN, hypervízory, ERP.  
> * OT / výrobné systémy: záplaty len po odsúhlasení s dodávateľom a Výrobou; ak nie je možné záplatovať – segmentácia a kontrolovaný vzdialený prístup.  
> * Nepodporované (end-of-life) systémy: register, plán náhrady, izolácia.  
> * Report súladu mesačne (KPI CISO).

# **6\. Správa zraniteľností**

| Činnosť | Rozsah | Frekvencia (návrh) | Zodpovedný |
| :---- | :---- | :---- | :---- |
| Automatizované skenovanie interné | Servery, koncové zariadenia, sieť | \[DOPLNIŤ\] (návrh: mesačne) | IT prevádzka / CISO |
| Skenovanie externého perimetra | Verejné IP, domény, VPN | \[DOPLNIŤ\] (návrh: týždenne) | IT prevádzka / CISO |
| Konfiguračný audit tenantu (Workspace / M365) | Zdieľanie, politiky, aplikácie | \[DOPLNIŤ\] (návrh: štvrťročne) | CISO |
| Penetračný test | Kritické systémy, externý perimeter | \[DOPLNIŤ\] (návrh: ročne a po zásadnej zmene) | Externý dodávateľ, A: CISO |
| Register zraniteľností | Všetky nálezy s vlastníkom a termínom | priebežne | CISO |
| Hlásenie zraniteľností v produktoch (ak obsahujú SW/firmvér) | Koordinované zverejňovanie; posúdiť nariadenie (EÚ) 2024/2847 | \[DOPLNIŤ\] | CISO / Vývoj |

 

# **7\. SIEM / SOC – úrovne alertov a reakcie**

| Úroveň | Charakter | Príklady | Prvá reakcia | Eskalácia |
| :---- | :---- | :---- | :---- | :---- |
| P1 – kritická | Prebiehajúci útok alebo vysoké riziko pre utajované / platby / výrobu | Ransomvér, použitie break-glass, nový globálny admin mimo zmeny, hromadné šifrovanie, zmena IBAN bez 4-eyes, exfiltrácia Dôverných dát | \[DOPLNIŤ\] | CISO ihneď → gestor bezpečnosti → krízový štáb (dokument 08 kap. 6–7) |
| P2 – vysoká | Pravdepodobná kompromitácia účtu alebo zariadenia | Nemožné cestovanie, vypnutie MFA, malware na zariadení, pravidlo presmerovania pošty mimo firmy, výpadok zberu logov z kritického zdroja | \[DOPLNIŤ\] | CISO, incident owner |
| P3 – stredná | Podozrivá aktivita vyžadujúca analýzu | Opakované neúspešné prihlásenia, nové zariadenie z rizikovej krajiny, neúspešná záloha | \[DOPLNIŤ\] | IT prevádzka; CISO informovaný v dennom prehľade |
| P4 – nízka | Informatívne / ladenie | Blokovaný phishing, politiky v režime audit | \[DOPLNIŤ\] | Týždenný prehľad |

 

## **7.1 Minimálne use-cases (detekcie)**

> * Prihlásenie z neobvyklej krajiny / nemožné cestovanie; prihlásenie bez MFA.  
> * Zmena alebo vypnutie MFA, pridanie nového faktora.  
> * Vytvorenie admin účtu alebo pridelenie admin roly mimo schválenej zmeny.  
> * Hromadné sťahovanie alebo externé zdieľanie zo zóny Dôverné.  
> * Zmena IBAN / kmeňových dát dodávateľa alebo agenta; platba na nový IBAN.  
> * Pravidlo presmerovania e-mailu mimo domény.  
> * Vypnutie EDR, detekcia ransomvéru, použitie nástrojov na šifrovanie.  
> * Zmena retencie alebo mazanie záloh / logov.  
> * Vzdialený prístup dodávateľa do OT mimo schváleného okna.  
> * Prístup do chránených priestorov mimo oprávnenia (fyzický systém).

Rozhodnutie interný SOC vs. externý (MDR/SOC služba) a pohotovosť 24/7: \[DOPLNIŤ\] – rozhodne predstavenstvo na návrh CISO.

# **8\. Väzba na reakciu na incidenty (schéma 08\)**

| Krok schémy 08 | Vstup z tohto štandardu | Výstup / dôkaz |
| :---- | :---- | :---- |
| 1\. Detekcia | Alert P1–P4 zo SIEM, hlásenie zamestnanca, dodávateľ | Záznam v záznamníku incidentov (čas zistenia) |
| 2\. Klasifikácia | Typ: kyber / osobné údaje / utajované / ABAC-sankcie; závažnosť | Rozhodnutie incident ownera, čas klasifikácie |
| 3\. Notifikácia interná | Komunikačný strom (dokument 08 kap. 7\) | Čas informovania gestora / štábu |
| 4\. Izolácia | PAM, blokovanie účtov, izolácia EDR | Zoznam opatrení, zachované logy a obrazy |
| 5\. Hlásenie orgánom | Tabuľka lehôt kap. 9 | Kópie hlásení, potvrdenia prijatia |
| 6\. Obnova a poučenie | DR runbooky (dokument 08 kap. 8\) | Záznam o obnove, nápravné opatrenia |

 

# **9\. Jednotná tabuľka lehôt hlásení (U-09)**

| Typ incidentu | Adresát | Lehota (overiť podľa aktuálneho znenia) | Kto hlási | Právny základ |
| :---- | :---- | :---- | :---- | :---- |
| Závažný kybernetický incident (ak je spoločnosť v pôsobnosti) | NBÚ (cez určený kanál / informačný systém NBÚ) | Včasné varovanie do 24 h od zistenia; hlásenie incidentu do 72 h; záverečná správa do 1 mesiaca | CISO (A: predstavenstvo) | Zákon č. 69/2018 Z. z. v znení zákona č. 366/2024 Z. z.; smernica (EÚ) 2022/2555 |
| Porušenie ochrany osobných údajov | ÚOOÚ SR; dotknuté osoby pri vysokom riziku | Do 72 h od zistenia (ÚOOÚ SR); dotknutým osobám bez zbytočného odkladu | DPO / CCO | Čl. 33 a 34 GDPR; zákon č. 18/2018 Z. z. |
| Bezpečnostný incident s utajovanými skutočnosťami | NBÚ (a pôvodca podľa zmluvy) | Bezodkladne – presnú lehotu a formu overí Bezpečnostný manažér | Bezpečnostný manažér | Zákon č. 215/2004 Z. z. a vykonávacie predpisy |
| Podozrenie na trestný čin (korupcia, podvod, kybernetický útok) | OČTK (polícia / prokuratúra) | Podľa posúdenia Legal (oznamovacia povinnosť podľa Trestného zákona) | Legal / CCO | Trestný zákon; zákon č. 91/2016 Z. z. |
| Porušenie sankcií / exportného režimu | Príslušný orgán (napr. MH SR) podľa posúdenia | Podľa posúdenia Legal a ECO | ECO / Legal | Nariadenie (EÚ) 2021/821; zákony č. 392/2011, 39/2011, 289/2016 Z. z. |
| Zmluvné hlásenie (konzorcium, zákazník) | Podľa zmluvy | \[DOPLNIŤ podľa zmlúv\] | Legal / Obchod | Zmluvy |

 

# **10\. NIS2 – povedomie a posúdenie pôsobnosti**

Smernica (EÚ) 2022/2555 (NIS2) bola do slovenského práva transponovaná novelou zákona č. 69/2018 Z. z. o kybernetickej bezpečnosti, vykonanou zákonom č. 366/2024 Z. z. (účinnosť od 1\. 1\. 2025). Orgánom je Národný bezpečnostný úrad. Či sa povinnosti vzťahujú na Delta Defence a.s., zatiaľ nebolo posúdené (audit – D05).

## **10.1 Kontrolný zoznam písomného posúdenia (D05)**

| \# | Otázka | Odpoveď | Zdroj / dôkaz |
| :---- | :---- | :---- | :---- |
| 1 | Pôsobí spoločnosť v sektore / podsektore uvedenom v prílohách zákona (napr. výroba vybraných produktov, digitálni poskytovatelia, dodávateľský reťazec)? | \[DOPLNIŤ\] | Predmet činnosti, NACE kódy |
| 2 | Spĺňa veľkostné kritériá (počet zamestnancov, obrat, súvaha) podľa aktuálneho znenia? | \[DOPLNIŤ\] | Účtovná závierka |
| 3 | Je spoločnosť určená ako subjekt bez ohľadu na veľkosť (osobitné kritériá) alebo je kritickým dodávateľom subjektu v pôsobnosti? | \[DOPLNIŤ\] | Zmluvy, oznámenia NBÚ |
| 4 | Vzťahujú sa na spoločnosť výnimky pre obranu / národnú bezpečnosť (časť činnosti)? | \[DOPLNIŤ\] | Legal – posúdenie |
| 5 | Záver: v pôsobnosti áno / nie; kategória subjektu | \[DOPLNIŤ\] | Podpis CISO \+ Legal |
| 6 | Ak áno: registrácia u NBÚ, lehota, zodpovedná osoba | \[DOPLNIŤ\] | Potvrdenie registrácie |
| 7 | Ak nie: dobrovoľné uplatnenie opatrení ako zmluvný štandard pre konzorciá | \[DOPLNIŤ\] | Rozhodnutie predstavenstva |

 

## **10.2 Čo z NIS2 platí pre spoločnosť prakticky aj bez ohľadu na záver**

> * **Zodpovednosť štatutárneho orgánu:** predstavenstvo schvaľuje opatrenia riadenia kybernetických rizík a dohliada na ich plnenie; členovia predstavenstva absolvujú školenie \[DOPLNIŤ frekvencia\].  
> * **Opatrenia:** analýza rizík, riešenie incidentov, kontinuita (dokument 08), bezpečnosť dodávateľského reťazca, bezpečnosť pri vývoji a údržbe, hodnotenie účinnosti, kybernetická hygiena a školenia, kryptografia, personálna bezpečnosť a riadenie prístupov, MFA.  
> * **Hlásenie incidentov:** viacstupňové (kap. 9).  
> * **Sankcie:** zákon upravuje pokuty a zodpovednosť – výšky sa v tomto dokumente zámerne neuvádzajú; overí Legal.  
> * **Zmluvný tlak:** zákazníci a konzorciá v pôsobnosti budú požadovať tieto opatrenia aj od dodávateľov.

# **11\. Utajované prostredie**

Logovanie, monitoring a bezpečnosť technických prostriedkov v utajovanom prostredí sa riadia výlučne bezpečnostným projektom a dokumentáciou podľa zákona č. 215/2004 Z. z. a požiadaviek NBÚ. Logy z utajovaného prostredia sa **neprenášajú** do bežného SIEM. Bežný SIEM monitoruje len fyzické a sieťové rozhranie (napr. pokusy o pripojenie neoprávnených zariadení v chránenom priestore), ak to bezpečnostná dokumentácia pripúšťa.

# **12\. RACI – kybernetická prevádzka**

| Činnosť | Predstavenstvo | CISO | IT prevádzka / SOC | Legal / DPO | Vlastníci dát | Bezp. manažér |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Schválenie štandardu | A | R | C | C | I | C |
| Konfigurácia logovania a SIEM | — | A | R | — | I | — |
| Posúdenie monitoringu zamestnancov | I | C | — | A/R | — | — |
| Vynútenie MFA, PAM | — | A | R | — | — | — |
| Patching, skenovanie | — | A (dohľad) | R | — | C | — |
| Vyhodnotenie alertov P1/P2 | I (P1) | A | R | C | C | C (rozhranie) |
| Hlásenie NBÚ (kyber) | A | R | C | C | — | — |
| Posúdenie NIS2 (D05) | A | R | — | R | — | — |

 

# **13\. Otvorené body**

> * Retencie pre každý zdroj logov \[DOPLNIŤ\].  
> * SLA záplat a časy reakcie \[DOPLNIŤ\].  
> * Výber SIEM / SOC a pohotovosti.  
> * Písomné posúdenie monitoringu zamestnancov (Legal \+ DPO) a informovanie zamestnancov.  
> * Písomné posúdenie pôsobnosti NIS2 (D05).  
> * Zapnutie audit logov v tenante, ERP a internetbankingu ako prvý dôkaz (audit kap. 8, výstup 8).

# **Správa dokumentu**

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý návrh štandardu logovania, monitoringu a kybernetickej prevádzky | NÁVRH – na posúdenie predstavenstvom, právnu a bezpečnostnú revíziu |

 