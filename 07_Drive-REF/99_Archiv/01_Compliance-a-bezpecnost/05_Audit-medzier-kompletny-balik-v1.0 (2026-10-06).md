**Audit medzier – kompletný balík compliance a bezpečnosti**

*Delta Defence a.s. · gap audit priečinka 01\_Compliance-a-bezpecnost voči cieľovému stavu pre SK výrobcu a predajcu v konzorciách s utajovanými skutočnosťami*  
Verzia 1.0 \| Dátum: 6\. 10\. 2026 \| Vypracoval: Márian Stančík \| Klasifikácia dokumentu: Interné – Dôverné (obsahuje popis slabých miest kontrol)

| NÁVRH – NIE JE PRÁVNA RADA. Tento audit je interné metodické posúdenie úplnosti dokumentácie, nie právne, bezpečnostné ani audítorské stanovisko a nenahrádza certifikačný audit (ISO/IEC 27001, ISO 37001), audit kybernetickej bezpečnosti podľa zákona č. 69/2018 Z. z. ani konanie Národného bezpečnostného úradu (NBÚ). Percentá zrelosti sú expertný odhad autora na základe obsahu priečinka k 6\. 10\. 2026, nie meranie. Právne predpisy sa uvádzajú v znení neskorších predpisov; konkrétne ustanovenia, lehoty a pôsobnosť je potrebné overiť s advokátom a bezpečnostným poradcom. Žiadne sumy, limity ani ceny sa v dokumente zámerne neuvádzajú. |
| :---- |

# **0\. Rozsah a metodika**

