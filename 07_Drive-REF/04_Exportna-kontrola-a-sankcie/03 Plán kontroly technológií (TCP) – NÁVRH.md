**Plán kontroly technológií (Technology Control Plan)**

IOTA Defence a.s. · Číslo: IOTA-EXP-03 · Verzia 1.0 · 20\. 10\. 2026 · Vlastník: ECO · Schvaľuje: predstavenstvo · Klasifikácia: Interné · Stav: NÁVRH

# **1\. Účel**

Určiť, kto smie mať prístup k akým technológiám, softvéru a technickým dátam, najmä keď vo vývoji pracujú ľudia z krajín mimo EÚ a keď môžeme používať americké technológie.

# **2\. Rozsah**

Technická dokumentácia, zdrojový kód, výrobné postupy a skúšobné dáta; všetci zamestnanci a externí spolupracovníci; IT systémy, cloud, cesty a práca zo zahraničia.

# **3\. Pojmy**

| Pojem | Význam v tomto dokumente |
| :---- | :---- |
| Kontrolovaná technológia | Technológia alebo softvér zaradený ako vojenský materiál (VM 21, VM 22), dual-use, alebo podliehajúci ITAR alebo EAR. |
| Deemed reexport | Sprístupnenie americkej technológie cudzincovi mimo USA, ktoré právo USA považuje za vývoz do krajiny jeho občianstva alebo trvalého pobytu. |
| Otvorený tím / kontrolovaný tím | Rozdelenie vývoja podľa návrhu organizačnej štruktúry v3.0. |

# **4\. Právny základ a štandardy**

