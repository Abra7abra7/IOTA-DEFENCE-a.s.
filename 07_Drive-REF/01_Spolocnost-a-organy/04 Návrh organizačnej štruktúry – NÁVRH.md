**Návrh organizačnej štruktúry IOTA Defence**

IOTA Defence a.s. · Verzia 3.0 · 20\. 10\. 2026 · Vypracoval: Márian Stančík · Klasifikácia: Interné – Dôverné · Stav: NÁVRH

| Upozornenie |
| :---- |
| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. Verzia 3.0 nahrádza verziu 2.0 (archivovaná v priečinku 99\_Archiv spolu s verziou 1.0) a zapracúva odpovede Mariana na otvorené otázky k verzii 2.0 z 20\. 10\. 2026\. Nadväzuje na [Rámec organizácie, compliance a bezpečnosti v1.1](https://docs.google.com/document/d/1zOz-IPOs1SoTmKwQo6jDrqPL_NZk29Tl5oDKKSCup8o/edit) a na [návrh uznesení predstavenstva U-01 až U-13](https://docs.google.com/document/d/1EMnq77eS-b8mEu_rFJHd2lYhST9t-6FloC3bJMfUpsQ/edit). Citácie predpisov boli overené v primárnych zdrojoch (Slov-Lex, EUR-Lex, Úradný vestník EÚ, eCFR, oficiálne stránky) k 20\. 10\. 2026\. Pred zavedením overí advokát, bezpečnostný poradca (NBÚ) a odborník na výbušniny (HBÚ). Údaje označené \[DOPLNIŤ\] treba doplniť. |

# **0\. Čo je nové vo verzii 3.0**

| Odpoveď Mariana | Čo z toho vyplýva pre návrh |
| :---- | :---- |
| Chairman bude predsedom dozornej rady | **Potvrdené.** Predpoklad z verzie 2.0 je odstránený. |
| Muníciu s výbušninou budeme vyrábať a skladovať sami na Slovensku | Útvar HSE a povolenia HBÚ a obvodného banského úradu sú pevnou súčasťou plánu. **Miesto skladu zatiaľ nie je určené** (otázka č. 1). |
| Či použijeme americké súčiastky alebo softvér, zatiaľ nevieme | Nová kapitola 8 opisuje postup pre obe možnosti: zaradenie každej súčiastky a softvéru už pri návrhu, kusovník s exportnou klasifikáciou, pravidlo de minimis podľa EAR, návrh bez súčiastok podliehajúcich ITAR („ITAR free“) a kto o čom rozhoduje. |
| Vo vývoji budú pracovať aj ľudia z krajín mimo EÚ | Nová kapitola 12: pobyt a povolenie na zamestnanie, kontrola prístupu podľa štátnej príslušnosti, deemed export pri amerických technológiách, previerky NBÚ pre cudzincov a ich obmedzenia, oddelené prístupy v IT a plán kontroly technológií. Vývoj sa delí na otvorený a kontrolovaný tím. |
| Agentov a distribútorov budeme mať po celom svete | Nová kapitola 10: úplný program pre tretie strany (stupne rizika, preverenie, zmluvné doložky, schvaľovanie, strop odmeny, monitorovanie, registre). Pribúda Výbor pre tretie strany a druhý analytik v compliance do 12 mesiacov. |
| 31\. človeka zatiaľ nevieme určiť | Východiskový organigram má 30 obsadených miest; 31\. miesto treba upresniť. |

# **1\. Zhrnutie**

IOTA Defence bude vyrábať drony, UAV systémy, muníciu a softvér a predávať ich do celého sveta. To je najprísnejšie regulovaná kombinácia v obrannom priemysle: munícia s výbušninou podlieha Hlavnému banskému úradu a obvodným banským úradom, každý vývoz mimo EÚ potrebuje licenciu MH SR s dokladom o konečnom užívateľovi, drony a softvér môžu byť vojenským materiálom aj položkami s dvojakým použitím a prenos softvéru cez cloud alebo e-mail do zahraničia je tiež vývoz. K tomu pribúda práca s utajovanými skutočnosťami stupňa Dôverné až Tajné.

Verzia 3.0 dopĺňa tri veci, ktoré pri tomto profile rozhodujú: (1) každá súčiastka a softvér dostane exportné zaradenie už pri návrhu, aby americký obsah nezablokoval predaj; (2) ľudia z krajín mimo EÚ môžu pracovať vo vývoji, ale len v otvorenom tíme a s prístupom, ktorý schváli ECO; (3) každý agent a distribútor prejde preverením podľa stupňa rizika a schválením compliance, má zmluvu s povinnými doložkami a strop odmeny.

Navrhujeme štruktúru v troch vrstvách. Navrchu sú orgány akciovej spoločnosti: valné zhromaždenie, dozorná rada (jej predsedom bude dnešný Chairman, potvrdené) a predstavenstvo. Pod CEO je šesť výkonných útvarov: Vývoj a inovácie, Výroba (UAV a munícia), Bezpečnosť výroby a výbušnín, Kvalita, Obchod a obranné zákazky a Financie a administratíva. Mimo obchodu a výroby stoja tri nezávislé útvary druhej línie, ktoré reportujú priamo predstavenstvu a majú priamy prístup k predsedovi dozornej rady: Compliance, Exportná kontrola a sankcie a Bezpečnosť (utajované skutočnosti a ochrana objektov). Interný audit reportuje dozornej rade.

Ľudia sa presúvajú bez prepúšťania. Treba však prijať alebo externe zabezpečiť približne 5 až 7 odborníkov: skúseného compliance officera, vedúceho exportnej kontroly (zodpovedného zástupcu podľa zákona o obchodovaní s výrobkami obranného priemyslu), bezpečnostného riaditeľa s previerkou NBÚ, zodpovedného zástupcu pre výbušniny s osvedčením HBÚ, pyrotechnika a softvérových vývojárov.

# **2\. Nová štruktúra – schéma**

**Poznámka:** východiskový organigram má 30 obsadených miest; 31\. miesto treba upresniť.

VALNÉ ZHROMAŽDENIE AKCIONÁROV (akcionári zo SR a EÚ)  
 \|  
 \+-- DOZORNÁ RADA (min. 3 členovia) – predseda: dnešný Chairman (potvrdené)  
 \|     \+-- Interný audit (externý, reportuje DR)  
 \|     .. priamy prístup: CCO, ECO, Bezpečnostný riaditeľ  
 \|  
 \+-- PREDSTAVENSTVO – predseda: CEO  
       \|  
       \+-- 2\. LÍNIA (nezávislé útvary, reportujú predstavenstvu)  
       \|     \+-- COMPLIANCE: CCO \+ analytik DD (+ 2\. analytik do 12 mesiacov)  
       \|     \|      program pre tretie strany; Výbor pre tretie strany (CCO, ECO, CFO)  
       \|     \|      CCO \= zodpovedná osoba pre oznamovateľov  
       \|     \+-- EXPORTNÁ KONTROLA A SANKCIE: ECO \+ 2 špecialisti  
       \|     \|      ECO \= zodpovedný zástupca (z. 392/2011) a osoba zodpovedná za transfery  
       \|     \|      klasifikácia a kusovník (BOM), plán kontroly technológií (TCP)  
       \|     \+-- BEZPEČNOSŤ: Bezpečnostný riaditeľ (vlastný, plný úväzok)  
       \|     \|      \+ osobitné pracovisko / registratúra utajovaných skutočností  
       \|     \|      \+ CISO (spočiatku externý, do 12 mesiacov vlastný)  
       \|     \+-- Externe: advokát, DPO  
       \|  
       \+-- CEO  
             \+-- Kvalita (manažér kvality, priamo CEO)  
             \+-- Bezpečnosť výroby a výbušnín (HSE) – zodpovedný zástupca podľa z. 58/2014  
             \+-- Vývoj a inovácie (CTO) – hardvér, softvér  
             \|     \+-- Otvorený tím (môžu byť aj ľudia mimo EÚ)  
             \|     \+-- Kontrolovaný tím (VM, kontrolované a utajované; len schválení ECO)  
             \+-- Výroba (vedúci výroby)  
             \|     \+-- Výroba UAV a systémov  
             \|     \+-- Výroba munície (len s povolením HBÚ)  
             \+-- Riaditeľ stratégie a obchodu (dnešný CSO)  
             \|     \+-- Obchod a obranné zákazky  
             \|     \+-- Programy a granty (PMO, EDF, EDIP)  
             \+-- CFO: Financie a administratíva  
                   \+-- Financie a controlling  
                   \+-- HR (aj pobyt a povolenia cudzincov)  
                   \+-- Nákup a dodávateľský reťazec  
                   \+-- IT prevádzka (oddelené zóny prístupov)

| Úroveň | Útvar | Vedie | Reportuje | Ľudia (návrh) |
| :---- | :---- | :---- | :---- | :---- |
| Orgány a.s. | Valné zhromaždenie | akcionári (SR a EÚ) | — | — |
| Orgány a.s. | Dozorná rada | predseda DR \= dnešný Chairman (potvrdené) | valnému zhromaždeniu | min. 3 (§ 200 ods. 1 ObZ) |
| Orgány a.s. | Predstavenstvo | predseda \= CEO | valnému zhromaždeniu; informuje DR | napr. 3: CEO, CFO, Riaditeľ stratégie a obchodu \[DOPLNIŤ podľa stanov\] |
| 3\. línia | Interný audit | externý dodávateľ | funkčne DR | externe |
| 2\. línia | Compliance | CCO | predstavenstvu; priamy prístup k predsedovi DR | 2 (CCO nový nábor \+ 1); do 12 mesiacov \+ 1 analytik DD |
| 2\. línia | Exportná kontrola a sankcie | ECO | predstavenstvu; priamy prístup k predsedovi DR | 3 (ECO \+ 2\) |
| 2\. línia | Bezpečnosť | Bezpečnostný riaditeľ | predstavenstvu (gestor bezpečnosti); priamy prístup k predsedovi DR | 2 \+ externý CISO |
| 1\. línia | Kvalita | manažér kvality | priamo CEO | 1 |
| 1\. línia | Bezpečnosť výroby a výbušnín (HSE) | zodpovedný zástupca podľa z. 58/2014 | priamo CEO (nie výrobe) | 1 \+ pyrotechnik (nový nábor) |
| 1\. línia | Vývoj a inovácie | CTO | CEO | 3 \+ noví vývojári; otvorený a kontrolovaný tím |
| 1\. línia | Výroba (UAV, munícia) | vedúci výroby | CEO | 6 (4 UAV \+ 2 munícia) |
| 1\. línia | Obchod; Programy a granty | Riaditeľ stratégie a obchodu | CEO | 1 \+ 3 \+ 1 |
| 1\. línia | Financie a administratíva | CFO | CEO | 1 \+ 6 |

Prečo takto: pri predaji do celého sveta je najväčšie riziko v licenciách, sankciách a agentoch. Zákon č. 91/2016 Z. z. umožňuje firme vyhnúť sa trestnej zodpovednosti len vtedy, ak preukáže účinné kontrolné mechanizmy (§ 4 ods. 7). Kontrola preto nesmie byť podriadená obchodu, výrobe ani financiám a odmena kontrolórov nesmie závisieť od obratu (Rámec v1.1, kap. 1.4). Bezpečnosť výroby munície je oddelená od výroby, aby tlak na termíny nikdy neprevážil bezpečnosť.

# **3\. Úloha CSO – stratégia verzus bezpečnosť**

Dnešný CSO (Chief Strategy Officer) sa stane **Riaditeľom stratégie a obchodu** (1. línia, reportuje CEO) a vedie obchod a programy. V obrannom priemysle a u NBÚ sa skratka CSO číta ako Chief Security Officer, preto ju v dokumentoch nepoužívame. Bezpečnosť vedie **Bezpečnostný riaditeľ** – vlastný zamestnanec na plný úväzok, písomne poverený ako bezpečnostný zamestnanec podľa § 9 ods. 1 zákona č. 215/2004 Z. z. Predpokladom je platné osvedčenie NBÚ a skúška bezpečnostného zamestnanca; pri stupni Tajné odporúčame previerku na stupeň Tajné.

# **4\. Povinné a nezávislé funkcie**

| Funkcia | Prečo ju potrebujeme | Kto ju vykonáva (návrh) | Komu reportuje | Čo nesmie |
| :---- | :---- | :---- | :---- | :---- |
| Zodpovedný zástupca pre obchod s výrobkami obranného priemyslu | Podmienka povolenia MH SR (§ 5 ods. 1 a § 8 z. 392/2011): vek 25 rokov, pobyt v SR, bezúhonnosť, spoľahlivosť, VŠ II. stupňa, pracovnoprávny vzťah, len pre jedného žiadateľa. | ECO | predstavenstvu | byť členom dozornej rady (§ 8 ods. 4\) |
| Zamestnanec zodpovedný za transfery a vývozy | Podmienka certifikátu príjemcu (§ 30 ods. 1 z. 392/2011; čl. 9 smernice 2009/43/ES). | ECO | predstavenstvu | byť podriadený obchodu |
| Zodpovedný zástupca podľa zákona o výbušninách | Žiadosť o povolenie HBÚ obsahuje doklad o odbornej spôsobilosti žiadateľa alebo jeho zodpovedného zástupcu (§ 42 ods. 2 písm. b) bod 5 z. 58/2014); pri munícii osvedčenie HBÚ podľa § 31 ods. 5\. Schvaľuje technologické postupy výroby. | vedúci HSE | CEO | byť podriadený vedúcemu výroby |
| Útvar alebo odborník BOZP pre výbušniny a technik požiarnej ochrany | § 3 ods. 5 písm. a) a b) z. 58/2014. | HSE (požiarnu ochranu možno externe) | CEO | — |
| Pyrotechnik skupiny C, D alebo E | Pri výskume, vývoji, skúšaní a výrobe smie privádzať výbušniny k výbuchu len pyrotechnik týchto skupín (§ 43 ods. 3 z. 58/2014). | nový nábor v HSE alebo vo Výrobe | vedúcemu HSE | — |
| Zodpovedná osoba držiteľa zbrojnej licencie | Len ak budeme vyvíjať alebo vyrábať strelné zbrane alebo strelivo (náboje do 20 mm): zbrojná licencia skupiny A (§ 29 a § 30 z. 190/2003). | vedúci HSE alebo vedúci výroby | CEO | — |
| Bezpečnostný zamestnanec a osobitné pracovisko | Úlohy podľa z. 215/2004 (§ 9 ods. 1); bezpečnostný projekt podnikateľa pre previerku NBÚ (§ 45); chránené priestory (§ 53). | Bezpečnostný riaditeľ \+ registrátor utajovaných skutočností | predstavenstvu; priamy prístup k predsedovi DR | kumulovať s obchodom alebo nákupom |
| Compliance officer (CCO) | Účinné kontrolné mechanizmy (§ 4 ods. 7 z. 91/2016); primerané postupy (s. 7 ods. 2 UK Bribery Act); ISO 37001 a ISO 37301\. | CCO (nový nábor) | predstavenstvu; priamy prístup k predsedovi DR | mať odmenu naviazanú na obrat |
| Zodpovedná osoba pre oznamovateľov | Povinná od 50 zamestnancov (§ 10 ods. 1 z. 54/2019); odporúčame hneď. | CCO; príjem oznámení môže byť externý (§ 10 ods. 2\) | predstavenstvu; pri podozrení na člena predstavenstva predsedovi DR | mať úlohy v konflikte záujmov |
| Manažér kvality | AQAP 2110 vyd. D, kap. 5.1.1: zástupca vedenia pre kvalitu s priamym reportom vrcholovému vedeniu. | manažér kvality | priamo CEO | byť podriadený výrobe |
| CISO | Riadenie kybernetických rizík; ISMS podľa ISO/IEC 27001; certifikovaný IT systém pre utajované skutočnosti (§ 55 a 56 z. 215/2004). | externý vCISO, do 12 mesiacov vlastný | predstavenstvu (gestor bezpečnosti) | vykonávať bežnú IT administráciu |
| Vlastník klasifikácie, kusovníka a plánu kontroly technológií | Bez zaradenia nemožno určiť licenciu ani americký obsah (15 CFR 734.4; 22 CFR 120.11(c)); plán bezpečnosti technológií pri ITAR (22 CFR 126.18(c)). | ECO a špecialista klasifikácie | predstavenstvu | schvaľovať vlastné obchodné prípady |
| Vlastník programu tretích strán | Zdokumentované preverenie partnerov podľa rizika a dohľad (odporúčanie OECD 2021, príloha II, A.6); zodpovednosť za sprostredkovateľov (§ 4 z. 91/2016; s. 7 UK Bribery Act). | CCO a analytik DD; Výbor pre tretie strany | predstavenstvu | byť odmeňovaný podľa objemu predaja |
| Interný audit | Nezávislé overenie kontrol vrátane exportu a výbušnín. | externý dodávateľ | funkčne DR | vykonávať činnosti 1\. alebo 2\. línie |

