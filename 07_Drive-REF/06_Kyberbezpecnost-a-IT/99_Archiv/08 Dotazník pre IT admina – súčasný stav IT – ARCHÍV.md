**Dotazník pre IT administrátora – súčasný stav IT**

IOTA Defence a.s. · Verzia 1.0 · 20\. 10\. 2026 · Vypracoval: Márian Stančík · Klasifikácia: Interné – Dôverné · Stav: NÁVRH

| Údaj | Vyplní respondent |
| :---- | :---- |
| Meno a priezvisko respondenta | ...................................................... |
| Funkcia / firma (interný alebo externý admin) | ...................................................... |
| Dátum a miesto rozhovoru | ...................................................... |
| Ďalší účastníci | ...................................................... |

# **1\. Účel a pokyny**

Cieľom dotazníka je zmapovať, ako IT vo firme funguje dnes: aké služby, účty, zariadenia, siete a dáta firma používa a kto ich spravuje. Odpovede sú podkladom pre IT architekta, ktorý navrhne cieľový stav IT a bezpečnosti. Dotazník nehodnotí prácu administrátora, ide len o zachytenie skutočného stavu.

> * **Priorita P1** – musíme vedieť ako prvé; preberieme na úvodnom rozhovore.  
> * **Priorita P2** – dôležité pre návrh; preberieme, ak zostane čas, inak písomne do 5 pracovných dní.  
> * **Priorita P3** – doplňujúce; stačí vyplniť písomne.  
> * Ak odpoveď nepoznáte, napíšte „neviem“ a kto by to mohol vedieť. Aj „nemáme“ je dôležitá odpoveď.  
> * Ak existuje dokument alebo export (zoznam, schéma), stačí ho uviesť a priložiť podľa časti 3\.  
> * **Neuvádzajte** heslá, PIN kódy, obnovovacie kľúče, prístupové tokeny ani obsah utajovaných skutočností. Schému siete a zoznamy účtov odovzdajte šifrovane alebo osobne, nie bežným e-mailom.

Dotazník má 148 otázok v 17 oblastiach: 53 s prioritou P1, 64 s prioritou P2 a 31 s prioritou P3. Rozhovor nad otázkami P1 trvá približne 60 až 90 minút.

**Odporúčaný priebeh rozhovoru**

| Časť | Oblasť | Otázok | Z toho P1 | Čas |
| :---- | :---- | :---- | :---- | :---- |
| A | Spoločnosť, lokality a kontakty | 7 | 3 | 4 min |
| B | Používatelia a účty | 10 | 6 | 7 min |
| C | Identita, prihlasovanie a privilegované účty | 10 | 3 | 6 min |
| D | Služby, aplikácie a cloudové služby | 13 | 4 | 7 min |
| E | Dáta a úložiská | 11 | 4 | 6 min |
| F | Koncové zariadenia | 11 | 5 | 6 min |
| G | Sieť a vzdialený prístup | 10 | 4 | 6 min |
| H | Výroba, sklad a testovacie prostredie | 8 | 3 | 5 min |
| I | Servery, cloud a infraštruktúra | 8 | 2 | 4 min |
| J | Bezpečnostná prevádzka | 9 | 2 | 5 min |
| K | Zálohovanie a obnova | 7 | 3 | 5 min |
| L | Utajované skutočnosti (NBÚ) | 8 | 3 | 5 min |
| M | Exportná kontrola v IT | 8 | 3 | 5 min |
| N | Dodávatelia a externá správa IT | 6 | 2 | 3 min |
| O | Vývoj softvéru a firmvéru | 10 | 3 | 5 min |
| P | Dokumentácia, politiky a súlad | 6 | 1 | 3 min |
| Q | Rozpočet, licencie, problémy a plány | 6 | 2 | 3 min |
|  | Spolu | 148 | 53 | 85 min |

**Ak je málo času: 10 kľúčových otázok**

