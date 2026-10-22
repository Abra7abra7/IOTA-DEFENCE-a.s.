# **Technologický stack a prax systému compliance a bezpečnosti – v1.0**

*Praktický sprievodca k rámcu „Organizačná štruktúra, compliance a bezpečnosť – rámec v1.0“: ako systém funguje v bežnej prevádzke a aké nástroje ho podporujú*

Verzia 1.0 | Dátum: 6\. 10\. 2026 | Vypracoval: Márian Stančík | Klasifikácia dokumentu: Interné

Nadväzuje na dokument: [Organizačná štruktúra, compliance a bezpečnosť – rámec v1.0 (2026-10-06)](https://docs.google.com/document/d/1mUZd3eoYDtxbJ4tXeeZJm9xfV4IiWikkT3SQ--IbdxA/edit)

| NÁVRH – NIE JE PRÁVNA RADA Tento dokument je praktický metodický podklad a nie je právnym, bezpečnostným ani obstarávacím poradenstvom. Uvedené produkty a služby sú len príklady bez odporúčania konkrétneho dodávateľa a bez uvedenia cien; ich výber, zmluvné podmienky, umiestnenie dát a súlad s predpismi je potrebné overiť (advokát, bezpečnostný poradca, pri utajovaných skutočnostiach Národný bezpečnostný úrad – NBÚ). Právne predpisy sa uvádzajú v znení neskorších predpisov. Rozhodujúce sú role, politiky a lehoty stanovené v nadväzujúcom rámci a v interných predpisoch. |
| ----- |

## **0\. Účel dokumentu a vzťah k rámcu**

Rámec v1.0 určuje **kto** za čo zodpovedá a **aké pravidlá** platia (organizačná štruktúra, RACI, politiky, kontroly, incidenty, roadmapa). Tento dokument dopĺňa **ako** to funguje v praxi: životný cyklus obchodného partnera, rozdelenie línií ochrany, dátové zóny a minimálny a cieľový technologický stack. Platí zásada: **najprv proces a zodpovednosť, potom nástroj**. Nástroj nesmie nahradiť rozhodnutie zodpovednej osoby, má ho iba zaznamenať, uľahčiť a urobiť preukázateľným (audit trail).

Tri základné princípy celého stacku:

> 1. **Jeden zdroj pravdy o partneroch** – každý agent, distribútor, subdodávateľ a konzorciálny partner má jedno ID v registri partnerov; CRM, ERP, zmluvy aj platby sa naň odkazujú.  
> 2. **Žiadna platba ani prístup bez platného stavu v registri** – ak due diligence alebo re-previerka nie je platná, systém (alebo aspoň kontrolný postup) platbu, podpis či prístup zastaví.  
> 3. **Utajované skutočnosti sú mimo bežného IT** – oddelené, certifikované prostredie bez pripojenia k internetu a bez bežného cloudu; bežné nástroje v tomto dokumente sa na utajované informácie nepoužívajú.

## **1\. Ako si to predstaviť v praxi – životný cyklus agenta**

### **1.1 Tok krokov (od nového agenta po ročnú re-previerku)**

> 1. **Nový agent (iniciácia)** – obchodník zapíše návrh nového agenta do registra partnerov (formulár): krajina, účel spolupráce, očakávaná provízia, kontakt s verejným sektorom. Bez zápisu sa nesmie začať rokovať o podmienkach.  
> 2. **Due diligence** – CCO (alebo poverený analytik) vykoná sankčný screening subjektu, štatutárov a konečného užívateľa výhod (KUV), rešerš negatívnych správ, rizikové skórovanie krajiny a sektora a vyhodnotí red flags podľa Prílohy A rámca. Export Control Officer posúdi produkty a krajiny. Výstup: schválené / schválené s podmienkami / zamietnuté.  
> 3. **Zmluva** – Legal pripraví agentskú zmluvu so štandardnými compliance doložkami a plnou mocou s presným rozsahom; podpis kvalifikovaným elektronickým podpisom (eIDAS). Podpísaná zmluva a plná moc sa ukladajú do archívu a ich limity sa zapíšu do CRM.  
> 4. **Onboarding** – ABAC školenie agenta v LMS s testom, podpis vyhlásení (ABAC, konflikt záujmov), založenie partnera v ERP s overeným IBAN (zámok IBAN), prípadne obmedzený prístup do partnerského portálu s MFA.  
> 5. **Platba** – faktúra a dôkaz o výkone sa spárujú s CRM (obchodný prípad) a zmluvou; platbu zadáva Financie, schvaľuje iná osoba (štyri oči), nad limit aj CCO. Platba ide len na zamknutý IBAN na meno agenta.  
> 6. **Ročná re-previerka** – systém (alebo kalendár v registri) 30 dní vopred upozorní vlastníka vzťahu; aktualizuje sa screening, KUV, ABAC certifikát, školenie a preskúmanie výkonu a provízií. Bez obnovenia sa partner automaticky označí ako „blokovaný pre platby“.

### **1.2 Diagram toku**

| 1\. Nový agent Obchod *Register partnerov* | → | 2\. Due diligence CCO \+ Export Control *Screening, skóre* | → | 3\. Zmluva Legal *e-podpis, plná moc* |
| ----- | ----- | ----- | ----- | :---: |
|  |  |  |  | **↓** |
| **6\. Ročná re-previerka** Vlastník vzťahu \+ CCO *Pripomienka, nový screening* | **←** | **5\. Platba** Financie (4 oči) *ERP, zamknutý IBAN* | **←** | **4\. Onboarding** CCO \+ CISO \+ Financie *LMS, ERP, MFA* |
| Ak re-previerka nie je včas dokončená alebo sa zistí red flag: **STOP** – blokácia platieb, pozastavenie plnej moci, eskalácia CCO → štatutár. |  |  |  |  |

### **1.3 Krok – zodpovednosť – nástroj – dôkaz**

| Krok | Kto vykonáva (R) | Kto schvaľuje (A) | Nástroj | Dôkaz pre audit |
| :---- | :---- | :---- | :---- | :---- |
| 1\. Nový agent | Obchodník (vlastník vzťahu) | Vedúci Obchodu | Register partnerov (formulár) | Záznam žiadosti s dátumom a odôvodnením potreby agenta |
| 2\. Due diligence | CCO / analytik, Export Control | CCO (pri vysokom riziku aj štatutár) | Register partnerov, sankčný screening, verejné registre | Výsledky screeningu (dátum, zoznamy), DD dotazník, rizikové skóre, záver |
| 3\. Zmluva | Legal | Štatutár (podľa podpisového poriadku) | Šablóny zmlúv, e-podpis, archív | Podpísaná zmluva a plná moc s rozsahom a dobou platnosti |
| 4\. Onboarding | CCO, CISO / IT, Financie | Vlastník vzťahu | LMS, ERP, IAM | Certifikát školenia, vyhlásenia, záznam o overení IBAN, pridelené prístupy |
| 5\. Platba | Financie (zadávateľ) | Financie (schvaľovateľ), nad limit CCO | ERP, internetbanking s dvojitým schválením | Faktúra, dôkaz o výkone, záznam o schválení dvoma osobami |
| 6\. Re-previerka | Vlastník vzťahu, CCO | CCO | Register partnerov (pripomienky), screening, LMS | Aktualizovaný DD záznam, ročný ABAC certifikát agenta |

### **1.4 Jeden bežný týždeň – ako to vyzerá v kalendári**

| Deň | Čo sa deje | Kto | Nástroj |
| :---- | :---- | :---- | :---- |
| Pondelok | Obchodník zadá návrh nového agenta pre nový trh; automatický (alebo manuálny) sankčný screening sa spustí ešte v ten deň. | Obchod, CCO | Register partnerov, sankčný screening |
| Utorok | Kontrola dávkového re-screeningu všetkých aktívnych partnerov po aktualizácii sankčných zoznamov; vyhodnotenie prípadných zhôd (false positive / true match). | CCO | Sankčný screening |
| Streda | Platobný deň: Financie pripraví dávku platieb, schvaľovateľ kontroluje párovanie faktúra – zmluva – výkon, provízia nad limit ide na CCO. | Financie, CCO | ERP, internetbanking |
| Štvrtok | Podpis agentskej zmluvy e-podpisom; nastavenie limitov plnej moci v CRM; zadanie ABAC školenia v LMS. | Legal, Obchod, CCO | E-podpis, CRM, LMS |
| Piatok | Týždenný prehľad: otvorené incidenty a podnety, nesplnené školenia, blížiace sa re-previerky, zmeny prístupov (on/offboarding). Krátky report štatutárovi. | CCO, CISO, Bezpečnostný manažér | Ticketing, LMS, IAM, register partnerov |

## **2\. Schéma troch línií ochrany**

| Štatutárny orgán (zodpovednosť, tone from the top) | Dozorná rada (dohľad) |  |  |
| ----- | ----- | ----- |
| **1\. línia – vlastníci rizika** Obchod, Nákup, Výroba, Financie | **2\. línia – metodika a dohľad** CCO, Bezpečnostný manažér, CISO, Export Control Officer, Legal | **3\. línia – nezávislé uistenie** Interný audit (reportuje DR) |
| **Čo robí:** vykonáva kontroly v každodennej práci – zápis partnera, register darov, štyri oči pri platbách, need-to-know vo výrobe. | **Čo robí:** nastavuje pravidlá a nástroje, schvaľuje rizikové prípady, robí screening, školí, monitoruje a eskaluje. | **Čo robí:** testuje vzorky (platby agentom, dary, prístupy, evidenciu utajovaných), hodnotí dizajn a účinnosť kontrol. |
| **Hlavné nástroje:** CRM, ERP, register darov a stretnutí, formuláre registra partnerov. | **Hlavné nástroje:** register partnerov a DD, sankčný screening, LMS, whistleblowing, IAM, EDR/SIEM, ticketing. | **Hlavné nástroje:** čítací prístup do všetkých registrov a logov, exporty z ERP, audit trail e-podpisu a IAM. |
| → hlási výnimky a incidenty 2\. línii | → reportuje štatutárovi, priamy prístup k DR | → reportuje dozornej rade |

*Praktické pravidlo pre nástroje:* 1\. línia dáta zapisuje, 2\. línia pravidlá konfiguruje a výnimky schvaľuje, 3\. línia má iba čítací prístup. Nikto z 1\. línie nesmie mať administrátorské práva k nástrojom 2\. línie (napr. obchodník nesmie meniť výsledok screeningu ani limity plnej moci).

## **3\. Schéma dátových zón**

| BEŽNÉ IT PROSTREDIE (firemný tenant M365 / Google Workspace, ERP, CRM, cloud s dátami v EÚ) |  |  |  | ODDELENÉ PROSTREDIE |
| :---: | :---: | :---: | :---- | :---: |
| **VEREJNÉ** web, katalógy, tlačové správy | **INTERNÉ** interné predpisy, bežná komunikácia, plány | **DÔVERNÉ** zmluvy, ceny, DD spisy, osobné údaje, technická dokumentácia, podnety whistleblowerov |  | **UTAJOVANÉ** (zákon č. 215/2004 Z. z.) len certifikované technické prostriedky, bez internetu, nie bežný cloud, evidencia a registratúra utajovaných písomností |

| Zóna | Kde sa ukladá | Kto má prístup | Minimálne technické opatrenia | Zakázané |
| :---- | :---- | :---- | :---- | :---- |
| **Verejné** | Web, verejné úložisko marketingu | Ktokoľvek; publikuje schválená osoba | Schvaľovací proces pred zverejnením (kontrola exportne citlivých technických údajov) | Zverejňovať technické parametre bez posúdenia Export Control |
| **Interné** | Firemný tenant (zdieľané disky / SharePoint), intranet | Zamestnanci a oprávnení externí s firemným účtom | Firemné účty, MFA, spravované zariadenia, zákaz zdieľania mimo organizácie bez dôvodu | Súkromné účty a súkromné cloudové úložiská |
| **Dôverné** | Vyhradené priečinky / knižnice s obmedzeným prístupom, ERP, CRM, register partnerov, whistleblowing platforma | Len podľa role a need-to-know; schvaľuje vlastník dát | Označovanie (citlivostné štítky), šifrovanie, obmedzenie sťahovania a externého zdieľania, logovanie prístupu, DLP podľa možností; pri prenose mimo EÚ posúdenie podľa GDPR | Posielanie na súkromné e-maily, neriadené USB, zdieľanie odkazom „ktokoľvek s odkazom“ |
| **Utajované** | Výlučne oddelené prostredie schválené/certifikované podľa požiadaviek NBÚ; fyzicky zabezpečené priestory; registratúra utajovaných písomností | Len osoby s platnou bezpečnostnou previerkou príslušného stupňa, poučením a need-to-know; určuje Bezpečnostný manažér | Fyzická, personálna, administratívna a objektová bezpečnosť, certifikované technické prostriedky, kryptografická ochrana, evidencia nosičov; detailné opatrenia určuje bezpečnostná dokumentácia schválená NBÚ | **Akýkoľvek bežný cloud, e-mail, CRM, ticketing, AI nástroje, súkromné zariadenia a prenos do bežnej siete** |

## **4\. Technologický stack podľa vrstiev**

Pre každú vrstvu sa uvádza minimálne riešenie, ktoré je možné zaviesť do troch mesiacov s existujúcimi nástrojmi, a cieľové riešenie na 9–18 mesiacov. Názvy produktov sú **príklady** na porovnanie, nie odporúčanie; ceny sa zámerne neuvádzajú a je potrebné ich získať priamo od dodávateľov. Pri každom cloudovom nástroji sa overí umiestnenie dát (preferovane EÚ), zmluva o spracúvaní osobných údajov (čl. 28 GDPR), MFA/SSO, export dát a audit log.

### **4.1 Tretie strany a zmluvy**

| Vrstva | Účel | Minimálne riešenie (0–3 mes.) | Cieľové riešenie (9–18 mes.) | Poznámka SK/EÚ |
| :---- | :---- | :---- | :---- | :---- |
| **Register partnerov \+ due diligence** | Jeden zdroj pravdy o agentoch, distribútoroch, subdodávateľoch a partneroch v konzorciách; stav DD, riziko, vlastník vzťahu, termín re-previerky. | Google Sheets / Excel so zamknutými stĺpcami, formulár (Google Forms / Microsoft Forms) na zadanie partnera, priečinok DD spisov v zóne Dôverné, pravidlo „bez ID partnera žiadna zmluva ani platba“. | Špecializovaná platforma na riadenie rizík tretích strán (TPRM/GRC modul) s workflow schvaľovania, dotazníkmi pre partnerov, pripomienkami re-previerky a integráciou na CRM a ERP. | Zdroje: obchodný register SR (ORSR), register konečných užívateľov výhod a register partnerov verejného sektora (RPVS, zákon č. 315/2016 Z. z.), komerčné databázy (napr. FinStat); KUV podľa zákona č. 297/2008 Z. z. |
| **Sankčný screening** | Kontrola partnera, štatutárov, KUV a strán transakcie voči sankčným zoznamom; pri novom partnerovi aj priebežne. | Manuálne vyhľadávanie v konsolidovanom zozname finančných sankcií EÚ a v otvorenej databáze OpenSanctions; zápis dátumu, rozsahu a výsledku do registra; pri zhode eskalácia na CCO a Export Control. | Automatizovaný screening (napr. OpenSanctions API alebo komerčná screeningová služba) s dávkovým re-screeningom celej databázy pri zmene zoznamov a s auditovateľným záznamom vyhodnotenia zhôd. | Reštriktívne opatrenia EÚ a zákon č. 289/2016 Z. z.; podľa väzieb aj zoznamy OSN, UK a USA (OFAC). Sankcie zahŕňajú aj nepriame vlastníctvo a kontrolu – sledovať KUV a štruktúru. |
| **Zmluvy \+ e-podpis (eIDAS)** | Štandardné šablóny s compliance doložkami, podpis, evidencia platnosti a plných mocí. | Schválené šablóny v zdieľanom priečinku (len na čítanie), register zmlúv v tabuľke (strany, platnosť, limity, plná moc), kvalifikovaný elektronický podpis cez občiansky preukaz s čipom (eID) alebo kvalifikovaný certifikát (napr. Disig). | Systém správy zmlúv (CLM) s workflow schvaľovania podľa podpisového poriadku, upozorneniami na koniec platnosti, integráciou na CRM a kvalifikovaným e-podpisom / pečaťou; podpisovanie s overením podpisu a dlhodobou platnosťou. | Nariadenie (EÚ) č. 910/2014 (eIDAS) v znení nariadenia (EÚ) 2024/1183 a zákon č. 272/2016 Z. z. o dôveryhodných službách. Kvalifikovaný podpis má účinky vlastnoručného podpisu; pri zahraničných partneroch overiť akceptáciu podpisu v danej krajine. |

### **4.2 Integrita, etika a školenia**

| Vrstva | Účel | Minimálne riešenie (0–3 mes.) | Cieľové riešenie (9–18 mes.) | Poznámka SK/EÚ |
| :---- | :---- | :---- | :---- | :---- |
| **Whistleblowing (zákon č. 54/2019 Z. z.)** | Bezpečný (aj anonymný) kanál na podávanie podnetov, evidencia a preverovanie, dôvernosť identity oznamovateľa. | Vyhradená e-mailová schránka a telefonická linka prístupná len zodpovednej osobe (CCO), možnosť osobného stretnutia, evidencia podnetov v zóne Dôverné; zverejnené pravidlá vnútorného systému. | Webová whistleblowing platforma s anonymnou obojsmernou komunikáciou a správou prípadov (napr. WhistleLink, EQS Integrity Line alebo iný poskytovateľ so serverom v EÚ, ktorý preukáže súlad so slovenskou úpravou). | Zákon č. 54/2019 Z. z. – vnútorný systém, zodpovedná osoba, zákonné lehoty a dôvernosť; Úrad na ochranu oznamovateľov. Prístup IT administrátorov k obsahu podnetov musí byť vylúčený alebo zmluvne a technicky obmedzený. |
| **LMS – školenia** | Priradenie povinných školení podľa role, testy, certifikáty, evidencia pre audit. | Prezentácie a videá v internom úložisku \+ test cez Google Forms / Microsoft Forms; evidencia absolvovania v tabuľke; pre agentov zaslanie materiálov a podpísané potvrdenie. | LMS (napr. Moodle, TalentLMS alebo modul HR systému) s automatickým priraďovaním podľa role z IAM, pripomienkami, testami a reportmi; prístup aj pre externých agentov. | Obsah podľa rámca: kódex, ABAC, informačná bezpečnosť, GDPR, exportná kontrola; osobitné poučenia pre utajované skutočnosti vedie Bezpečnostný manažér mimo bežného LMS. |
| **Register darov a stretnutí** | Evidencia poskytnutých a prijatých darov a pohostení, stretnutí s verejnými funkcionármi, schvaľovanie nad limit. | Formulár (Google Forms / Microsoft Forms) zapisujúci do chránenej tabuľky; e-mailové schválenie CCO pri verejných funkcionároch a nad limit; mesačná kontrola CCO. | Modul registra darov a konfliktov záujmov v compliance/GRC platforme s workflow schvaľovania, prepojením na výdavky v ERP (cestovné náhrady, reprezentačné). | Limity stanovuje interný predpis (nie tento dokument). Pri verejných zákazkách a štátnych zákazníkoch zvýšená opatrnosť; register slúži aj ako dôkaz pre zákon č. 91/2016 Z. z. |

### **4.3 Obchod a financie**

| Vrstva | Účel | Minimálne riešenie (0–3 mes.) | Cieľové riešenie (9–18 mes.) | Poznámka SK/EÚ |
| :---- | :---- | :---- | :---- | :---- |
| **CRM \+ limity plných mocí** | Obchodné prípady, kontakty s verejným sektorom, väzba na agenta a jeho oprávnenia (úkony, suma, krajiny, platnosť). | Existujúce CRM alebo tabuľka obchodných prípadov s povinným ID partnera; v profile agenta polia „rozsah plnej moci“, „finančný limit“, „územie“, „platnosť do“. | CRM (napr. HubSpot, Pipedrive) s vlastnými poľami a validáciou: ponuka nad limit alebo mimo územia vyžaduje schválenie; blokácia prípadu, ak DD partnera nie je platná; synchronizácia s registrom partnerov. | Osobné údaje kontaktov podľa GDPR (právny základ, doba uchovávania). Ponuky do štátnych tendrov podáva spoločnosť, nie agent bez osobitného splnomocnenia. |
| **ERP / účtovníctvo \+ 4 oči \+ IBAN lock** | Párovanie faktúr so zmluvou a výkonom, oddelenie zadania a schválenia platby, ochrana proti podvodnej zmene bankového účtu. | Súčasný účtovný systém (napr. Pohoda, Money S3); dvojité schválenie platieb v internetbankingu (dve rôzne osoby); zmena IBAN len na základe formulára a spätného telefonického overenia na známom kontakte, zapísaného do registra. | ERP (napr. SAP Business One alebo vyššia verzia existujúceho systému) so schvaľovacím workflow podľa limitov, zamknutým kmeňovým záznamom bankového účtu (zmena len cez rolu Financie \+ schválenie inou osobou), blokáciou platby partnerovi bez platnej DD a reportom provízií agentov. | Zákon č. 431/2002 Z. z. o účtovníctve (preukázateľnosť, archivácia); pri platbách do tretích krajín sankčná kontrola banky nenahrádza vlastnú kontrolu. Úplné zákazy platieb v hotovosti a tretím stranám podľa rámca. |

### **4.4 Identity a IT bezpečnosť**

| Vrstva | Účel | Minimálne riešenie (0–3 mes.) | Cieľové riešenie (9–18 mes.) | Poznámka SK/EÚ |
| :---- | :---- | :---- | :---- | :---- |
| **IAM / MFA / on-offboarding** | Jedna firemná identita na osobu, MFA, prístupy podľa role, odobratie prístupov v deň odchodu. | Microsoft Entra ID alebo Google Workspace ako jediný adresár; povinné MFA pre všetkých (aj externých); zoznam aplikácií a ich vlastníkov; checklist on/offboardingu z Prílohy B rámca s podpisom IT. | SSO do všetkých aplikácií (CRM, ERP, LMS, ticketing), podmienený prístup (len spravované zariadenia, rizikové prihlásenia), skupiny podľa rolí, automatický on/offboarding na základe udalosti v HR, pravidelná recertifikácia prístupov, správa privilegovaných účtov. | NIS2 vyžaduje riadenie prístupov a viacfaktorovú autentifikáciu ako súčasť opatrení; utajované prostredie má samostatnú správu identít mimo firemného adresára. |
| **IT bezpečnosť NIS2 (EDR, zálohy, SIEM)** | Ochrana koncových zariadení, obnova po incidente, centrálny záznam a vyhodnocovanie bezpečnostných udalostí. | EDR na všetkých zariadeniach (napr. Microsoft Defender for Business / Microsoft 365 Defender), správa zariadení a aktualizácií, zálohy podľa pravidla 3-2-1 s jednou offline / nemennou kópiou a otestovanou obnovou, centrálne logovanie v rámci tenantu. | SIEM/SOC (napr. Microsoft Sentinel, open-source Wazuh alebo externá SOC služba) s 24/7 monitoringom alebo dohodnutou pohotovosťou, správa zraniteľností, bezpečnosť dodávateľov IKT, ISMS podľa ISO/IEC 27001\. | Zákon č. 69/2018 Z. z. o kybernetickej bezpečnosti a smernica (EÚ) 2022/2555 (NIS2) – najprv posúdiť, či spoločnosť spadá do pôsobnosti; hlásenie incidentov podľa kapitoly 7 rámca (24 h / 72 h / 1 mesiac). |
| **Prostredie pre utajované (NBÚ)** | Spracúvanie a uchovávanie utajovaných skutočností oddelene od bežného IT. | Kým nie je prostredie certifikované: **žiadne elektronické spracúvanie utajovaných informácií**; len postupy schválené Bezpečnostným manažérom (listinná forma, zabezpečené uloženie, registratúra), konzultácia s NBÚ. | Oddelené (air-gapped) pracovisko s technickými prostriedkami certifikovanými/schválenými podľa požiadaviek NBÚ, v zabezpečenom priestore, s bezpečnostnou dokumentáciou, evidenciou nosičov a kryptografickou ochranou podľa stupňa utajenia; nadväzne bezpečnostná previerka podnikateľa. | Zákon č. 215/2004 Z. z. a vykonávacie predpisy; požiadavky NATO/EÚ pri ich utajovaných informáciách. Riešenie sa navrhuje s bezpečnostným poradcom; konkrétne produkty tento dokument neuvádza. |

### **4.5 Prevádzka, komunikácia so štátom a archív**

| Vrstva | Účel | Minimálne riešenie (0–3 mes.) | Cieľové riešenie (9–18 mes.) | Poznámka SK/EÚ |
| :---- | :---- | :---- | :---- | :---- |
| **Incident / ticketing** | Jednotné prijatie, evidencia a riešenie incidentov (kybernetických, únikov osobných údajov, compliance podozrení) s časovou stopou pre zákonné lehoty. | Zdieľaná schránka „incident@“ (s obmedzeným prístupom) \+ tabuľka incidentov s časom zistenia, typom, vlastníkom a stavom hlásenia; jednostranové playbooky. | Ticketing (napr. Jira Service Management, Freshservice) s kategóriami podľa kapitoly 7 rámca, časovačmi pre lehoty hlásení, oddelenými projektmi s obmedzeným prístupom (compliance prípady nevidí bežné IT). | Lehoty: NIS2 (24 h / 72 h / 1 mesiac), GDPR (72 h). Podnety whistleblowerov sa v bežnom ticketingu neevidujú. Utajované incidenty len mimo bežných systémov. |
| **eSchránka \+ archív** | Prijímanie úradných rozhodnutí a doručovanie štátu, dlhodobé uchovávanie zmlúv, DD spisov a záznamov pre audit. | Elektronická schránka právnickej osoby na slovensko.sk s určenými oprávnenými osobami a zástupcami, notifikáciami a denným kontrolným režimom; archívne priečinky s retenciou a obmedzeným mazaním. | Registratúrny/DMS systém s registratúrnym plánom, retenčnými pravidlami, integráciou na eSchránku a e-podpis, uchovávaním kvalifikovaných podpisov s dlhodobou overiteľnosťou (služba uchovávania podľa eIDAS). | Zákon č. 305/2013 Z. z. o e-Governmente (aktivovaná schránka – doručovanie s právnymi účinkami); zákon č. 395/2002 Z. z. o archívoch a registratúrach (ak sa uplatní); lehoty uchovávania podľa zákona o účtovníctve, daňových predpisov a interného registratúrneho poriadku. |

### **4.6 Integrácie – minimálny tok dát**

| Zdroj | Cieľ | Čo sa prenáša | Účel kontroly |
| :---- | :---- | :---- | :---- |
| Register partnerov | CRM, ERP | ID partnera, stav DD (platná / blokovaná), dátum re-previerky | Žiadna ponuka nad limit ani platba bez platnej DD |
| Sankčný screening | Register partnerov | Výsledok a dátum screeningu, nové zhody | Okamžitá blokácia pri zhode |
| Zmluvy / e-podpis | CRM, archív | Rozsah plnej moci, finančný limit, platnosť zmluvy | Agent koná len v rozsahu splnomocnenia |
| HR / IAM | Všetky aplikácie, LMS | Nástup, zmena role, odchod | Prístupy a školenia podľa role; odobratie prístupov v deň odchodu |
| EDR, IAM, aplikácie | SIEM, ticketing | Bezpečnostné udalosti a výstrahy | Detekcia a dodržanie lehôt hlásenia |

## **5\. RACI-lite – kto používa ktorý nástroj**

Legenda: **A** – vlastník nástroja (konfigurácia, pravidlá, kvalita dát, prístupy); **R** – aktívne používa a zapisuje; **C** – konzultovaný alebo schvaľuje vo workflow; **I** – len čítanie / reporty. Prázdne pole znamená bez prístupu. Interný audit má čítací prístup (I) ku všetkým nástrojom okrem obsahu podnetov whistleblowerov a utajovaného prostredia (tam len podľa osobitných pravidiel).

| Nástroj / vrstva | CCO | CISO | Bezp. manažér | Obchod | Financie | Legal |
| :---- | ----- | ----- | ----- | ----- | ----- | ----- |
| Register partnerov \+ DD | A |  | C | R | I | C |
| Sankčný screening | A/R |  |  | I | I | C |
| Zmluvy \+ e-podpis | C |  | C | R | I | A |
| Whistleblowing | A/R |  |  |  |  | C |
| LMS – školenia | A | R | C | R | R | R |
| Register darov a stretnutí | A |  |  | R | I | I |
| CRM \+ limity plných mocí | I |  |  | A/R | I | C |
| ERP \+ 4 oči \+ IBAN lock | C | C |  | I | A/R |  |
| IAM / MFA / on-offboarding | I | A/R | C | C | C | I |
| IT bezpečnosť NIS2 (EDR, zálohy, SIEM) | I | A/R | C |  |  |  |
| Prostredie pre utajované (NBÚ) |  | C | A/R |  |  |  |
| Incident / ticketing | R | A | R | I | I | C |
| eSchránka \+ archív | I | C |  |  | R | A |

*Poznámka:* Konkrétnu osobu s prístupom do utajovaného prostredia určuje Bezpečnostný manažér podľa previerky a need-to-know – nie podľa funkcie. Pri eSchránke sa odporúča určiť aspoň dve oprávnené osoby (zastupovanie) a denne kontrolovať doručené správy.

## **6\. Fázový plán zavedenia (checklist)**

| Fáza 1: 0–3 mesiace (minimum, rýchle kontroly) | Fáza 2: 3–9 mesiacov (zavedenie a prepojenie) | Fáza 3: 9–18 mesiacov (cieľový stav a overenie) |
| :---- | :---- | :---- |
| ☐ Register partnerov v tabuľke \+ formulár; inventúra všetkých agentov a partnerov ☐ Sankčný screening všetkých existujúcich partnerov a zápis výsledkov ☐ Dvojité schválenie platieb v internetbankingu; postup overenia zmeny IBAN ☐ Povinné MFA pre všetky účty; jediný firemný adresár (Entra ID / Google Workspace) ☐ EDR na všetkých zariadeniach; zálohy 3-2-1 s offline kópiou a test obnovy ☐ Whistleblowing kanál (schránka \+ linka) a zverejnené pravidlá ☐ Register darov a stretnutí (formulár) ☐ Schválené šablóny zmlúv a kvalifikovaný e-podpis pre štatutárov ☐ Kontrola nastavenia eSchránky, oprávnených osôb a notifikácií ☐ Tabuľka incidentov a jednostranové playbooky ☐ Pravidlo: žiadne utajované informácie v bežnom IT; konzultácia s NBÚ | ☐ Výber a zavedenie CRM s poľami plných mocí a väzbou na ID partnera ☐ Re-kontraktácia agentov s doložkami a presnými plnými mocami (e-podpis) ☐ LMS a prvé ročné školenia s testom (aj pre agentov) ☐ SSO pre kľúčové aplikácie; recertifikácia prístupov ☐ Ticketing s kategóriami a časovačmi lehôt ☐ Výber whistleblowing platformy a migrácia evidencie ☐ ERP workflow schvaľovania a zamknutý kmeňový záznam IBAN ☐ Posúdenie pôsobnosti NIS2 a zavedenie ISMS ☐ Návrh oddeleného utajovaného prostredia s bezpečnostným poradcom ☐ Pravidlá retencie v archíve a registratúrny plán | ☐ Platforma TPRM/GRC s workflow DD a automatickými pripomienkami re-previerky ☐ Automatizovaný sankčný screening s dávkovým re-screeningom ☐ Integrácie register partnerov ↔ CRM ↔ ERP (blokácia bez platnej DD) ☐ SIEM / SOC služba a správa zraniteľností ☐ Automatický on/offboarding z HR ☐ Certifikované utajované prostredie a bezpečnostná previerka podnikateľa (NBÚ) ☐ DMS / registratúra s integráciou na eSchránku a e-podpis ☐ Interný audit nástrojov a kontrol; cvičenie incident response ☐ Podklady pre certifikácie ISO/IEC 27001 a ISO 37001 ☐ Revízia stacku a dokumentu na verziu 2.0 |

## **7\. Príloha – mini-schémy postupov**

### **Príloha A – Platba agentovi**

| Krok | Činnosť | Kto | Systém | Kontrola / STOP podmienka |
| ----- | :---- | :---- | :---- | :---- |
| 1 | Prijatie faktúry od agenta s odkazom na zmluvu a obchodný prípad | Financie | ERP, eSchránka / e-mail fakturácie | STOP, ak chýba ID partnera alebo odkaz na zmluvu |
| 2 | Overenie platnosti DD a sankčného screeningu partnera | Financie | Register partnerov | STOP, ak je DD neplatná, re-previerka po termíne alebo partner blokovaný |
| 3 | Párovanie: faktúra – zmluva (sadzba provízie) – dôkaz o výkone (správa, obchodný prípad v CRM) | Obchod (potvrdí výkon), Financie | CRM, ERP | STOP, ak výška nezodpovedá zmluve, chýba dôkaz o výkone alebo ide o zálohu bez výkonu |
| 4 | Kontrola príjemcu: IBAN na meno agenta, krajina sídla/pôsobenia, zhoda so zamknutým záznamom | Financie | ERP (IBAN lock) | STOP pri platbe tretej strane, do inej krajiny, v hotovosti alebo pri nedávnej zmene IBAN bez overenia |
| 5 | Zadanie platby jednou osobou | Financie – zadávateľ | ERP / internetbanking | Zadávateľ nesmie byť schvaľovateľ |
| 6 | Schválenie druhou osobou; nad interný limit alebo pri red flag aj CCO | Financie – schvaľovateľ, CCO | Internetbanking (dvojité schválenie) | Pri red flag eskalácia CCO; pri podozrení postup podľa kapitoly 7 rámca |
| 7 | Archivácia podkladov a záznamu o schválení; mesačný report provízií agentov | Financie, CCO | ERP, archív | Vzorka pre interný audit |

### **Príloha B – Onboarding zahraničného obchodníka / agenta**

| Krok | Činnosť | Kto | Systém | Výstup |
| ----- | :---- | :---- | :---- | :---- |
| 1 | Odôvodnenie potreby agenta (trh, služby, prečo nie priamy predaj) a zápis do registra | Obchod (vlastník vzťahu) | Register partnerov (formulár) | ID partnera, stav „v preverovaní“ |
| 2 | DD dotazník agenta, výpis z registra, KUV, referencie, väzby na verejných funkcionárov | Agent, Obchod, CCO | Register partnerov, priečinok DD (Dôverné) | Kompletný DD spis |
| 3 | Sankčný screening, adverse media, rizikové skóre krajiny; posúdenie produktov a krajín exportnou kontrolou | CCO, Export Control Officer | Sankčný screening, register | Rizikové skóre, záver, prípadné podmienky |
| 4 | Schválenie spolupráce (pri vysokom riziku aj štatutár) | CCO / štatutár | Register partnerov (workflow) | Stav „schválený“ alebo „zamietnutý“ |
| 5 | Agentská zmluva s compliance doložkami, audit right, zákazom platieb tretím stranám; plná moc s rozsahom, limitom, územím a platnosťou | Legal, štatutár | Šablóny, e-podpis, archív | Podpísaná zmluva a plná moc; limity zapísané v CRM |
| 6 | ABAC školenie s testom, ročný ABAC certifikát, vyhlásenie o konflikte záujmov | Agent, CCO | LMS / formulár | Certifikát a podpísané vyhlásenia |
| 7 | Založenie partnera v ERP, overenie a zamknutie IBAN (spätné overenie na známom kontakte) | Financie | ERP | Zamknutý bankový účet na meno agenta |
| 8 | Prístupy: len partnerský portál alebo zdieľaný priestor s MFA, výlučne údaje potrebné pre jeho trh; žiadny prístup k utajovaným ani exportne citlivým technickým údajom bez posúdenia | CISO / IT, vlastník vzťahu | IAM | Pridelené a zdokumentované prístupy |
| 9 | Nastavenie termínu ročnej re-previerky a hlásenia kontaktov s verejnými funkcionármi | CCO, Obchod | Register partnerov, register stretnutí | Aktívny partner s termínom re-previerky |

## **8\. Správa dokumentu**

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý návrh – prax a technologický stack k rámcu v1.0 | NÁVRH – na právne, bezpečnostné a IT overenie |

Vlastníkmi dokumentu sú spoločne Chief Compliance Officer (procesy a compliance nástroje) a CISO (IT a bezpečnostné nástroje); časť o utajovanom prostredí schvaľuje Bezpečnostný manažér. Dokument sa reviduje najmenej raz ročne a pri zmene nástrojov, legislatívy alebo obchodného modelu.