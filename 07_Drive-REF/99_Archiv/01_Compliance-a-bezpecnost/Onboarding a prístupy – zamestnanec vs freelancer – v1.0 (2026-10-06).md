# **Onboarding a prístupy – zamestnanec vs. freelancer – v1.0**

*Praktický postup pre nástup, pridelenie prístupov a ukončenie spolupráce: (A) freelancer na zmluvu o dielo / SZČO a (B) zamestnanec v pracovnom pomere (TPP)*  
Verzia 1.0 \| Dátum: 6\. 10\. 2026 \| Vypracoval: Márian Stančík \| Spoločnosť: Delta Defence a.s. \| Klasifikácia dokumentu: Interné  
Nadväzuje na dokumenty: [Organizačná štruktúra, compliance a bezpečnosť – rámec v1.0 (2026-10-06)](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) (najmä kap. 4 a Príloha B) a [Technologický stack a prax systému compliance a bezpečnosti – v1.0 (2026-10-06)](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) (najmä kap. 3 Dátové zóny a 4.4 IAM).

| NÁVRH – NIE JE PRÁVNA RADA. Tento dokument je metodický návrh a nie je právnym, pracovnoprávnym ani bezpečnostným poradenstvom. Pred zavedením ho treba overiť s advokátom (najmä odlíšenie závislej práce podľa Zákonníka práce pri freelanceroch), s bezpečnostným poradcom a pri utajovaných skutočnostiach s Národným bezpečnostným úradom (NBÚ). Konkrétne lehoty, limity a zoznamy systémov stanoví interný predpis. Právne predpisy sa uvádzajú v znení neskorších predpisov. |
| :---- |

## **1\. Účel a rozsah**

Dokument určuje, **ako** sa nová osoba dostane k firemnej technike, účtom a informáciám, **čo smie vidieť** podľa typu vzťahu a **ako sa prístupy odoberú v ten istý deň** pri ukončení. Vzťahuje sa na všetkých zamestnancov (TPP, aj na kratší pracovný čas, dohody mimo pracovného pomeru sa riadia procesom B s obmedzeniami podľa role) a na všetkých externých spolupracovníkov – fyzické osoby SZČO a dodávateľov služieb na zmluvu o dielo (proces A). Agenti a obchodní zástupcovia sa riadia osobitným postupom v Prílohe B dokumentu Technologický stack.  
Základné princípy:

> 1. **Jedna osoba \= jedna firemná identita** s MFA; žiadne zdieľané ani súkromné účty na firemné dáta.  
> 2. **Need-to-know a least privilege** – prístup sa prideľuje podľa role a konkrétnej úlohy, nie podľa pozície ani „pre istotu“.  
> 3. **Každá osoba má vlastníka vzťahu** (priamy nadriadený alebo interný zadávateľ zákazky), ktorý prístupy schvaľuje a zodpovedá za offboarding.  
> 4. **Offboarding v ten istý deň** – najneskôr do konca posledného pracovného dňa alebo okamžite pri mimoriadnom ukončení.  
> 5. **Utajované skutočnosti len s platnou bezpečnostnou previerkou NBÚ**, poučením a need-to-know; nikdy v bežnom IT prostredí.

## **2\. Dva procesy – porovnanie A (freelancer) a B (zamestnanec)**