| Č. | Otázka |
| :---- | :---- |
| B1 | Koľko je aktívnych používateľských účtov celkom? Koľko z nich patrí zamestnancom, externistom, partnerom a koľko je servisných účtov? |
| B4 | Pracujú pre firmu vývojári alebo iní ľudia mimo EÚ? V ktorých krajinách a k čomu majú prístup? |
| C1 | Aký adresár účtov sa používa (Microsoft Entra ID, Active Directory na vlastnom serveri, Google Workspace, iný, žiadny centrálny)? |
| C2 | Je zapnuté viacfaktorové overenie (MFA)? Pre koho a akou metódou (aplikácia, SMS, hardvérový kľúč)? Aké sú výnimky? |
| C3 | Koľko ľudí má administrátorské práva (tenant, servery, firewall, aplikácie)? Majú na to oddelené admin účty? |
| E3 | Kde sú uložené technické dáta: výkresy, CAD modely, firmvér, zdrojový kód, výsledky testov, dokumentácia dronov a munície? |
| J2 | Bol za posledné 3 roky bezpečnostný incident (phishing, ransomware, únik dát, napadnutý účet, strata zariadenia)? Čo sa stalo a ako sa to riešilo? |
| K3 | Kedy bola naposledy vyskúšaná obnova zo zálohy a s akým výsledkom? |
| L1 | Pracuje dnes firma s utajovanými skutočnosťami (vlastnými, od MO SR, NATO, EÚ alebo zahraničných partnerov)? Akého stupňa? |
| M3 | Používajú sa vo vývoji alebo vo výrobe americké komponenty, softvér, knižnice alebo nástroje (napr. CAD, kompilátory, šifrovanie)? Ktoré? |

# **2\. Otázky**

## **A. Spoločnosť, lokality a kontakty**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| A1 | Aké lokality firma používa (sídlo, kancelárie, výroba, sklad munície, testovacie plochy, vývoj)? Uveďte adresu a počet ľudí na každej. | **P1** |  |
| A2 | Kto spravuje IT (interný admin, externá firma, kombinácia)? Uveďte meno, rolu, rozsah úväzku a zástup. | **P1** |  |
| A3 | Kto vo firme rozhoduje o IT (schvaľuje nákupy, zmeny a prístupy)? | **P1** |  |
| A4 | Existuje kontakt pre núdzové situácie mimo pracovného času (pohotovosť)? | P2 |  |
| A5 | Pracujú niektorí ľudia trvalo z domu alebo zo zahraničia? Z ktorých krajín? | P2 |  |
| A6 | Je firma súčasťou skupiny (materská alebo sesterská firma) a zdieľa s ňou IT (tenant, sieť, účty)? | P2 |  |
| A7 | Aké zmeny sa plánujú v najbližších 12 mesiacoch (nové lokality, nábor, nové projekty)? | P3 |  |

## **B. Používatelia a účty**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| B1 | Koľko je aktívnych používateľských účtov celkom? Koľko z nich patrí zamestnancom, externistom, partnerom a koľko je servisných účtov? | **P1** |  |
| B2 | Existuje aktuálny zoznam používateľov s rolou, oddelením a dátumom nástupu? Kto ho vedie? | **P1** |  |
| B3 | Koľko externých osôb (freelanceri, dodávatelia, obchodní agenti) má prístup do firemných systémov? Do ktorých? | **P1** |  |
| B4 | Pracujú pre firmu vývojári alebo iní ľudia mimo EÚ? V ktorých krajinách a k čomu majú prístup? | **P1** |  |
| B5 | Používajú sa zdieľané účty (napr. info@, admin, spoločné prihlásenie do stroja alebo aplikácie)? Ktoré a kto ich pozná? | **P1** |  |
| B6 | Ako prebieha nástup nového človeka (kto žiada, kto zakladá účet, čo dostane)? Je postup zapísaný? | P2 |  |
| B7 | Ako prebieha odchod (kedy sa účet zablokuje, kto odoberá prístupy, zariadenie a súbory)? Sú ešte aktívne účty bývalých zamestnancov? | **P1** |  |
| B8 | Odoberajú sa staré prístupy pri zmene pozície alebo projektu? | P2 |  |
| B9 | Používajú sa na firemnú prácu súkromné e-mailové účty alebo súkromné úložiská? | P2 |  |
| B10 | Ako často sa kontroluje, kto má k čomu prístup? Kedy to bolo naposledy? | P3 |  |