**Predmet auditu:** všetky súbory v priečinku [01\_Compliance-a-bezpecnost](https://drive.google.com/drive/folders/1KR6yWpbcPSXMf7ShKL2XWJjclu36Obr0) k 6\. 10\. 2026: 5 Google Docs (Rámec, Tech stack, Onboarding, Nákup/P2P, INDEX) a 10 obrázkov schém (sada 01–08 \+ 2 predchádzajúce verzie schém 03 a 04). Všetky dokumenty boli prečítané v plnom znení, schémy vizuálne skontrolované.  
**Kritérium:** čo potrebuje slovenská akciová spoločnosť vo výrobe a predaji, účastník konzorcií, s globálnou sieťou agentov a subdodávateľov a so stykom s utajovanými skutočnosťami, aby mala **úplnú, zavedenú a preukázateľnú** štruktúru: kompetencie/role/RACI, postupy, audit, logovanie, obnova/BCP/DR, kybernetická bezpečnosť (zákon č. 69/2018 Z. z. / NIS2, ISO/IEC 27001), ABAC (ISO 37001, zákon č. 91/2016 Z. z.), exportná kontrola a sankcie, GDPR, whistleblowing, personálna, fyzická, administratívna a objektová bezpečnosť utajovaných skutočností (zákon č. 215/2004 Z. z., NBÚ).  
**Hodnotiaca stupnica zrelosti (0–5):** 0 – neexistuje; 1 – zmienka / zámer; 2 – osnova alebo návrh procesu; 3 – schválený dokument s menovaným vlastníkom; 4 – zavedené, existujú záznamy a dôkazy; 5 – merané, testované a pravidelne preskúmavané (interný audit, cvičenia, manažérske preskúmanie). Status v matici: **HOTOVÉ** (návrh je obsahovo dostatočný na schválenie), **ČIASTOČNÉ** (téma je otvorená, chýba plný text, postup alebo záznam), **CHÝBA** (v balíku nie je).

# **1\. Verdikt**

| Celkový verdikt: balík NIE JE pripravený na zavedenie ani na externý audit; je to kvalitný architektonický základ. • Dokumentačná úplnosť (dizajn): cca 30 % cieľového balíka. • Preukázateľné zavedenie (dôkazy, záznamy, menovania): cca 0–5 % – v priečinku nie je žiadne menovanie, schválenie, register, záznam ani dôkaz o vykonaní kontroly; všetky dokumenty majú stav NÁVRH. • Zrelosť: úroveň 1–2 z 5 (najlepšie P2P a onboarding ≈ 2; logovanie, BCP/DR, zálohy, správa zraniteľností ≈ 0–1). • Silné stránky: konzistentná architektúra 3 línií, nezávislosť 2\. línie, dátové zóny s tvrdým oddelením utajovaného prostredia, praktické STOP podmienky v platbách agentom a P2P, IBAN lock, offboarding v ten istý deň, DD checklist agenta. • Kritické medzery (P0): (1) nie sú menované osoby ani zástupcovia pre žiadnu funkciu 2\. línie; (2) politiky sú len v osnove (11 politík bez plného textu); (3) úplne chýba BCP/DR, zálohovanie s testom obnovy, štandard logovania a monitoringu; (4) nevykonané posúdenie pôsobnosti zákona č. 69/2018 Z. z. v znení zákona č. 366/2024 Z. z. (registrácia, lehoty); (5) chýba bezpečnostná dokumentácia pre utajované skutočnosti a plán bezpečnostnej previerky podnikateľa; (6) chýba ICP exportnej kontroly a klasifikácia produktov; (7) schvaľovacie limity a podpisový poriadok sú \[DOPLNIŤ\]; (8) nekonzistentná línia reportingu medzi rámcom a schémami 01/02. |
| :---- |

## **1.1 Zrelosť podľa domén**

| Doména | Dizajn v balíku (odhad %) | Zrelosť 0–5 | Hlavný dôvod hodnotenia |
| :---- | :---- | :---- | :---- |
| Riadenie, organizácia, RACI | 55 % | 2 | Rámec kap. 2–3 dobrý; chýbajú mená, zástupcovia, organizačný a podpisový poriadok; orgány a.s. nesprávne pomenované („konateľ“, „spoločníci“); HR, IT prevádzka, Kvalita a DPO nie sú v štruktúre. |
| Politiky (plné texty) | 15 % | 1 | Rámec kap. 5 \= osnova 11 politík (účel, pravidlá, vlastník); žiadna politika nie je spracovaná ako samostatný schváliteľný interný predpis. |
| ABAC, dary, konflikt záujmov | 45 % | 2 | Pravidlá a STOP body existujú; chýbajú limity, šablóny registrov, sponzoring/charita, ISO 37001 prvky (risk assessment, manažérske preskúmanie). |
| Due diligence tretích strán, agenti | 55 % | 2 | Checklist agenta (Príloha A), schéma 07, tok v Tech stacku; chýba metodika skórovania, DD dotazník, benchmark provízií, kontinuálny monitoring. |
| Exportná kontrola a sankcie | 30 % | 1 | Právny rámec správny; chýba ICP, klasifikácia položiek, SOP sankčného screeningu, evidencia a archivácia, postup pri nehmotnom prenose technológií. |
| Nákup, platby (P2P) | 60 % | 2 | Najlepší dokument balíka; limity \[DOPLNIŤ\], chýba cestovná smernica, smernica o pokladni a kartách, AVL, kontrola falzifikátov ako postup. |
| Onboarding, IAM, prístupy | 60 % | 2 | Dobré matice prístupov; chýba štandard privilegovaných prístupov (PAM), SOP recertifikácie, job descriptions s profilmi prístupov. |
| GDPR | 20 % | 1 | Len osnova 5.9 a incident 72 h; chýbajú záznamy o spracovateľských činnostiach, rozhodnutie o DPO, informačné povinnosti, retenčný plán, DPIA, SCC/TIA register. |
| Whistleblowing | 25 % | 1 | Kanál načrtnutý; chýba vnútorný predpis podľa zákona č. 54/2019 Z. z., menovanie zodpovednej osoby, šablóny a evidencia. |
| Kybernetická bezpečnosť / ISMS / NIS2 | 20 % | 1 | Ciele a nástroje uvedené; chýba posúdenie pôsobnosti, analýza rizík, SoA, bezpečnostné politiky ISMS. |
| Logovanie a monitoring | 5 % | 0–1 | Iba zmienky („logovanie prístupu“, „SIEM cieľovo“); žiadny štandard zdrojov, retencie, integrity a revízie logov. |
| Zálohy, BCP, DR | 5 % | 0–1 | Iba „3-2-1 \+ test obnovy“ v Tech stacku; žiadna BIA, RPO/RTO, plán kontinuity, DR runbook ani test. |
| Reakcia na incidenty | 30 % | 1–2 | Rámec kap. 7 \+ schéma 08; chýbajú playbooky, kontakty, šablóny hlásení, záznamník incidentov, cvičenia. |
| Utajované skutočnosti (NBÚ) | 20 % | 1 | Správne oddelenie a princípy; chýba bezpečnostná dokumentácia, plán previerok osôb a podnikateľa, režim objektov a chránených priestorov, administratívna bezpečnosť ako postup. |
| Interný audit a monitoring 2\. línie | 15 % | 1 | Funkcia definovaná; chýba štatút interného auditu, ročný plán, metodika testovania, plán monitoringu 2\. línie. |
| Školenia a povedomie | 20 % | 1 | Obsah školení vymenovaný; chýba kalendár, cieľové skupiny, testy, evidencia. |
| Záznamy, dôkazy, retencia | 10 % | 1 | Princíp „dôkaz pre audit“ v Tech stacku; chýba registratúrny poriadok/plán a matica uchovávania dôkazov. |
| Reporting štatutárovi a DR | 10 % | 1 | Frekvencia nejednotná (rámec: najmenej ročne; schéma 01: štvrťročne); chýba šablóna a sada KPI/KRI. |

# **2\. Čo už máme – inventár**

| Dokument / schéma | Čo pokrýva | Kvalita | Hlavné nedostatky |
| :---- | :---- | :---- | :---- |
| [Organizačná štruktúra, compliance a bezpečnosť – rámec v1.0](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) | Účel, rozsah, 3 línie, nezávislosť 2\. línie, org. schéma, kompetencie 12 funkcií, RACI 11 procesov, segmentácia osôb podľa rizika, osnova 11 politík, kontroly, incidenty (4 typy), certifikácie, fázový plán, DD checklist agenta, on/offboarding checklist. | **Vysoká** | Orgány a.s. nepresné; žiadne mená; politiky len osnova; chýba BCP/DR, logovanie, GDPR detail; RACI bez Výroby/Kvality/HR/IT prevádzky; frekvencia reportingu DR „najmenej raz ročne“. |
| [Technologický stack a prax – v1.0](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) | Životný cyklus agenta, týždenný kalendár, 3 línie v praxi, dátové zóny, stack po vrstvách (min./cieľ), integrácie, RACI nástrojov, fázový checklist, mini-postupy platba agentovi a onboarding agenta. | **Vysoká** | Stack bez štandardov (logovanie, zálohy, šifrovanie, patching len heslovito); CISO je súčasne A aj R pre IT prevádzku – konflikt 2\. vs 1\. línie; bez cieľových RPO/RTO. |
| [Onboarding a prístupy – zamestnanec vs freelancer v1.0](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) | Procesy A/B, technická politika (notebook, mobil, e-mail, VPN, MFA, USB, AI nástroje), matica zón a systémov, need-to-know, checklisty, offboarding časová os, RACI. | **Vysoká** | Chýba HR v org. štruktúre rámca; odkazuje na „popis pracovného miesta“, ktorý neexistuje; recertifikácia bez SOP a záznamu; PAM len zmienka; monitoring zamestnancov bez právneho posúdenia (Zákonník práce § 13 ods. 4, GDPR). |
| [Nákup, objednávanie a platby – proces v1.0](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) | P2P tok, kategórie (event, dary, IT, komponenty, služby, cestovné), limity 1-eye/4-eyes/CCO, záväzné pravidlá, 4 toky, vendor onboarding checklist, RACI, 10 STOP podmienok. | **Vysoká** | Všetky limity \[DOPLNIŤ\]; cestovné len skrátený tok; chýba AVL ako dokument, postup proti falzifikátom, smernica o pokladni a platobných kartách; zákon č. 394/2012 Z. z. o obmedzení platieb v hotovosti nie je zmienený. |
| [00\_INDEX – Schémy a procesy v1.0](https://docs.google.com/document/d/1jx6cFVPe6w4Pw1NS_hzGn5kIdsq04PLHOT9dh0LiRpA/edit) | Zoznam schém 01–08 s odkazmi, súvisiace dokumenty, predchádzajúce verzie, poradie čítania. | **Stredná** | Neobsahuje register všetkých dokumentov s verziou, vlastníkom a stavom; tvrdí „CCO/CISO/Bezpečnosť reportujú do DR“ – v rozpore s rámcom. |
| [Schéma 01](https://drive.google.com/file/d/1IlmpLZsxgrlKj0iEiwUzQwNC6RAJiz8B/view) – Organizačná štruktúra | Vizuálna hierarchia, nezávislosť, utajované oddelene. | **Stredná** | Reporting 2\. línie do DR (rámec: štatutárovi s prístupom k DR); „štvrťročný compliance report“ nie je v texte rámca. |
| [Schéma 02](https://drive.google.com/file/d/1mYHyoPDqv5c-CEvz43rzQgjUsCFUZTQY/view) – Tri línie | 1./2./3. línia. | **Stredná** | Legal chýba v 2\. línii (v rámci je). |
| [Schéma 03](https://drive.google.com/file/d/10_rGtPrZbInuF3w7BrMBjbcvLJ_e0Ha6/view) – Onboarding Freelancer vs TPP | Spoločná brána, rozdiely A/B. | **Stredná** | „Prístupy podľa job description“ – JD neexistujú. Duplicitná staršia verzia [03 (predchádzajúca)](https://drive.google.com/file/d/1Il21S8Py9t5tku_A0oO5CDPHs5VtAinV/view) v tom istom priečinku. |
| [Schéma 04](https://drive.google.com/file/d/1gNxGVKUbCaMkilzq7cv1o1WZWtMca-Om/view) – P2P | Tok \+ STOP pravidlá. | **Stredná** | Zjednodušené: chýba 3-way match, konflikt záujmov, delenie nákupu. Duplicitná staršia verzia [04-P2P (predchádzajúca)](https://drive.google.com/file/d/1tydn5P3pbTIHVuzsApkCpjGEWnn9tsmv/view). |
| [Schéma 05](https://drive.google.com/file/d/18dzCOe1RYn7n4GpjySAi9Sz7gk9bVeQf/view) – Dátové zóny | 4 zóny, pravidlá, smer citlivosti. | **Vysoká** | Bez väzby na označovanie (štítky) a šifrovací štandard. |
| [Schéma 06](https://drive.google.com/file/d/1v6lOnwb9o1pY0gi4bcz_51wkyhNlsSay/view) – Platba agentovi | Tok 6 krokov, STOP pravidlá. | **Vysoká** | V súlade s Tech stack Príloha A. |
| [Schéma 07](https://drive.google.com/file/d/1lkFKXPlDpuPuPk685D4v7PQBU7HgDkC0/view) – Due diligence partnera | Tok, výstup skóre, checklist. | **Stredná** | Zápis do registra je krok 6 (po zmluve) – v rozpore s Tech stackom (registrácia je krok 1, „bez zápisu sa nesmie rokovať“). |
| [Schéma 08](https://drive.google.com/file/d/1jOGWJlyEH-Kcxahrm7t4-Cd082yTKPmo/view) – Incident response | 6 krokov, 4 typy, pravidlá. | **Stredná** | Lehota NIS2 len „orientačne rýchle“ (rámec uvádza 24 h / 72 h / 1 mesiac); chýba incident owner per typ, kontakty a väzba na BCP. |

# **3\. Matica pokrytia**

| Téma | Status | Odkaz v balíku | Medzera (gap) |
| :---- | :---- | :---- | :---- |
| Organizačná štruktúra a orgány a.s. | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2; [Schéma 01](https://drive.google.com/file/d/1IlmpLZsxgrlKj0iEiwUzQwNC6RAJiz8B/view) | Opraviť na predstavenstvo / valné zhromaždenie akcionárov / dozorná rada (Obchodný zákonník – úprava akciovej spoločnosti); doplniť HR, IT prevádzku, Kvalitu, DPO; organizačný poriadok. |
| Kompetencie a menovania osôb | **CHÝBA** | — | Žiadne menovacie dekréty, zástupcovia ani kumulácie; pozri kap. 5\. |
| RACI hlavných procesov | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 3; [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 5; [Onboarding](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) 9; [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) 8 | Chýba RACI pre BCP/DR, zmeny, zálohy, exportnú klasifikáciu, NBÚ previerky, interný audit, reporting DR, retenciu. |
| Podpisový poriadok a schvaľovacie limity | **CHÝBA** | [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) 4 (\[DOPLNIŤ\]) | Limity a podpisové právo neurčené; bez nich nefungujú 4-eyes ani CCO prahy. |
| Popisy pracovných miest (CCO, CISO, Bezp. manažér, ECO) | **CHÝBA** | — | Kvalifikácia, nezávislosť, zastupovanie, previerka NBÚ, KPI. |
| Kódex správania | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.1 | Len osnova; chýba plný text a podpisový formulár. |
| ABAC politika | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.2; [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) 6.1 | Plný text, limity darov a pohostenia, sponzoring a charita, politické príspevky, ABAC risk assessment. |
| Register darov, pohostení a stretnutí | **ČIASTOČNÉ** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.2 | Šablóna (polia), workflow schválenia a mesačná kontrola nie sú vytvorené. |
| Konflikt záujmov | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.7; [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) 5 | Formulár vyhlásenia a register chýbajú. |
| Due diligence tretích strán | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) Príl. A; [Schéma 07](https://drive.google.com/file/d/1lkFKXPlDpuPuPk685D4v7PQBU7HgDkC0/view) | Metodika rizikového skóre (váhy, prahy), DD dotazník, benchmark provízií, kontinuálny monitoring. |
| Agenti a plné moci | **HOTOVÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 4.2; [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) Príl. B; [Schéma 06](https://drive.google.com/file/d/1v6lOnwb9o1pY0gi4bcz_51wkyhNlsSay/view) | Dizajn dostatočný; chýba šablóna agentskej zmluvy a plnej moci. |
| Konzorciá a subdodávatelia (flow-down) | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.11 | Zmluvné doložky (knižnica), súťažnoprávny protokol výmeny informácií (clean team). |
| Sankčný screening | **ČIASTOČNÉ** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.1 | SOP: rozsah strán, zdroje, frekvencia, vyhodnotenie zhôd, 50 % vlastníctvo/kontrola, dokumentovanie. |
| Exportná kontrola – ICP a klasifikácia | **CHÝBA** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.4 (osnova) | ICP podľa odporúčania Komisie (EÚ) 2019/1318; klasifikačný register položiek; licencie; uchovávanie záznamov podľa nariadenia (EÚ) 2021/821; nehmotné prenosy. |
| Preverovanie zahraničných investícií | **CHÝBA** | — | Posúdiť, či sa na spoločnosť vzťahuje zákon č. 497/2022 Z. z. o preverovaní zahraničných investícií (pri zmene akcionárov / vstupe investora) – overiť s advokátom. |
| AML / KYC, hotovosť | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.10 | Posúdenie, či je spoločnosť povinnou osobou podľa zákona č. 297/2008 Z. z.; doplniť zákon č. 394/2012 Z. z. o obmedzení platieb v hotovosti. |
| P2P a platby | **HOTOVÉ** | [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit); [Schéma 04](https://drive.google.com/file/d/1gNxGVKUbCaMkilzq7cv1o1WZWtMca-Om/view) | Dizajn dostatočný okrem limitov; doplniť pokladňu a karty. |
| Cestovné náhrady (travel & expense) | **ČIASTOČNÉ** | [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) 3 | Samostatná smernica podľa zákona č. 283/2002 Z. z.; cesty do rizikových krajín (travel security, „clean“ zariadenia). |
| Onboarding / offboarding | **HOTOVÉ** | [Onboarding](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit); [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) Príl. B; [Schéma 03](https://drive.google.com/file/d/10_rGtPrZbInuF3w7BrMBjbcvLJ_e0Ha6/view) | Dizajn dostatočný; chýba záznam (formulár) a väzba na HR systém. |
| Riadenie prístupov a recertifikácia | **ČIASTOČNÉ** | [Onboarding](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) 6; [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 6 | SOP recertifikácie (kto, kedy, záznam, nápravy) a šablóna. |
| Privilegované prístupy (PAM) | **CHÝBA** | [Onboarding](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) 4.1 (zmienka) | Štandard: oddelené admin účty, FIDO2, JIT, break-glass, logovanie relácií. |
| GDPR – program | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.9 | Záznamy o spracovateľských činnostiach (čl. 30), rozhodnutie o DPO (čl. 37), informácie dotknutým osobám (čl. 13/14), DPIA, register SCC/TIA, postup práv dotknutých osôb, kamerový systém. |
| Whistleblowing | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.8; [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.2 | Vnútorný predpis podľa zákona č. 54/2019 Z. z., menovanie zodpovednej osoby, evidencia, lehoty, zastupovanie pri konflikte. |
| ISMS / ISO/IEC 27001 | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 5.5; [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.4 | Rozsah ISMS, analýza rizík, vyhlásenie o aplikovateľnosti (SoA), politiky, ciele, manažérske preskúmanie. |
| Pôsobnosť zákona č. 69/2018 Z. z. (NIS2) | **CHÝBA** | — | Písomné posúdenie podľa sektorov a veľkosti v znení zákona č. 366/2024 Z. z.; ak áno – registrácia a lehoty. |
| Klasifikácia a označovanie informácií | **HOTOVÉ** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 3; [Schéma 05](https://drive.google.com/file/d/18dzCOe1RYn7n4GpjySAi9Sz7gk9bVeQf/view) | Dizajn dostatočný; chýba technické nastavenie štítkov a väzba na šifrovanie. |
| Šifrovanie a správa kľúčov | **CHÝBA** | [Onboarding](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) 3 (zmienka) | Štandard šifrovania (disky, prenos, e-mail, zálohy, kľúče); utajované len podľa NBÚ. |
| Logovanie a monitoring | **CHÝBA** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.4 (zmienka) | Štandard zdrojov logov, retencie, integrity, prístupu, revízie, SIEM use-cases; právne posúdenie monitoringu zamestnancov. |
| Zálohovanie a test obnovy | **CHÝBA** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.4 (zmienka 3-2-1) | Štandard zálohovania, rozvrh, offline/nemenná kópia, test obnovy so záznamom. |
| BCP / DR / BIA | **CHÝBA** | — | BIA, RPO/RTO, plán kontinuity, DR runbooky, krízový štáb, cvičenia (ISO 22301 ako referencia). |
| Riadenie zmien (change management) | **CHÝBA** | — | Postup zmien IT a OT/výroby, CAB, núdzové zmeny, väzba na zálohy a logovanie. |
| Inventár aktív (HW, SW, dáta, cloud) | **CHÝBA** | [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) 6.2 (evidencia majetku) | Register aktív s vlastníkom, klasifikáciou, umiestnením dát; zoznam aplikácií. |
| Patch & vulnerability management | **CHÝBA** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.4 (cieľovo) | SLA záplat podľa kritickosti, skenovanie, penetračné testy, výnimky. |
| Reakcia na incidenty – playbooky | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 7; [Schéma 08](https://drive.google.com/file/d/1jOGWJlyEH-Kcxahrm7t4-Cd082yTKPmo/view) | 4 playbooky, kontakty, šablóny hlásení (NBÚ, ÚOOÚ SR, OČTK), záznamník, cvičenia. |
| Bezpečnosť dodávateľov IKT – kontinuálny monitoring | **ČIASTOČNÉ** | [Nákup/P2P](https://docs.google.com/document/d/1TAp4WyZ7ajM9fD-noDJgE0fEqGk2QgG9DnTmyQx3mXA/edit) 7 bod 8 | Bezpečnostný dotazník, zmluvné minimum, ročné prehodnotenie, register kritických dodávateľov. |
| Secure SDLC (ak vyvíja SW/firmvér) | **CHÝBA** | — | Bezpečný vývoj, code review, SBOM, správa zraniteľností produktov; posúdiť nariadenie (EÚ) 2024/2847 (Cyber Resilience Act) pre produkty mimo výlučne obranného použitia. |
| Utajované – personálna bezpečnosť | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2.2, 5.6 | Zoznam funkcií vyžadujúcich previerku a jej stupeň, plán podania, poučenia, evidencia. |
| Utajované – priemyselná bezpečnosť (previerka podnikateľa) | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 8 | Plán a podklady pre bezpečnostnú previerku podnikateľa podľa zákona č. 215/2004 Z. z. |
| Utajované – administratívna bezpečnosť | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2.2 | Postup evidencie, manipulácie, prepravy, kópií a ničenia utajovaných písomností; registratúra. |
| Utajované – fyzická a objektová bezpečnosť | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2.2; [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.4 | Plán ochrany objektu a chránených priestorov, režim vstupu, kľúčový režim, návštevy. |
| Utajované – bezpečnosť technických prostriedkov a kryptografia | **ČIASTOČNÉ** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.4 | Bezpečnostný projekt a certifikácia technických prostriedkov podľa požiadaviek NBÚ. |
| Fyzická bezpečnosť bežných priestorov (výroba, sklad) | **CHÝBA** | — | Zóny areálu, kamerový systém (GDPR), návštevy, sklad citlivých komponentov. |
| Školenia – kalendár a evidencia | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 6; [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.2 | Ročný kalendár, cieľové skupiny, testy, evidencia; školenie štatutárov (NIS2). |
| Interný audit | **ČIASTOČNÉ** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2.2 | Štatút, ročný plán, metodika, šablóna správy, sledovanie náprav. |
| Reporting štatutárovi a DR | **CHÝBA** | — (zmienky) | Šablóna správy, KPI/KRI, frekvencia (zjednotiť). |
| Registratúra, retencia, dôkazy | **ČIASTOČNÉ** | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 4.5 | Registratúrny poriadok a plán, matica retencie dôkazov kontrol. |
| Disciplinárne a nápravné opatrenia | **CHÝBA** | — | Postup pri porušení (v súlade so Zákonníkom práce), zmluvné sankcie pre externých. |
| Interné vyšetrovania | **CHÝBA** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 7 (zmienka) | Postup, nezávislosť, zachovanie dôkazov, ochrana práv vyšetrovaných. |
| Kvalita (ISO 9001 / AQAP 2110\) | **CHÝBA** | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 8 | Mimo rozsahu tohto balíka, ale RACI a väzby (kontrola falzifikátov) treba nadviazať. |
| Riadenie dokumentácie (verzie, schvaľovanie) | **ČIASTOČNÉ** | [INDEX](https://docs.google.com/document/d/1jx6cFVPe6w4Pw1NS_hzGn5kIdsq04PLHOT9dh0LiRpA/edit) | Register dokumentov s verziou, vlastníkom, stavom, dátumom revízie. |

**Súhrn matice:** 50 tém – HOTOVÉ 4, ČIASTOČNÉ 26, CHÝBA 20\.

## **3.1 Nekonzistencie medzi dokumentmi (opraviť pred schválením)**

| \# | Nekonzistencia | Kde | Návrh riešenia |
| :---- | :---- | :---- | :---- |
| N1 | Reporting 2\. línie: rámec – štatutárovi s priamym prístupom k DR; schéma 01 a INDEX – „reportujú do DR“. | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 1.4, 2.2 vs [Schéma 01](https://drive.google.com/file/d/1IlmpLZsxgrlKj0iEiwUzQwNC6RAJiz8B/view), [INDEX](https://docs.google.com/document/d/1jx6cFVPe6w4Pw1NS_hzGn5kIdsq04PLHOT9dh0LiRpA/edit) | Rozhodnúť štatutárom; odporúčanie: administratívne štatutárovi, funkčne priamy prístup k DR (ako v rámci); prekresliť schému 01 a upraviť INDEX. |
| N2 | Frekvencia reportingu DR: „najmenej raz ročne“ vs „štvrťročný compliance report“. | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 1.4 vs [Schéma 01](https://drive.google.com/file/d/1IlmpLZsxgrlKj0iEiwUzQwNC6RAJiz8B/view) | Zjednotiť (návrh: štvrťročne prehľad, ročne plná správa) v šablóne reportingu. |
| N3 | Orgány: „konateľ / predstavenstvo“, „valné zhromaždenie / spoločníci“ – pre a.s. nesprávne. | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2.1–2.2 | Pre a.s.: predstavenstvo, valné zhromaždenie akcionárov, dozorná rada; zákaz konkurencie členov predstavenstva podľa Obchodného zákonníka. |
| N4 | Legal je v rámci 2\. línia, v schéme 02 chýba. | [Schéma 02](https://drive.google.com/file/d/1mYHyoPDqv5c-CEvz43rzQgjUsCFUZTQY/view) | Doplniť Legal do 2\. línie. |
| N5 | Poradie DD: Tech stack – zápis do registra je krok 1; schéma 07 – krok 6 po zmluve. | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 1.1 vs [Schéma 07](https://drive.google.com/file/d/1lkFKXPlDpuPuPk685D4v7PQBU7HgDkC0/view) | Schéma 07: krok 1 \= zápis do registra (stav „v preverovaní“), krok 6 \= aktivácia partnera. |
| N6 | Lehoty NIS2: rámec 24 h / 72 h / 1 mesiac; schéma 08 „orientačne rýchle, over“. | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 7 vs [Schéma 08](https://drive.google.com/file/d/1jOGWJlyEH-Kcxahrm7t4-Cd082yTKPmo/view) | Po overení aktuálneho znenia zákona č. 69/2018 Z. z. uviesť rovnaké lehoty a adresáta v oboch. |
| N7 | CISO je A/R pre IAM, EDR, zálohy (prevádzka \= 1\. línia) aj nezávislá 2\. línia. | [Tech stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) 5; [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 3 | Oddeliť IT prevádzku (R, 1\. línia – interný IT / externý správca) od CISO (A pre politiku a dohľad). |
| N8 | „Zodpovedná osoba“ – v GDPR (DPO) aj v zákone č. 54/2019 Z. z. (whistleblowing). | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2.2 | V slovníku pojmov rozlíšiť „zodpovedná osoba (DPO)“ a „zodpovedná osoba podľa zákona č. 54/2019 Z. z.“. |
| N9 | HR vystupuje v Onboardingu ako R, v organizačnej štruktúre rámca chýba. | [Onboarding](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) 9 vs [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2 | Doplniť HR (1. línia) do štruktúry a RACI. |
| N10 | Duplicitné staršie schémy 03 a 04 v rovnakom priečinku; dokumenty nemajú NN\_ prefixy. | [INDEX](https://docs.google.com/document/d/1jx6cFVPe6w4Pw1NS_hzGn5kIdsq04PLHOT9dh0LiRpA/edit) 3 | Presunúť do 99\_Archiv; premenovať Docs podľa stromu v kap. 7\. |
| N11 | Terminológia utajovaných: „zabezpečené priestory“ – zákon č. 215/2004 Z. z. používa vlastnú terminológiu (napr. objekt, chránený priestor). | [Rámec](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) 2.2, 5.6 | Zjednotiť terminológiu so zákonom a vykonávacími predpismi NBÚ (overí bezpečnostný poradca). |

## **3.2 Kontrola právnych odkazov**

| Odkaz v balíku | Posúdenie | Poznámka / odporúčanie |
| :---- | :---- | :---- |
| Zákon č. 69/2018 Z. z. o kybernetickej bezpečnosti; smernica (EÚ) 2022/2555 (NIS2) | Správne, neúplné | Doplniť, že NIS2 bola transponovaná zákonom č. 366/2024 Z. z. (novela zákona č. 69/2018 Z. z., účinnosť od 1\. 1\. 2025). Pôsobnosť, registrácia a lehoty sa posudzujú podľa aktuálneho znenia; orgánom je NBÚ. |
| Zákon č. 215/2004 Z. z. o ochrane utajovaných skutočností | Správne | Doplniť odkaz na vykonávacie predpisy NBÚ všeobecne (bez konkrétnych čísel do overenia). |
| Zákon č. 54/2019 Z. z. o ochrane oznamovateľov | Správne | Overiť aktuálne lehoty (potvrdenie prijatia, preverenie) a prah povinnosti zamestnávateľa v aktuálnom znení; Úrad na ochranu oznamovateľov – správne. |
| Nariadenie (EÚ) 2016/679 a zákon č. 18/2018 Z. z. | Správne | Čl. 28, 33, 34 – správne. Doplniť čl. 30 (záznamy), čl. 35 (DPIA), čl. 37 (DPO). |
| Zákon č. 91/2016 Z. z.; Trestný zákon § 328–336 | Správne | Bez pripomienok. |
| Nariadenie (EÚ) 2021/821; zákon č. 39/2011 Z. z.; zákon č. 392/2011 Z. z.; spoločná pozícia 2008/944/SZBP | Správne | Doplniť odporúčanie Komisie (EÚ) 2019/1318 k ICP pre položky s dvojakým použitím; pri transferoch v rámci EÚ smernicu 2009/43/ES (všeobecne). |
| Zákon č. 289/2016 Z. z. o vykonávaní medzinárodných sankcií | Správne | Bez pripomienok. |
| Zákon č. 297/2008 Z. z.; zákon č. 315/2016 Z. z. | Správne | Doplniť zákon č. 394/2012 Z. z. o obmedzení platieb v hotovosti. |
| eIDAS (EÚ) 910/2014 v znení (EÚ) 2024/1183; zákon č. 272/2016 Z. z. | Správne | Bez pripomienok. |
| Zákon č. 305/2013 Z. z.; zákon č. 395/2002 Z. z.; zákon č. 431/2002 Z. z.; zákon č. 283/2002 Z. z. | Správne | Retenčné lehoty neuvádzať z pamäti – prevziať z aktuálneho znenia do registratúrneho plánu. |
| Obchodný zákonník – orgány | Nepresné | Pozri N3 (a.s.). |
| Chýbajúce odkazy | Doplniť | Zákonník práce (č. 311/2001 Z. z.) – monitoring zamestnancov, disciplinárne opatrenia; zákon č. 497/2022 Z. z. o preverovaní zahraničných investícií (posúdiť); nariadenie (EÚ) 2024/2847 (CRA) – posúdiť pri produktoch s digitálnymi prvkami; zákon o hospodárskej mobilizácii – posúdiť, ak je spoločnosť určená ako subjekt hospodárskej mobilizácie; zákon o verejnom obstarávaní pri štátnych tendroch. |

# **4\. Chýbajúce dokumenty a politiky (prioritizované)**

**P0** – bez nich systém nemôže fungovať alebo hrozí porušenie zákona / neschopnosť preukázať primerané opatrenia (zavedenie 0–3 mesiace). **P1** – potrebné na zavedenie a certifikáciu (3–9 mesiacov). **P2** – zrelosť a optimalizácia (9–18 mesiacov).

| ID | Priorita | Dokument / politika | Prečo | Vlastník (návrh) |
| :---- | :---- | :---- | :---- | :---- |
| D01 | **P0** | Menovacie dekréty a štatút funkcií 2\. línie (CCO, Bezp. manažér, CISO, ECO, zástupcovia) | Bez menovaných osôb nie je nikto A v RACI. | Predstavenstvo |
| D02 | **P0** | Organizačný poriadok a podpisový poriadok so schvaľovacími limitmi | Doplní \[DOPLNIŤ\] limity v P2P; základ 4-eyes a CCO prahov. | Predstavenstvo / Financie |
| D03 | **P0** | Popisy pracovných miest: CCO, CISO, Bezpečnostný manažér, Export Control Officer, (DPO) | Nezávislosť, kvalifikácia, previerka NBÚ, zastupovanie, KPI. | HR \+ Predstavenstvo |
| D04 | **P0** | Plné texty politík: Kódex správania, ABAC, Sankcie a export, Informačná bezpečnosť, Whistleblowing (vnútorný predpis), GDPR | Rámec obsahuje len osnovu; schváliteľný interný predpis je podmienkou účinnosti. | CCO / CISO / ECO |
| D05 | **P0** | Posúdenie pôsobnosti zákona č. 69/2018 Z. z. (v znení 366/2024 Z. z.) a NIS2 – písomný záznam | Určuje povinnosti, registráciu a lehoty. | CISO \+ Legal |
| D06 | **P0** | Štandard zálohovania a test obnovy (vrátane záznamu testu) | Odolnosť voči ransomvéru; dnes len heslo „3-2-1“. | CISO / IT prevádzka |
| D07 | **P0** | Štandard logovania a monitoringu (vrátane právneho posúdenia monitoringu zamestnancov) | Bez logov nie je detekcia, vyšetrovanie ani dôkaz. | CISO \+ Legal \+ DPO |
| D08 | **P0** | BIA \+ plán kontinuity (BCP) \+ DR plán s RPO/RTO | Úplne chýba; kľúčové pre výrobu a zmluvné záväzky v konzorciách. | Predstavenstvo / CISO / Výroba |
| D09 | **P0** | Incident response playbooky (kyber, osobné údaje, utajované, korupcia/sankcie) s kontaktmi a šablónami hlásení | Rámec kap. 7 to výslovne predpokladá; lehoty 24/72 h nezvládnuteľné bez prípravy. | CISO / CCO / Bezp. manažér |
| D10 | **P0** | Bezpečnostná dokumentácia a plán NBÚ: zoznam funkcií na previerku, plán previerky podnikateľa, dočasný režim listinnej manipulácie | Podmienka utajovaných zmlúv a konzorcií. | Bezpečnostný manažér |
| D11 | **P0** | ICP exportnej kontroly \+ register klasifikácie produktov a technológií | Bez klasifikácie nemožno rozhodovať o licenciách ani STOP. | Export Control Officer |
| D12 | **P0** | SOP sankčného screeningu (rozsah, zdroje, frekvencia, vyhodnotenie zhôd, záznam) | Denná kontrola v Tech stacku nemá záväzný postup. | CCO / ECO |
| D13 | **P0** | Register darov/pohostení/stretnutí a register konfliktu záujmov – šablóny | Rámec ich vyžaduje, neexistujú. | CCO |
| D14 | **P1** | Štandard privilegovaných prístupov (PAM) a SOP recertifikácie prístupov | Najčastejší vektor kompromitácie; recertifikácia bez záznamu nie je kontrolou. | CISO |
| D15 | **P1** | Riadenie zmien (IT a výrobné systémy) | Bez neho nie je integrita systémov ani audit trail zmien. | IT prevádzka / CISO |
| D16 | **P1** | Inventár aktív (HW, SW, cloud, dáta) s vlastníkmi a klasifikáciou | Základ ISMS, analýzy rizík a NIS2. | CISO / IT |
| D17 | **P1** | Štandard šifrovania a správy kľúčov | Dátové zóny ho predpokladajú. | CISO |
| D18 | **P1** | Patch & vulnerability management štandard (SLA podľa kritickosti) | Dnes len „cieľovo“. | CISO / IT prevádzka |
| D19 | **P1** | Analýza rizík ISMS \+ vyhlásenie o aplikovateľnosti (SoA) ISO/IEC 27001 | Predpoklad certifikácie a opatrení podľa analýzy rizík. | CISO |
| D20 | **P1** | Vendor risk – bezpečnostný dotazník IKT a kontinuálny monitoring kritických dodávateľov | Bezpečnosť dodávateľského reťazca (NIS2). | CISO \+ Nákup |
| D21 | **P1** | Metodika rizikového skórovania tretích strán \+ DD dotazník \+ benchmark provízií | Konzistentné rozhodnutia CCO. | CCO |
| D22 | **P1** | GDPR balík: záznamy o spracovateľských činnostiach, rozhodnutie o DPO, informačné povinnosti, DPIA šablóna, register prenosov (SCC/TIA), postup práv dotknutých osôb | Dnes len osnova. | CCO / DPO |
| D23 | **P1** | Šablóna reportingu predstavenstvu a DR (KPI/KRI) – štvrťročná a ročná | Zjednotí N1/N2; dôkaz „tone from the top“. | CCO |
| D24 | **P1** | Štatút interného auditu a ročný plán auditu | 3\. línia bez mandátu a plánu. | DR / Interný audit |
| D25 | **P1** | Ročný kalendár školení a evidencia (vrátane školenia štatutárov podľa NIS2) | Povinné ročné školenia bez plánu. | CCO / CISO / HR |
| D26 | **P1** | Registratúrny poriadok a plán \+ matica retencie dôkazov kontrol | Preukázateľnosť pre audit a zákon č. 91/2016 Z. z. | Legal / Financie |
| D27 | **P1** | Smernica o cestovných náhradách (travel & expense) vrátane cestovania do rizikových krajín | P2P má len skrátený tok. | Financie / CISO |
| D28 | **P1** | Plán fyzickej bezpečnosti areálu (výroba, sklad, návštevy, kamerový systém) | Mimo utajovaného režimu chýba úplne. | Bezp. manažér / Výroba |
| D29 | **P1** | Knižnica zmluvných doložiek (ABAC, sankcie, export, flow-down NBÚ a kyber, audit right, GDPR) \+ šablóny agentskej zmluvy a plnej moci | Rámec ich vyžaduje. | Legal |
| D30 | **P1** | Postup interných vyšetrovaní a disciplinárnych opatrení | Rámec kap. 7 na to odkazuje. | CCO \+ Legal \+ HR |
| D31 | **P2** | Secure SDLC (ak spoločnosť vyvíja softvér / firmvér) \+ posúdenie CRA | Len ak relevantné pre produkty. | CISO / Vývoj |
| D32 | **P2** | SOC/SIEM runbooky a use-cases | Nadväzuje na D07 a výber SIEM/SOC. | CISO |
| D33 | **P2** | Súťažnoprávny protokol pre konzorciá (clean team) | Výmena informácií medzi konkurentmi. | Legal |
| D34 | **P2** | Smernica o pokladni a firemných platobných kartách | Doplnok P2P. | Financie |
| D35 | **P2** | Politika používania AI nástrojov (rozšírenie Onboarding kap. 3\) | Dnes jedno pravidlo. | CISO / CCO |
| D36 | **P2** | Register dokumentov (verzie, vlastník, stav, revízia) – rozšírenie INDEX | Riadenie dokumentácie. | CCO |
| D37 | **P2** | Slovník pojmov (zodpovedná osoba, vlastník dát, vlastník vzťahu...) | Rieši N8. | CCO |

# **5\. Kompetencie a riadenie – medzery**

| Funkcia / oblasť | Čo má vlastniť (podľa balíka) | Stav | Čo je TBD |
| :---- | :---- | :---- | :---- |
| Predstavenstvo | Schválenie politík, limitov, rizikového apetítu; menovania; NIS2 zodpovednosť štatutára. | **TBD** | Kto z členov predstavenstva je gestor compliance a gestor bezpečnosti; schválenie rizikového apetítu; vlastné školenie. |
| Dozorná rada | Dohľad, plán interného auditu, prijímanie správ. | **TBD** | Kontaktná osoba (predseda) pre eskalácie CCO; frekvencia správ (N2). |
| CCO | ABAC, sankcie (s ECO), AML/KYC, GDPR koordinácia, COI, whistleblowing, DD, školenia, risk assessment. | **TBD** | Meno, zástupca, kapacita (príliš veľa agend pre 1 osobu), rozhodnutie či CCO \= zodpovedná osoba podľa zákona č. 54/2019 Z. z. |
| Bezpečnostný manažér (bezpečnostný zamestnanec) | Personálna, administratívna, fyzická a objektová bezpečnosť, technické prostriedky, priemyselná bezpečnosť, NBÚ. | **TBD** | Meno, stupeň previerky, zástupca; súlad kumulácie so zákonom č. 215/2004 Z. z. |
| CISO | ISMS, NIS2, IAM politika, incidenty, dodávatelia IKT. | **TBD** | Interný vs. externý (vCISO); oddelenie od IT prevádzky (N7). |
| IT prevádzka (správca) | Reálne vykonanie IAM, záloh, záplat, EDR, logovania. | **Chýba** | Kto je R – interný IT alebo externý správca (zmluva, PAM, SLA). |
| Export Control Officer | Klasifikácia, licencie MH SR, EUC, screening strán, ICP. | **TBD** | Meno; kumulácia s CCO áno/nie; zástupca s oprávnením STOP. |
| Legal | Zmluvy, doložky, plné moci, vyšetrovania. | **TBD** | Interný vs. externý advokát; kto drží knižnicu doložiek. |
| DPO / zodpovedná osoba (GDPR) | Dohľad nad GDPR, ÚOOÚ SR. | **Chýba** | Písomné rozhodnutie, či je DPO povinná (čl. 37 GDPR); ak nie, kto je koordinátor. |
| HR | Onboarding/offboarding B, JD, disciplinárne konanie, školenia. | **Chýba v štruktúre** | Doplniť do org. štruktúry a RACI rámca. |
| Kvalita | AQAP, vstupná kontrola, falzifikáty. | **Chýba v štruktúre** | Doplniť; väzba na Nákup tok 3\. |
| Vlastníci dát | Schvaľovanie prístupu do zóny Dôverné. | **TBD** | Zoznam dátových množín a ich vlastníkov (napr. Financie \= ERP, HR \= mzdy, Obchod \= CRM). |
| Vlastník BCP / krízový štáb | Aktivácia plánu kontinuity, komunikácia. | **Chýba** | Kto vedie krízu, zloženie, zastupovanie mimo pracovného času. |
| Incident owner (per typ) | Vedie incident. | **ČIASTOČNÉ** | Kontakty 24/7, zástupcovia, oprávnenie odpojiť systém. |
| Interný audit | Nezávislé uistenie, plán auditu. | **TBD** | Interný vs. outsourcing; štatút; nezávislosť od 2\. línie. |
| Schvaľovacie limity | 1-eye / 4-eyes / CCO. | **TBD** | Všetky sumy \[DOPLNIŤ\] – rozhodne predstavenstvo v podpisovom poriadku. |

## **5.1 Rozhodnutia, ktoré musí urobiť predstavenstvo**

> * R1 – menovanie osôb a zástupcov pre všetky funkcie 2\. línie a povolené kumulácie;  
> * R2 – línia reportingu 2\. línie a frekvencia správ DR (N1, N2);  
> * R3 – schvaľovacie limity a podpisový poriadok;  
> * R4 – CISO interný / externý a oddelenie IT prevádzky;  
> * R5 – rozhodnutie o DPO;  
> * R6 – zodpovedná osoba podľa zákona č. 54/2019 Z. z. a kanál pri konflikte (podnet proti štatutárovi);  
> * R7 – rozsah ISMS a cieľ certifikácie ISO/IEC 27001 a ISO 37001;  
> * R8 – záväzok k bezpečnostnej previerke podnikateľa a rozpočet na chránené priestory;  
> * R9 – cieľové RPO/RTO na základe BIA (bez nich nie je DR plán);  
> * R10 – rizikový apetít (krajiny, typy partnerov, agentské provízie).

# **6\. Kybernetická bezpečnosť – čo chýba**

| Oblasť | Čo balík obsahuje | Čo chýba | Minimum na definovanie (bez sumy, hodnoty stanoví BIA / CISO) |
| :---- | :---- | :---- | :---- |
| Pôsobnosť NIS2 / zákon č. 69/2018 Z. z. | „Posúdiť, či spadá do pôsobnosti.“ | Posúdenie nebolo vykonané; chýba odkaz na zákon č. 366/2024 Z. z. | Záznam: sektor, veľkosť, záver, prípadná registrácia, termíny, zodpovednosť štatutára. |
| Riadenie rizík (ISMS) | ISO/IEC 27001 ako cieľ. | Analýza rizík, register rizík, SoA, ciele, manažérske preskúmanie. | Metodika rizík, ročný cyklus, schválenie zvyškových rizík predstavenstvom. |
| MFA | Povinné pre všetkých, FIDO2 pre privilegované (Onboarding 3). | Záznam o vynútení (konfigurácia), výnimky, servisné účty, break-glass. | Politika podmieneného prístupu, register výnimiek, mesačná kontrola pokrytia. |
| Privilegované prístupy | Oddelený admin účet, JIT pre externého správcu (zmienka). | Štandard PAM, zoznam privilegovaných účtov, záznam relácií. | Zoznam, schvaľovateľ, max. doba platnosti, logovanie, kvartálna recertifikácia. |
| Logovanie | „Centrálne logovanie v rámci tenantu“, „logovanie prístupu“. | Zdroje logov, retencia, synchronizácia času, integrita, kto číta logy a ako často. | Minimálne zdroje: IdP/prihlásenia, admin aktivity tenantu, e-mail, EDR, VPN/firewall, ERP/internetbanking (schválenia, zmeny IBAN), register partnerov, fyzický prístup; retencia \[DOPLNIŤ podľa analýzy a právnych požiadaviek\]; ochrana proti zmazaniu; mesačná revízia. |
| SIEM / SOC | Cieľovo (9–18 mes.). | Use-cases, eskalačná matica, pohotovosť, rozhodnutie interný vs. externý SOC. | Zoznam detekcií (napr. nemožné prihlásenie, vypnutie MFA, hromadné sťahovanie, zmena IBAN, nový admin), SLA reakcie. |
| EDR | Na všetkých zariadeniach (minimum). | Pokrytie a reporting, reakcia na výstrahy, kto rieši mimo pracovného času. | Týždenný report pokrytia, playbook „malware na koncovom zariadení“. |
| Zálohy | „3-2-1 s offline / nemennou kópiou a otestovanou obnovou.“ | Rozsah (čo sa zálohuje vrátane SaaS – Workspace/M365, ERP), frekvencia, šifrovanie, oddelené prístupové údaje, test obnovy. | Štandard \+ rozvrh \+ záznam testu obnovy aspoň \[DOPLNIŤ frekvenciu\] a po každej zásadnej zmene. |
| RPO / RTO | Neuvádza sa. | BIA a cieľové hodnoty pre kritické procesy (výroba, fakturácia, platby, e-mail, eSchránka). | Hodnoty určí BIA a schváli predstavenstvo (R9); dokument ich zámerne nevymýšľa. |
| DR a obnova po incidente | Rámec 7: „izolácia, zachovanie dôkazov, obnova“. | DR runbooky, poradie obnovy, náhradné pracovisko/postupy, kontakty dodávateľov. | Runbook pre ransomvér, výpadok IdP, výpadok ERP, kompromitáciu e-mailu. |
| Cvičenia (drills) | „Testujú sa najmenej raz ročne.“ | Plán cvičení, scenáre, záznamy, nápravy. | Ročne tabletop (kyber \+ GDPR \+ utajované), technický test obnovy, phishingová simulácia. |
| Patching | „Správa zariadení a aktualizácií“. | SLA podľa kritickosti, výnimky, OT/výrobné systémy, firmvér sieťových prvkov. | Štandard so SLA \[DOPLNIŤ\], mesačný report súladu. |
| Správa zraniteľností | Cieľovo. | Pravidelné skenovanie, externé penetračné testy, koordinované zverejňovanie zraniteľností (ak vyrába produkty s SW). | Rozvrh skenov, ročný penetračný test kritických systémov, register zraniteľností. |
| Riadenie zmien | — | Úplne chýba. | Žiadosť → posúdenie rizika → schválenie → záloha → zmena → overenie → záznam; núdzové zmeny. |
| Inventár aktív | Evidencia majetku pri nákupe IT. | Register aktív a aplikácií s vlastníkom, klasifikáciou, umiestnením dát. | Jeden register prepojený s MDM a IdP; štvrťročná aktualizácia. |
| Šifrovanie | Šifrovaný disk, šifrované USB. | Štandard (algoritmy podľa aktuálnych odporúčaní, kľúče, e-mail, zálohy, prenos). | Štandard šifrovania; utajované výlučne podľa NBÚ. |
| Bezpečnosť dodávateľov IKT | Bod v vendor checkliste. | Klasifikácia kritických dodávateľov, zmluvné minimum, ročné prehodnotenie. | Register kritických IKT dodávateľov \+ dotazník \+ zmluvná príloha. |
| OT / výrobné systémy | — | Neriešené (CNC, PLC, testovacie zariadenia). | Segmentácia OT, vzdialený prístup dodávateľov, zálohy konfigurácií. |
| Utajované prostredie | Air-gapped, certifikované podľa NBÚ (cieľ). | Bezpečnostný projekt, časový plán, kto je správca. | Do certifikácie žiadne elektronické spracúvanie (už stanovené) – doplniť kontrolu dodržiavania. |

# **7\. Odporúčaný cieľový strom priečinka**

Návrh čísluje priečinky NN\_ a dokumenty NN.MM\_ pre jednoznačné odkazovanie. Existujúce dokumenty sa presunú (bez zmeny obsahu); duplicitné staršie schémy do 99\_Archiv. Tento audit zostáva v koreňovom priečinku ako 05\_ podľa zadania, po schválení stromu ho odporúčam presunúť do 11\_Audit-a-monitoring.

| 01\_Compliance-a-bezpecnost/├── 00\_INDEX-a-register-dokumentov        (INDEX, register dokumentov, slovník pojmov)├── 01\_Riadenie-a-organizacia│   ├── 01.01\_Ramec-organizacna-struktura-compliance-bezpecnost (existuje)│   ├── 01.02\_Organizacny-poriadok│   ├── 01.03\_Podpisovy-poriadok-a-schvalovacie-limity│   ├── 01.04\_Menovacie-dekrety-a-statuty-funkcii│   ├── 01.05\_Popisy-pracovnych-miest (CCO, CISO, Bezp. manazer, ECO, DPO)│   └── 01.06\_RACI-master├── 02\_Politiky (plné texty, schválené)│   ├── 02.01\_Kodex-spravania   02.02\_ABAC   02.03\_Konflikt-zaujmov│   ├── 02.04\_Sankcie-a-exportna-kontrola   02.05\_Informacna-bezpecnost│   ├── 02.06\_Ochrana-utajovanych-skutocnosti   02.07\_Whistleblowing│   ├── 02.08\_GDPR   02.09\_AML-KYC   02.10\_Konzorcia-a-subdodavatelia├── 03\_Procesy-a-SOP│   ├── 03.01\_Nakup-objednavanie-platby-P2P (existuje)│   ├── 03.02\_Onboarding-a-pristupy (existuje)│   ├── 03.03\_Due-diligence-tretich-stran-metodika│   ├── 03.04\_Sankcny-screening-SOP   03.05\_Cestovne-nahrady│   ├── 03.06\_Recertifikacia-pristupov-SOP   03.07\_Interne-vysetrovania├── 04\_Schemy (01–08 JPEG, aktuálne)├── 05\_Kyberneticka-bezpecnost-ISMS│   ├── 05.01\_Tech-stack-a-prax (existuje)   05.02\_Posudenie-posobnosti-NIS2│   ├── 05.03\_Analyza-rizik-a-SoA   05.04\_Inventar-aktiv│   ├── 05.05\_Standard-logovania-a-monitoringu   05.06\_Standard-PAM│   ├── 05.07\_Standard-sifrovania   05.08\_Patch-a-vulnerability-mgmt│   ├── 05.09\_Change-management   05.10\_Vendor-risk-IKT   05.11\_Secure-SDLC (ak relevantné)├── 06\_Kontinuita-BCP-DR│   ├── 06.01\_BIA   06.02\_BCP   06.03\_DR-runbooky   06.04\_Zalohy-a-test-obnovy│   └── 06.05\_Zaznamy-cviceni├── 07\_Incidenty│   ├── 07.01\_Playbook-kyber   07.02\_Playbook-osobne-udaje│   ├── 07.03\_Playbook-utajovane   07.04\_Playbook-korupcia-sankcie│   └── 07.05\_Kontakty-a-sablony-hlaseni   (záznamník incidentov – obmedzený prístup)├── 08\_Export-a-sankcie│   ├── 08.01\_ICP   08.02\_Register-klasifikacie   08.03\_Licencie-a-EUC (obmedzený prístup)├── 09\_Utajovane-NBU (iba neutajované riadiace dokumenty; nikdy utajovaný obsah)│   ├── 09.01\_Plan-previerok-osob   09.02\_Plan-previerky-podnikatela│   └── 09.03\_Rezim-objektu-a-chranenych-priestorov   09.04\_Administrativna-bezpecnost-postup├── 10\_Zmluvy-a-sablony (doložky, agentská zmluva, plná moc, NDA, čl. 28\)├── 11\_Audit-a-monitoring│   ├── 11.01\_Statut-interneho-auditu   11.02\_Plan-auditu   11.03\_Audit-medzier (tento dokument)│   └── 11.04\_Reporting-predstavenstvo-DR (šablóny, správy)├── 12\_Skolenia (kalendár, materiály, evidencia)├── 13\_Registre (dary, stretnutia, COI, partneri – Dôverné, obmedzený prístup)├── 14\_Fyzicka-bezpecnost (areál, kamery, návštevy)├── 15\_Retencia-a-dokazy (registratúrny poriadok/plán, matica dôkazov)└── 99\_Archiv (staršie verzie schém 03 a 04\) |
| :---- |

**Pravidlo pre registre a záznamy:** registre (13\_), záznamník incidentov a whistleblowing evidencia patria do zóny Dôverné s obmedzeným prístupom (nie do zdieľaného priečinka balíka); podnety whistleblowerov nesmú byť dostupné IT administrátorom. Utajované skutočnosti sa v Google Drive neukladajú nikdy.

# **8\. Najbližších 10 konkrétnych výstupov na uzavretie P0**

Termíny sú relatívne od schválenia tohto auditu (T \= dátum schválenia predstavenstvom).

| \# | Výstup | Obsah / definícia hotového stavu | Vlastník | Závislosť | Termín |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | Rozhodnutie predstavenstva R1–R10 \+ menovacie dekréty (D01) | Podpísané uznesenie: mená a zástupcovia CCO, Bezp. manažéra, CISO, ECO; línia reportingu (N1) a frekvencia správ (N2); CISO interný/externý. | Predstavenstvo | — | T \+ 2 týždne |
| 2 | Opravená verzia Rámca v1.1 a schém 01, 02, 07, 08 \+ INDEX | Odstránené N1–N11; orgány a.s.; HR, IT prevádzka, Kvalita, DPO doplnené; zosúladené lehoty; staršie schémy v 99\_Archiv. | Autor (Márian Stančík) \+ CCO | 1 | T \+ 3 týždne |
| 3 | Podpisový poriadok a schvaľovacie limity (D02) | Všetky \[DOPLNIŤ\] v P2P nahradené schválenými hodnotami; podpisové práva v banke zosúladené. | Predstavenstvo \+ Financie | 1 | T \+ 4 týždne |
| 4 | Popisy pracovných miest 2\. línie (D03) | JD pre CCO, CISO, Bezp. manažéra, ECO: zodpovednosti, kvalifikácia, nezávislosť, právo STOP, previerka NBÚ, zastupovanie, KPI. | HR \+ CCO | 1 | T \+ 4 týždne |
| 5 | Posúdenie pôsobnosti zákona č. 69/2018 Z. z. (D05) | Písomný záznam so záverom; ak v pôsobnosti – plán registrácie a opatrení v zákonných lehotách. | CISO \+ Legal | 1 | T \+ 4 týždne |
| 6 | Plné texty P0 politík (D04) | Kódex, ABAC, Sankcie a export, Informačná bezpečnosť, Whistleblowing (vnútorný predpis podľa zákona č. 54/2019 Z. z.), GDPR – pripravené na schválenie po právnej revízii. | CCO / CISO / ECO \+ advokát | 1, 2 | T \+ 8 týždňov |
| 7 | Zálohy a test obnovy (D06) \+ BIA a RPO/RTO (D08 – časť 1\) | Štandard zálohovania vrátane SaaS; prvý zdokumentovaný test obnovy; BIA kritických procesov a návrh RPO/RTO na schválenie (R9). | CISO / IT prevádzka \+ Výroba \+ Financie | 1 | T \+ 6 týždňov |
| 8 | Štandard logovania a monitoringu (D07) | Zdroje, retencia, integrita, prístup, revízia; právne posúdenie monitoringu zamestnancov (GDPR, Zákonník práce); zapnuté audit logy v tenante a ERP/internetbankingu. | CISO \+ Legal \+ DPO | 1, 5 | T \+ 6 týždňov |
| 9 | 4 incident playbooky \+ kontakty a šablóny hlásení (D09) | Kyber, osobné údaje, utajované, korupcia/sankcie; kontakty 24/7, zástupcovia, šablóny pre NBÚ a ÚOOÚ SR; záznamník incidentov; prvé tabletop cvičenie. | CISO / CCO / Bezp. manažér | 1, 5 | T \+ 8 týždňov |
| 10 | Export a NBÚ štartovací balík (D10, D11, D12, D13) | Register klasifikácie produktov (prvá verzia), SOP sankčného screeningu, zoznam funkcií na previerku NBÚ a plán previerky podnikateľa, šablóny registrov darov a konfliktov záujmov. | ECO / CCO / Bezp. manažér | 1 | T \+ 8 týždňov |

**Kritérium uzavretia P0:** všetky výstupy 1–10 schválené predstavenstvom, uložené v cieľovom strome s vlastníkom a dátumom revízie, a pri 5, 7, 8, 9 existuje aspoň jeden záznam o vykonaní (posúdenie, test obnovy, konfigurácia logov, cvičenie). Opakovaný audit odporúčam po T \+ 3 mesiace; cieľ: dizajn ≥ 60 %, zrelosť ≥ 2,5 v doménach P0.

# **9\. Správa dokumentu**

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý audit medzier kompletného balíka (5 Docs, 10 schém) | NÁVRH – na posúdenie predstavenstvom, právnu a bezpečnostnú revíziu |

Vlastníkom dokumentu je Chief Compliance Officer (po menovaní). Audit sa opakuje po uzavretí P0 a následne najmenej raz ročne.