# **5\. Presun ľudí z dnešných oddelení**

Presun je návrh podľa názvov oddelení; mená a zaradenie treba potvrdiť podľa toho, čo ľudia dnes robia a čo vedia.

| Dnes | Počet | Kam v novej štruktúre | Počet | Poznámka |
| :---- | :---- | :---- | :---- | :---- |
| Chairman of the Board | 1 | predseda dozornej rady | 1 | potvrdené |
| CEO | 1 | predseda predstavenstva a CEO | 1 | gestor bezpečnosti |
| CSO (stratégia) | 1 | Riaditeľ stratégie a obchodu | 1 | člen predstavenstva podľa stanov |
| CFO | 1 | CFO – Financie a administratíva | 1 | člen predstavenstva podľa stanov |
| Strategy management | 7 | Obchod a obranné zákazky | 2 | spolu s dnešným obchodníkom 3 |
|  |  | Programy a granty (PMO, EDF, EDIP) | 1 |  |
|  |  | Compliance – analytik DD agentov, distribútorov a offsetov | 1 | po zaškolení |
|  |  | Exportná kontrola a sankcie – klasifikácia, licencie, screening | 2 | jeden z nich môže byť ECO, ak spĺňa § 8 z. 392/2011 |
|  |  | Bezpečnosť – kandidát na Bezpečnostného riaditeľa | 1 | ak spĺňa podmienky NBÚ (občianstvo SR, previerka); inak nový nábor |
| Manufacture | 8 | Výroba UAV a systémov | 4 | vedúci výroby \+ 3 |
|  |  | Výroba munície | 2 | až po povolení HBÚ; dovtedy UAV |
|  |  | Kvalita | 1 | reportuje CEO |
|  |  | Bezpečnosť výroby a výbušnín (HSE) | 1 | kandidát na zodpovedného zástupcu, ak získa osvedčenie HBÚ |
| Office management | 7 | Financie a controlling | 2 | platby so štyrmi očami |
|  |  | HR | 1 | nástupy, previerky, pobyt a povolenia cudzincov, kontrola štátnej príslušnosti spolu s ECO, školenia |
|  |  | Nákup a dodávateľský reťazec | 2 | preverovanie dodávateľov, pôvod komponentov (EÚ, USA) |
|  |  | IT prevádzka | 1 | 1\. línia; dohľad robí CISO |
|  |  | Bezpečnosť – osobitné pracovisko (registratúra utajovaných skutočností) | 1 | potrebuje osvedčenie NBÚ |
| Development | 3 | Vývoj a inovácie (hardvér, softvér) | 3 | jeden z nich ako CTO |
| Sales | 1 | Obchod a obranné zákazky | 1 |  |
| 31\. miesto | — | \[upresniť\] | — | východiskový organigram má 30 obsadených miest; 31\. treba upresniť |
| **Spolu** | **30 \+ 1 na upresnenie** |  | **30 \+ 1 na upresnenie** |  |

**Nový nábor alebo externé zmluvy:** CCO, ECO (ak ho nemáme interne), zodpovedný zástupca pre výbušniny s osvedčením HBÚ (ak ho nemáme interne), pyrotechnik, 2 až 3 softvéroví vývojári, neskôr vlastný CISO. Externe: advokát, DPO, interný audit, technik požiarnej ochrany, poskytovateľ oznamovacieho kanála. Pri raste na 50 ľudí je oznamovací systém povinný a zamestnanci volia tretinu dozornej rady.

# **6\. Munícia, výbušniny a bezpečnosť výroby a skladov**

**Potvrdené vo verzii 3.0:** muníciu s výbušninou budeme vyrábať aj skladovať sami na Slovensku. **Miesto skladu zatiaľ nie je určené.** Pri výbere miesta treba počítať s tým, že o umiestnení rozhoduje stavebný úrad na základe záväzného stanoviska obvodného banského úradu a stavbu skladu povoľuje obvodný banský úrad (§ 18 a 19 z. 58/2014). Výroba munície sa spustí až po rozhodnutí HBÚ a povolení skladu.

**Ktorý zákon platí.** Zákon č. 58/2014 Z. z. o výbušninách, výbušných predmetoch a munícii upravuje výskum, vývoj, výrobu, skúšanie, skladovanie, evidenciu a ničenie munície (§ 1 ods. 1). Muníciou je kompletné zariadenie vrátane častí zbraňových systémov, ktoré obsahuje výbušninu a využíva ju na dopravu na cieľ a vyvolanie účinku; patria sem aj náboje od kalibru 20 mm (§ 2 písm. c)). Bojová hlavica dronu alebo samostatná munícia pre UAV teda patrí pod tento zákon. Zákon sa nevzťahuje na strelné zbrane a strelivo (§ 1 ods. 2 písm. a)); na tie platí zákon č. 190/2003 Z. z. o strelných zbraniach a strelive.

| Povinnosť | Čo presne | Kto | Zdroj |
| :---- | :---- | :---- | :---- |
| Povolenie HBÚ | Výskum, vývoj, pokusnú výrobu, výrobu, skúšanie, uskladňovanie, delaboráciu a ničenie munície možno vykonávať len na základe rozhodnutia Hlavného banského úradu (§ 41 písm. a) bod 2). Žiadosť obsahuje okrem iného doklad o bezpečnosti objektov, kolaudačné rozhodnutia, doklad o odbornej spôsobilosti zodpovedného zástupcu a spôsob vedenia evidencie (§ 42 ods. 2). | HSE; CEO | § 41, § 42 z. 58/2014 |
| Odborná spôsobilosť | Osvedčenie HBÚ na priame organizovanie a riadenie prác s výbušninami, výbušnými predmetmi a muníciou (§ 31 ods. 5); osvedčenie o odbornej spôsobilosti pre pracovníkov (§ 31 ods. 1); pyrotechnik C, D alebo E pri vývoji a skúšaní (§ 43 ods. 3). | HSE; HR | § 31, § 43 z. 58/2014 |
| Sklad munície | O umiestnení skladu rozhoduje stavebný úrad na základe záväzného stanoviska obvodného banského úradu (§ 18 ods. 1 písm. b)); stavbu skladu povoľuje obvodný banský úrad (§ 19 ods. 1). Skladovať možno len v povolených objektoch (§ 21 ods. 1). Novela č. 243/2026 Z. z. (stavebný zákon) mení od 1\. 1\. 2027 aj tento zákon – postup overí advokát. | HSE; CFO (investícia) | § 18, § 19, § 21 z. 58/2014 |
| Zabezpečenie skladu | Dokumentácia o prevádzkovaní skladu (§ 20 ods. 1); zabezpečenie proti odcudzeniu a oznámenie spôsobu zabezpečenia Policajnému zboru (§ 20 ods. 2); elektrická zabezpečovacia signalizácia vyvedená na stálu strážnu službu alebo pult centrálnej ochrany, ak sklad nie je trvalo strážený (§ 20 ods. 3). | HSE a Bezpečnostný riaditeľ | § 20 z. 58/2014 |
| Vnútorné pravidlá a BOZP | Vnútorný predpis pre jednotlivé stupne riadenia; ochranné prostriedky; zákaz vstupu nepovolaných osôb (§ 3 ods. 4); útvar alebo odborne spôsobilý zamestnanec BOZP a technik požiarnej ochrany (§ 3 ods. 5); technologický postup pre každú výrobnú operáciu schvaľuje oprávnená osoba alebo zodpovedný zástupca. | HSE | § 3 z. 58/2014 |
| Evidencia | Elektronicky alebo v záznamových knihách, oddelene od ostatnej evidencie, pre každý druh zvlášť; uchovávať najmenej 10 rokov (§ 12 ods. 3 a 5). | HSE; Výroba | § 12 z. 58/2014 |
| Strelivo a zbrane (ak budú) | Zbrojná licencia skupiny A na vývoj a výrobu zbraní alebo streliva (§ 29 ods. 2 písm. a)); vydáva policajný útvar; členovia štatutárneho orgánu musia byť bezúhonní a spoľahliví (§ 30 ods. 1 a 2). | HSE; predstavenstvo | § 29, § 30 z. 190/2003 |