## **C. Identita, prihlasovanie a privilegované účty**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| C1 | Aký adresár účtov sa používa (Microsoft Entra ID, Active Directory na vlastnom serveri, Google Workspace, iný, žiadny centrálny)? | **P1** |  |
| C2 | Je zapnuté viacfaktorové overenie (MFA)? Pre koho a akou metódou (aplikácia, SMS, hardvérový kľúč)? Aké sú výnimky? | **P1** |  |
| C3 | Koľko ľudí má administrátorské práva (tenant, servery, firewall, aplikácie)? Majú na to oddelené admin účty? | **P1** |  |
| C4 | Používa sa jednotné prihlásenie (SSO) do aplikácií? Do ktorých áno a do ktorých nie? | P2 |  |
| C5 | Aké sú pravidlá hesiel (dĺžka, zmena, zákaz opakovania)? Sú nastavené technicky? | P2 |  |
| C6 | Používa sa firemný správca hesiel? Kde sú uložené admin heslá a prístupy k službám? | P2 |  |
| C7 | Existujú núdzové účty pre prípad výpadku MFA alebo nedostupnosti admina? Kde sú uložené prístupové údaje? | P2 |  |
| C8 | Sú nastavené pravidlá podmieneného prístupu (napr. len zo spravovaného zariadenia, blokovanie krajín)? | P2 |  |
| C9 | Majú bežní používatelia administrátorské práva na svojom počítači? | P3 |  |
| C10 | Ako sa riadi vstup do budov a miestností (karty, kľúče)? Je prepojený s IT účtami? | P3 |  |

## **D. Služby, aplikácie a cloudové služby**

Otázky doplňte prehľadovou tabuľkou na konci tejto časti. Ak existuje zoznam licencií, stačí ho priložiť.

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| D1 | Aký e-mail a kancelársky balík sa používa (Microsoft 365, Google Workspace, iný)? Aká edícia a koľko licencií? | **P1** |  |
| D2 | V akej krajine alebo regióne sú uložené dáta tohto tenantu (napr. EU Data Boundary, dátové regióny)? | **P1** |  |
| D3 | Ktoré domény firma vlastní, kde sú registrované a kto spravuje DNS? Sú nastavené SPF, DKIM a DMARC? | **P1** |  |
| D4 | Čím sa komunikuje (Teams, Slack, WhatsApp, Signal, iné)? Používajú sa na prácu aj súkromné telefóny a aplikácie? | P2 |  |
| D5 | Aký účtovný alebo ERP systém sa používa? Kto ho prevádzkuje a kde beží? | P2 |  |
| D6 | Používa sa CRM? Aké a kto má prístup (aj obchodní agenti v zahraničí)? | P2 |  |
| D7 | Aké systémy sa používajú na HR, mzdy a dochádzku? | P2 |  |
| D8 | Aké nástroje sa používajú na konštrukciu a technickú dokumentáciu (CAD, PLM/PDM, simulácie)? Aké sú licencie a kde sú dáta? | **P1** |  |
| D9 | Používa sa ticketing, helpdesk alebo evidencia úloh (napr. Jira)? | P2 |  |
| D10 | Aké ďalšie cloudové služby firma platí (aj kartou zamestnanca)? Existuje ich zoznam? | P2 |  |
| D11 | Používajú zamestnanci nástroje umelej inteligencie (ChatGPT, Copilot, iné)? Firemné alebo súkromné účty? Vkladajú sa tam firemné dáta? | P2 |  |
| D12 | Kto má prístup k elektronickej schránke na slovensko.sk a ku kvalifikovanému elektronickému podpisu? | P3 |  |
| D13 | Kde je hostovaný firemný web a kto ho spravuje? | P3 |  |

**Prehľad služieb a aplikácií**

