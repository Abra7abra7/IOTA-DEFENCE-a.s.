**Úvodné zistenie – ako funguje IT**

Delta Defence a.s. · 20\. 10\. 2026 · Pripravil: Márian Stančík · Interné

Ahoj, cieľom je zistiť aktuálny stav našej IT infraštruktúry – čo máme nasadené, kde to beží a ako to dnes funguje. Spíš tam prosím to, čo vieš (pokojne stručne a heslovito). Ak v prehľade niečo chýba alebo je nepresné, doplň to a potom si to spolu prejdeme. 

*Heslá, PIN kódy ani prístupové kľúče sem nepíš, tie si odovzdáme osobne.*

Vyplnil: ............................................ Dátum: ................

# **A. Rýchly prehľad**

| Údaj | Odpoveď |
| :---- | :---- |
| **Počet používateľských účtov (približne, ak vieš)** | ................ |
| **– z toho spoločné alebo servisné účty (ak vieš)** | ................ |
| **Kto spravuje IT (ty, externá firma, ďalší ľudia)** | ............................................ |
| **Kto ťa zastupuje, keď nie si k dispozícii** | ............................................ |
| **Kde má firma kancelárie a prevádzky s IT (ak vieš)** | ............................................ |
| **Servery: vlastné / v cloude (poskytovateľ, krajina)** | ............................................ |
| **Kde sú uložené súbory (miesto, krajina)** | ............................................ |
| **E-mail (služba, napr. Microsoft 365, Google)** | ............................................ |
| **Komunikácia (Teams, WhatsApp, Slack, iné)** | ............................................ |
| **Antivírus (názov)** | ............................................ |
| **Firewall (áno / nie, aký)** | ............................................ |
| **Zálohovanie (čo, kam, ako často)** | ............................................ |
| **Dvojstupňové overenie 2FA (áno / nie, pre koho)** | ............................................ |
| **VPN (áno / nie, aká)** | ............................................ |
| **Kde je IT dokumentácia (ak existuje)** | ............................................ |

# 

# 

# 

# 

# **B. Systémy a prístupy**

| Systém | Aký program (názov) | Kto ho používa (ak vieš) | Kto spravuje prístupy | Platí sa? Koľko licencií | 2FA áno / nie |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **E-mail** | ................ | ................ | ................ | ........ | ........ |
| **Komunikácia (Teams, WhatsApp, Slack, iné)** | ................ | ................ | ................ | ........ | ........ |
| **Úložisko súborov** | ................ | ................ | ................ | ........ | ........ |
| **Interné programy (vlastný softvér)** | ................ | ................ | ................ | ........ | ........ |
| **Fakturácia a účtovníctvo** | ................ | ................ | ................ | ........ | ........ |
| **Produkty, sklad, výroba (ERP)** | ................ | ................ | ................ | ........ | ........ |
| **Dochádzka a HR** | ................ | ................ | ................ | ........ | ........ |
| **CRM a obchod** | ................ | ................ | ................ | ........ | ........ |
| **Vývoj (Git, CAD)** | ................ | ................ | ................ | ........ | ........ |
| **Web a doména** | ................ | ................ | ................ | ........ | ........ |
| **Iné: ...........................** | ................ | ................ | ................ | ........ | ........ |

# **C. Krátke otázky**

## **1\. Správa IT a dokumentácia**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 1.1 | Spravuješ IT ako zamestnanec firmy, externe, alebo spolu s inou firmou? Koľko času mu približne venuješ? | ............................................ |
| 1.2 | Existuje IT dokumentácia (popis systémov, postupy, nastavenia)? Kde je uložená a kto k nej má prístup? | ............................................ |
| 1.3 | Kto okrem teba pozná prístupy a nastavenia, keby si bol dlhšie nedostupný (napr. dovolenka, choroba)? | ............................................ |

