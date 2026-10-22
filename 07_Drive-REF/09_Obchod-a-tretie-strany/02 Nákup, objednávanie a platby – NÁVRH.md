# **Nákup, objednávanie a platby – proces v1.0**

*Praktický postup od požiadavky po platbu (Procure-to-Pay): požiadavka → schválenie → objednávka → príjem → faktúra → platba*  
Verzia 1.0 \| Dátum: 6\. 10\. 2026 \| Vypracoval: Márian Stančík \| Spoločnosť: IOTA Defence a.s. \| Klasifikácia dokumentu: Interné  
Nadväzuje na dokumenty: [Organizačná štruktúra, compliance a bezpečnosť – rámec v1.0 (2026-10-06)](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit) (najmä ABAC 5.2, konflikt záujmov 5.7, kontroly kap. 6), [Technologický stack a prax systému compliance a bezpečnosti – v1.0 (2026-10-06)](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) (najmä 4.3 ERP \+ 4 oči \+ IBAN lock, Príloha A Platba agentovi) a [Onboarding a prístupy – zamestnanec vs freelancer – v1.0 (2026-10-06)](https://docs.google.com/document/d/17hHTDkmX4kmjQhvP8UMN_79c04q7JJq5Gx_gXtuHmuA/edit) (freelanceri a technika).

| NÁVRH – NIE JE PRÁVNA RADA. Tento dokument je metodický návrh a nie je právnym, daňovým ani účtovným poradenstvom. Schvaľovacie limity sú zámerne uvedené ako \[DOPLNIŤ limity\] a stanoví ich štatutárny orgán interným predpisom (podpisový poriadok). Pred zavedením overiť s advokátom, účtovníkom a pri verejných zákazkách / obranných zmluvách aj súlad so zmluvnými požiadavkami zákazníka. Právne predpisy sa uvádzajú v znení neskorších predpisov. |
| :---- |

## **1\. Účel, rozsah a základné princípy**

Dokument určuje jednotný postup pre všetky nákupy tovarov a služieb a súvisiace platby – od firemnej večere cez notebooky a výrobné komponenty až po externých freelancerov. Cieľom je, aby každý výdavok bol **odôvodnený, schválený pred vznikom záväzku, doručený, správne zaúčtovaný a zaplatený správnemu príjemcovi**, a aby to bolo preukázateľné pre audit a na účely zákona č. 91/2016 Z. z. o trestnej zodpovednosti právnických osôb.

> 1. **Najprv schválenie, potom záväzok** – žiadna objednávka ani zmluva bez schválenej požiadavky.  
> 2. **Žiadna platba bez objednávky (PO) alebo schválenia** a bez potvrdenia príjmu (3-way match: objednávka – príjem – faktúra).  
> 3. **Oddelenie povinností** – ten, kto žiada, neschvaľuje; kto objednáva, nezadáva platbu; kto zadáva platbu, neschvaľuje ju.  
> 4. **Len preverení dodávatelia** – nový dodávateľ prejde vendor onboardingom pred prvou objednávkou.  
> 5. **Zákaz delenia nákupov** na menšie časti s cieľom obísť schvaľovací limit.

## **2\. Hlavný tok P2P – diagram**

| 1\. Požiadavka Žiadateľ *Čo, prečo, koľko, kategória* | → | 2\. Schválenie Manažér (+ Financie / CCO podľa limitu) *rozpočet, limit* | → | 3\. Objednávka (PO) Nákup *preverený dodávateľ, číslo PO* |
| ----- | ----- | ----- | ----- | :---: |
|  |  |  |  | **↓** |
| **6\. Platba** Financie (4 oči) *zamknutý IBAN, dávka* | **←** | **5\. Faktúra** Financie *3-way match PO – príjem – faktúra* | **←** | **4\. Príjem** Žiadateľ / sklad *dodací list, akceptačný protokol* |
| Ak v ktoromkoľvek kroku platí niektorá STOP podmienka (kap. 9): **STOP** – proces sa zastaví a eskaluje na Financie / CCO. |  |  |  |  |

### **2.1 Kroky – kto, čo, dôkaz**

| Krok | Čo sa deje | Kto vykonáva | Dôkaz / výstup |
| :---- | :---- | :---- | :---- |
| 1\. Požiadavka | Popis potreby, odhad ceny, kategória, nákladové stredisko / projekt, navrhovaný dodávateľ, príp. 2–3 ponuky nad limit \[DOPLNIŤ limity\]. | Žiadateľ | Žiadosť (formulár / ERP) s dátumom |
| 2\. Schválenie | Kontrola potreby, rozpočtu a limitu; pri darovaní / pohostení tretej strany aj ABAC kontrola. | Manažér; nad limit Financie, CCO | Elektronické schválenie v systéme / e-mail |
| 3\. Objednávka | Vystavenie PO len preverenému dodávateľovi; obchodné podmienky, dodacia lehota, pri komponentoch klasifikácia exportnej kontroly a kvalitatívne požiadavky. | Nákup | Číslo PO / podpísaná zmluva |
| 4\. Príjem | Potvrdenie dodania tovaru alebo akceptácie služby (množstvo, kvalita, sériové čísla). | Žiadateľ / sklad / kvalita | Príjemka, dodací list, akceptačný protokol |
| 5\. Faktúra | Faktúra musí obsahovať číslo PO; párovanie PO – príjem – faktúra; kontrola náležitostí podľa zákona o DPH. | Financie | Zaúčtovaná faktúra so záznamom párovania |
| 6\. Platba | Zadanie platby na overený (zamknutý) IBAN, schválenie druhou osobou, nad limit CCO. | Financie – zadávateľ a schvaľovateľ | Výpis z internetbankingu so záznamom dvoch schválení |

## **3\. Kategórie nákupu s príkladmi**

| Kategória | Príklady | Tok | Osobitné pravidlá |
| :---- | :---- | :---- | :---- |
| **Firemný event / večera** | Teambuilding, výročná večera, večera s tímom po projekte, firemná konferencia | Tok 1 | Rozpočet na osobu \[DOPLNIŤ limity\]; ak sa zúčastnia tretie strany, platia pravidlá pre pohostenie (ABAC); zoznam účastníkov k účtovnému dokladu. |
| **Dary / pohostenie** | Obchodný obed so zákazníkom, reklamné predmety, darček partnerovi, pozvanie na veľtrh | Tok 1 | Vždy zápis do registra darov a pohostení; pri verejných funkcionároch, zástupcoch štátnych podnikov a ozbrojených zložiek **predchádzajúce schválenie CCO**; zákaz hotovosti a poukazov ekvivalentných hotovosti; pozri ABAC politiku – [rámec, kap. 5.2](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit). |
| **Technika (notebooky)** | Notebooky, monitory, telefóny, sieťové prvky, softvérové licencie | Tok 2 | Nákup len cez IT (štandardné konfigurácie); zaradenie do MDM a evidencie majetku pred odovzdaním; bezpečnosť dodávateľa IKT (NIS2). |
| **Komponenty / materiál** | Elektronické súčiastky, mechanické diely, suroviny, špeciálne náradie pre výrobu | Tok 3 | Schválený dodávateľ (zoznam AVL), certifikáty zhody a pôvodu, kontrola falzifikátov, exportná klasifikácia a sankčný screening, flow-down kvality (AQAP, ak sa vyžaduje). |
| **Služby / freelancer** | Vývoj softvéru, konzultant, preklady, marketingová agentúra, externý IT správca | Tok 4 | Zmluva o dielo / o poskytovaní služieb pred začiatkom práce; výkaz alebo akceptačný protokol; prístupy podľa dokumentu [Onboarding a prístupy](https://docs.google.com/document/d/17hHTDkmX4kmjQhvP8UMN_79c04q7JJq5Gx_gXtuHmuA/edit). |
| **Cestovné** | Letenky, hotel, vlak, služobné auto, diéty, vstupné na veľtrh | Zjednodušený: cestovný príkaz → schválenie manažérom → rezervácia → vyúčtovanie do \[DOPLNIŤ\] dní | Schválenie cesty pred rezerváciou; zákon č. 283/2002 Z. z. o cestovných náhradách; cesty do rizikových krajín a s exportne citlivými údajmi konzultovať s Export Control a CISO; hradenie ciest tretích strán \= pohostenie (ABAC). |

## **4\. Schvaľovacie limity (1-eye / 4-eyes / CCO)**

Limity sú výslovne **zástupné hodnoty**; stanoví ich štatutárny orgán. Hodnota sa posudzuje za celý nákup / zmluvu (pri opakovanom plnení za 12 mesiacov), bez DPH.

| Úroveň | Hodnota nákupu | Kto schvaľuje požiadavku | Platba | Poznámka |
| :---- | :---- | :---- | :---- | :---- |
| **1-eye** | do \[DOPLNIŤ limity\] EUR | Priamy manažér | Zadáva Financie, schvaľuje iná osoba (4 oči pri platbe platí vždy) | Len štandardné kategórie, existujúci preverený dodávateľ; nie pre dary tretím stranám verejného sektora. |
| **4-eyes** | od \[DOPLNIŤ limity\] do \[DOPLNIŤ limity\] EUR | Manažér \+ vedúci Financií (alebo štatutár) | Dve osoby z Financií | Min. \[DOPLNIŤ\] porovnateľné ponuky alebo odôvodnenie jediného dodávateľa. |
| **CCO** | nad \[DOPLNIŤ limity\] EUR alebo bez ohľadu na sumu pri rizikovom prípade | Manažér \+ Financie \+ CCO (podľa podpisového poriadku aj štatutár) | Dve osoby z Financií \+ CCO | Vždy CCO: dar / pohostenie verejného funkcionára, platba agentovi nad limit, dodávateľ z rizikovej krajiny, red flag, konflikt záujmov, výnimka z tohto procesu. |

## **5\. Záväzné pravidlá**

| Pravidlo | Obsah | Vlastník kontroly |
| :---- | :---- | :---- |
| **Žiadna platba bez PO / schválenia** | Faktúra bez čísla PO alebo bez doloženej schválenej požiadavky sa vráti žiadateľovi; dodatočné schválenie („after-the-fact“) len výnimočne, evidované a reportované CCO mesačne. Výnimky bez PO: energie, nájom, dane a odvody podľa schváleného zoznamu. | Financie |
| **Overenie zmeny IBAN** | Zmena bankového účtu dodávateľa len na základe písomnej žiadosti a **spätného telefonického overenia na vopred známom kontakte** (nie na kontakte z žiadosti); vykoná osoba iná ako zadávateľ platieb; prvá platba na nový účet s dodatočnou kontrolou. Platí aj pri „urgentnej“ žiadosti od vedenia (podvod typu CEO fraud). | Financie |
| **Žiadna hotovosť agentom** | Agentom, obchodným zástupcom a sprostredkovateľom sa nikdy neplatí v hotovosti, tretím stranám ani do inej krajiny než krajiny ich sídla / pôsobenia; len proti faktúre a dokladu o výkone (pozri Príloha A dokumentu Technologický stack). Hotovostné platby všeobecne len z pokladne do \[DOPLNIŤ limity\] EUR. | Financie / CCO |
| **Vendor onboarding** | Nový dodávateľ pred prvou objednávkou: identifikácia (ORSR / ŽR), IČ DPH, KUV, sankčný screening, overenie IBAN, pri službách a komponentoch aj DD dotazník a compliance doložka; zápis do registra partnerov (pozri kap. 7). | Nákup / CCO |
| **Konflikt záujmov** | Žiadateľ, schvaľovateľ ani nákupca nesmie byť osobne prepojený s dodávateľom (rodina, majetková účasť, vedľajšia činnosť); konflikt oznámi vopred a vylúči sa z rozhodovania; zákaz prijímania darov od dodávateľov nad limit podľa ABAC. | CCO |
| **Zákaz delenia nákupov** | Rozdelenie jedného nákupu na viacero objednávok s cieľom obísť limit je disciplinárnym previnením; Financie mesačne kontroluje opakované nákupy u rovnakého dodávateľa tesne pod limitom. | Financie / Interný audit |
| **Firemné platobné karty** | Len pre určené osoby, s limitom \[DOPLNIŤ limity\]; doklad a účel k každej transakcii do \[DOPLNIŤ\] dní; nie na dary tretím stranám bez zápisu do registra. | Financie |

## **6\. Samostatné toky podľa kategórie**

### **6.1 Tok 1 – Event a pohostenie (vrátane darov)**

| Požiadavka účel, účastníci, suma/osoba | → | ABAC kontrola tretie strany? verejní funkcionári? | → | Schválenie manažér / CCO | → | Rezervácia / PO | → | Vyúčtovanie \+ register |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |

| Krok | Činnosť | Kto | STOP podmienka |
| :---- | :---- | :---- | :---- |
| 1 | Požiadavka: účel (interný event / obchodné pohostenie / dar), zoznam účastníkov alebo príjemcov, suma na osobu, miesto. | Žiadateľ | Chýba účel alebo zoznam účastníkov. |
| 2 | ABAC kontrola: sú prítomní zákazníci, verejní funkcionári, zástupcovia štátnych podnikov / ozbrojených zložiek? Prebieha tender s týmto zákazníkom? | Žiadateľ \+ CCO | Prebiehajúci tender alebo rozhodovanie príjemcu o spoločnosti; hotovosť / poukaz; hradenie rodinných príslušníkov; luxus neprimeraný obchodnému účelu. |
| 3 | Schválenie podľa limitu; pri verejnom funkcionárovi vždy CCO vopred. | Manažér / CCO | Chýba predchádzajúce schválenie CCO. |
| 4 | Rezervácia alebo PO; platba firemnou kartou alebo na faktúru. | Žiadateľ / Nákup | Platba súkromne s následnou náhradou bez schválenia. |
| 5 | Vyúčtovanie: doklad \+ skutočný zoznam účastníkov; zápis do registra darov a pohostení do \[DOPLNIŤ\] dní. | Žiadateľ, Financie | Bez zápisu v registri sa náklad neprepláca. |

### **6.2 Tok 2 – IT hardvér (notebooky, telefóny, licencie)**

| Požiadavka vedúci → IT | → | Štandardná konfigurácia IT | → | Schválenie podľa limitu | → | PO \+ príjem IT | → | MDM \+ majetok \+ odovzdanie |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |

| Krok | Činnosť | Kto | STOP podmienka |
| :---- | :---- | :---- | :---- |
| 1 | Požiadavka na zariadenie pre konkrétnu osobu / rolu (nový nástup, výmena). | Vedúci útvaru | Nákup techniky mimo IT (priamo zamestnancom). |
| 2 | Výber zo štandardných konfigurácií; overenie dodávateľa (autorizovaný predajca, záruka, bezpečnosť dodávateľa IKT). | IT / CISO | Neautorizovaný alebo neoverený zdroj (riziko kompromitovaného hardvéru). |
| 3 | Schválenie podľa limitu (kap. 4). | Manažér / Financie | Chýba schválenie. |
| 4 | PO a príjem: kontrola sériových čísel a neporušenosti balenia. | Nákup / IT | Nesúlad sériových čísel alebo porušené balenie. |
| 5 | Zaradenie do MDM, EDR, šifrovanie, evidencia majetku; odovzdanie na protokol. | IT | Zariadenie sa neodovzdá bez MDM a evidencie. |

### **6.3 Tok 3 – Výrobné komponenty a materiál**

| Požiadavka výroba / plánovanie | → | AVL \+ export \+ screening Nákup, Export Control | → | Schválenie \+ PO | → | Vstupná kontrola kvalita, certifikáty | → | Faktúra \+ platba |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |

| Krok | Činnosť | Kto | STOP podmienka |
| :---- | :---- | :---- | :---- |
| 1 | Požiadavka z plánu výroby / kusovníka (číslo dielu, množstvo, špecifikácia, projekt). | Výroba / plánovanie | Chýba technická špecifikácia. |
| 2 | Dodávateľ zo zoznamu schválených dodávateľov (AVL); sankčný screening dodávateľa a výrobcu; exportná klasifikácia a pôvod (pri US pôvode EAR/ITAR); požiadavky zákazníka (flow-down, AQAP). | Nákup, Export Control, Kvalita | Dodávateľ mimo AVL; zhoda v sankčnom zozname; nejasný pôvod; broker bez autorizácie výrobcu (riziko falzifikátu). |
| 3 | Schválenie podľa limitu, vystavenie PO s kvalitatívnymi a exportnými podmienkami; pri rámcovej zmluve odvolávka. | Manažér výroby, Financie, Nákup | Prekročenie rámcovej zmluvy bez dodatku. |
| 4 | Vstupná kontrola: množstvo, certifikát zhody (CoC), certifikát pôvodu, šarže / sériové čísla; nevyhovujúce → karanténa. | Sklad, Kvalita | Chýbajúci CoC alebo podozrenie na falzifikát – karanténa, neprijatie. |
| 5 | 3-way match a platba na zamknutý IBAN. | Financie | Nesúlad PO – príjem – faktúra. |

### **6.4 Tok 4 – Externé služby a freelanceri**

| Požiadavka predmet, rozsah, doba | → | Vendor onboarding DD, COI, IBAN | → | Zmluva \+ PO Legal, Nákup | → | Akceptácia výkaz / protokol | → | Faktúra \+ platba |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |

| Krok | Činnosť | Kto | STOP podmienka |
| :---- | :---- | :---- | :---- |
| 1 | Požiadavka: predmet diela / služby, výstupy, rozsah, doba, odhad ceny, potrebné prístupy k dátam. | Žiadateľ (budúci vlastník vzťahu) | Práca už začala bez zmluvy. |
| 2 | Vendor onboarding: registre, KUV, screening, konflikt záujmov, overenie IBAN, DD dotazník; pri poradcoch s kontaktom na verejný sektor rozšírená DD (CCO). | Nákup, CCO | Dodávateľ je blízka osoba zamestnanca; poradca „so známosťami“ bez jasného výstupu; neprimeraná odmena. |
| 3 | Zmluva (ZoD / služby) s compliance doložkou, NDA, IP, čl. 28 GDPR; PO; onboarding prístupov podľa dokumentu Onboarding a prístupy (proces A). | Legal, Nákup, IT | Prístupy požadované nad rámec predmetu (HR, mzdy, celé CRM, IAM admin, utajované bez NBÚ). |
| 4 | Akceptácia: výkaz práce alebo akceptačný protokol potvrdený vlastníkom vzťahu. | Vlastník vzťahu | Faktúra bez dokladu o výkone; „paušál“ bez definovaného plnenia. |
| 5 | 3-way match a platba; po skončení zmluvy offboarding v ten istý deň. | Financie, IT | Platba na účet tretej osoby alebo do inej krajiny. |

## **7\. Vendor onboarding – checklist nového dodávateľa**

| Č. | Kontrolný bod | Splnené | Poznámka / dôkaz |
| :---- | :---- | :---- | :---- |
| 1 | Identifikácia: výpis z ORSR / Živnostenského registra, IČO, DIČ, IČ DPH (overenie platiteľa DPH a zoznamu rizikových platiteľov) | ☐ |  |
| 2 | Konečný užívateľ výhod (KUV); pri verejných zákazkách RPVS | ☐ |  |
| 3 | Sankčný screening dodávateľa, štatutárov a KUV | ☐ |  |
| 4 | Overenie IBAN (účet na meno dodávateľa, krajina sídla; pri platiteľoch DPH zverejnený účet) | ☐ |  |
| 5 | Vyhlásenie o konflikte záujmov žiadateľa a nákupcu | ☐ |  |
| 6 | DD dotazník a compliance doložka (služby, komponenty, dodávatelia nad limit) | ☐ |  |
| 7 | Pri komponentoch: zaradenie do AVL, kvalitatívne požiadavky, exportná klasifikácia | ☐ |  |
| 8 | Pri IT dodávateľoch: bezpečnostné požiadavky (NIS2), umiestnenie dát, čl. 28 GDPR | ☐ |  |
| 9 | Zápis do registra partnerov (ID dodávateľa) a založenie v ERP so zamknutým IBAN | ☐ |  |

## **8\. RACI – nákup a platby**

Legenda: R – vykonáva, A – schvaľuje / nesie zodpovednosť, C – konzultovaný, I – informovaný. Pre každú činnosť je práve jedno A.

| Činnosť | Žiadateľ | Manažér | Nákup | Financie | CCO |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Požiadavka a odôvodnenie | R | A | C | I | – |
| Schválenie do limitu 1-eye | I | A/R | I | I | – |
| Schválenie 4-eyes | I | R | I | A | I |
| Schválenie nad limit CCO / rizikový prípad | I | R | C | C | A |
| Vendor onboarding | C | I | R | C | A |
| Vystavenie objednávky (PO) | C | I | A/R | I | – |
| Potvrdenie príjmu / akceptácie | R | A | I | I | – |
| Spracovanie faktúry (3-way match) | C | I | C | A/R | – |
| Platba (zadanie \+ schválenie) | – | I | – | A/R | C (nad limit) |
| Zmena IBAN dodávateľa | – | – | C | A/R | I |
| Dar / pohostenie tretej strane | R | C | – | I | A |
| Konflikt záujmov | R (oznámi) | C | R (oznámi) | I | A |

## **9\. STOP podmienky (zhrnutie)**

Ak nastane ktorákoľvek z podmienok, proces sa **okamžite zastaví**, nepokračuje sa v objednávke ani platbe a vec sa eskaluje na Financie a CCO (pri podozrení na trestný čin postup podľa kap. 7 rámca).

| Č. | STOP podmienka | Eskalácia |
| :---- | :---- | :---- |
| 1 | Chýba schválená požiadavka alebo číslo PO (mimo schválených výnimiek). | Financie |
| 2 | Dodávateľ neprešiel vendor onboardingom alebo má neplatnú DD. | Nákup / CCO |
| 3 | Zmena IBAN bez nezávislého spätného overenia; „urgentná“ žiadosť o platbu mimo procesu. | Financie |
| 4 | Platba v hotovosti agentovi, platba tretej strane alebo do inej krajiny než sídla / pôsobenia. | CCO |
| 5 | Nesúlad PO – príjem – faktúra alebo chýba doklad o výkone. | Financie |
| 6 | Zhoda pri sankčnom screeningu, nejasný pôvod komponentu, chýbajúca exportná klasifikácia. | Export Control / CCO |
| 7 | Neoznámený konflikt záujmov alebo dodávateľ prepojený so zamestnancom. | CCO |
| 8 | Dar / pohostenie verejného funkcionára bez predchádzajúceho schválenia CCO alebo počas tendra. | CCO |
| 9 | Delenie nákupu s cieľom obísť limit. | Financie / CCO |
| 10 | Zadávateľ platby je zároveň schvaľovateľom. | Financie |

## **10\. Správa dokumentu**

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý návrh procesu nákupu, objednávania a platieb | NÁVRH – limity \[DOPLNIŤ limity\], na právne a účtovné overenie |

Vlastníkom dokumentu je vedúci Financií v spolupráci s Nákupom; ABAC a konflikt záujmov schvaľuje CCO. Revízia najmenej raz ročne a pri zmene limitov, systémov alebo legislatívy.