| Oblasť | Produkt a dodávateľ | Licencie / používatelia | Vlastník vo firme | Krajina uloženia dát | Koniec zmluvy | Náklady / mesiac |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| E-mail a kancelársky balík |  |  |  |  |  |  |
| Komunikácia a videohovory |  |  |  |  |  |  |
| Úložisko dokumentov |  |  |  |  |  |  |
| Účtovníctvo / ERP |  |  |  |  |  |  |
| CRM |  |  |  |  |  |  |
| HR, mzdy, dochádzka |  |  |  |  |  |  |
| CAD / PLM / PDM |  |  |  |  |  |  |
| Repozitár zdrojového kódu |  |  |  |  |  |  |
| CI/CD a build |  |  |  |  |  |  |
| Ticketing / helpdesk |  |  |  |  |  |  |
| Správca hesiel |  |  |  |  |  |  |
| Antivírus / EDR |  |  |  |  |  |  |
| Správa zariadení (MDM) |  |  |  |  |  |  |
| Zálohovanie |  |  |  |  |  |  |
| Web a DNS |  |  |  |  |  |  |
| E-podpis a eSchránka |  |  |  |  |  |  |
| Výroba a sklad (MES / WMS) |  |  |  |  |  |  |
| Iné: ............................... |  |  |  |  |  |  |

## **E. Dáta a úložiská**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| E1 | Kde sú uložené firemné dokumenty (cloudový disk, súborový server, NAS, lokálne disky, USB)? Uveďte všetky miesta. | **P1** |  |
| E2 | V ktorej krajine fyzicky sú dáta na každom z týchto miest (dátové centrum, región cloudu)? | **P1** |  |
| E3 | Kde sú uložené technické dáta: výkresy, CAD modely, firmvér, zdrojový kód, výsledky testov, dokumentácia dronov a munície? | **P1** |  |
| E4 | Kto má prístup k týmto technickým dátam? Je prístup obmedzený podľa projektov? | **P1** |  |
| E5 | Rozdeľujú sa dáta podľa citlivosti (verejné, interné, dôverné)? Používajú sa označenia alebo štítky? | P2 |  |
| E6 | Ako sa zdieľajú súbory navonok (zákazníci, agenti, dodávatelia)? Sú povolené odkazy typu „ktokoľvek s odkazom“? | P2 |  |
| E7 | Sú citlivé dáta šifrované (na diskoch, na serveroch, pri prenose)? | P2 |  |
| E8 | Kde sa uchovávajú osobné údaje (zamestnanci, zákazníci, uchádzači) a kto k nim má prístup? | P2 |  |
| E9 | Používajú sa USB kľúče a externé disky? Sú obmedzené alebo šifrované? | P3 |  |
| E10 | Koľko dát firma má (GB/TB) a ako rýchlo pribúdajú? | P3 |  |
| E11 | Existujú pravidlá na uchovávanie a mazanie dát? | P3 |  |

## **F. Koncové zariadenia**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| F1 | Koľko je zariadení: notebooky, stolné počítače, CAD stanice, mobily, tablety? Sú firemné alebo súkromné? | **P1** |  |
| F2 | Aké operačné systémy a verzie sa používajú? Sú medzi nimi systémy bez podpory výrobcu? | **P1** |  |
| F3 | Sú zariadenia spravované centrálne (MDM, napr. Intune, Jamf)? Aká časť zariadení? | **P1** |  |
| F4 | Je zapnuté šifrovanie diskov (BitLocker, FileVault)? Kde sú uložené obnovovacie kľúče? | **P1** |  |
| F5 | Aký antivírus alebo EDR sa používa? Na koľkých zariadeniach? Kto sleduje upozornenia? | **P1** |  |
| F6 | Používajú ľudia na firemnú prácu súkromné zariadenia? Na čo (e-mail, dokumenty, technické dáta)? | P2 |  |
| F7 | Ako sa inštalujú aktualizácie systému a aplikácií? Automaticky? Do koľkých dní? | P2 |  |
| F8 | Čo sa robí pri strate alebo krádeži zariadenia (napr. vzdialené vymazanie)? | P2 |  |
| F9 | Existuje evidencia zariadení (sériové čísla, kto má aké zariadenie)? | P3 |  |
| F10 | Berú si ľudia firemné zariadenia na cesty do zahraničia? Do ktorých krajín a s akými pravidlami? | P3 |  |
| F11 | Koľko je tlačiarní, skenerov a multifunkčných zariadení? Sú v sieti a ukladajú dokumenty? | P3 |  |