## **2\. Účty**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 2.1 | Ako sa zakladá účet pre nového človeka: kto o tom rozhodne, kto ho vytvorí a ako dlho to zvyčajne trvá? | ............................................ |
| 2.2 | Ako sa ruší účet pri odchode a ako rýchlo sa to zvyčajne stane? Ostali niekde aktívne účty ľudí, ktorí už vo firme nepracujú? | ............................................ |
| 2.3 | Čo sa deje pri zmene pozície: pridá sa nový prístup a odoberie sa starý? | ............................................ |

## **3\. Správa identít, rolí a prístupov**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 3.1 | Kde je hlavný zoznam účtov (Entra ID, Active Directory, Google, iné)? Sú systémy napojené na jedno prihlásenie (SSO), alebo má každý systém vlastné účty? | ............................................ |
| 3.2 | Ako sa dnes prideľujú prístupy? (označ, čo platí) ☐ ručne každému zvlášť ☐ cez skupiny ☐ podľa rolí (RBAC – napr. vývojár, účtovník) ☐ podľa vlastností (ABAC – napr. oddelenie, krajina, citlivosť dát) ☐ iné / neviem | ............................................ |
| 3.3 | Existuje zoznam rolí (napr. bežný používateľ, vedúci, administrátor) a toho, čo ktorá rola smie? Kto má administrátorské práva? | ............................................ |
| 3.4 | Kto prístup schvaľuje, kto ho nastaví alebo odoberie a zapisuje sa to niekde? | ............................................ |
| 3.5 | Kontroluje sa niekedy, kto má k čomu prístup? Ako často a kto to robí? | ............................................ |
| 3.6 | Ako sa spravujú admin a servisné účty a ich heslá (správca hesiel, trezor)? Používaš na správu oddelený admin účet? | ............................................ |
| 3.7 | Majú bežní používatelia administrátorské práva na svojom počítači? | ............................................ |

**Roly a prístupy (nepovinné, ak existujú)**

| Rola | Do akých systémov | Aké práva (čítanie, úprava, admin) |
| :---- | :---- | :---- |
| ................ | ............................................ | ............................................ |
| ................ | ............................................ | ............................................ |
| ................ | ............................................ | ............................................ |
| ................ | ............................................ | ............................................ |

## **4\. Zariadenia**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 4.1 | Aké zariadenia ľudia dostávajú (notebook, mobil, iné) a kto ich pripravuje? | ............................................ |
| 4.2 | Ako sa zariadenia evidujú (tabuľka, systém, preberací protokol)? | ............................................ |
| 4.3 | Čo sa deje so zariadením a dátami pri odchode? Pracujú ľudia aj na súkromných zariadeniach? | ............................................ |
| 4.4 | Sú zariadenia spravované centrálne (napr. Intune alebo iný MDM)? Je zapnuté šifrovanie diskov (BitLocker, FileVault)? | ............................................ |
| 4.5 | Je nejako obmedzené používanie USB kľúčov a externých diskov? | ............................................ |

## **5\. Úložiská a zálohy**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 5.1 | Kde sú uložené súbory (server, NAS, OneDrive, Google Drive, iné) a v ktorej krajine alebo kancelárii? | ............................................ |
| 5.2 | Čo sa zálohuje, kam a ako často? | ............................................ |
| 5.3 | Skúšala sa niekedy obnova zo zálohy? Ako to dopadlo? | ............................................ |
| 5.4 | Je niektorá záloha mimo siete alebo taká, ktorú sa nedá zmazať ani zašifrovať vírusom? | ............................................ |

## **6\. Prihlasovanie a 2FA**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 6.1 | Ako sa ľudia prihlasujú (firemný účet Microsoft alebo Google, účet v počítači, iné)? Majú jeden účet na všetko? | ............................................ |
| 6.2 | Je zapnuté dvojstupňové overenie (2FA)? Pre koho áno a pre koho nie? | ............................................ |
| 6.3 | Dá sa prihlásiť aj mimo pracoviska (z domu, zo zahraničia)? Cez VPN? Akú? | ............................................ |