**Štruktúra:** vedúci útvaru Bezpečnosť výroby a výbušnín (HSE) je zodpovedným zástupcom podľa zákona č. 58/2014 Z. z., reportuje priamo CEO a môže zastaviť výrobu alebo skúšku pri nebezpečnom stave. Fyzickú ochranu skladu (signalizácia, prístupy, kľúče) zabezpečuje spolu s Bezpečnostným riaditeľom. Výroba munície sa spustí až po rozhodnutí HBÚ a kolaudácii skladu. Pri skúšaní dronov treba dodržať aj zákaz lietania bezpilotných lietadiel v blízkosti označených budov NBÚ (§ 64a z. 215/2004) a pravidlá civilného letectva.

# **7\. Klasifikácia výrobkov – vojenský materiál alebo dvojaké použitie**

Každý výrobok, súčiastku, softvér a technológiu musí ECO zaradiť ešte pred prvou ponukou. Od zaradenia závisí, aké povolenie potrebujeme.

| Výrobok | Kam pravdepodobne patrí | Čo to znamená | Zdroj |
| :---- | :---- | :---- | :---- |
| Munícia, zapaľovače a ich súčasti | VM 3 (munícia pre zbrane z VM 1, VM 2, VM 12\) alebo VM 4 (bomby, rakety, riadené strely, iné výbušné zariadenia a nálože) | vojenský materiál – povolenie MH SR a licencia na každý vývoz | Spoločný zoznam vojenského materiálu EÚ z 23\. 2\. 2026 |
| Vojenské drony a UAV | VM 10 („bezpilotné vzdušné prostriedky“ špeciálne navrhnuté alebo upravené na vojenské použitie); elektronika VM 11 | vojenský materiál | Spoločný zoznam vojenského materiálu EÚ |
| Softvér a technológie pre vojenské položky | VM 21 (softvér) a VM 22 (technológia na vývoj, výrobu, prevádzku a údržbu) | aj samotný softvér a výkresy sú vojenský materiál | Spoločný zoznam vojenského materiálu EÚ |
| Drony, ktoré nie sú vojenské | 9A012 (UAV s určitými vlastnosťami, napr. výdrž a odolnosť voči vetru) alebo 9A112 (UAV s doletom 300 km a ďalšie); technológia 9E001 | položka s dvojakým použitím – povolenie na vývoz mimo EÚ (čl. 3 nariadenia 2021/821) | príloha I nariadenia 2021/821 v znení nariadenia 2025/2003 |
| Šifrovanie v riadení a komunikácii | 5A002 a 5D002 (kategória 5, časť 2 „bezpečnosť informácií“); výnimka pre bežne predávané produkty podľa Poznámky o kryptografii | položka s dvojakým použitím, ak nespĺňa výnimku | príloha I nariadenia 2021/821 |
| Výpočtová technika | kategória 4 (počítače) | spravidla bez povolenia, ale treba overiť | príloha I nariadenia 2021/821 |
| Dlhý dolet | MTCR kategória I: kompletné UAV systémy s doletom aspoň 300 km a užitočným zaťažením aspoň 500 kg (najväčšia zdržanlivosť); kategória II: UAV s doletom aspoň 300 km | vývoz takmer vylúčený alebo veľmi obmedzený | MTCR Guidelines a Annex |

Položka, ktorá je v zozname vojenského materiálu, sa riadi zákonom č. 392/2011 Z. z.; položka s dvojakým použitím nariadením (EÚ) 2021/821 a zákonom č. 39/2011 Z. z. Výrobkom obranného priemyslu sú podľa § 3 písm. c) zákona č. 392/2011 Z. z. aj služby, napríklad poskytovanie informácií alebo vysielanie odborníkov na vývoj, výrobu, údržbu a ovládanie. Aj školenie zahraničného zákazníka alebo servis na diaľku preto môže potrebovať licenciu.

# **8\. Americké súčiastky a softvér – postup pre obe možnosti**

Zatiaľ nevieme, či budeme používať americké súčiastky alebo softvér. Rozhodnutie má veľký vplyv na to, komu a kam budeme môcť predávať, preto ho treba urobiť už pri návrhu výrobku, nie až pri predaji.

## **9.1 Pravidlo pre všetky výrobky: zaradenie už pri návrhu**

> * **Žiadna súčiastka ani softvér sa nedostane do kusovníka (BOM) bez exportného zaradenia.** Pre každú položku sa zapíše: výrobca, krajina pôvodu, zaradenie podľa EÚ (VM alebo dual-use kód, alebo „bez kontroly“), zaradenie podľa USA (kategória USML podľa ITAR, kód ECCN podľa EAR alebo EAR99, alebo „nepodlieha“), cena a zdroj informácie (vyhlásenie dodávateľa, vlastné posúdenie).  
> * **Vyhlásenie dodávateľa** o krajine pôvodu a exportnom zaradení je podmienkou objednávky; zabezpečuje ho Nákup.  
> * **Kontrolný bod v návrhu** (design gate): pred schválením návrhu a pred každou zmenou ECO potvrdí zaradenie celého výrobku, jeho softvéru a technickej dokumentácie.  
> * Pri pochybnosti možno požiadať americký úrad BIS o určenie ECCN (15 CFR 748.3) alebo americké ministerstvo zahraničných vecí (DDTC) o určenie, či položka patrí do USML (22 CFR 120.4). Postup a jeho vhodnosť posúdi externý poradca pre americké exportné právo.

## **9.2 Možnosť A: bez amerických súčiastok podliehajúcich ITAR („ITAR free“) a s minimom položiek podliehajúcich EAR**

> * Výrobok bez akejkoľvek súčiastky, softvéru alebo technických dát z USML. Dôvod: položka z USML zostáva pod ITAR aj po zabudovaní do iného výrobku (22 CFR 120.11(c)) a na ďalší predaj alebo reexport potrebujeme súhlas DDTC (22 CFR 123.9). ITAR nepozná pravidlo de minimis.  
> * ITAR free je dizajnové rozhodnutie, nie úradné povolenie. Musí byť doložené kusovníkom, vyhláseniami dodávateľov a záznamom, že vývojári nepoužili americké technické dáta z USML.  
> * Prednosť majú dodávatelia z EÚ a spojeneckých krajín s doloženým pôvodom. Americké položky zaradené ako EAR99 alebo s nízkou kontrolou možno použiť, ak výpočet de minimis (8.3) vyjde pod limitom.  
> * Výhoda: rýchlejší a voľnejší predaj do celého sveta. Nevýhoda: obmedzený výber súčiastok a vyššie náklady na vývoj.

## **9.3 Možnosť B: s americkými súčiastkami alebo softvérom**

> * Americké položky podliehajú EAR kdekoľvek na svete (15 CFR 734.3(a)(2)).  
> * **Pravidlo de minimis** (15 CFR 734.4): zahraničný výrobok nepodlieha EAR, ak kontrolovaný americký obsah nepresiahne 25 % jeho hodnoty (734.4(d)); pri vývoze do krajín skupín E:1 a E:2 je limit 10 % (734.4(c)).  
> * **Výnimky bez de minimis**: napríklad zahraničná šifrovacia technológia obsahujúca americkú technológiu 5E002 (734.4(a)(2)); položky obsahujúce americké položky „600 series“ alebo 9x515 do krajín skupiny D:5 (734.4(a)(6)). Americký softvér vyvážaný samostatne (nie spolu s výrobkom) de minimis nepoužije (poznámky k 734.4(c)(1)).  
> * Pri šifrovaní platia osobitné podmienky pre americké položky 5A002, 5D002 a ďalšie (734.4(b)).  
> * Ak niektorá súčiastka patrí do USML, celý výrobok sa riadi ITAR a každý reexport potrebuje súhlas DDTC (22 CFR 120.11(c) a 123.9).  
> * Ak americký obsah prekročí de minimis alebo ide o ITAR, každý predaj mimo EÚ potrebuje okrem licencie MH SR aj americké povolenie. Na to treba počítať s časom a nákladmi.

## **9.4 Kto o čom rozhoduje**

| Rozhodnutie | Kto rozhoduje | Kto pripravuje |
| :---- | :---- | :---- |
| Stratégia: ITAR free alebo americké súčiastky | predstavenstvo (na návrh CTO a ECO) | CTO, ECO, Obchod (cieľové krajiny) |
| Zaradenie každej položky a výrobku | ECO (môže zablokovať zaradenie do kusovníka) | CTO a vývojári, Nákup |
| Výpočet de minimis a jeho evidencia | ECO | Financie (hodnoty), Nákup (pôvod) |
| Žiadosť o americké určenie alebo povolenie | ECO so súhlasom predstavenstva | externý poradca pre právo USA |
| Výnimka z pravidla „bez zaradenia nie je objednávka“ | nie je možná | — |

# **9\. Globálny vývoz, sankcie a sprostredkovatelia**

## **8.1 Licencia na každý vývoz**

> * Vývoz a dovoz vojenského materiálu mimo EÚ je možný len s licenciou MH SR, ktorá sa udeľuje na každý prípad zvlášť (§ 15 ods. 1 a 3 z. 392/2011).  
> * K žiadosti o vývoznú licenciu patrí doklad o konečnom užívateľovi potvrdený príslušným orgánom štátu konečného užívateľa, nie starší ako 6 mesiacov (§ 16 ods. 4 písm. b)).  
> * MH SR rozhodne do 60 dní po vyjadrení MZV, MV, MO, SIS a NBÚ; záporné vyjadrenie ministerstva obrany k vývozu je záväzné (§ 17 ods. 1 a 3).  
> * Čerpanie licencie hlásime MH SR štvrťročne do 25\. dňa nasledujúceho mesiaca a na požiadanie predložíme certifikát o overení dodávky z krajiny určenia (§ 18 ods. 1).  
> * Pokuta za obchod bez povolenia alebo licencie alebo v rozpore s nimi je 3 320 až 166 000 eur (§ 39 ods. 1 písm. d) a ods. 3).  
> * Transfery v rámci EÚ idú na transferové licencie (§ 24 až 26\) a pri prijímaní na všeobecnú licenciu potrebujeme certifikát podľa § 30\.

## **8.2 Podľa čoho štát rozhoduje – 8 kritérií EÚ**

Členské štáty posudzujú každú žiadosť podľa ôsmich kritérií Spoločnej pozície Rady 2008/944/SZBP (čl. 2): (1) medzinárodné záväzky a zbrojné embargá OSN, EÚ a OBSE; (2) ľudské práva a medzinárodné humanitárne právo v krajine určenia; (3) vnútorná situácia a ozbrojené konflikty; (4) regionálny mier a stabilita; (5) bezpečnosť členských štátov a spojencov; (6) správanie kupujúcej krajiny, najmä k terorizmu; (7) riziko zmeny konečného užívateľa alebo nežiaduceho reexportu; (8) súlad s technickou a hospodárskou kapacitou krajiny. Licencia sa udeľuje len pri spoľahlivých znalostiach o konečnom použití; spravidla sa vyžaduje preverené osvedčenie o konečnom užívateľovi (čl. 5). Kritériá sa uplatňujú aj na položky s dvojakým použitím, ak je konečným užívateľom armáda alebo bezpečnostné zložky (čl. 6). Licenciu vyžaduje aj nehmotný prenos softvéru a technológií (čl. 1 ods. 2).