| Oblasť | A – Freelancer (zmluva o dielo / SZČO) | B – Zamestnanec (TPP) |
| :---- | :---- | :---- |
| **Zmluvný základ** | Zmluva o dielo alebo rámcová zmluva o poskytovaní služieb s vymedzeným predmetom a výstupmi; compliance doložka, NDA, audit right, ochrana osobných údajov (čl. 28 GDPR, ak spracúva údaje), duševné vlastníctvo k výstupom. | Pracovná zmluva, popis pracovného miesta, záväzok mlčanlivosti, poučenie o BOZP, Kódex správania; prípadne dohoda o zákaze konkurencie. |
| **Kto iniciuje** | Interný zadávateľ (vlastník vzťahu) cez žiadosť o externú službu (proces Nákup – tok 4 v dokumente Nákup, objednávanie a platby). | Vedúci útvaru v spolupráci s HR. |
| **Preverenie** | Due diligence dodávateľa: výpis zo živnostenského / obchodného registra, DIČ/IČ DPH, referencie, konflikt záujmov, sankčný screening; overenie IBAN. | Overenie identity, vzdelania a praxe, referencie; pri citlivých rolách výpis z registra trestov (ak to umožňuje právny predpis a je to primerané). |
| **Riziko „švarcsystému“** | Freelancer nesmie vykonávať závislú prácu (podriadenosť, pevný pracovný čas, pokyny ako zamestnanec). Výstup sa definuje ako dielo / služba. Pri pochybnostiach posúdi Legal. | Neuplatňuje sa. |
| **Technika** | Prednostne firemný notebook (zapožičaný proti protokolu); výnimočne vlastné zariadenie len cez virtuálnu plochu / prehliadač s podmieneným prístupom, nikdy pre zónu Dôverné s možnosťou sťahovania. | Firemný notebook a podľa role firemný telefón. |
| **E-mail a identita** | Firemný účet s označením externého (napr. meno.priezvisko.ext@…), časovo obmedzený do konca zmluvy, MFA povinné. | Firemný účet bez časového obmedzenia, MFA povinné. |
| **Rozsah prístupov** | Len projektové priestory a systémy nevyhnutné pre predmet zmluvy; predvolene zóna Interné (výber), Dôverné len konkrétny priečinok so schválením vlastníka dát. | Podľa role; predvolene zóna Interné, Dôverné podľa útvaru a need-to-know. |
| **Školenia** | Skrátené úvodné školenie: informačná bezpečnosť, GDPR, ABAC, pravidlá exportnej kontroly pre technické údaje. | Plné úvodné školenie (kódex, ABAC, informačná bezpečnosť, GDPR, exportná kontrola podľa role), ročné opakovanie. |
| **Platnosť prístupov** | Automatické vypršanie k dátumu konca zmluvy; predĺženie len na základe novej objednávky / dodatku. | Do ukončenia pracovného pomeru; recertifikácia najmenej raz ročne. |

### **2.1 Diagram – proces A (freelancer)**

| A1. Žiadosť Vlastník vzťahu *predmet, doba, potrebné prístupy* | → | A2. Due diligence Nákup \+ CCO *registre, COI, screening* | → | A3. Zmluva Legal *ZoD, NDA, compliance doložka* |
| :---- | ----- | :---- | ----- | ----- |
|  |  |  |  | **↓** |
| **A6. Offboarding** Vlastník vzťahu \+ IT *v deň konca zmluvy* | **←** | **A5. Prístupy** IT / CISO *účet .ext, MFA, expirácia* | **←** | **A4. Onboarding** Vlastník vzťahu *školenie, technika, protokol* |

### **2.2 Diagram – proces B (zamestnanec TPP)**

| B1. Nábor Vedúci útvaru \+ HR *rola, profil prístupov* | → | B2. Preverenie HR (+ Bezp. manažér) *identita, referencie, NBÚ ak treba* | → | B3. Pracovná zmluva HR \+ štatutár *mlčanlivosť, kódex* |
| :---- | ----- | :---- | ----- | ----- |
|  |  |  |  | **↓** |
| **B6. Offboarding** HR \+ vedúci \+ IT *posledný pracovný deň* | **←** | **B5. Prístupy podľa role** IT / CISO *skupiny, MFA, recertifikácia* | **←** | **B4. Nástup (deň 1\)** HR \+ vedúci \+ IT *technika, školenia, BOZP* |

## **3\. Firemná technická politika**

| Prvok | Pravidlo | Zamestnanec (TPP) | Freelancer (ZoD / SZČO) |
| :---- | :---- | :---- | :---- |
| **Notebook** | Len spravované zariadenie (MDM), šifrovaný disk, EDR, automatické aktualizácie, zámok obrazovky, bez lokálnych administrátorských práv. Odovzdanie a vrátenie na protokol. | Firemný notebook – povinne. | Firemný notebook – štandard. Vlastné zariadenie len výnimočne so schválením CISO, iba cez virtuálnu plochu / webový prístup bez sťahovania; nikdy pre zónu Dôverné. |
| **Mobilný telefón** | Firemný telefón alebo súkromný telefón so spravovaným pracovným profilom (oddelenie firemných dát, možnosť vzdialeného vymazania pracovného profilu). Autentifikačná aplikácia pre MFA. | Firemný telefón podľa role (Obchod, vedenie, pohotovosť); ostatní pracovný profil. | Spravidla bez firemného telefónu; MFA cez autentifikačnú aplikáciu alebo hardvérový kľúč. Firemný e-mail v súkromnom telefóne len cez spravovanú aplikáciu. |
| **E-mail** | Výlučne firemná doména; zákaz preposielania na súkromné schránky a automatického presmerovania; externé zdieľanie Dôverných dát len cez schválené nástroje. | meno.priezvisko@… | meno.priezvisko.ext@… (zreteľné označenie externého), platnosť do konca zmluvy; komunikácia s klientmi spoločnosti len so súhlasom vlastníka vzťahu. |
| **VPN / vzdialený prístup** | Prístup do interných systémov len cez firemnú VPN alebo podmienený prístup (zero-trust) z spravovaného zariadenia; logovanie pripojení. | VPN profil podľa role. | VPN len do segmentu / aplikácií projektu, časovo obmedzený, bez prístupu do celej internej siete. |
| **MFA** | Povinné pre všetky účty bez výnimky (preferovane aplikácia alebo FIDO2 kľúč, nie SMS); pre privilegované účty FIDO2 kľúč. | Povinné. | Povinné; bez aktívneho MFA sa účet neaktivuje. |
| **Úložiská a USB** | Firemný tenant (Google Workspace / M365) podľa dátových zón; zákaz súkromných cloudov; USB nosiče len šifrované a evidované. | Podľa zóny. | Zakázané USB nosiče a lokálne kópie Dôverných dát. |
| **AI a online nástroje** | Do verejných AI nástrojov a prekladačov sa nesmú vkladať Dôverné ani Utajované údaje; povolené len schválené firemné nástroje. | Podľa zoznamu schválených nástrojov. | Rovnako; porušenie je dôvodom na okamžité ukončenie zmluvy. |