## **G. Sieť a vzdialený prístup**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| G1 | Aké internetové pripojenie je na každej lokalite (poskytovateľ, rýchlosť, záložná linka)? | **P1** |  |
| G2 | Aký firewall sa používa (výrobca, model, kto ho spravuje, kedy bol naposledy aktualizovaný)? | **P1** |  |
| G3 | Je sieť rozdelená na časti (kancelária, hostia, výroba, sklad, vývoj, testovanie dronov, servery)? Ako? | **P1** |  |
| G4 | Ako sa ľudia pripájajú zvonku (VPN, vzdialená plocha, len cloud)? Majú vzdialený prístup aj dodávatelia alebo ľudia zo zahraničia? | **P1** |  |
| G5 | Ako je zabezpečená Wi-Fi (WPA2/WPA3, podnikové prihlasovanie, oddelená sieť pre hostí)? | P2 |  |
| G6 | Sú lokality navzájom prepojené (VPN medzi lokalitami)? | P2 |  |
| G7 | Sú z internetu dostupné niektoré služby vo firme (otvorené porty, vzdialená plocha, webové rozhrania zariadení)? | P2 |  |
| G8 | Existuje aktuálna schéma siete a zoznam IP rozsahov? | P3 |  |
| G9 | Používa sa filtrovanie webu alebo DNS? | P3 |  |
| G10 | Aké sieťové prvky sa používajú (switche, prístupové body)? Kto ich spravuje a je ich firmvér aktuálny? | P3 |  |

## **H. Výroba, sklad a testovacie prostredie**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| H1 | Sú vo výrobe alebo sklade zariadenia pripojené na sieť (stroje, CNC, 3D tlačiarne, meracie zariadenia, riadenie výroby)? Sú oddelené od kancelárskej siete? | **P1** |  |
| H2 | Aké systémy chránia sklad munície a výrobu (kamery, alarm, kontrola vstupu)? Sú pripojené do IT siete alebo cloudu? Kto ich spravuje? | **P1** |  |
| H3 | Ako sú zabezpečené pozemné riadiace stanice dronov a laboratóriá (počítače, rádiové spojenie, telemetria)? Sú pripojené na internet? | **P1** |  |
| H4 | Používa sa systém na evidenciu skladu a výroby (WMS, MES, evidencia výbušnín)? Kde beží? | P2 |  |
| H5 | Ako sa nahráva firmvér do dronov a výrobkov? Z ktorých počítačov a kto to smie robiť? | P2 |  |
| H6 | Kam sa ukladajú letové a testovacie dáta (logy, video)? | P2 |  |
| H7 | Majú dodávatelia strojov vzdialený servisný prístup? | P3 |  |
| H8 | Bežia vo výrobe staršie počítače bez aktualizácií? | P3 |  |

## **I. Servery, cloud a infraštruktúra**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| I1 | Aké servery má firma vo vlastných priestoroch (počet, účel, operačný systém)? Kde stoja a ako je miestnosť chránená? | **P1** |  |
| I2 | Akých poskytovateľov cloudu firma používa (Azure, AWS, Google Cloud, Hetzner, iné)? V ktorých regiónoch? | **P1** |  |
| I3 | Používa sa virtualizácia (VMware, Hyper-V, Proxmox)? Aké verzie a licencie? | P2 |  |
| I4 | Kto má administrátorský prístup k serverom a cloudu? Sú cloudové účty viazané na firemné účty s MFA? | P2 |  |
| I5 | Existuje zoznam serverov a služieb (čo kde beží, kto je vlastník)? | P2 |  |
| I6 | Je zálohované napájanie (UPS, generátor)? Ako dlho vydrží? | P2 |  |
| I7 | Ako sa spravujú certifikáty (SSL/TLS) a ich platnosť? | P3 |  |
| I8 | Aké staršie systémy bežia a nedajú sa ľahko vymeniť? | P3 |  |