Zmluva o obchode so zbraňami (ATT) zaväzuje štáty zakázať prevod pri porušení embarga BR OSN (čl. 6), posúdiť riziká vývozu (čl. 7), regulovať sprostredkovanie (čl. 10\) a predchádzať odkloneniu zbraní (čl. 11); vzťahuje sa aj na muníciu (čl. 3). Pre nás to znamená, že bez úplných údajov o konečnom užívateľovi a trase licenciu nedostaneme.

## **8.3 Sankcie a embargá**

> * Pred každou ponukou, zmluvou, dodávkou a platbou preveríme zákazníka, jeho vlastníkov, konečného užívateľa, dopravcu, banku a agenta voči zoznamom EÚ, OSN a USA (OFAC) a voči zbrojným embargám.  
> * Podľa pravidla 50 % OFAC je blokovaný aj subjekt, ktorý blokované osoby vlastnia spolu aspoň z 50 %, aj nepriamo (OFAC FAQ 398 až 401).  
> * Americké sankcie zaväzujú najmä osoby USA, ale zákon IEEPA zakazuje aj „spôsobiť porušenie“ (50 U.S.C. § 1705(a)). Pre nás je riziko najmä pri platbách v USD, pri amerických bankách, komponentoch a zamestnancoch.  
> * Pri predaji citlivých položiek do tretích krajín je v zmluve povinná doložka zákazu reexportu do Ruska (čl. 12g nariadenia 833/2014). Podozrenie na sankcionovanú stranu treba hlásiť (§ 15 z. 289/2016).

## **8.4 Sprostredkovanie, reexport a konečný užívateľ**

> * Sprostredkovanie obchodu s vojenským materiálom potrebuje povolenie MH SR (§ 2 ods. 1 písm. b) a § 5 ods. 1 z. 392/2011). Spoločná pozícia 2003/468/SZBP počíta s licenciou alebo písomným povolením na každú transakciu sprostredkovania (čl. 3 ods. 1\) a s registrom sprostredkovateľov (čl. 4); agentov preto evidujeme a každú transakciu nechávame posúdiť ECO.  
> * Pri dual-use položkách môže štát vyžadovať povolenie na sprostredkovanie aj technickú pomoc (čl. 6 a 8 nariadenia 2021/821).  
> * Každá zmluva obsahuje vyhlásenie o konečnom užívateľovi a konečnom použití a zákaz reexportu bez súhlasu SR.  
> * Ak výrobok obsahuje americký obsah: ITAR vyžaduje súhlas DDTC na reexport alebo ďalší prevod (22 CFR 123.9); EAR sa vzťahuje na americké položky kdekoľvek a na zahraničné výrobky s americkým obsahom nad limit de minimis (15 CFR 734.3 a 734.4).

## **9.5 Agenti, distribútori a offsety**

Agenti, distribútori a offsety sú najväčšie korupčné riziko v medzinárodnom obchode so zbraňami. Celý program pre nich je v kapitole 10\. Offsety len na základe písomnej zmluvy so štátom alebo jeho určenou organizáciou, po preverení všetkých príjemcov; schvaľuje predstavenstvo na návrh CCO.

# **10\. Program pre tretie strany – agenti, distribútori a ďalší partneri**

Pri predaji po celom svete je preverovanie partnerov najdôležitejšou ochranou firmy. Firma zodpovedá za korupciu aj vtedy, keď ju urobí sprostredkovateľ v jej prospech (§ 332 a § 336 TZ; § 4 z. 91/2016) a podľa UK Bribery Act aj za „spojenú osobu“, napríklad agenta (s. 7). Odporúčanie OECD z roku 2021 v prílohe II odporúča firmám pre obchodných partnerov zdokumentované preverenie podľa rizika a priebežný dohľad, oboznámenie partnera s pravidlami a jeho vzájomný záväzok, zmluvu s presným opisom služby a primeranou odmenou, právo auditu a právo zmluvu ukončiť (príloha II, bod A.6).

## **10.1 Na koho sa program vzťahuje**

Agenti a sprostredkovatelia, distribútori a predajcovia, konzultanti a lobisti, partneri v offsetoch, konzorciách a spoločných podnikoch, dopravcovia a špeditéri pri vojenskom materiáli a dodávatelia, ktorí za nás jednajú so štátom. Sprostredkovanie obchodu s výrobkami obranného priemyslu je navyše viazané na povolenie MH SR (§ 2 ods. 1 písm. b) a § 5 ods. 1 z. 392/2011).

## **10.2 Stupne rizika**

Stupeň rizika určí CCO podľa štyroch faktorov: **krajina**, **úloha partnera** (kontakt s verejnými činiteľmi, provízia za úspech), **výrobok** (vojenský materiál alebo dual-use) a **hodnota obchodu**. Pre krajinu používame Index vnímania korupcie (CPI) Transparency International; CPI 2025 hodnotí 182 krajín na stupnici 0 (veľmi skorumpované) až 100 (veľmi čisté). Hranice stupňov sú naše interné rozhodnutie a predstavenstvo ich môže upraviť:

| Stupeň | Kedy | Preverenie | Schvaľuje |
| :---- | :---- | :---- | :---- |
| Zakázané | Krajina alebo strana pod zbrojným embargom alebo sankciami EÚ, OSN alebo USA; sankcionovaný vlastník (aj podľa pravidla 50 % OFAC) | žiadna spolupráca | — |
| Vysoké | CPI pod 40, alebo kontakt so štátnymi úradníkmi, alebo provízia za úspech, alebo konfliktná oblasť, alebo hodnota nad \[DOPLNIŤ €\] | hĺbkové: všetko zo stredného \+ nezávislá externá správa o partnerovi, osobné stretnutie alebo návšteva sídla | CCO a predstavenstvo; obchod len navrhuje |
| Stredné | CPI 40 až 59 | rozšírené: všetko zo základného \+ overenie konečných užívateľov výhod, väzieb na politicky exponované osoby, mediálna kontrola, referencie, finančné výkazy, pohovor | CCO |
| Nízke | CPI 60 a viac a žiadny z vysokých faktorov | základné: dotazník, výpis z registra, vlastníci, sankčný screening, podpis kódexu | CCO alebo analytik DD |

## **10.3 Postup od prvého kontaktu po platbu**

> 1. Obchod zapíše partnera do registra tretích strán so stavom „v preverovaní“; dovtedy nesmie podpísať nič okrem dohody o mlčanlivosti.  
> 2. Partner vyplní dotazník (vlastníci, konečný užívateľ výhod, väzby na verejných činiteľov, referencie, bankový účet, odôvodnenie potreby partnera).  
> 3. Sankčný screening robí ECO; preverenie podľa stupňa rizika robí analytik DD.  
> 4. CCO (pri vysokom riziku aj predstavenstvo) schváli alebo zamietne; dôvody sa zapíšu.  
> 5. Podpis zmluvy so všetkými povinnými doložkami (10.4) a protikorupčné školenie partnera.  
> 6. Platba len proti faktúre s opisom služby a dôkazom vykonanej práce, na účet partnera v krajine jeho sídla, nikdy v hotovosti; schvaľuje CFO po kontrole CCO.

## **10.4 Povinné zmluvné doložky**

| Doložka | Obsah |
| :---- | :---- |
| Protikorupčná | Zákaz úplatkov a urýchľovacích platieb; dodržiavanie TZ, FCPA, UK Bribery Act a miestneho práva; ročné potvrdenie dodržiavania. |
| Sankcie a exportná kontrola | Partner nie je sankcionovaný; dodrží licencie, konečné použitie a konečného užívateľa; zákaz reexportu bez súhlasu SR. |
| No Russia | Zákaz predaja do Ruska alebo na použitie v Rusku pri citlivých položkách podľa čl. 12g nariadenia 833/2014 a zmluvná pokuta za porušenie. |
| Audit a záznamy | Právo IOTA nahliadnuť do kníh a záznamov partnera týkajúcich sa našej zmluvy (odporúčanie OECD, príloha II, A.6 v)). |
| Opis služby a odmena | Presný opis činností, odmena primeraná službe (príloha II, A.6 iv)), strop odmeny, platba len na účet partnera. |
| Ďalší sprostredkovatelia | Zákaz poveriť ďalšiu osobu bez písomného súhlasu IOTA. |
| Ukončenie | Okamžité ukončenie bez náhrady pri porušení protikorupčnej, sankčnej alebo exportnej doložky (príloha II, A.6 vi)). |
| Spolupráca a oznamovanie | Povinnosť spolupracovať pri vnútornom vyšetrovaní a oznámiť podozrenie; prístup k nášmu oznamovaciemu kanálu. |

## **10.5 Strop odmeny, monitorovanie a registre**

> * **Strop odmeny**: \[DOPLNIŤ %\] z hodnoty obchodu pre agentov a \[DOPLNIŤ %\] zľava pre distribútorov; prekročenie len so súhlasom predstavenstva na návrh CCO. Výšku stropu odporúčame určiť po porovnaní s trhom.  
> * **Monitorovanie**: automatický sankčný screening všetkých partnerov pri každej zmene zoznamov; opätovné preverenie raz ročne pri vysokom riziku, každé 2 roky pri strednom a každé 3 roky pri nízkom; ročná kontrola platieb agentom interným auditom.  
> * **Varovné signály**: platba tretej osobe alebo do inej krajiny, neobvykle vysoká provízia, partner odporúčaný úradníkom, žiadosť o hotovosť, tajnosť alebo zmenu konečného užívateľa. Obchod sa zastaví, kým CCO nerozhodne.  
> * **Registre**: register tretích strán (stav, stupeň rizika, dátum preverenia, schválenie), register platieb agentom a distribútorom, register varovných signálov a výnimiek, register darov a pohostení.  
> * **Výbor pre tretie strany**: CCO (predseda), ECO a CFO; zasadá mesačne a pri vysokom riziku. Riaditeľ stratégie a obchodu partnera navrhuje, ale nehlasuje. Štvrťročný prehľad dostáva predstavenstvo a dozorná rada.

# **11\. Softvér, technológie a prenos dát**

