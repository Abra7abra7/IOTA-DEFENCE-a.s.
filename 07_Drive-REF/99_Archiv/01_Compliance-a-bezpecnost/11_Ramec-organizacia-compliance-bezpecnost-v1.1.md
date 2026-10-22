**Organizačná štruktúra, compliance a bezpečnosť – rámec v1.1**

*Delta Defence a.s. · aktualizovaný rámec so zapracovaním uznesení predstavenstva U-01 až U-13 (dokument 06\)*  
Delta Defence a.s. · Verzia 1.1 · Dátum: 6\. 10\. 2026 · Vypracoval: Márian Stančík · Klasifikácia: Interné – Dôverné · Stav: **NÁVRH**

| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. Táto verzia nahrádza [Rámec v1.0](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) a zapracúva návrhy uznesení z [06 Rozhodnutia predstavenstva](https://docs.google.com/document/d/13uxplGUKF7SnboJJWRWwvhspKRk2zbBY3mkuu8G9UEI/edit) (U-01–U-09, U-11) a zistenia [Auditu medzier v1.0](https://docs.google.com/document/d/1oa3LVfSQMg650WgsDGcbmFZm4kkl-vFfYSmYSngAnXs/edit) (N1–N11). Je účinná až po prijatí uznesení predstavenstvom. Mená, sumy, lehoty a limity sú zámerne \[DOPLNIŤ\]. Pred zavedením overí advokát (stanovy, Obchodný zákonník – úprava a.s.) a bezpečnostný poradca (zákon č. 215/2004 Z. z., požiadavky NBÚ). |
| :---- |

## **Prehľad zmien oproti v1.0**

| Oblasť | v1.0 | v1.1 (opravené) | Zdroj |
| :---- | :---- | :---- | :---- |
| Orgány | „konateľ / spoločníci / štatutár“ | Valné zhromaždenie akcionárov, Predstavenstvo, Dozorná rada | U-01, N3 |
| Reporting 2\. línie | štatutárovi, DR „najmenej raz ročne“ | Predstavenstvu cez gestora; štvrťročný report aj DR; priamy prístup CCO a Bezp. manažéra k predsedovi DR | U-02, U-03, N1, N2 |
| Interný audit | reportuje DR | funkčne DR, administratívne predstavenstvu; nevykonáva 1\. ani 2\. líniu | U-04 |
| Legal | 2\. línia len v texte | 2\. línia pre právne riziko vo všetkých schémach a RACI | U-05, N4 |
| CISO vs IT | CISO aj prevádzka | IT prevádzka \= 1\. línia (R výkon); CISO \= 2\. línia (A politika, dohľad) | U-06, N7 |
| Štruktúra | bez HR, IT prevádzky, Kvality, DPO | doplnené | U-07, N9 |
| Due diligence | zápis do registra po zmluve (schéma 07\) | krok 1 „v preverovaní“ → krok 6 aktivácia po zmluve | U-08, N5 |
| Incidenty | lehoty bez jednotného zdroja | odkaz na jednotnú tabuľku dokumentu 09 kap. 9 | U-09, N6 |
| Terminológia | „zodpovedná osoba“ dvojznačne; „zabezpečené priestory“ | DPO podľa GDPR vs. zodpovedná osoba podľa zákona č. 54/2019 Z. z.; terminológia zákona č. 215/2004 Z. z. | U-11, N8, N11 |

# **1\. Úvod a rozsah**

## ---

**1.1 Účel**

Účelom rámca je stanoviť organizačnú štruktúru, rozdelenie zodpovedností a základné politiky v oblasti compliance a bezpečnosti tak, aby Delta Defence a.s. plnila požiadavky práva EÚ a SR, predchádzala korupcii, porušeniu sankcií a pravidiel exportnej kontroly, chránila utajované skutočnosti, osobné údaje a informačné aktíva a vedela preukázať primerané a účinné opatrenia (najmä na účely zákona č. 91/2016 Z. z. o trestnej zodpovednosti právnických osôb).

## **1.2 Rozsah**

Rámec sa vzťahuje na predstavenstvo, dozornú radu, všetkých zamestnancov a primerane na externých spolupracovníkov (SZČO, dodávatelia služieb, externý účtovník, externý IT správca), obchodných zástupcov a agentov v SR aj v zahraničí, partnerov v konzorciách a subdodávateľov – na vývoj, výrobu, nákup, predaj, export, účasť v tendroch a správu informácií.

## **1.3 Princíp troch línií ochrany**

Schéma: [02b Tri línie ochrany v1.1](https://drive.google.com/file/d/1JxwG5y71YjC-9SEMwSCxgASghFkuwtmC/view).

| Línia | Kto | Úloha |
| :---- | :---- | :---- |
| 1\. línia | Obchod (vrátane agentov), Nákup, Výroba, Financie, **HR**, **IT prevádzka**, **Kvalita** | Vlastnia riziká vo svojich procesoch, uplatňujú kontroly, vedú evidencie (dary, stretnutia, zmluvy, prístupy). IT prevádzka je R za výkon IAM, záloh, záplat, EDR a logovania. |
| 2\. línia | CCO, Bezpečnostný manažér (NBÚ), CISO, Export Control Officer (ECO), **Legal**, **DPO / koordinátor GDPR** | Politiky a metodika, schvaľovanie rizikových transakcií, monitoring, testovanie kontrol, školenia, posúdenie rizík. Reportujú predstavenstvu (kap. 1.4). |
| 3\. línia | Interný audit (interný / outsourcing \[DOPLNIŤ\]) | Nezávisle overuje dizajn a účinnosť kontrol 1\. a 2\. línie; funkčne reportuje dozornej rade, administratívne predstavenstvu. |

## **1.4 Nezávislosť a reporting 2\. línie**

> * CCO, Bezpečnostný manažér, CISO a ECO **reportujú predstavenstvu** prostredníctvom povereného člena predstavenstva – **gestora compliance** \[DOPLNIŤ\] (CCO, ECO, Legal, DPO) a **gestora bezpečnosti** \[DOPLNIŤ\] (Bezpečnostný manažér, CISO). Gestor nesmie byť zodpovedný za obchod / predaj; ak to nie je možné, reportuje sa celému predstavenstvu (U-02 a).  
> * Funkcie 2\. línie nie sú podriadené Obchodu, Nákupu, Výrobe ani Financiám; ich odmeňovanie nie je naviazané na obchodné výsledky (U-02 b).  
> * **Štvrťročný report** 2\. línie (compliance, utajované skutočnosti, kybernetická bezpečnosť, exportná kontrola) sa predkladá predstavenstvu a v rovnakom znení **dozornej rade** do \[DOPLNIŤ\] pracovných dní po skončení štvrťroka; **ročná správa** o účinnosti systému; **ad hoc hlásenie** bezodkladne pri závažnom zistení (U-03). Šablóna KPI/KRI: D23 (CCO). Utajované informácie len v neutajovanej forme.  
> * CCO a Bezpečnostný manažér majú **právo priameho prístupu k predsedovi dozornej rady** bez súhlasu predstavenstva, najmä ak sa podozrenie týka člena predstavenstva alebo ak predstavenstvo nekoná (U-02 c).  
> * Odvolanie CCO, CISO, Bezpečnostného manažéra alebo ECO oznámi predstavenstvo dozornej rade **vopred** s odôvodnením (U-02 d); rovnako zníženie ich rozpočtu.  
> * 2\. línia má neobmedzený prístup k informáciám a osobám potrebným na výkon funkcie a právo zastaviť rizikovú transakciu do rozhodnutia predstavenstva ([12 Podpisový poriadok](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) kap. 5).

# **2\. Organizačná štruktúra**

## ---

**2.1 Schéma**

Platná schéma: [01b Organizačná štruktúra v1.1](https://drive.google.com/file/d/1h80n6jkM5joB0PDeMDJkRc28EP0c9hyv/view) (nahrádza [schému 01 v1.0](https://drive.google.com/file/d/1IlmpLZsxgrlKj0iEiwUzQwNC6RAJiz8B/view)).

| Úroveň | Orgán / funkcia |
| :---- | :---- |
| Akcionári | **Valné zhromaždenie akcionárov** – najvyšší orgán; volí a odvoláva členov dozornej rady a podľa stanov aj predstavenstva \[DOPLNIŤ\] |
| Kontrola | **Dozorná rada** – kontrolný orgán; dohliada na výkon pôsobnosti predstavenstva; prijíma štvrťročné reporty 2\. línie a správy interného auditu |
| Riadenie | **Predstavenstvo** – štatutárny orgán; gestor compliance \[DOPLNIŤ\], gestor bezpečnosti \[DOPLNIŤ\] |
| 2\. línia | CCO · ECO · Legal · DPO (gestor compliance) \| Bezpečnostný manažér · CISO (gestor bezpečnosti) |
| 1\. línia | Obchod · Nákup · Výroba · Financie · HR · IT prevádzka · Kvalita |
| 3\. línia | Interný audit → funkčne dozorná rada |

## **2.2 Hierarchia a kompetencie**

| Funkcia | Podriadenosť / reporting | Kľúčové zodpovednosti a právny rámec |
| :---- | :---- | :---- |
| **Valné zhromaždenie akcionárov** | — | Pôsobnosť podľa Obchodného zákonníka a stanov; volí / odvoláva členov DR (a predstavenstva, ak to stanovy určujú) \[DOPLNIŤ\]. |
| **Dozorná rada** | Valné zhromaždenie | Dohľad nad výkonom pôsobnosti predstavenstva a systémom vnútornej kontroly; schvaľuje plán interného auditu; prijíma štvrťročné a ročné reporty 2\. línie; dohliada na nezávislosť 2\. a 3\. línie; prijíma priame podnety CCO a Bezpečnostného manažéra. |
| **Predstavenstvo** | Valné zhromaždenie; informuje DR | Riadi spoločnosť a koná v jej mene; celková zodpovednosť za compliance a bezpečnosť („tone from the top“); schvaľuje politiky, rozpočet, rizikový apetít a podpisový poriadok ([dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit)); menuje funkcie 2\. línie (U-10); rozhoduje o eskalovaných prípadoch; schvaľuje opatrenia riadenia kybernetických rizík. |
| **Chief Compliance Officer (CCO)** | Predstavenstvo (gestor compliance); priamy prístup k predsedovi DR | ABAC, sankčný compliance (s ECO), AML/KYC, konflikt záujmov, whistleblowing (koordinácia so zodpovednou osobou podľa zákona č. 54/2019 Z. z.), due diligence tretích strán (A, register partnerov), školenia, risk assessment, štvrťročný report. JD: [dok. 07](https://docs.google.com/document/d/1dGiRAkzxfogUno00VR0eU2j5EbKVYDfLaq16odA1LgY/edit). |
| **Bezpečnostný manažér (utajované skutočnosti / NBÚ)** | Predstavenstvo (gestor bezpečnosti); priamy prístup k predsedovi DR | Ochrana utajovaných skutočností podľa zákona č. 215/2004 Z. z.: personálna, administratívna, fyzická a objektová bezpečnosť (chránené priestory – terminológiu overí bezpečnostný poradca), bezpečnosť technických prostriedkov, kryptografická ochrana (s CISO), priemyselná bezpečnosť (bezpečnostná previerka podnikateľa), komunikácia s NBÚ. JD: [dok. 07](https://docs.google.com/document/d/1dGiRAkzxfogUno00VR0eU2j5EbKVYDfLaq16odA1LgY/edit). |
| **CISO** | Predstavenstvo (gestor bezpečnosti) | **2\. línia, A** za politiku informačnej bezpečnosti, štandardy, dohľad, testovanie kontrol, posúdenie rizík a hlásenia podľa zákona č. 69/2018 Z. z. v znení zákona č. 366/2024 Z. z. (NIS2), ISMS (ISO/IEC 27001). **Nevykonáva bežnú administráciu** a nemá trvalé privilegované účty mimo režimu break-glass (U-06). JD: [dok. 07](https://docs.google.com/document/d/1dGiRAkzxfogUno00VR0eU2j5EbKVYDfLaq16odA1LgY/edit). |
| **Export Control Officer (ECO)** | Predstavenstvo (gestor compliance); koordinácia s CCO | Klasifikácia položiek – nariadenie (EÚ) 2021/821, zákon č. 39/2011 Z. z.; výrobky obranného priemyslu – zákon č. 392/2011 Z. z.; licencie MH SR; sankcie EÚ a zákon č. 289/2016 Z. z.; end-user certifikáty, reexport, ICP. JD: [dok. 07](https://docs.google.com/document/d/1dGiRAkzxfogUno00VR0eU2j5EbKVYDfLaq16odA1LgY/edit). |
| **Legal** (2. línia) | Predstavenstvo | Právne riziko: zmluvné doložky, plné moci, posúdenie pôsobnosti predpisov (NIS2, DPO), oznamovacie povinnosti, interné vyšetrovania. Pri bežnej podpore zmlúv poradca 1\. línie, rozhodnutie o právnom riziku nezávislé od Obchodu (U-05). Forma: interný / externý advokát \[DOPLNIŤ\]. |
| **DPO / koordinátor ochrany osobných údajov** (2. línia) | Predstavenstvo | GDPR a zákon č. 18/2018 Z. z.; záznamy o spracovateľských činnostiach, DPIA, porušenia ochrany OÚ (s CISO). Povinnosť určiť DPO podľa čl. 37 GDPR posúdi Legal (U-13, R5). |
| **Interný audit** (3. línia) | Funkčne DR, administratívne predstavenstvo | Nezávislé overovanie kontrol (platby agentom, dary, prístupy, evidencia utajovaných skutočností, nastavenie banky voči podpisovému poriadku). Ročný plán schvaľuje DR. Štatút D24 \[DOPLNIŤ\]. |
| **Obchod** (1. línia) | Predstavenstvo | Vlastník vzťahov so zákazníkmi a agentmi; ABAC; register darov a stretnutí; iniciuje DD a zápis partnera do registra (krok 1). |
| **Nákup** (1. línia) | Predstavenstvo | Vendor onboarding, AVL, flow-down požiadaviek ([P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit)). |
| **Výroba** (1. línia) | Predstavenstvo | Fyzická bezpečnosť výroby, need-to-know k technickej dokumentácii, OT prístupy dodávateľov. |
| **Financie** (1. línia) | Predstavenstvo | 4 oči pri platbách, overenie IBAN, platby agentom proti dokladom, nastavenie banky podľa [dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit). |
| **HR** (1. línia) | Predstavenstvo | Nástup/odchod zamestnancov, popisy pracovných miest, menovacie dekréty (U-10), evidencia školení, disciplinárne konanie podľa Zákonníka práce, informovanie zamestnancov o monitoringu ([dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit) kap. 2.2). |
| **IT prevádzka** (1. línia) | Predstavenstvo (vedúci IT \[DOPLNIŤ\] / externý správca so SLA) | R za správu identít a prístupov, zálohy a obnovu ([dok. 08](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit)), záplaty, EDR, konfiguráciu logovania ([dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit)). |
| **Kvalita** (1. línia) | Predstavenstvo | Vstupná kontrola, falzifikáty, AQAP / ISO 9001\. |

*Kumulácia funkcií:* CCO a ECO možno kumulovať; 2\. línia nikdy s vedením Obchodu, Nákupu alebo Financií; **CISO nie s IT prevádzkou** – dočasne len so súhlasom predstavenstva, s dobou trvania \[DOPLNIŤ\] a kompenzačnými kontrolami (štvrťročná nezávislá kontrola, záznam každého privilegovaného prístupu, report DR). Kumulácia funkcie Bezpečnostného manažéra len ak to pripúšťa zákon č. 215/2004 Z. z. Matica nezlučiteľnosti: [dok. 07](https://docs.google.com/document/d/1dGiRAkzxfogUno00VR0eU2j5EbKVYDfLaq16odA1LgY/edit).

# **3\. Matica zodpovedností RACI**

---

R – vykonáva, A – nesie konečnú zodpovednosť, C – konzultovaný, I – informovaný. Pre každý proces práve jedno A.

| Proces | Predst. | CCO | Bezp. man. | CISO | IT prev. | ECO | Legal | Financie | HR | Obchod / Nákup | IA |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Nový partner / agent – DD a register (U-08) | I (A pri vysokom riziku\*) | A | C |  |  | C | C | C |  | R | I |
| Zmluva nad limit ([dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit)) | A | C | C |  |  | C | R | C |  | R | I |
| Vstup do konzorcia | A | C | C | C |  | C | R | C |  | R | I |
| Platba agentovi / provízia | I | C |  |  |  |  |  | A |  | R | I |
| Dar / pohostenie |  | A |  |  |  |  |  | I |  | R | I |
| Export / licencia | I | C | C |  |  | A | C | I |  | R | I |
| Prístup k utajovaným informáciám | I |  | A/R | C |  |  |  |  | C | I | I |
| Onboarding / offboarding osoby |  | C | C | C | R (technika) |  | C | I | R (zamestnanci) | A (vlastník vzťahu) | I |
| Správa identít, záloh, záplat, EDR |  |  |  | A (dohľad) | R |  |  |  |  |  | I |
| Kybernetický incident / hlásenie NBÚ | A (hlásenie) | I | C | R | R (izolácia) |  | C |  |  |  | I |
| Porušenie ochrany OÚ | I | A (DPO/CCO) |  | R | C |  | C |  |  |  | I |
| Incident s utajovanými skutočnosťami | I | I | A/R | C | C |  | C |  |  |  | I |
| Oznámenie whistleblowera | I\*\* | A/R |  |  |  |  | C |  |  |  | I\*\* |
| Menovania 2\. línie (U-10) | A | C |  |  |  |  | C |  | R |  | I |

\* Pri vysokom riziku schvaľuje aj predstavenstvo. \*\* Len anonymizovane; ak sa podnet týka člena predstavenstva, CCO informuje priamo predsedu DR. RACI nástrojov: Tech stack kap. 5 sa upraví podľa U-06 ([Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit)).

# **4\. Rozdelenie osôb podľa vzťahu a rizika**

---

Bez vecnej zmeny oproti [v1.0 kap. 4](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) (zamestnanec, obchodník, freelancer, externý účtovník, agent – najvyššie riziko, partner v konzorciu). Spresnenia v1.1:

> * Onboarding a offboarding zamestnancov vykonáva **HR**, technické prístupy **IT prevádzka**; vlastník vzťahu je A ([Onboarding a prístupy](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit), [schéma 03](https://drive.google.com/file/d/10_rGtPrZbInuF3w7BrMBjbcvLJ_e0Ha6/view)).  
> * Agent: plná moc s presným rozsahom a limitom \[DOPLNIŤ EUR\] – schvaľuje predstavenstvo ([dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) kap. 3.4–3.5); žiadna plná moc ani platba pred aktiváciou v registri.  
> * Externý IT správca: zmluva so SLA, MFA \+ JIT prístup schválený CISO, záznam relácií ([dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit) kap. 3–4).

# **5\. Osnova politík**

---

Politiky 5.1–5.11 ostávajú podľa [v1.0 kap. 5](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit); plné texty sú otvorená úloha D04. Všetky politiky schvaľuje **predstavenstvo**. Zmeny v1.1:

| Politika | Zmena v1.1 | Vlastník |
| :---- | :---- | :---- |
| 5.2 ABAC | Limity darov a pohostenia podľa [dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) kap. 3.3 (\[DOPLNIŤ EUR\]); verejný funkcionár vždy CCO vopred | CCO |
| 5.3 Third-Party DD | Poradie krokov podľa U-08 (kap. 9, Príloha A) | CCO |
| 5.5 Information Security | IT prevádzka R / CISO A; MFA, PAM, logovanie podľa [dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit); zálohy a obnova podľa [dok. 08](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit) | CISO |
| 5.6 Ochrana utajovaných skutočností | Terminológia výlučne podľa zákona č. 215/2004 Z. z. a vykonávacích predpisov NBÚ (U-11) | Bezpečnostný manažér |
| 5.8 Whistleblowing | „Zodpovedná osoba podľa zákona č. 54/2019 Z. z.“ – odlišná od DPO; kanál pri podnete proti členovi predstavenstva (U-13, R6) | CCO |
| 5.9 GDPR | „Zodpovedná osoba (DPO) podľa GDPR“ – po rozhodnutí podľa čl. 37 GDPR | DPO / CCO |
| Nové: Podpisový poriadok | [12 Limity schvaľovania a podpisový poriadok](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) | Predstavenstvo / Financie |
| Nové: BCP/DR | Kontinuita a obnova – [08 BCP/DR](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit) | CISO \+ Výroba \+ Financie |
| Nové: Logovanie a monitoring | Štandard – [09 Logging/cyber](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit) | CISO |

# **6\. Kontroly v praxi**

---

| Kontrola | Popis | Vlastník |
| :---- | :---- | :---- |
| Platby agentom | Len bankovým prevodom na účet na meno agenta v krajine sídla / pôsobenia; nikdy hotovosť ani tretie strany; len proti faktúre a dokladu o výkone; až po aktivácii v registri. | Financie |
| 4 oči a limity | Zadávateľ ≠ autorizátor; úrovne L1–L4 a CCO podľa [dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) (\[DOPLNIŤ EUR\]). | Financie / CCO |
| Ročné školenia | Kódex, ABAC, IB, GDPR; prísnejší program pre Obchod a Nákup; evidencia v HR; osobitné školenia pre utajované a export; školenie predstavenstva k NIS2. | CCO / CISO / Bezp. manažér / HR |
| Registre | Dary a pohostenie, stretnutia s verejnými funkcionármi, konflikty záujmov, partneri (stavy DD), plné moci, podpisové práva. | CCO / Financie |
| Risk assessment | Krajina × produkt × typ partnera; rizikový apetít schvaľuje predstavenstvo (U-13, R10). | CCO \+ ECO |
| Zmena IBAN | Len po nezávislom overení na vopred známom kontakte; logované a monitorované (alert P1 bez 4-eyes). | Financie |
| Preskúmanie prístupov | Ročne, privilegované štvrťročne; vykonáva IT prevádzka, dohliada CISO. | IT prevádzka / CISO / Bezp. manažér |
| Logovanie a monitoring | Minimálne zdroje, retencie \[DOPLNIŤ\], SIEM P1–P4 – [dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit). | CISO (A), IT prevádzka (R) |
| Zálohy a test obnovy | 3-2-1-1-0, testy obnovy, RTO/RPO \[DOPLNIŤ\] – [dok. 08](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit). | IT prevádzka (R), CISO (A) |

# **7\. Reakcia na incidenty**

---

Platná schéma: [08b Incident response v1.1](https://drive.google.com/file/d/1J_0XgArJD_RQPz1hAMeNjCR0-6LrbqpU/view). **Záväzné lehoty a adresáti sú výlučne v jednotnej tabuľke [dokumentu 09 kap. 9](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit)** (U-09); tento rámec ich len sumarizuje. Pred schválením ich potvrdí Legal podľa aktuálneho znenia predpisov.

| Typ incidentu | Vedie | Adresát a lehota (súhrn dok. 09 kap. 9\) | Právny rámec |
| :---- | :---- | :---- | :---- |
| Závažný kybernetický incident | CISO (A hlásenia: predstavenstvo) | NBÚ – včasné varovanie do 24 h, hlásenie do 72 h, záverečná správa do 1 mesiaca – ak je spoločnosť v pôsobnosti (posúdenie D05) | Zákon č. 69/2018 Z. z. v znení zákona č. 366/2024 Z. z.; smernica (EÚ) 2022/2555 |
| Porušenie ochrany osobných údajov | DPO / CCO \+ CISO | ÚOOÚ SR do 72 h od zistenia; dotknutým osobám bez zbytočného odkladu pri vysokom riziku | Čl. 33, 34 GDPR; zákon č. 18/2018 Z. z. |
| Bezpečnostný incident s utajovanými skutočnosťami | Bezpečnostný manažér | NBÚ **bezodkladne** (a pôvodca podľa zmluvy); formu a lehotu overí Bezpečnostný manažér | Zákon č. 215/2004 Z. z. |
| Podozrenie z korupcie / trestného činu | CCO \+ Legal | OČTK podľa posúdenia Legal; zastaviť platby, zachovať dôkazy, informovať predstavenstvo a DR | Trestný zákon; zákon č. 91/2016 Z. z. |
| Porušenie sankcií / exportu | ECO \+ Legal | Príslušný orgán (napr. MH SR) podľa posúdenia | Nariadenie (EÚ) 2021/821; zákony č. 392/2011, 39/2011, 289/2016 Z. z. |
| Zmluvné hlásenie | Legal / Obchod | Podľa zmlúv \[DOPLNIŤ\] | Zmluvy |

Interná eskalácia: P1 → CISO ihneď → gestor bezpečnosti → krízový štáb ([dok. 08](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit) kap. 6–7); obnova podľa DR runbookov ([dok. 08](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit) kap. 8). Plné playbooky, kontakty a šablóny hlásení – otvorená úloha D09; cvičenie najmenej raz ročne.

# **8\. Certifikácie a roadmapa**

---

Cieľové certifikácie (ISO 37001, ISO/IEC 27001, bezpečnostná previerka podnikateľa NBÚ, AQAP 2110\) a fázový plán ostávajú podľa [v1.0 kap. 8](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit). Rozsah ISMS a cieľ certifikácie rozhodne predstavenstvo (U-13, R7); záväzok k previerke podnikateľa a rozpočet (R8). Fáza 1 sa dopĺňa o: prijatie uznesení U-01–U-13, menovacie dekréty (U-10), podpisový poriadok ([dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit)), BIA a RTO/RPO ([dok. 08](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit)), posúdenie NIS2 (D05, [dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit) kap. 10).

# **9\. Prílohy**

## ---

**Príloha A – Checklist due diligence agenta / partnera (poradie podľa U-08)**

Schéma: [07b Due diligence partnera v1.1](https://drive.google.com/file/d/1QcnwcpikUDBphWLt2Tai1uz1b4L5JhTM/view).

| Krok | Kontrolný bod | Stav v registri | Splnené / dôkaz |
| :---- | :---- | :---- | :---- |
| 1 | Zápis partnera do registra partnerov pred akýmkoľvek rokovaním o obchodných podmienkach; určený vlastník vzťahu | V PREVEROVANÍ |  |
| 2 | Identifikácia (OR, sídlo, štatutári, vlastnícka štruktúra), KUV, sankčný screening (EÚ, OSN, UK, US), PEP, adverse media | V PREVEROVANÍ |  |
| 3 | Rizikové skóre krajiny (CPI) a sektora, interakcia s verejným sektorom, primeranosť odmeny voči benchmarku; stupeň DD | V PREVEROVANÍ |  |
| 4 | Dotazník, ABAC vyhlásenie, konflikt záujmov; vyhodnotenie red flags; rozhodnutie CCO (vysoké riziko aj predstavenstvo) alebo STOP | V PREVEROVANÍ / ZAMIETNUTÝ |  |
| 5 | Zmluva: compliance doložka, audit right, zákaz platieb tretím stranám, okamžité ukončenie; plná moc s rozsahom; IBAN na meno partnera v krajine sídla; podpis podľa [dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) | V PREVEROVANÍ |  |
| 6 | Aktivácia partnera v registri až po podpise zmluvy; ABAC školenie agenta; termín ročnej re-previerky | SCHVÁLENÝ |  |

Žiadna platba, záloha ani plná moc pred krokom 6\.

## **Príloha B – Checklist onboarding / offboarding**

Podľa [v1.0 Príloha B](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) a dokumentu [Onboarding a prístupy](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit); zodpovednosť: HR (zamestnanci), IT prevádzka (technika a prístupy), vlastník vzťahu (A), Bezpečnostný manažér (utajované). Offboarding v deň ukončenia vrátane odvolania plných mocí a podpisových práv ([dok. 12](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) kap. 7).

## **Príloha C – Súvisiace dokumenty a schémy**

| Dokument | Odkaz |
| :---- | :---- |
| Rámec v1.0 (nahradený) | [otvoriť](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) |
| 05 Audit medzier | [otvoriť](https://docs.google.com/document/d/1oa3LVfSQMg650WgsDGcbmFZm4kkl-vFfYSmYSngAnXs/edit) |
| 06 Rozhodnutia predstavenstva | [otvoriť](https://docs.google.com/document/d/13uxplGUKF7SnboJJWRWwvhspKRk2zbBY3mkuu8G9UEI/edit) |
| 07 Job descriptions CCO, CISO, Bezp. manažér, ECO | [otvoriť](https://docs.google.com/document/d/1dGiRAkzxfogUno00VR0eU2j5EbKVYDfLaq16odA1LgY/edit) |
| 08 BCP / DR | [otvoriť](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit) |
| 09 Logging, monitoring, cyber | [otvoriť](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit) |
| 10 P0 STATUS | [otvoriť](https://docs.google.com/document/d/1khTK6SmYlnwFW93e7U0duXK0SNSk62oZBK-C5HjxTNA/edit) |
| 12 Limity schvaľovania a podpisový poriadok | [otvoriť](https://docs.google.com/document/d/1Mbuomsyr-pHPGPeVXd7Regy6nxvOrxX6PTfKB2oJgvc/edit) |
| Tech stack | [otvoriť](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) |
| Onboarding a prístupy | [otvoriť](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) |
| Nákup, objednávanie a platby | [otvoriť](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) |
| Schémy: 01b · 02b · 07b · 08b (v1.1) | [01b](https://drive.google.com/file/d/1h80n6jkM5joB0PDeMDJkRc28EP0c9hyv/view) · [02b](https://drive.google.com/file/d/1JxwG5y71YjC-9SEMwSCxgASghFkuwtmC/view) · [07b](https://drive.google.com/file/d/1QcnwcpikUDBphWLt2Tai1uz1b4L5JhTM/view) · [08b](https://drive.google.com/file/d/1J_0XgArJD_RQPz1hAMeNjCR0-6LrbqpU/view) |
| INDEX schém | 13\_INDEX-Schemy-v1.1 (v priečinku) |

# **10\. Schválenie**

---

| Funkcia | Meno | Podpis | Dátum |
| :---- | :---- | :---- | :---- |
| Predseda predstavenstva | \[DOPLNIŤ\] |  |  |
| Člen predstavenstva (gestor compliance) | \[DOPLNIŤ\] |  |  |
| Člen predstavenstva (gestor bezpečnosti) | \[DOPLNIŤ\] |  |  |
| Na vedomie: predseda dozornej rady | \[DOPLNIŤ\] |  |  |

Vlastníkom dokumentu je CCO. Revízia najmenej raz ročne a pri podstatnej zmene právnej úpravy alebo obchodného modelu.

# **Správa dokumentu**

---

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý návrh rámca | Nahradený |
| 1.1 | 6\. 10\. 2026 | Márian Stančík | Zapracovanie U-01–U-09, U-11 (orgány a.s., reporting, Legal, CISO vs IT, HR/IT/Kvalita/DPO, poradie DD, lehoty IR, terminológia); väzby na dok. 07, 08, 09, 12 | NÁVRH – na schválenie predstavenstvom, právnu a bezpečnostnú revíziu |