## **J. Bezpečnostná prevádzka**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| J1 | Zbierajú sa logy (prihlásenia, zmeny adminov, firewall, servery) na jednom mieste? Kde a ako dlho sa uchovávajú? | **P1** |  |
| J2 | Bol za posledné 3 roky bezpečnostný incident (phishing, ransomware, únik dát, napadnutý účet, strata zariadenia)? Čo sa stalo a ako sa to riešilo? | **P1** |  |
| J3 | Používa sa SIEM alebo externé monitorovanie (SOC)? Kto reaguje na upozornenia a do akého času? | P2 |  |
| J4 | Ako sa hľadajú a opravujú zraniteľnosti (skenovanie, aktualizácie serverov a sieťových prvkov)? | P2 |  |
| J5 | Bol urobený penetračný test alebo bezpečnostný audit? Kedy, kto ho robil, aké boli hlavné zistenia a sú opravené? | P2 |  |
| J6 | Existuje postup pri incidente (kto čo robí, koho informovať)? Bol niekedy precvičený? | P2 |  |
| J7 | Školia sa zamestnanci o bezpečnosti (napr. phishing)? Ako často? | P2 |  |
| J8 | Je zapnutá ochrana e-mailu (antispam, antiphishing, kontrola príloh)? | P3 |  |
| J9 | Hlásila firma niekedy incident úradu (NBÚ, Úrad na ochranu osobných údajov, polícia)? | P3 |  |

## **K. Zálohovanie a obnova**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| K1 | Čo sa zálohuje (servery, cloudový e-mail a disky, ERP, repozitáre kódu, CAD dáta, notebooky)? Čo sa nezálohuje? | **P1** |  |
| K2 | Kde sú zálohy uložené? Je aspoň jedna kópia offline alebo nemenná (nedá sa zmazať ani zašifrovať)? | **P1** |  |
| K3 | Kedy bola naposledy vyskúšaná obnova zo zálohy a s akým výsledkom? | **P1** |  |
| K4 | Ako často sa zálohuje a ako dlho sa zálohy uchovávajú? | P2 |  |
| K5 | Koľko dát môže firma najviac stratiť (RPO) a ako dlho môže byť bez systému (RTO)? Uveďte pre e-mail, ERP, technické dáta a výrobu. | P2 |  |
| K6 | Sú zálohy šifrované? Kto má prístup k zálohovaciemu systému a ku kľúčom? | P2 |  |
| K7 | Existuje zapísaný plán obnovy po havárii (napr. požiar, ransomware)? | P3 |  |

## **L. Utajované skutočnosti (NBÚ)**

Na otázky odpovedajte len áno/nie a všeobecne. Obsah utajovaných skutočností sem neuvádzajte.

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| L1 | Pracuje dnes firma s utajovanými skutočnosťami (vlastnými, od MO SR, NATO, EÚ alebo zahraničných partnerov)? Akého stupňa? | **P1** |  |
| L2 | Má firma potvrdenie o priemyselnej bezpečnosti (bezpečnostná previerka podnikateľa), alebo prebieha konanie na NBÚ? Na aký stupeň? | **P1** |  |
| L3 | Spracúvajú sa utajované informácie elektronicky? Ak áno, na akom systéme a je certifikovaný NBÚ? | **P1** |  |
| L4 | Existuje oddelená sieť alebo počítač bez pripojenia na internet? Na čo slúži, kde je a kto má prístup? | P2 |  |
| L5 | Koľko ľudí má bezpečnostnú previerku a akého stupňa? Je určený bezpečnostný zamestnanec alebo manažér? | P2 |  |
| L6 | Používajú sa šifrovacie prostriedky schválené NBÚ? Kto ich spravuje? | P2 |  |
| L7 | Dostala sa niekedy utajovaná informácia do bežného IT (e-mail, cloud, bežný počítač)? | P2 |  |
| L8 | Očakávate zákazky, pri ktorých bude potrebná práca s utajovanými informáciami? Kedy a akého stupňa? | P3 |  |