> * **Prenos je vývoz.** Vývozom je aj prenos softvéru alebo technológie elektronickými médiami, faxom, telefónom alebo e-mailom do miesta mimo EÚ a sprístupnenie v elektronickej forme osobám mimo EÚ, aj hlasom (čl. 2 bod 2 písm. d) nariadenia 2021/821). Pri vojenskom materiáli to isté vyžaduje čl. 1 ods. 2 Spoločnej pozície 2008/944/SZBP a § 3 písm. c) z. 392/2011.  
> * **Cloud, e-mail a repozitáre.** Technické dáta zóny „Controlled“ (podľa [IT štruktúry](https://docs.google.com/document/d/1H83T1Oa3hwzx7FhapHuClGH_09tSdpYuPbE1hJeW9o8/edit)) ukladáme len v EÚ, s prístupom podľa rolí a záznamom prístupov. Žiadne zdieľanie odkazov s osobami mimo firmy bez súhlasu ECO. Vzdialený prístup zo zahraničia len po schválení ECO.  
> * **Americké pravidlá pre cloud.** EAR a ITAR nepovažujú za vývoz uloženie nezaradených (neutajovaných) dát, ak sú šifrované end-to-end (FIPS 140-2 alebo rovnocenne) a zámerne neuložené v zakázaných krajinách (15 CFR 734.18(a)(5); 22 CFR 120.54(a)(5)). Inak sa za odovzdanie považuje aj sprístupnenie prístupových údajov (22 CFR 120.56).  
> * **Zahraniční zamestnanci („deemed export“).** Podľa práva USA je odovzdanie americkej technológie alebo zdrojového kódu cudzincovi mimo USA tzv. deemed reexport do krajiny jeho občianstva alebo trvalého pobytu (15 CFR 734.14(b)); pri ITAR do všetkých krajín jeho občianstva (22 CFR 120.51(b)). Nariadenie EÚ tento pojem v rovnakej šírke nepozná, ale technická pomoc a sprístupnenie osobám mimo EÚ podliehajú kontrole (čl. 2 bod 2 písm. d) a čl. 8). Preto HR a ECO pred nástupom overia občianstvo a ECO určí, k čomu má človek prístup (podrobne kapitola 12).  
> * **Utajované skutočnosti** sa nikdy nespracúvajú v bežnom cloude ani e-maile; len v certifikovanom a schválenom systéme (kapitola 13).  
> * **Plán kontroly technológií** (Technology Control Plan): zoznam kontrolovaných dát, kto k nim má prístup, ako sa prenášajú a ako sa zaznamenávajú. Vlastník je ECO, vykonáva CTO a IT prevádzka, dohliada CISO.

# **12\. Zahraniční zamestnanci vo vývoji**

Ľudia z krajín mimo EÚ môžu vo vývoji pracovať, ale len s jasnými pravidlami, kto smie vidieť čo. Platia tri samostatné okruhy pravidiel: slovenské pravidlá pobytu a zamestnania, exportná kontrola technológií a ochrana utajovaných skutočností.

| Oblasť | Čo to znamená | Kto | Zdroj |
| :---- | :---- | :---- | :---- |
| Pobyt a zamestnanie | Zamestnávateľ môže zamestnať štátneho príslušníka tretej krajiny len s príslušným oprávnením, napríklad s modrou kartou alebo s prechodným pobytom na účel zamestnania (§ 21 ods. 1 z. 5/2004). Prechodný pobyt na účel zamestnania udeľuje policajný útvar na základe potvrdenia o možnosti obsadenia voľného pracovného miesta alebo povolenia na zamestnanie, najviac na 5 rokov (§ 23 z. 404/2011). Modrá karta je pre vysokokvalifikované zamestnanie (§ 37 z. 404/2011). | HR | Slov-Lex 5/2004, 404/2011 |
| Kontrola podľa krajiny | Pred nástupom HR a ECO overia všetky štátne občianstva a trvalé pobyty uchádzača a sankčný status. ECO určí, k akým technológiám môže mať prístup; zo sankcionovaných alebo embargových krajín bez prístupu ku kontrolovaným technológiám. | HR; ECO | kapitola 10.2; EU Sanctions Map |
| Americké technológie | Sprístupnenie americkej technológie alebo zdrojového kódu cudzincovi mimo USA je deemed reexport do krajiny jeho posledného občianstva alebo trvalého pobytu (15 CFR 734.14(b)); pri ITAR do všetkých jeho občianstiev (22 CFR 120.51(b)). EAR nepovažuje za deemed reexport napríklad sprístupnenie, ak by vývoz z USA do krajiny občianstva alebo trvalého pobytu zamestnanca bol povolený bez licencie (15 CFR 734.20(a)), sprístupnenie stálemu zamestnancovi z krajiny skupiny A:5 (734.20(b)) alebo stálemu zamestnancovi z inej krajiny pri splnení ďalších podmienok vrátane preverenia, dohody o mlčanlivosti a postupov proti odkloneniu (734.20(c)). ITAR umožňuje prenos neutajovaných obranných položiek zamestnancom s dvojitým alebo cudzím občianstvom v rámci schválenej licencie, ak firma preveruje zamestnancov a vedie plán bezpečnosti technológií so záznamami 5 rokov (22 CFR 126.18). | ECO; HR; CTO | eCFR 734.14, 734.20, 120.51, 126.18 |
| Licencia na prenos technológie | Vojenská technológia a služby (poskytovanie informácií, vysielanie odborníkov) sú výrobkom obranného priemyslu (§ 3 písm. c) z. 392/2011). Prenos technológie mimo EÚ, aj e-mailom, cloudom, na služobnej ceste alebo pri práci zo zahraničia, je vývoz (čl. 2 bod 2 písm. d) nariadenia 2021/821; čl. 1 ods. 2 Spoločnej pozície 2008/944/SZBP). Pri amerických obranných službách treba dohodu schválenú DDTC (technical assistance agreement, 22 CFR 124.1). | ECO | Slov-Lex 392/2011; EUR-Lex; eCFR 124.1 |
| Previerky NBÚ | Osvedčenie NBÚ predpokladá štátne občianstvo SR (§ 10 ods. 1 písm. a) z. 215/2004); výnimky upravuje § 36\. Cudzinec z krajiny, ktorá má so SR zmluvu o ochrane vymieňaných utajovaných skutočností, sa môže oboznamovať so stupňom Dôverné až Prísne tajné len s písomným súhlasom vedúceho príslušného štátneho orgánu a s osvedčením NBÚ, ktoré NBÚ vydá až po vyjadrení úradu jeho krajiny (§ 36 ods. 1 až 3). Výnimku môže udeliť len vláda SR (§ 36 ods. 5). V praxi preto cudzinci na utajovaných projektoch pracovať nebudú. | Bezpečnostný riaditeľ | § 10, § 36 z. 215/2004 |
| Oddelené prístupy v IT | Prístupy podľa roly, štátnej príslušnosti a previerky: zóna „Internal“ pre všetkých, zóna „Project“ podľa projektu, zóna „Controlled“ len so súhlasom ECO, utajované skutočnosti len v certifikovanom systéme. Oddelené repozitáre a projekty pre kontrolované technológie, záznam prístupov, pravidelná kontrola oprávnení. | CISO; IT prevádzka; ECO | IT štruktúra a identity; kapitola 11 |
| Plán kontroly technológií (TCP) | Zoznam kontrolovaných technológií a ich zaradenie, matica „kto smie čo“ podľa krajiny a previerky, postup preverenia zamestnancov, dohody o mlčanlivosti, pravidlá ciest a práce zo zahraničia, záznamy o preverení (najmenej 5 rokov pri ITAR, 22 CFR 126.18(c)), školenia a kontrola. | ECO (vlastník); CTO, HR, CISO | 22 CFR 126.18; 15 CFR 734.20 |

**Štruktúra vývoja:** Vývoj sa delí na **otvorený tím** (môžu v ňom byť ľudia z krajín mimo EÚ; pracuje na nekontrolovaných alebo schválených častiach) a **kontrolovaný tím** (vojenský materiál, kontrolované technológie a utajované projekty; len ľudia schválení ECO a pri utajovaných projektoch len občania SR s previerkou NBÚ).

# **13\. Utajované skutočnosti (predpoklad Dôverné až Tajné, NATO a EÚ)**

| Oblasť | Čo treba | Kto | Zdroj |
| :---- | :---- | :---- | :---- |
| Stupne | Prísne tajné, Tajné, Dôverné, Vyhradené. Plánujeme Dôverné až Tajné. | Bezpečnostný riaditeľ | § 3 z. 215/2004 |
| Priemyselná bezpečnosť | Bezpečnostná previerka podnikateľa na žiadosť štatutárneho orgánu s bezpečnostným projektom a previerkou štatutára (§ 45); potvrdenie o priemyselnej bezpečnosti platí najviac 5 rokov (§ 50 ods. 3); NBÚ rozhodne do 4 mesiacov pri stupni Dôverné a do 7 mesiacov pri stupni Tajné (§ 51). | predstavenstvo; Bezpečnostný riaditeľ | § 45 až 51 z. 215/2004 |
| Ľudia | Osvedčenie NBÚ pre každého, kto sa oboznamuje s utajovanými skutočnosťami; predpokladom je okrem iného štátne občianstvo SR (§ 10 ods. 1). Bezpečnostný zamestnanec potrebuje osvedčenie a skúšku (§ 9 ods. 1). | HR; Bezpečnostný riaditeľ | § 9, § 10 z. 215/2004 |
| Zabezpečené priestory | Ochrana objektov a chránených priestorov mechanickými a technickými prostriedkami, fyzickou ochranou a režimovými opatreniami podľa bezpečnostného štandardu; chránené priestory na rokovania o utajovaných skutočnostiach; bezpečnostná dokumentáciu schvaľuje vedúci (§ 53). | Bezpečnostný riaditeľ | § 53 z. 215/2004 |
| IT pre utajované skutočnosti | Len certifikované technické prostriedky schválené do prevádzky (§ 55 ods. 3 a 4); certifikácia po posúdení bezpečnostného projektu technického prostriedku (§ 56 ods. 2, § 58); platnosť pre Tajné najviac 5 rokov, pre Dôverné najviac 7 rokov (§ 55 ods. 5, § 56 ods. 5). Systém je fyzicky oddelený od bežného IT. | CISO; Bezpečnostný riaditeľ | § 55 až 58 z. 215/2004 |
| NATO a EÚ utajované | Utajované skutočnosti cudzej moci chránime podľa zákona, ak to ustanovuje medzinárodná zmluva (§ 60 ods. 1); o poskytnutí utajovaných skutočností medzi slovenskou firmou a zahraničnou osobou rozhoduje NBÚ (§ 60 ods. 4). Pri zmluvách s inštitúciami EÚ platia minimálne normy priemyselnej bezpečnosti (čl. 11 rozhodnutia Rady 2013/488/EÚ). | Bezpečnostný riaditeľ | § 60 z. 215/2004; rozhodnutie 2013/488/EÚ |
| Cudzinci | Cudzinec z krajiny so zmluvou so SR o ochrane vymieňaných utajovaných skutočností len so súhlasom vedúceho štátneho orgánu a osvedčením NBÚ po vyjadrení úradu jeho krajiny; výnimku môže udeliť len vláda (§ 36 ods. 1 až 5); stupeň Vyhradené so súhlasom štátneho orgánu (§ 37). Pozri kapitolu 12\. | Bezpečnostný riaditeľ; HR | § 36, § 37 z. 215/2004 |
| Projekty EDF a EDIP | Pri utajovaných projektoch previerky ľudí a zariadení. | Bezpečnostný riaditeľ; PMO | čl. 9 nariadení 2021/697 a 2025/2643 |

# **14\. Prehľad regulácií a čo z nich vyplýva pre štruktúru**