| Predpis alebo štandard | Ustanovenie | Čo z neho vyplýva |
| :---- | :---- | :---- |
| [nariadenie (EÚ) 2021/821](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0821) | čl. 2 bod 2 písm. d); čl. 8 | Elektronický prenos a sprístupnenie mimo EÚ je vývoz; technická pomoc. |
| [zákon č. 392/2011 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2011/392/20240201.html) | § 3 písm. c) | Služby, poskytovanie informácií a vysielanie odborníkov sú výrobkom obranného priemyslu. |
| [Spoločná pozícia Rady 2008/944/SZBP](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:02008E0944-20190917) | čl. 1 ods. 2 | Nehmotný prenos technológie. |
| [15 CFR 734.14](https://www.ecfr.gov/current/title-15/section-734.14) | (b) | Deemed reexport do krajiny posledného občianstva alebo trvalého pobytu. |
| [22 CFR 120.51](https://www.ecfr.gov/current/title-22/section-120.51) | (b) | Pri ITAR deemed reexport do všetkých krajín občianstva. |
| [15 CFR 734.20](https://www.ecfr.gov/current/title-15/section-734.20) | (a), (b), (c) | Situácie, ktoré nie sú deemed reexport (vrátane stálych zamestnancov pri splnení podmienok). |
| [22 CFR 126.18](https://www.ecfr.gov/current/title-22/section-126.18) | (c) | Prenos zamestnancom s dvojitým alebo cudzím občianstvom: preverenie, plán bezpečnosti technológií, záznamy 5 rokov k dispozícii DDTC. |
| [22 CFR 124.1](https://www.ecfr.gov/current/title-22/section-124.1) | celý paragraf | Obranné služby len so schválenou dohodou (TAA). |
| [15 CFR 734.18](https://www.ecfr.gov/current/title-15/section-734.18) | (a)(5) | Šifrované uloženie (FIPS 140-2) nie je vývoz. |
| [22 CFR 120.54](https://www.ecfr.gov/current/title-22/section-120.54) | (a)(5) | Obdobne pri ITAR. |
| [22 CFR 120.56](https://www.ecfr.gov/current/title-22/section-120.56) | celý paragraf | Sprístupnenie prístupových údajov môže byť odovzdaním. |
| [zákon č. 215/2004 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2004/215/20250501.html) | § 10 ods. 1 písm. a); § 36 | Utajované skutočnosti len pre občanov SR, výnimky pre cudzincov len podľa § 36\. |

# **5\. Zodpovednosti**

| Funkcia | Úloha | Reportuje |
| :---- | :---- | :---- |
| ECO | Vlastník plánu, zaraďuje technológie, schvaľuje prístupy do zóny Controlled. | predstavenstvu |
| CTO | Rozdelenie tímov, označovanie dokumentácie, dodržiavanie v praxi. | CEO |
| HR | Overenie občianstiev a pobytov pri nástupe, dohody o mlčanlivosti. | CFO |
| CISO a IT prevádzka | Technické oddelenie prístupov, záznamy, kontrola oprávnení. | predstavenstvu |
| Bezpečnostný riaditeľ | Utajované skutočnosti. | predstavenstvu |

# **6\. Postup**

## **6.1 Matica prístupov**

| Zóna | Obsah | Kto má prístup |
| :---- | :---- | :---- |
| Internal | Bežné firemné informácie | všetci zamestnanci |
| Project | Nekontrolovaný vývoj, otvorený tím | členovia projektu vrátane cudzincov po preverení |
| Controlled | Kontrolované technológie, VM 21 a VM 22, americké technické dáta | len osoby schválené ECO podľa krajiny, previerky a licencie |
| Utajované | Utajované skutočnosti | len občania SR s osvedčením NBÚ, v certifikovanom systéme |

## **6.2 Postup pri nástupe**

> 1. HR zistí všetky štátne občianstva a trvalé pobyty uchádzača (vyhlásenie a doklady).  
> 2. ECO vykoná sankčný screening a pri americkej technológii posúdi deemed reexport a výnimky (15 CFR 734.20, 22 CFR 126.18).  
> 3. Pri ITAR sa preverí, či zamestnanec nemá podstatné kontakty s krajinami podľa 22 CFR 126.1; záznam o preverení sa uchová 5 rokov.  
> 4. Zamestnanec podpíše dohodu o mlčanlivosti a ochrane technológií.  
> 5. ECO určí zónu prístupu; IT nastaví prístupy len podľa schválenia.

## **6.3 Prenosy a cesty**

> * Kontrolované dáta sa ukladajú len v EÚ, šifrovane; zdieľanie mimo spoločnosti len so súhlasom ECO.  
> * Služobná cesta alebo práca zo zahraničia s prístupom do zóny Controlled len so súhlasom ECO; vývoz notebooku s kontrolovanými dátami je vývozom.  
> * Návštevy cudzincov v priestoroch vývoja len s doprovodom a so záznamom.  
> * Technická pomoc alebo školenie zahraničného zákazníka len po posúdení ECO (licencia MH SR, pri USA dohoda TAA).

## **6.4 Kontrola**

IT raz za štvrťrok vytvorí zoznam prístupov do zóny Controlled; ECO ho porovná so schváleniami a odchýlky odstráni do 5 pracovných dní.

# **7\. Evidencia a lehoty**

| Záznam | Kto vedie | Lehota alebo uchovávanie |
| :---- | :---- | :---- |
| Matica schválených prístupov | ECO | priebežne; 10 rokov |
| Záznamy o preverení zamestnancov (ITAR) | ECO a HR | najmenej 5 rokov (22 CFR 126.18(c)) |
| Dohody o mlčanlivosti | HR | počas pracovného pomeru a 10 rokov |
| Záznamy prístupov IT | CISO | podľa politiky logovania, najmenej …………………… mesiacov |

# **8\. Kontrola a sankcie**

> * Štvrťročná kontrola prístupov (6.4).  
> * Interný audit raz ročne.

Porušenie tohto dokumentu zamestnancom je porušením povinnosti dodržiavať predpisy vzťahujúce sa na vykonávanú prácu, s ktorými bol riadne oboznámený (§ 81 písm. c) [Zákonníka práce](https://static.slov-lex.sk/static/SK/ZZ/2001/311/20260901.html)), a môže viesť k pracovnoprávnym opatreniam vrátane skončenia pracovného pomeru. Pri obchodných partneroch je porušenie dôvodom na pozastavenie plnenia a ukončenie zmluvy. Ak porušenie môže byť trestným činom alebo správnym deliktom, predstavenstvo na návrh príslušného gestora rozhodne o oznámení orgánu činnému v trestnom konaní alebo príslušnému úradu.

# **9\. Súvisiace dokumenty**

> * Postup prijímania cudzincov (10\_HR-a-skolenia)  
> * Pravidlá oddelených prístupov v IT (06\_Kyberbezpecnost-a-IT)  
> * IT štruktúra a identity: [otvoriť](https://docs.google.com/document/d/1H83T1Oa3hwzx7FhapHuClGH_09tSdpYuPbE1hJeW9o8/edit)

# **10\. Schválenie a účinnosť**

Tento dokument nadobúda účinnosť dňom schválenia. Vlastník ho preskúma najmenej raz ročne a vždy pri zmene predpisov, organizácie alebo činnosti spoločnosti.

|  | Meno | Funkcia | Dátum | Podpis |
| :---- | :---- | :---- | :---- | :---- |
| Vypracoval | …………………… | ECO | …………………… | …………………… |
| Preskúmal (advokát) | …………………… | externý advokát | …………………… | …………………… |
| Schválil | …………………… | predstavenstvo | …………………… | …………………… |
| Účinnosť od |  |  | …………………… |  |

| Verzia | Dátum | Zmena |
| :---- | :---- | :---- |
| 1.0 | 20\. 10\. 2026 | Prvé vydanie (NÁVRH) |