## **4\. Matica prístupov podľa dátových zón**

Legenda: **Áno** – štandardne; **Podľa role** – ak to vyžaduje pracovná náplň a schváli vlastník dát; **Výnimočne** – len konkrétny priečinok / záznam, časovo obmedzene, so schválením vlastníka dát a CISO, bez možnosti sťahovania; **Nie** – zakázané. Zóny zodpovedajú kapitole 3 dokumentu Technologický stack.

| Zóna | Príklady obsahu | Zamestnanec – bežná rola | Zamestnanec – citlivá rola (Financie, HR, Obchod, Legal, CCO) | Freelancer (ZoD / SZČO) | Kto schvaľuje |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **Verejné** | Web, katalógy, tlačové správy | Áno | Áno | Áno | Bez schválenia (publikovanie schvaľuje Marketing \+ Export Control) |
| **Interné** | Interné predpisy, intranet, bežná komunikácia, plány | Áno | Áno | Podľa role – len projektový priestor a potrebné predpisy, nie celý intranet | Vlastník vzťahu |
| **Dôverné** | Zmluvy, ceny, DD spisy, osobné údaje, HR, mzdy, CRM, technická dokumentácia | Podľa role (need-to-know) | Podľa role – len dáta vlastného útvaru | Výnimočne – konkrétny priečinok pre predmet zmluvy; nikdy HR, mzdy, celé CRM | Vlastník dát \+ CISO (pri freelancerovi aj CCO pri osobných údajoch) |
| **Utajované** | Utajované skutočnosti podľa zákona č. 215/2004 Z. z. | Nie – len s previerkou NBÚ, poučením a need-to-know | Nie – len s previerkou NBÚ, poučením a need-to-know | Nie – bez platnej previerky NBÚ príslušného stupňa vylúčené; s previerkou len ak to umožňuje utajovaná zmluva a bezpečnostná dokumentácia | Bezpečnostný manažér |

### **4.1 Matica prístupov k systémom (predvolené profily)**

| Systém | Zamestnanec – bežná rola | Freelancer | Poznámka |
| :---- | :---- | :---- | :---- |
| E-mail, kalendár, chat | Áno | Áno (účet .ext) | Externý nevidí celý adresár skupín, ak to nie je potrebné. |
| Zdieľané disky / projektové priestory | Podľa útvaru | Len projektový priestor | Zdieľanie „ktokoľvek s odkazom“ zakázané. |
| CRM | Podľa role (Obchod) | Nie; výnimočne čítanie konkrétnych záznamov | Žiadny export kontaktov. |
| ERP / účtovníctvo | Podľa role (Financie, Nákup) | Nie | Externý účtovník má osobitný profil podľa mandátnej zmluvy. |
| HR a mzdový systém | Len HR a určení vedúci | Nie | Osobné údaje zamestnancov – zóna Dôverné. |
| IAM / administrácia tenantu | Len IT správcovia (privilegovaný účet oddelený od bežného) | Nie | Výnimka pre externého IT správcu len so zmluvou, PAM, logovaním a časovo obmedzeným prístupom (just-in-time), schvaľuje CISO. |
| Vývojové / technické repozitáre | Podľa projektu | Podľa projektu – len konkrétne repozitáre | Exportne citlivé technické údaje len po posúdení Export Control. |
| Register partnerov, whistleblowing, incidenty | Nie (len CCO, CISO, určené osoby) | Nie | Podľa RACI v dokumente Technologický stack. |
| Utajované prostredie | Nie, okrem osôb určených Bezp. manažérom | Nie | Samostatná správa identít mimo firemného adresára. |