## **M. Exportná kontrola v IT**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| M1 | Kto môže otvoriť technické dáta (výkresy, kód, firmvér, špecifikácie)? Je medzi nimi niekto, kto nie je občanom EÚ alebo sa pripája zo zahraničia? | **P1** |  |
| M2 | Pripájajú sa ľudia do firemných systémov zo zahraničia (služobné cesty, agenti, vývojári mimo EÚ)? Z ktorých krajín? Dá sa to technicky obmedziť? | **P1** |  |
| M3 | Používajú sa vo vývoji alebo vo výrobe americké komponenty, softvér, knižnice alebo nástroje (napr. CAD, kompilátory, šifrovanie)? Ktoré? | **P1** |  |
| M4 | Dá sa z logov zistiť, kto a odkiaľ otvoril alebo stiahol technické dáta? | P2 |  |
| M5 | Ako sa posielajú technické dáta zákazníkom a partnerom v zahraničí (e-mail, odkaz z cloudu, USB)? Kto to schvaľuje? | P2 |  |
| M6 | Sú cloudové služby s technickými dátami nastavené tak, aby dáta zostali v EÚ (vrátane záloh a podpory poskytovateľa)? | P2 |  |
| M7 | Má firma zoznam produktov, softvéru a technológií zaradených podľa kontrolných zoznamov? Je prepojený s úložiskom dát? | P3 |  |
| M8 | Ako sa zabezpečujú notebooky a telefóny pri cestách do rizikových krajín? | P3 |  |

## **N. Dodávatelia a externá správa IT**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| N1 | Ktorí externí dodávatelia spravujú IT alebo doň majú prístup (správa IT, účtovník, web, vývoj, servis strojov)? | **P1** |  |
| N2 | Majú s nimi uzavreté zmluvy s bezpečnostnými požiadavkami, NDA a zmluvu o spracúvaní osobných údajov? | **P1** |  |
| N3 | Ako sa dodávatelia pripájajú (vlastné účty, zdieľané heslo, TeamViewer, AnyDesk)? Je prístup trvalý alebo len na požiadanie? | P2 |  |
| N4 | Aké sú dohodnuté časy reakcie (SLA) a pohotovosť? | P2 |  |
| N5 | Sú niektorí dodávatelia alebo ich pracovníci mimo EÚ? | P2 |  |
| N6 | Od koho sa kupuje hardvér a licencie? Existujú rámcové zmluvy? | P3 |  |

## **O. Vývoj softvéru a firmvéru**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| O1 | Kde je uložený zdrojový kód (GitHub, GitLab, Bitbucket, vlastný server)? V ktorej krajine? | **P1** |  |
| O2 | Kto má prístup do repozitárov (počet, interní, externí, mimo EÚ)? Sú repozitáre oddelené podľa citlivosti projektov? | **P1** |  |
| O3 | Kde sú uložené tajné údaje (API kľúče, heslá, certifikáty, kľúče na podpis firmvéru)? Nie sú priamo v kóde? | **P1** |  |
| O4 | Aké nástroje sa používajú na build a nasadenie (CI/CD)? Kde buildy bežia? | P2 |  |
| O5 | Je povinná kontrola kódu (code review), sú chránené hlavné vetvy a majú účty vývojárov MFA? | P2 |  |
| O6 | Podpisuje sa softvér a firmvér digitálne? Kde je podpisový kľúč a kto ho môže použiť? | P2 |  |
| O7 | Používajú vývojári firemné alebo súkromné počítače a účty (napr. súkromný GitHub)? | P2 |  |
| O8 | Ako sa sledujú použité open-source knižnice, ich licencie a zraniteľnosti (SBOM)? | P2 |  |
| O9 | Sú oddelené vývojové, testovacie a produkčné prostredia? | P3 |  |
| O10 | Používajú vývojári AI asistentov pri písaní kódu? Ktoré a s akým nastavením? | P3 |  |

## **P. Dokumentácia, politiky a súlad**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| P1 | Aké IT a bezpečnostné dokumenty dnes existujú (bezpečnostná politika, smernice, prevádzkové príručky)? Sú schválené? | **P1** |  |
| P2 | Posudzovala firma, či spadá pod zákon o kybernetickej bezpečnosti (NIS2)? S akým výsledkom? Je registrovaná na NBÚ? | P2 |  |
| P3 | Má firma certifikáty ISO 9001, ISO 27001 alebo AQAP 2110, prípadne ich plánuje? Kedy? | P2 |  |
| P4 | Požadujú zákazníci (MO SR, NATO, zahraniční odberatelia) bezpečnostné dotazníky alebo audity IT? | P2 |  |
| P5 | Je určená zodpovedná osoba (DPO) a vedie sa záznam o spracovateľských činnostiach podľa GDPR? | P3 |  |
| P6 | Kto a kedy naposledy kontroloval IT (audit, revízia)? | P3 |  |