| Predpis | Čo od nás chce | Kto to zabezpečí | Vplyv na štruktúru | Zdroj |
| :---- | :---- | :---- | :---- | :---- |
| **Zákon č. 392/2011 Z. z.** | Výrobca potrebuje živnosť na výrobu výrobkov obranného priemyslu (§ 4); obchod a sprostredkovanie len s povolením MH SR (§ 5\) na najviac 5 rokov (§ 9 ods. 2 písm. g)); zodpovedný zástupca (§ 8); licencia na každý vývoz (§ 15 až 18); certifikát príjemcu transferov (§ 30). | ECO; predstavenstvo | Útvar Exportná kontrola a sankcie s vlastným ECO. | [Slov-Lex](https://static.slov-lex.sk/static/SK/ZZ/2011/392/20240201.html) |
| **Spoločná pozícia 2008/944/SZBP** a **Spoločný zoznam vojenského materiálu EÚ** (23. 2\. 2026\) | 8 kritérií pre vývozné licencie, doklad o konečnom užívateľovi, kontrola nehmotných prenosov; zoznam VM 1 až VM 22\. | ECO | Klasifikácia každého výrobku; dokumentácia konečného užívateľa. | [EUR-Lex 2008/944 (konsolidované)](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:02008E0944-20190917); [Ú. v. EÚ C/2026/1640](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=OJ:C_202601640) |
| **Spoločná pozícia 2003/468/SZBP** (sprostredkovanie) | Licencia alebo písomné povolenie na každú transakciu sprostredkovania (čl. 3); možný register sprostredkovateľov (čl. 4). | ECO; CCO | Register agentov a sprostredkovateľov. | [EUR-Lex 32003E0468](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32003E0468) |
| **Nariadenie (EÚ) 2021/821** (dual-use), príloha I v znení **nariadenia 2025/2003**; **zákon č. 39/2011 Z. z.** | Povolenie na vývoz (čl. 3), catch-all (čl. 4), sprostredkovanie (čl. 6), technická pomoc (čl. 8), ICP pri globálnom povolení (čl. 12 ods. 4), záznamy 5 rokov (čl. 27); vývoz zahŕňa elektronický prenos (čl. 2 bod 2 písm. d)). | ECO; CTO; IT | Plán kontroly technológií; ICP. | [EUR-Lex 32021R0821](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0821); [EUR-Lex 32025R2003](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32025R2003); [Slov-Lex 39/2011](https://static.slov-lex.sk/static/SK/ZZ/2011/39/20240201.html) |
| **MTCR** | Najväčšia zdržanlivosť pri UAV systémoch s doletom aspoň 300 km a užitočným zaťažením aspoň 500 kg (kategória I); UAV s doletom aspoň 300 km sú v kategórii II. Režim zaväzuje štáty; v EÚ sa uplatňuje cez prílohu I nariadenia 2021/821 (napr. 9A112). | ECO; CTO | Kontrola doletu a nosnosti pri návrhu nových dronov. | [MTCR Guidelines](https://www.mtcr.info/en/mtcr-guidelines) |
| **ATT** a **Wassenaarské dojednanie** | Zaväzujú štáty: zákaz pri embargu (čl. 6), posúdenie vývozu (čl. 7), sprostredkovanie (čl. 10), odklonenie (čl. 11); vrátane munície (čl. 3). | ECO | Úplné údaje o konečnom užívateľovi a trase. | [ATT – text OSN](https://treaties.un.org/doc/Treaties/2013/04/20130410%2012-01%20PM/Ch_XXVI_08.pdf); [Wassenaar](https://www.wassenaar.org/about-us/) |
| **Zákon č. 58/2014 Z. z.** o výbušninách, výbušných predmetoch a munícii | Povolenie HBÚ (§ 41, § 42), osvedčenia (§ 31), sklady a OBÚ (§ 18 až 21), BOZP a vnútorný predpis (§ 3), evidencia 10 rokov (§ 12), pyrotechnik (§ 43). | HSE; Bezpečnostný riaditeľ | Útvar HSE so zodpovedným zástupcom, reportuje CEO. | [Slov-Lex 58/2014](https://static.slov-lex.sk/static/SK/ZZ/2014/58/20240102.html) |
| **Zákon č. 190/2003 Z. z.** o strelných zbraniach a strelive | Len ak budeme vyvíjať alebo vyrábať strelné zbrane alebo strelivo: zbrojná licencia skupiny A (§ 29, § 30). | HSE; predstavenstvo | Zodpovedná osoba držiteľa licencie. | [Slov-Lex 190/2003](https://static.slov-lex.sk/static/SK/ZZ/2003/190/20250701.html) |
| **Zákon č. 215/2004 Z. z.** a **rozhodnutie Rady 2013/488/EÚ** | Previerka podnikateľa (§ 45 až 51), bezpečnostný zamestnanec (§ 9), chránené priestory (§ 53), certifikované IT (§ 55 až 58), NATO a EÚ utajované (§ 60; čl. 11 rozhodnutia 2013/488/EÚ). | Bezpečnostný riaditeľ; CISO | Vlastný Bezpečnostný riaditeľ a osobitné pracovisko. | [Slov-Lex 215/2004](https://static.slov-lex.sk/static/SK/ZZ/2004/215/20250501.html); [EUR-Lex 32013D0488](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32013D0488) |
| **Sankcie EÚ, OSN a USA** | Screening všetkých strán; zbrojné embargá; doložka „no Russia“ (čl. 12g nariadenia 833/2014); hlásenie (§ 15 z. 289/2016); OFAC pravidlo 50 %; IEEPA zakazuje spôsobiť porušenie (50 U.S.C. § 1705(a)). | ECO (screening); CCO | Sankčný screening v útvare Exportná kontrola a sankcie. | [EU Sanctions Map](https://www.sanctionsmap.eu/); [OSN – zoznam](https://main.un.org/securitycouncil/en/content/un-sc-consolidated-list); [OFAC FAQ](https://ofac.treasury.gov/faqs/topic/1521); [50 U.S.C. § 1705](https://www.govinfo.gov/content/pkg/USCODE-2023-title50/html/USCODE-2023-title50-chap35-sec1705.htm); [FAQ k čl. 12g](https://finance.ec.europa.eu/publications/no-re-export-russia-clause_en); [Slov-Lex 289/2016](https://static.slov-lex.sk/static/SK/ZZ/2016/289/20260601.html) |
| **ITAR** a **EAR** (USA) | Americké položky a technológie kdekoľvek (EAR 734.3, 734.4); reexport ITAR len so súhlasom DDTC (123.9); deemed export a reexport pri cudzincoch (EAR 734.13(b), 734.14(b); ITAR 120.50(b), 120.51(b)); šifrovaný cloud (EAR 734.18(a)(5); ITAR 120.54(a)(5)). | ECO; Nákup; HR; CTO | Evidencia pôvodu komponentov; kontrola občianstva pri prístupe k dátam. | [734.3](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.3); [734.4](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.4); [734.13](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.13); [734.14](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.14); [734.18](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.18); [123.9](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-123/section-123.9); [120.50](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.50); [120.51](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.51); [120.54](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.54); [120.56](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.56) |
| **EAR 734.4, 734.20, 748.3**; **ITAR 120.4, 120.11(c), 124.1, 126.18** (USA) | De minimis 25 % alebo 10 % a výnimky; ITAR zostáva aj po zabudovaní; určenie ECCN alebo USML; dohody o obranných službách; prenos zamestnancom s cudzím občianstvom len s preverením a plánom bezpečnosti technológií (záznamy 5 rokov). | ECO; CTO; Nákup; HR | Klasifikácia už pri návrhu, kusovník s exportným zaradením, rozhodnutie predstavenstva o ITAR free, plán kontroly technológií. | [eCFR 734.4](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.4); [734.20](https://www.ecfr.gov/current/title-15/section-734.20); [748.3](https://www.ecfr.gov/current/title-15/section-748.3); [120.4](https://www.ecfr.gov/current/title-22/section-120.4); [120.11](https://www.ecfr.gov/current/title-22/section-120.11); [124.1](https://www.ecfr.gov/current/title-22/section-124.1); [126.18](https://www.ecfr.gov/current/title-22/section-126.18) |
| **Zákon č. 404/2011 Z. z.** o pobyte cudzincov a **zákon č. 5/2004 Z. z.** o službách zamestnanosti | Zamestnať štátneho príslušníka tretej krajiny len s modrou kartou alebo povolením (§ 21 z. 5/2004); potvrdenie o možnosti obsadenia voľného miesta (§ 21a) alebo povolenie na zamestnanie (§ 22); prechodný pobyt na účel zamestnania najviac 5 rokov (§ 23 z. 404/2011); modrá karta (§ 37). | HR | Postup prijímania cudzincov; spolupráca HR a ECO pred nástupom. | [Slov-Lex 404/2011](https://static.slov-lex.sk/static/SK/ZZ/2011/404/20261001.html); [Slov-Lex 5/2004](https://static.slov-lex.sk/static/SK/ZZ/2004/5/20260801.html) |
| **Zákon č. 315/2016 Z. z.** o registri partnerov verejného sektora | Kto prijíma plnenia od štátu alebo z verejných zdrojov, je partnerom verejného sektora a musí byť zapísaný v registri; neplatí pri jednorazovom plnení do 100 000 € a pri opakujúcich sa plneniach úhrnne do 250 000 € (§ 2 ods. 1 až 3). | CFO; externý advokát | Pred prvou veľkou štátnou zákazkou alebo grantom overiť povinnosť zápisu. | [Slov-Lex 315/2016](https://static.slov-lex.sk/static/SK/ZZ/2016/315/20191101.html) |
| **Odporúčanie OECD 2021** proti podplácaniu (OECD/LEGAL/0378), príloha II | Pre obchodných partnerov: preverenie podľa rizika, dohľad, vzájomný záväzok, primeraná odmena, právo auditu, právo ukončiť zmluvu (bod A.6). Nezáväzné pre firmy, ale je to medzinárodný štandard. | CCO | Program pre tretie strany (kapitola 10). | [OECD/LEGAL/0378](https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0378) |
| **Zákon č. 497/2022 Z. z.**, **NV č. 61/2023 Z. z.**, **nariadenie 2019/452** | IOTA je kritická investícia (§ 1 písm. b) a c) NV 61/2023). Súčasní akcionári sú zo SR a EÚ, preto sa ich to netýka. Každý budúci investor mimo EÚ alebo ním ovládaný potrebuje povolenie vopred (§ 11 ods. 1), už pri 10 % (§ 2 ods. 4). | predstavenstvo; Legal | Kontrola každej zmeny akcionárov. | [Slov-Lex 497/2022](https://static.slov-lex.sk/static/SK/ZZ/2022/497/20250101.html); [Slov-Lex 61/2023](https://static.slov-lex.sk/static/SK/ZZ/2023/61/20230301.html); [EUR-Lex 32019R0452](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32019R0452) |
| **EDF** (2021/697) a **EDIP** (2025/2643), čl. 9 | Usadenie a riadenie v EÚ, žiadna kontrola z nepridruženej tretej krajiny. | predstavenstvo; PMO | S akcionármi zo SR a EÚ pravdepodobne splnené. | [EUR-Lex 32021R0697](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0697); [EUR-Lex 32025R2643](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32025R2643) |
| **Smernica 2009/81/ES** | Obstarávatelia žiadajú bezpečnosť informácií (čl. 22), bezpečnosť dodávok (čl. 23), technickú spôsobilosť (čl. 42). | Obchod; Bezpečnosť; Kvalita | Tendrový tím spolupracuje s 2\. líniou. | [EUR-Lex 32009L0081](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32009L0081) |
| **NIS2** a **zákon č. 69/2018 Z. z.** | Výroba elektroniky (C26) a dopravných prostriedkov (C30) je v prílohe II; platí od stredného podniku. Pri 31 ľuďoch pravdepodobne nie, overí Legal. | CISO | ISMS aj bez povinnosti. | [EUR-Lex 32022L2555](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32022L2555); [Slov-Lex 69/2018](https://static.slov-lex.sk/static/SK/ZZ/2018/69/20260430.html) |
| **AQAP 2110**, **ISO 9001**, **AS/EN 9100**, **ISO/IEC 27001** | Kvalita s priamym reportom vedeniu; riadenie konfigurácie; ISMS. | Kvalita; CISO | Kvalita mimo výroby. | [EDA EDSTAR](https://edstar.eda.europa.eu/Standards/Details/aad7da24-5ab4-419c-a2c6-e7b3835f8fa1); [IAQG](https://iaqg.org/standard/9100-qms-requirements-for-aviation-space-and-defense-organizations/); [ISO 27001](https://www.iso.org/standard/27001) |
| **Trestný zákon**, **zákon č. 91/2016 Z. z.**, **FCPA**, **UK Bribery Act**, **Dohovor OECD**, **ISO 37001:2025**, **ISO 37301** | Korupcia priamo aj cez sprostredkovateľa; zodpovednosť firmy; obrana účinnými kontrolami (§ 4 ods. 7); FCPA pri konaní na území USA; UKBA s. 7 a s. 12 ods. 5\. | CCO | Nezávislý CCO; pravidlá pre agentov a offsety. | [TZ](https://static.slov-lex.sk/static/SK/ZZ/2005/300/20260818.html); [91/2016](https://static.slov-lex.sk/static/SK/ZZ/2016/91/20260817.html); [FCPA](https://www.govinfo.gov/content/pkg/USCODE-2023-title15/html/USCODE-2023-title15-chap2B-sec78dd-3.htm); [UKBA s. 7](https://www.legislation.gov.uk/ukpga/2010/23/section/7); [OECD](https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0293); [ISO 37001](https://www.iso.org/standard/65034.html); [ISO 37301](https://www.iso.org/standard/75080.html) |
| **Smernica 2019/1937** a **zákon č. 54/2019 Z. z.** | Pozri kapitolu 15.4. | CCO | Nezávislá zodpovedná osoba. | [EUR-Lex 32019L1937](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32019L1937); [Slov-Lex 54/2019](https://static.slov-lex.sk/static/SK/ZZ/2019/54/20260324.html) |
| **GDPR**, **zákon č. 297/2008 Z. z.**, **Obchodný zákonník** | Ochrana osobných údajov (čl. 37 – DPO podľa posúdenia); AML len pri hotovosti od 10 000 € (§ 5 ods. 3); dozorná rada (§ 197, § 200). | DPO; CFO; predstavenstvo | DR dostáva reporty 2\. a 3\. línie. | [GDPR](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32016R0679); [297/2008](https://static.slov-lex.sk/static/SK/ZZ/2008/297/20260817.html); [ObZ](https://static.slov-lex.sk/static/SK/ZZ/1991/513/20260817.html) |

# **15\. Compliance, protikorupcia a whistleblowing**

## **15.1 Compliance systém**

Compliance vedie **CCO**. Reportuje celému predstavenstvu (štvrťročne, ročne a okamžite pri závažnom zistení) a má priamy prístup k predsedovi dozornej rady, najmä ak sa podozrenie týka člena predstavenstva. CCO má prístup ku všetkým informáciám a môže zastaviť rizikovú transakciu do rozhodnutia predstavenstva (Rámec v1.1, kap. 1.4; U-02). Systém stavia na prvkoch ISO 37301:2021: posúdenie rizík, politiky, zodpovednosti, školenia, kontroly, oznamovanie, vyšetrovanie a preskúmanie vedením. Exportná kontrola je samostatný útvar, ale CCO a ECO spolu rozhodujú o každom novom agentovi, distribútorovi a krajine.

| Prvok | Čo to znamená v IOTA | Zodpovedný |
| :---- | :---- | :---- |
| Kódex správania | Jednoduché pravidlá pre všetkých, podpis pri nástupe a raz ročne. | CCO |
| Konflikt záujmov | Ročné vyhlásenie vedúcich, obchodu a nákupu; register konfliktov záujmov. | CCO; HR |
| Due diligence partnerov | Každý zákazník, dodávateľ, agent, distribútor a partner v konzorciu sa preverí pred rokovaním (U-08); agenti a distribútori podľa kapitoly 10\. | CCO a analytik DD |
| Sankčný screening | Pred ponukou, zmluvou, dodávkou a platbou (EÚ, OSN, OFAC). | ECO a špecialisti |
| Školenia | Úvodné pri nástupe, ročné pre všetkých, rozšírené pre obchod, nákup, financie, vývoj (prenos technológií) a vedenie. | CCO; ECO; HR |
| Interný audit | Ročný plán schvaľuje DR; kontrola platieb agentom, offsetov, darov, licencií, screeningu, prenosov dát a evidencie výbušnín. | externý interný audit |

## **15.2 Protikorupčná politika**

> * **Nulová tolerancia** úplatkov vrátane urýchľovacích platieb.  
> * **Darčeky a pohostenie** do limitu \[DOPLNIŤ €\] na osobu a rok, vždy v registri; voči verejným činiteľom a obstarávateľom len so súhlasom CCO; nikdy počas tendra; žiadne peniaze ani poukážky.  
> * **Agenti, distribútori a offsety** podľa kapitoly 10\.  
> * **Sponzoring a dary** len so súhlasom predstavenstva; žiadne politické príspevky.  
> * **Účtovníctvo** úplné a pravdivé, bez skrytých platieb.  
> * **Zahraničie**: pri obchode s UK alebo cez UK platí UK Bribery Act aj za konanie mimo UK (s. 7, s. 12 ods. 5); pri konaní na území USA FCPA (15 U.S.C. § 78dd-3).  
> * **Certifikácia** ISO 37001:2025 je dobrovoľná; pri predaji do celého sveta ju odporúčame do 12 až 18 mesiacov.

## **15.3 KYC, AML a sankcie**

IOTA nie je povinnou osobou podľa zákona č. 297/2008 Z. z., pokiaľ nerobí hotovostné obchody aspoň 10 000 € (§ 5 ods. 3); tie vnútorný predpis zakáže. Partnerov preverujeme vždy kvôli korupcii, sankciám a exportu. Podozrenie na sankcionovanú stranu ECO alebo CCO bezodkladne oznámi príslušnému orgánu a SIS (§ 15 z. 289/2016).

## **15.4 Whistleblowing – ochrana oznamovateľov**

Povinnosť zriadiť vnútorný systém platí od 50 zamestnancov (§ 10 ods. 1 z. 54/2019; čl. 8 ods. 3 smernice 2019/1937). IOTA má 31 ľudí; **odporúčame zaviesť systém hneď**, lebo pri munícii, vývoze a agentoch je včasné vnútorné oznámenie najlepší spôsob, ako problém zachytiť.

| Pravidlo | Obsah | Zdroj |
| :---- | :---- | :---- |
| Zodpovedná osoba | CCO; odborné predpoklady; viazaná len pokynmi štatutárneho orgánu; nesmie byť postihovaná. | § 10 ods. 1 a 4 z. 54/2019 |
| Externý príjem | Príjem oznámení môže zabezpečiť externá osoba; pri menej ako 250 zamestnancoch aj preverovanie. | § 10 ods. 2 z. 54/2019 |
| Kanál | Aspoň jeden spôsob nepretržite; písomne aj ústne; na požiadanie osobné stretnutie. | § 10 ods. 5 z. 54/2019 |
| Lehoty | Potvrdenie do 7 dní; výsledok do 90 dní. | § 10 ods. 6 a 8 z. 54/2019; čl. 9 smernice |
| Mlčanlivosť a evidencia | Dôvernosť totožnosti; evidencia 3 roky. | § 10 ods. 7, § 11 ods. 1 z. 54/2019 |
| Zákaz odvety | Žiadny postih; oznamovateľ môže požiadať Úrad na ochranu oznamovateľov o pozastavenie pracovnoprávneho úkonu do 15 dní. | čl. 19 smernice; § 12 z. 54/2019 |
| Vnútorný predpis | Podávanie, preverovanie, mlčanlivosť, evidencia. | § 10 ods. 9 z. 54/2019 |

# **16\. Zoznam interných dokumentov (politík)**

Existujúce návrhy sú v priečinku [04\_Politiky](https://drive.google.com/drive/folders/1br_1aCzqzOl3EH5JjRi3RMwtTAvsazO6) a treba ich zosúladiť so štruktúrou 3.0; ostatné sú nové.

| Č. | Dokument | Stav | Vlastník | Schvaľuje | Termín |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | Organizačný poriadok 3.0 a štatúty útvarov 2\. línie | nový | CEO; CCO | predstavenstvo | hneď |
| 2 | Kódex správania | existuje návrh (POL 15\) | CCO | predstavenstvo | hneď |
| 3 | Protikorupčná politika (ABAC) vrátane darčekov a sponzoringu | existuje návrh (POL 16\) | CCO | predstavenstvo | hneď |
| 4 | Program pre tretie strany: stupne rizika, dotazník, postup preverenia, matica schvaľovania, strop odmeny, monitorovanie; štatút Výboru pre tretie strany | nový | CCO | predstavenstvo | hneď |
| 5 | Vzorové zmluvné doložky pre agentov a distribútorov (protikorupcia, sankcie, no Russia, audit, ukončenie) | nový | CCO; Legal; ECO | predstavenstvo | hneď |
| 6 | Pravidlá pre offsety | nový | CCO; Legal | predstavenstvo | do 3 mesiacov |
| 7 | Konflikt záujmov a register | existuje (POL 21, register) | CCO | predstavenstvo | hneď |
| 8 | Due diligence tretích strán (KYC); register tretích strán, register platieb agentom a distribútorom, register varovných signálov a výnimiek | existuje návrh (POL 17), treba rozšíriť | CCO | predstavenstvo | hneď |
| 9 | Politika sankcií a exportnej kontroly; postup sankčného screeningu (EÚ, OSN, OFAC 50 %) | existuje návrh (POL 18, SOP 03), treba rozšíriť | ECO | predstavenstvo | hneď |
| 10 | Postup klasifikácie výrobkov (VM, dual-use, MTCR) a kusovník (BOM) s exportným zaradením a pôvodom každej položky; kontrolný bod v návrhu | nový | ECO; CTO | predstavenstvo | hneď |
| 11 | Postup pre americký obsah: výpočet de minimis (15 CFR 734.4), evidencia, žiadosti o určenie ECCN a USML | nový | ECO | predstavenstvo | do 3 mesiacov |
| 12 | Smernica pre návrh bez ITAR (ITAR free) a vyhlásenia dodávateľov o pôvode a zaradení | nový | CTO; ECO; Nákup | predstavenstvo | do 3 mesiacov |
| 13 | Postup licencovania vývozu, dokladov o konečnom užívateľovi a hlásení MH SR | nový | ECO | predstavenstvo | do 3 mesiacov |
| 14 | Program vnútorného súladu (ICP) podľa nariadenia 2021/821 a odporúčania 2019/1318 | nový | ECO | predstavenstvo | do 6 mesiacov |
| 15 | Opis systému riadenia transferov a vývozov (certifikát § 30 z. 392/2011) | nový | ECO | predstavenstvo | do 12 mesiacov |
| 16 | Plán kontroly technológií (TCP): matica prístupov podľa štátnej príslušnosti a previerky, preverenie zamestnancov a záznamy 5 rokov, pravidlá prenosu softvéru (cloud, e-mail, repozitáre, cesty, práca zo zahraničia) | nový | ECO; CTO; CISO; HR | predstavenstvo | hneď |
| 17 | Postup prijímania cudzincov (pobyt, povolenie na zamestnanie, kontrola občianstva a sankcií, prístupy, NDA) | nový | HR; ECO | predstavenstvo | pred prvým nástupom cudzinca |
| 18 | Pravidlá oddelených prístupov v IT (zóny Internal, Project, Controlled, utajované) | nový | CISO; IT prevádzka | predstavenstvo | do 3 mesiacov |
| 19 | Vnútorný predpis pre prácu s výbušninami a muníciou (§ 3 ods. 4 z. 58/2014) a technologické postupy | nový | HSE | predstavenstvo | pred žiadosťou HBÚ |
| 20 | Dokumentácia prevádzky skladu munície, evidencia (§ 12, § 20 z. 58/2014), havarijný a požiarny plán | nový | HSE; Bezpečnostný riaditeľ | predstavenstvo | pred kolaudáciou skladu |
| 21 | Politika ochrany utajovaných skutočností vrátane NATO a EÚ | existuje návrh (POL 20), treba rozšíriť | Bezpečnostný riaditeľ | predstavenstvo | do 3 mesiacov |
| 22 | Bezpečnostný projekt podnikateľa (§ 45 z. 215/2004) | nový | Bezpečnostný riaditeľ | predstavenstvo | do 6 mesiacov |
| 23 | Bezpečnostná dokumentácia fyzickej a objektovej bezpečnosti (§ 53 ods. 4\) | nový | Bezpečnostný riaditeľ | CEO (vedúci) | do 6 mesiacov |
| 24 | Bezpečnostný projekt technického prostriedku pre utajované IT (§ 58\) | nový | CISO; Bezpečnostný riaditeľ | predstavenstvo | do 6 mesiacov |
| 25 | Vnútorný predpis o preverovaní oznámení (§ 10 ods. 9 z. 54/2019) | existuje návrh (POL 22), treba doplniť | CCO | predstavenstvo | hneď |
| 26 | AML a KYC vrátane zákazu hotovosti nad 10 000 € | existuje návrh (POL 24\) | CCO; CFO | predstavenstvo | do 3 mesiacov |
| 27 | Informačná bezpečnosť a ISMS | existuje návrh (POL 19\) | CISO | predstavenstvo | do 6 mesiacov |
| 28 | Ochrana osobných údajov | existuje návrh (POL 23\) | DPO | predstavenstvo | do 3 mesiacov |
| 29 | Konzorciá a subdodávatelia | existuje návrh (POL 25\) | CCO; Nákup | predstavenstvo | do 6 mesiacov |
| 30 | Limity schvaľovania a podpisový poriadok | existuje (v1.2), doplniť licencie a offsety | CFO | predstavenstvo | hneď |
| 31 | Štatút interného auditu | nový | predseda DR | dozorná rada | do 6 mesiacov |
| 32 | Postup interného vyšetrovania | nový | CCO; Legal | predstavenstvo | do 6 mesiacov |
| 33 | Plán školení (compliance, export, prenos technológií, výbušniny, utajované) | nový | CCO; ECO; HSE; HR | predstavenstvo | do 3 mesiacov |
| 34 | Príručka kvality (ISO 9001, AQAP 2110\) | nový | manažér kvality | CEO | do 6 mesiacov |
| 35 | Popisy pracovných miest (CCO, ECO, Bezpečnostný riaditeľ, HSE, CISO, manažér kvality, analytik DD, špecialista klasifikácie) | existuje návrh (dok. 04 JD), doplniť HSE, analytika DD a špecialistu klasifikácie | HR | predstavenstvo | hneď |

# **17\. Fázovanie**

| Obdobie | Čo urobiť | Kto |
| :---- | :---- | :---- |
| **Hneď (do 3 mesiacov)** | Predstavenstvo schváli štruktúru 3.0 a uznesenia U-01 až U-13; dnešný Chairman sa stane predsedom dozornej rady. Menovať CCO, ECO, Bezpečnostného riaditeľa a vedúceho HSE; kde chýbajú ľudia, uzavrieť zmluvy s externými poradcami a začať nábor. Upresniť 31\. miesto v organigrame. Zaviesť pravidlo „bez exportného zaradenia nie je objednávka“; zostaviť kusovník s exportným zaradením pre všetky súčasné výrobky; vyžiadať vyhlásenia dodávateľov. Po zostavení kusovníka predstavenstvo rozhodne: ITAR free, alebo americké súčiastky s výpočtom de minimis. Klasifikovať všetky výrobky, softvér a technológie (VM 3, VM 4, VM 10, VM 11, VM 21, VM 22; 9A012, 9A112, 5A002; MTCR). Podať žiadosť o povolenie MH SR na obchodovanie a overiť živnosť na výrobu výrobkov obranného priemyslu. Vybrať miesto výroby a skladu munície a začať konzultáciu s HBÚ a príslušným obvodným banským úradom. Pred prvým nástupom cudzinca: postup prijímania cudzincov, plán kontroly technológií, oddelené zóny v IT a rozdelenie vývoja na otvorený a kontrolovaný tím. Zastaviť nové dohody s agentmi a distribútormi, kým neprejdú programom pre tretie strany; spustiť sankčný screening všetkých partnerov; založiť register tretích strán a Výbor pre tretie strany. Začať pripravovať bezpečnostný projekt podnikateľa pre NBÚ (Dôverné až Tajné). Schváliť kódex, protikorupčnú politiku, program pre tretie strany, vzorové doložky a konflikt záujmov; spustiť oznamovací kanál. | predstavenstvo; CCO; ECO; CTO; HR; Bezpečnostný riaditeľ; HSE |
| **Do 6 mesiacov** | Program vnútorného súladu (ICP), postup licencovania a vzory dokladov o konečnom užívateľovi; prvé vývozné licencie. Pri americkom obsahu: výpočty de minimis, prípadne žiadosti o určenie ECCN alebo USML a americké povolenia. Podať žiadosť HBÚ podľa § 42 z. 58/2014 (vnútorný predpis, evidencia, osvedčenia); projekt a povolenie skladu. Podať žiadosť NBÚ o bezpečnostnú previerku podnikateľa; previerky štatutára a kľúčových ľudí; projekt chránených priestorov a utajovaného IT systému. Ukončiť preverenie všetkých existujúcich agentov a distribútorov; podpísať dodatky s povinnými doložkami; offsetové pravidlá. Útvar Kvalita, príručka kvality a riadenie konfigurácie (AQAP 2110); ISMS; interný audit; školenia vrátane školení partnerov. | ECO; HSE; Bezpečnostný riaditeľ; CCO; manažér kvality; CISO |
| **Do 12 mesiacov** | Rozhodnutie HBÚ a kolaudácia skladu; až potom spustenie výroby munície. Potvrdenie NBÚ o priemyselnej bezpečnosti (rozhodnutie do 4 mesiacov pri Dôverné, do 7 mesiacov pri Tajné) a certifikácia a schválenie utajovaného IT systému. Druhý analytik DD v compliance podľa počtu partnerov; vlastný CISO. Certifikácia ISO 9001 a AQAP 2110, podľa zákazníkov AS/EN 9100; ISO/IEC 27001; rozhodnutie o ISO 37001\. Certifikát príjemcu transferov podľa § 30, ak ho budeme potrebovať. Prvý interný audit exportu, kusovníkov, agentov a platieb, prístupov cudzincov, evidencie výbušnín a utajovaných skutočností; ročná správa pre predstavenstvo a DR. | predstavenstvo; všetky útvary |

# **18\. Otvorené otázky na Mariana**

> 1. Kde by mohol byť sklad munície (obec alebo areál)? Od toho závisí povolenie stavebného úradu a obvodného banského úradu.  
> 2. Z ktorých krajín budú vývojári mimo EÚ? Od toho závisí, k čomu môžu mať prístup.  
> 3. V ktorých krajinách chcete začať s agentmi a distribútormi? Od toho závisí stupeň rizika a rozsah preverenia.

Ďalšie údaje na doplnenie počas práce (bez potreby odpovede teraz): 31\. miesto v organigrame, výška stropu odmeny agentov a hranica hodnoty obchodu pre vysoké riziko (označené \[DOPLNIŤ\]).

# **19\. Zdroje**

> * [Zákon č. 392/2011 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2011/392/20240201.html)  
> * [Zákon č. 58/2014 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2014/58/20240102.html)  
> * [Zákon č. 243/2026 Z. z. (novela)](https://static.slov-lex.sk/static/SK/ZZ/2026/243/)  
> * [Zákon č. 190/2003 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2003/190/20250701.html)  
> * [Zákon č. 39/2011 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2011/39/20240201.html)  
> * [Zákon č. 215/2004 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2004/215/20250501.html)  
> * [Zákon č. 497/2022 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2022/497/20250101.html)  
> * [NV SR č. 61/2023 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2023/61/20230301.html)  
> * [Zákon č. 69/2018 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2018/69/20260430.html)  
> * [Zákon č. 54/2019 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2019/54/20260324.html)  
> * [Zákon č. 91/2016 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2016/91/20260817.html)  
> * [Trestný zákon č. 300/2005 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2005/300/20260818.html)  
> * [Zákon č. 289/2016 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2016/289/20260601.html)  
> * [Zákon č. 297/2008 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2008/297/20260817.html)  
> * [Obchodný zákonník](https://static.slov-lex.sk/static/SK/ZZ/1991/513/20260817.html)  
> * [Spoločná pozícia 2008/944/SZBP (konsolidované znenie)](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:02008E0944-20190917)  
> * [Spoločný zoznam vojenského materiálu EÚ, C/2026/1640](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=OJ:C_202601640)  
> * [Spoločná pozícia 2003/468/SZBP](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32003E0468)  
> * [Nariadenie (EÚ) 2021/821](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0821)  
> * [Delegované nariadenie (EÚ) 2025/2003](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32025R2003)  
> * [Odporúčanie (EÚ) 2019/1318](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32019H1318)  
> * [Rozhodnutie Rady 2013/488/EÚ](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32013D0488)  
> * [Smernica 2009/43/ES](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32009L0043)  
> * [Smernica 2009/81/ES](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32009L0081)  
> * [Nariadenie (EÚ) 2019/452](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32019R0452)  
> * [Smernica (EÚ) 2022/2555](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32022L2555)  
> * [Smernica (EÚ) 2019/1937](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32019L1937)  
> * [GDPR](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32016R0679)  
> * [Nariadenie (EÚ) 2021/697](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0697)  
> * [Nariadenie (EÚ) 2025/2643](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32025R2643)  
> * [FAQ Komisie k čl. 12g nariadenia 833/2014](https://finance.ec.europa.eu/publications/no-re-export-russia-clause_en)  
> * [EU Sanctions Map](https://www.sanctionsmap.eu/)  
> * [Konsolidovaný zoznam BR OSN](https://main.un.org/securitycouncil/en/content/un-sc-consolidated-list)  
> * [OFAC FAQ – pravidlo 50 %](https://ofac.treasury.gov/faqs/topic/1521)  
> * [50 U.S.C. § 1705](https://www.govinfo.gov/content/pkg/USCODE-2023-title50/html/USCODE-2023-title50-chap35-sec1705.htm)  
> * [MTCR Guidelines](https://www.mtcr.info/en/mtcr-guidelines)  
> * [Zmluva o obchode so zbraňami (OSN)](https://treaties.un.org/doc/Treaties/2013/04/20130410%2012-01%20PM/Ch_XXVI_08.pdf)  
> * [Wassenaarské dojednanie](https://www.wassenaar.org/about-us/)  
> * [EAR 15 CFR 734.3](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.3)  
> * [EAR 15 CFR 734.4](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.4)  
> * [EAR 15 CFR 734.13](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.13)  
> * [EAR 15 CFR 734.14](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.14)  
> * [EAR 15 CFR 734.18](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734/section-734.18)  
> * [ITAR 22 CFR 120.50](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.50)  
> * [ITAR 22 CFR 120.51](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.51)  
> * [ITAR 22 CFR 120.54](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.54)  
> * [ITAR 22 CFR 120.56](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-120/subpart-C/section-120.56)  
> * [ITAR 22 CFR 123.9](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-123/section-123.9)  
> * [NATO AQAP-2110 (EDA EDSTAR)](https://edstar.eda.europa.eu/Standards/Details/aad7da24-5ab4-419c-a2c6-e7b3835f8fa1)  
> * [IAQG 9100](https://iaqg.org/standard/9100-qms-requirements-for-aviation-space-and-defense-organizations/)  
> * [ISO 37001](https://www.iso.org/standard/65034.html)  
> * [ISO 37301](https://www.iso.org/standard/75080.html)  
> * [ISO/IEC 27001](https://www.iso.org/standard/27001)  
> * [Dohovor OECD](https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0293)  
> * [FCPA 15 U.S.C. § 78dd-3](https://www.govinfo.gov/content/pkg/USCODE-2023-title15/html/USCODE-2023-title15-chap2B-sec78dd-3.htm)  
> * [UK Bribery Act s. 7](https://www.legislation.gov.uk/ukpga/2010/23/section/7)  
> * [UK Bribery Act s. 12](https://www.legislation.gov.uk/ukpga/2010/23/section/12)  
> * [EAR 15 CFR 734.20](https://www.ecfr.gov/current/title-15/section-734.20)  
> * [EAR 15 CFR 748.3](https://www.ecfr.gov/current/title-15/section-748.3)  
> * [ITAR 22 CFR 120.4](https://www.ecfr.gov/current/title-22/section-120.4)  
> * [ITAR 22 CFR 120.11](https://www.ecfr.gov/current/title-22/section-120.11)  
> * [ITAR 22 CFR 124.1](https://www.ecfr.gov/current/title-22/section-124.1)  
> * [ITAR 22 CFR 126.18](https://www.ecfr.gov/current/title-22/section-126.18)  
> * [Zákon č. 404/2011 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2011/404/20261001.html)  
> * [Zákon č. 5/2004 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2004/5/20260801.html)  
> * [Zákon č. 315/2016 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2016/315/20191101.html)  
> * [Odporúčanie OECD 2021 (OECD/LEGAL/0378)](https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0378)  
> * [Transparency International – CPI 2025](https://www.transparency.org/en/cpi/2025)  
> * [Verzia 2.0 tohto dokumentu (archív)](https://docs.google.com/document/d/1ZHZNKcI7xTYn57nA7wl1JKvhNqChxvyRb25aP0-xago/edit)

Súvisiace interné dokumenty: [Rámec v1.1](https://docs.google.com/document/d/1zOz-IPOs1SoTmKwQo6jDrqPL_NZk29Tl5oDKKSCup8o/edit), [Rozhodnutia predstavenstva P0](https://docs.google.com/document/d/1EMnq77eS-b8mEu_rFJHd2lYhST9t-6FloC3bJMfUpsQ/edit), [IT štruktúra a identity](https://docs.google.com/document/d/1H83T1Oa3hwzx7FhapHuClGH_09tSdpYuPbE1hJeW9o8/edit), [Popisy pracovných miest 2\. línie](https://docs.google.com/document/d/1KvYwlYO2e6qD5Y4YOaPD4w4L_IaYZBQU-MjV3SWdBmU/edit), [04\_Politiky](https://drive.google.com/drive/folders/1br_1aCzqzOl3EH5JjRi3RMwtTAvsazO6).