## **5\. Čo freelancer smie a nesmie vidieť**

| Smie (len v rozsahu predmetu zmluvy) | Nesmie (bez výnimky, ak nie je uvedené inak) |
| :---- | :---- |
| Verejné informácie a vybrané interné predpisy (bezpečnosť, kódex, pravidlá projektu). Projektový priestor, zadanie, technické podklady nevyhnutné pre dielo. Konkrétne repozitáre, testovacie prostredie a dáta (preferovane anonymizované / testovacie). Kontakty členov projektového tímu. Vlastné objednávky, akceptačné protokoly a faktúry. | **HR údaje** – osobné spisy, hodnotenia, nábor, zdravotné údaje. **Mzdy a odmeňovanie** – mzdový systém, výplatné pásky, bonusy. **Celé CRM** – zoznamy klientov, pipeline, ceny, export kontaktov. **Administráciu IAM / tenantu** – správa účtov, skupín, politík, logov (výnimka: zmluvný IT správca podľa 4.1). **Utajované skutočnosti bez platnej previerky NBÚ** príslušného stupňa, poučenia a need-to-know. Register partnerov a DD spisy, whistleblowing, interné vyšetrovania. Bankové účty, internetbanking, schvaľovanie platieb. Cenové kalkulácie a ponuky do tendrov, konzorciálne rokovania (ak nie sú predmetom zmluvy so schválením CCO). |

## **6\. Need-to-know – praktické pravidlá**

> * Prístup sa žiada **pre konkrétnu úlohu** (projekt, proces) s odôvodnením a dobou trvania; schvaľuje vlastník dát, nie žiadateľ.  
> * Prístupy sa prideľujú **cez skupiny podľa rolí**, nie individuálne výnimky; výnimky sa evidujú a majú dátum skončenia.  
> * Pri zmene role sa **staré prístupy odoberú** do 5 pracovných dní (žiadne hromadenie práv).  
> * **Recertifikácia**: bežné prístupy ročne, Dôverné a privilegované polročne, freelanceri pri každom predĺžení zmluvy.  
> * Senioritou ani funkciou (vrátane vedenia) nevzniká automatický prístup k Dôverným ani Utajovaným informáciám.  
> * Pri utajovaných skutočnostiach rozhoduje výlučne Bezpečnostný manažér podľa previerky, poučenia a need-to-know (zákon č. 215/2004 Z. z.).

## **7\. Onboarding checklist**

| Č. | Krok | A – Freelancer | B – Zamestnanec | Zodpovedá |
| :---- | :---- | :---- | :---- | :---- |
| 1 | Žiadosť / schválenie pozície alebo zákazky | ☐ Žiadosť o službu \+ schválená objednávka | ☐ Schválená pozícia | Vlastník vzťahu / vedúci |
| 2 | Preverenie | ☐ DD dodávateľa, registre, screening, COI | ☐ Identita, referencie, prípadne register trestov | Nákup \+ CCO / HR |
| 3 | Zmluva a vyhlásenia | ☐ ZoD \+ NDA \+ compliance doložka \+ čl. 28 GDPR | ☐ Pracovná zmluva \+ mlčanlivosť \+ Kódex | Legal / HR |
| 4 | Vyhlásenie o konflikte záujmov | ☐ | ☐ | CCO |
| 5 | Profil prístupov (zóny, systémy) schválený vlastníkom | ☐ Minimálny, s dátumom expirácie | ☐ Podľa role | Vlastník vzťahu |
| 6 | Firemný účet a MFA | ☐ Účet .ext, MFA, expirácia \= koniec zmluvy | ☐ Účet, MFA | IT / CISO |
| 7 | Technika na protokol | ☐ Notebook (príp. schválená výnimka) | ☐ Notebook, telefón podľa role | IT |
| 8 | VPN / vzdialený prístup | ☐ Len segment projektu | ☐ Podľa role | IT |
| 9 | Úvodné školenie | ☐ Skrátené (bezpečnosť, GDPR, ABAC, export) | ☐ Plné \+ BOZP | CCO / CISO / HR |
| 10 | Utajované skutočnosti (ak sa vyžadujú) | ☐ Previerka NBÚ \+ poučenie \+ určenie Bezp. manažérom | ☐ Previerka NBÚ \+ poučenie | Bezpečnostný manažér |
| 11 | Zápis do evidencie osôb a prístupov | ☐ Vrátane dátumu konca zmluvy | ☐ | IT / HR |