## **Q. Rozpočet, licencie, problémy a plány**

| Č. | Otázka | Priorita | Odpoveď |
| :---- | :---- | :---- | :---- |
| Q1 | Čo sú dnes najväčšie problémy v IT (čo nefunguje, čo zdržuje, na čo sa ľudia sťažujú)? | **P1** |  |
| Q2 | Aké IT zmeny sú už rozbehnuté alebo naplánované (projekty, nákupy, migrácie)? | **P1** |  |
| Q3 | Aký je ročný rozpočet na IT (licencie, hardvér, služby, ľudia)? | P2 |  |
| Q4 | Ktoré licencie alebo zmluvy končia v najbližších 12 mesiacoch? | P2 |  |
| Q5 | Koľko času týždenne venujete správe IT a čo by ste potrebovali posilniť? | P2 |  |
| Q6 | Čo by ste zmenili ako prvé, keby ste mohli? | P3 |  |

# **3\. Dokumenty na vyžiadanie**

Prosíme o poskytnutie nasledujúcich podkladov, ak existujú. Ak dokument neexistuje, označte „nie je“. Citlivé podklady odovzdajte šifrovane alebo osobne.

| Č. | Dokument | Priorita | Dodané (áno / nie / nie je) | Poznámka |
| :---- | :---- | :---- | :---- | :---- |
| 1 | Schéma siete (všetky lokality, IP rozsahy, firewall, prepojenia) | **P1** |  |  |
| 2 | Inventár zariadení (notebooky, PC, mobily, servery, sieťové prvky) | **P1** |  |  |
| 3 | Zoznam používateľov a skupín vrátane externých a servisných účtov (export z adresára) | **P1** |  |  |
| 4 | Zoznam administrátorov a privilegovaných účtov | **P1** |  |  |
| 5 | Zoznam licencií a predplatných s cenou a koncom platnosti | **P1** |  |  |
| 6 | Zoznam aplikácií a cloudových služieb s vlastníkmi | **P1** |  |  |
| 7 | Popis zálohovania a záznam z posledného testu obnovy | **P1** |  |  |
| 8 | Zmluvy s IT dodávateľmi vrátane NDA, SLA a zmlúv o spracúvaní osobných údajov | P2 |  |  |
| 9 | Existujúce IT a bezpečnostné politiky, smernice a prevádzkové postupy | P2 |  |  |
| 10 | Správy z bezpečnostných auditov a penetračných testov | P2 |  |  |
| 11 | Záznamy o bezpečnostných incidentoch za posledné 3 roky | P2 |  |  |
| 12 | Zoznam repozitárov kódu s prístupmi | P2 |  |  |
| 13 | Prehľad nastavení tenantu (MFA, podmienený prístup, bezpečnostné skóre) | P2 |  |  |
| 14 | Zoznam dokumentov NBÚ (potvrdenie o priemyselnej bezpečnosti, certifikáty systémov) – len zoznam, nie obsah | P2 |  |  |
| 15 | Popis fyzickej ochrany lokalít (alarm, kamery, kontrola vstupu) | P3 |  |  |
| 16 | Plán obnovy po havárii alebo plán kontinuity, ak existuje | P3 |  |  |

# **4\. Ďalší postup**

> * Úvodný rozhovor nad otázkami P1 (60 až 90 minút).  
> * Písomné doplnenie otázok P2 a P3 a dodanie dokumentov do 5 pracovných dní.  
> * Spracovanie zistení do správy o súčasnom stave IT a návrh cieľovej architektúry IT architektom.  
> * Krátke overovacie stretnutie nad nejasnosťami.

Respondent potvrdzuje, že odpovede zodpovedajú jeho najlepšej vedomosti ku dňu vyplnenia.

Podpis respondenta: ...................................................... Dátum: ....................................