## **7\. Externisti**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 7.1 | Pracujú pre firmu externisti (vývojári, dodávatelia, obchodní agenti)? Z ktorých krajín, ak vieš? | ............................................ |
| 7.2 | Ako sa pripájajú a k čomu majú prístup? | ............................................ |
| 7.3 | Má každý externista vlastný účet s dátumom ukončenia? Kto mu prístup dáva a kto ho zruší, keď spolupráca skončí? | ............................................ |

## **8\. Komunikácia**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 8.1 | Čím ľudia komunikujú (e-mail, Teams, WhatsApp, iné)? Je to firemné alebo súkromné? | ............................................ |
| 8.2 | Používajú sa na prácu súkromné telefóny? Kto zakladá pracovné skupiny? | ............................................ |
| 8.3 | Posielajú sa cez chat citlivé veci (výkresy, zmluvy, ceny, údaje o zákazníkoch)? | ............................................ |

## **9\. Bezpečnosť**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 9.1 | Aký antivírus a firewall sa používa a kto ich spravuje? | ............................................ |
| 9.2 | Zaznamenáva sa, kto sa kedy prihlásil a k čomu pristupoval? Ako dlho sa tieto záznamy (logy) uchovávajú? | ............................................ |
| 9.3 | Pozerá sa niekto na tieto záznamy? Ako často? | ............................................ |
| 9.4 | Stalo sa niekedy niečo nepríjemné (podvodný e-mail, vírus, napadnutý účet, stratený notebook)? Ako sa to riešilo? | ............................................ |
| 9.5 | Je e-mail chránený (antispam, nastavenie SPF, DKIM, DMARC)? Archivuje sa e-mail? | ............................................ |

## **10\. Výpadky**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 10.1 | Boli výpadky (internet, e-mail, server, iné)? Ako dlho trvali? | ............................................ |
| 10.2 | Kto výpadky rieši? | ............................................ |
| 10.3 | Je nejaké náhradné riešenie (záložný internet, náhradný notebook, dohodnutý postup)? | ............................................ |
| 10.4 | Ktoré systémy sú podľa teba najdôležitejšie, teda bez nich sa nedá pracovať? | ............................................ |
| 10.5 | Existuje zapísaný postup obnovy po väčšej havárii (požiar, vírus)? | ............................................ |

## **11\. Citlivé dáta**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 11.1 | Kde sú uložené výkresy, technické dokumenty a zdrojový kód? | ............................................ |
| 11.2 | Kto k nim má prístup? | ............................................ |
| 11.3 | Posielajú sa tieto dáta mimo firmu (e-mail, USB, zdieľaný odkaz)? Kto to schvaľuje? | ............................................ |

# **D. Infraštruktúra a ďalšie smerovanie**

**Nepovinné – vyplň, čo vieš.** Táto časť mi pomôže rozhodnúť, ako IT ďalej rozvíjať.

**Lokality**

| Lokalita | Adresa / čo tam je | Internet (poskytovateľ, rýchlosť, záložná linka) | Servery a sieťové prvky |
| :---- | :---- | :---- | :---- |
| **Sídlo / kancelária** | ................ | ................ | ................ |
| **Výroba** | ................ | ................ | ................ |
| **Sklad** | ................ | ................ | ................ |
| **Vývoj / laboratórium** | ................ | ................ | ................ |
| **Testovacia plocha** | ................ | ................ | ................ |
| **Iná: ...........................** | ................ | ................ | ................ |

## **12\. Sieť**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 12.1 | Je sieť rozdelená na oddelené časti (kancelária, výroba, vývoj, Wi-Fi pre hostí)? | ............................................ |
| 12.2 | Existuje schéma siete? Kto spravuje firewall, Wi-Fi a switche? | ............................................ |
| 12.3 | Kto spravuje firemnú doménu a DNS a u koho je doména registrovaná? | ............................................ |
| 12.4 | Aké ďalšie zariadenia sú v sieti (tlačiarne, kamery, alarm, vstupný systém)? | ............................................ |