## **8\. Offboarding v ten istý deň**

Offboarding sa vykoná **najneskôr v posledný deň** zmluvy alebo pracovného pomeru; pri okamžitom ukončení, podozrení z porušenia alebo bezpečnostnom incidente **okamžite** (prístupy sa zablokujú pred oznámením osobe, ak to odporučí CISO alebo Legal).

### **8.1 Časová os**

| Kedy | Čo | Kto |
| :---- | :---- | :---- |
| D-5 (plánovaný odchod) | Oznámenie IT, CCO a Bezp. manažérovi; zoznam prístupov, zariadení, dokumentov; odovzdanie práce a dát (handover). | HR / vlastník vzťahu |
| Deň D – do 12:00 | Prevod vlastníctva súborov a schránky na nástupcu; kontrola, či nedošlo k neobvyklému sťahovaniu dát. | Vedúci \+ IT |
| Deň D – do konca pracovného času | Zablokovanie účtu, MFA, VPN, SSO relácií, prístupov do aplikácií a budovy; vrátenie techniky na protokol; vymazanie pracovného profilu v telefóne. | IT / CISO, správa budovy |
| Deň D | Odovzdanie utajovaných dokumentov podľa evidencie a poučenie o trvajúcej mlčanlivosti; odvolanie plných mocí a podpisových práv. | Bezp. manažér, Legal |
| D+1 až D+30 | Zmena zdieľaných hesiel a kódov; po 30 dňoch odstránenie / archivácia účtu podľa retenčných pravidiel; záverečný záznam v evidencii. | IT |

### **8.2 Offboarding checklist**

| Č. | Krok | A – Freelancer | B – Zamestnanec |
| :---- | :---- | :---- | :---- |
| 1 | Zablokovanie firemného účtu, MFA, SSO a VPN | ☐ | ☐ |
| 2 | Odobratie prístupov do aplikácií (CRM, ERP, repozitáre, projektové priestory) a zdieľaní | ☐ | ☐ |
| 3 | Deaktivácia vstupnej karty a prístupu do zabezpečených priestorov | ☐ | ☐ |
| 4 | Vrátenie notebooku, telefónu, nosičov, kľúčov (protokol) | ☐ | ☐ |
| 5 | Potvrdenie o vymazaní firemných dát zo súkromných zariadení (ak boli povolené) | ☐ Písomné vyhlásenie | ☐ |
| 6 | Odovzdanie utajovaných dokumentov a poučenie | ☐ ak relevantné | ☐ ak relevantné |
| 7 | Odvolanie plných mocí, podpisových práv, práv v internetbankingu | ☐ | ☐ |
| 8 | Akceptácia diela / záverečná faktúra; zablokovanie dodávateľa pre ďalšie objednávky, ak sa nepokračuje | ☐ | – |
| 9 | Exit pohovor a pripomenutie povinností (NDA, zákaz konkurencie, IP) | ☐ | ☐ |
| 10 | Zmena zdieľaných hesiel; záznam v evidencii; informovanie CCO / CISO / Bezp. manažéra | ☐ | ☐ |

## **9\. Zodpovednosti (RACI)**

Legenda: R – vykonáva, A – schvaľuje / nesie zodpovednosť, C – konzultovaný, I – informovaný.

| Činnosť | Vlastník vzťahu / vedúci | HR | Nákup | IT / CISO | CCO | Bezp. manažér | Legal |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Onboarding freelancera (A) | A | – | R | R | C | C | C |
| Onboarding zamestnanca (B) | A | R | – | R | I | C | I |
| Pridelenie prístupu do zóny Dôverné | R | – | – | C | C | – | – |
| Prístup k utajovaným skutočnostiam | I | – | – | C | – | A/R | – |
| Recertifikácia prístupov | R | I | – | A | I | C | – |
| Offboarding (v ten istý deň) | A | R | I | R | I | R | C |

*Poznámka:* Vlastník dát (napr. vedúci Financií pre ERP) schvaľuje prístup k svojim dátam; v RACI je zahrnutý v stĺpci „Vlastník vzťahu / vedúci“.

## **10\. Správa dokumentu**

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý návrh – onboarding, technická politika, matica prístupov, offboarding | NÁVRH – na právne, HR a bezpečnostné overenie |

Vlastníkom dokumentu je CISO v spolupráci s HR; časť o utajovaných skutočnostiach schvaľuje Bezpečnostný manažér. Revízia najmenej raz ročne a pri zmene systémov alebo organizácie.