## **13\. Servery, cloud a vek zariadení**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 13.1 | Má firma vlastné servery alebo serverovňu? Je tam záložný zdroj (UPS) a klimatizácia? | ............................................ |
| 13.2 | Čo beží na vlastných serveroch a čo v cloude? Ktorý poskytovateľ a v ktorej krajine? | ............................................ |
| 13.3 | Používa sa virtualizácia (VMware, Hyper-V, Proxmox, iné)? | ............................................ |
| 13.4 | Aký starý je hardvér? Bežia ešte systémy bez podpory výrobcu (napr. Windows 10 a starší, starý server)? | ............................................ |
| 13.5 | Ako sa inštalujú aktualizácie systémov a programov? | ............................................ |

## **14\. Osobitné požiadavky**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 14.1 | Vieš, či firma pracuje s utajovanými skutočnosťami alebo má izolovaný počítač bez internetu? (Stačí áno / nie / neviem.) | ............................................ |
| 14.2 | Majú ľudia mimo EÚ (vývojári, dodávatelia, agenti) prístup k technickým dátam alebo do cloudu? | ............................................ |
| 14.3 | Používa sa vo vývoji alebo výrobe americký softvér alebo komponenty (CAD, knižnice, čipy)? | ............................................ |
| 14.4 | Vieš, či firma spadá pod zákon o kybernetickej bezpečnosti (NIS2), alebo má certifikáty ISO 27001 či AQAP 2110? (Stačí áno / nie / neviem.) | ............................................ |
| 14.5 | Robila sa niekedy externá kontrola bezpečnosti alebo penetračný test? | ............................................ |

## **15\. Vývoj a výroba**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 15.1 | Kde je zdrojový kód (GitHub, GitLab, vlastný server) a kde sa program zostavuje (build)? | ............................................ |
| 15.2 | Kde je uložený firmvér dronov a kto ho nahráva do dronov? | ............................................ |
| 15.3 | Je oddelené testovacie prostredie (laboratórium, testovacie drony)? | ............................................ |
| 15.4 | Sú stroje vo výrobe (CNC, 3D tlačiarne, meracie zariadenia) pripojené do siete? | ............................................ |

## **16\. Dodávatelia a náklady**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 16.1 | Pomáha s IT externá firma? Je s ňou zmluva a dohodnutý čas reakcie? | ............................................ |
| 16.2 | Ako sa dodávateľ pripája (vlastný účet, TeamViewer, AnyDesk, iné)? | ............................................ |
| 16.3 | Približne koľko stojí IT ročne a koľko z toho licencie, ak vieš? | ............................................ |

## **17\. Do budúcnosti**

| Č. | Otázka | Odpoveď |
| :---- | :---- | :---- |
| 17.1 | Čo ťa v IT najviac trápi alebo by si chcel zlepšiť? | ............................................ |
| 17.2 | Plánuje sa niečo kúpiť alebo zmeniť? | ............................................ |
| 17.3 | Čo by si preferoval: Microsoft 365, Google Workspace, alebo vlastné servery? Prečo? | ............................................ |
| 17.4 | Čo je podľa teba dôležité zachovať, aby sa práca neprerušila? | ............................................ |

# **E. Dokumenty, ktoré by pomohli (ak existujú)**

Nič z toho netreba vytvárať nanovo, stačí poslať to, čo už existuje.

> 1. IT dokumentácia (popis IT, postupy, nastavenia).  
> 2. Schéma siete.  
> 3. Zoznam serverov a zariadení.  
> 4. Zoznam licencií a platených služieb.  
> 5. Zoznam používateľských účtov.  
> 6. Zoznam rolí a oprávnení.  
> 7. Zmluvy s IT dodávateľmi.  
> 8. Popis zálohovania, prípadne záznam o skúške obnovy.  
> 9. Správa z poslednej kontroly bezpečnosti alebo testu, ak bola.

Zoznam účtov, schému siete a zoznam serverov radšej odovzdaj osobne alebo šifrovane, nie bežným e-mailom.