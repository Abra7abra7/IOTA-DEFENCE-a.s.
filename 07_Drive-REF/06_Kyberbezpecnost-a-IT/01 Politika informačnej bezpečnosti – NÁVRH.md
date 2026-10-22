**Politika informačnej bezpečnosti**

IOTA Defence a.s. · Číslo: IOTA-IT-01 · Verzia 1.0 · 20\. 10\. 2026 · Vlastník: CISO · Schvaľuje: predstavenstvo · Klasifikácia: Interné · Stav: NÁVRH

# **1\. Účel**

Chrániť dôvernosť, integritu a dostupnosť informácií spoločnosti, najmä technických dát, zdrojového kódu a údajov o zákazníkoch, a vytvoriť systém riadenia informačnej bezpečnosti podľa normy ISO/IEC 27001\.

# **2\. Rozsah**

Všetky informačné systémy, zariadenia, cloudové služby, zamestnanci a dodávatelia s prístupom k informáciám spoločnosti. Utajované skutočnosti upravuje osobitná smernica.

# **3\. Pojmy**

| Pojem | Význam v tomto dokumente |
| :---- | :---- |
| ISMS | Systém riadenia informačnej bezpečnosti. |
| Zóny dát | Internal, Project, Controlled, Utajované (podľa Plánu kontroly technológií). |

# **4\. Právny základ a štandardy**

| Predpis alebo štandard | Ustanovenie | Čo z neho vyplýva |
| :---- | :---- | :---- |
| [ISO/IEC 27001](https://www.iso.org/standard/27001) | celá norma | Požiadavky na ISMS (dobrovoľná certifikácia). |
| [nariadenie (EÚ) 2016/679 (GDPR)](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32016R0679) | čl. 32 | Bezpečnosť spracúvania osobných údajov. |
| [nariadenie (EÚ) 2021/821](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0821) | čl. 2 bod 2 písm. d) | Prenos technológie elektronicky mimo EÚ je vývoz. |
| [15 CFR 734.18](https://www.ecfr.gov/current/title-15/section-734.18) | (a)(5) | Šifrované uloženie (FIPS 140-2) nie je vývoz podľa EAR. |
| [22 CFR 120.54](https://www.ecfr.gov/current/title-22/section-120.54) | (a)(5) | Obdobne pri ITAR. |
| [zákon č. 215/2004 Z. z.](https://static.slov-lex.sk/static/SK/ZZ/2004/215/20250501.html) | § 55 až 58 | Utajované skutočnosti len v certifikovaných systémoch. |
| [69](https://static.slov-lex.sk/static/SK/ZZ/2018/69/20260430.html) | celý zákon | Zákon o kybernetickej bezpečnosti; pôsobnosť na spoločnosť posúdi advokát (pri 31 zamestnancoch pravdepodobne nie). |

# **5\. Zodpovednosti**

| Funkcia | Úloha | Reportuje |
| :---- | :---- | :---- |
| CISO | Vlastník ISMS, riziká, incidenty, kontrola prístupov. | predstavenstvu |
| IT prevádzka | Správa systémov, záloh a prístupov podľa schválení. | CFO; odborne CISO |
| ECO | Schvaľuje prístupy do zóny Controlled. | predstavenstvu |
| Zamestnanci | Dodržiavajú pravidlá, hlásia incidenty. | nadriadenému |

# **6\. Postup**

## **6.1 Základné pravidlá**

> * Prihlásenie len viacfaktorovou autentifikáciou; zdieľané účty sú zakázané.  
> * Prístupy podľa roly a potreby; schvaľuje vedúci, do zóny Controlled ECO.  
> * Firemné zariadenia so šifrovaním disku a správou zariadení; súkromné zariadenia len s povolením CISO a nikdy pre zónu Controlled.  
> * Kontrolované dáta len v EÚ, šifrované; žiadne verejné odkazy.  
> * Zálohy podľa plánu obnovy; test obnovy raz za štvrťrok.  
> * Logovanie a monitorovanie podľa existujúceho dokumentu o logovaní.  
> * Nový dodávateľ IT alebo cloudu len po posúdení CISO, DPO a ECO.

## **6.2 Incidenty**

> 1. Okamžité nahlásenie CISO.  
> 2. Posúdenie a obmedzenie do 4 hodín.  
> 3. Ak ide o osobné údaje, DPO posúdi oznámenie do 72 hodín; ak ide o kontrolované dáta, ECO posúdi, či nedošlo k nepovolenému vývozu.  
> 4. Uzavretie, analýza príčin, opatrenia.

## **6.3 Plán zavedenia ISMS**

| Krok | Termín |
| :---- | :---- |
| Rozsah ISMS a inventár aktív | …………………… |
| Analýza rizík a vyhlásenie o aplikovateľnosti | …………………… |
| Zavedenie opatrení a školenia | …………………… |
| Interný audit a preskúmanie vedením | …………………… |
| Rozhodnutie o certifikácii | …………………… |

# **7\. Evidencia a lehoty**

| Záznam | Kto vedie | Lehota alebo uchovávanie |
| :---- | :---- | :---- |
| Register aktív a rizík | CISO | priebežne |
| Evidencia incidentov | CISO | 5 rokov |
| Zoznamy prístupov a ich kontroly | CISO | štvrťročne; 5 rokov |

# **8\. Kontrola a sankcie**

> * Kontrola prístupov štvrťročne; test obnovy štvrťročne; interný audit ISMS raz ročne.

Porušenie tohto dokumentu zamestnancom je porušením povinnosti dodržiavať predpisy vzťahujúce sa na vykonávanú prácu, s ktorými bol riadne oboznámený (§ 81 písm. c) [Zákonníka práce](https://static.slov-lex.sk/static/SK/ZZ/2001/311/20260901.html)), a môže viesť k pracovnoprávnym opatreniam vrátane skončenia pracovného pomeru. Pri obchodných partneroch je porušenie dôvodom na pozastavenie plnenia a ukončenie zmluvy. Ak porušenie môže byť trestným činom alebo správnym deliktom, predstavenstvo na návrh príslušného gestora rozhodne o oznámení orgánu činnému v trestnom konaní alebo príslušnému úradu.

# **9\. Súvisiace dokumenty**

> * Pravidlá oddelených prístupov v IT  
> * Plán kontroly technológií  
> * IT štruktúra a identity: [otvoriť](https://docs.google.com/document/d/1H83T1Oa3hwzx7FhapHuClGH_09tSdpYuPbE1hJeW9o8/edit)  
> * Logovanie a monitoring: [otvoriť](https://docs.google.com/document/d/1h88dJv-OX-tX_I-MIDv8WOWzZ3lg8jK8Imy4isqvzRU/edit)

# **10\. Schválenie a účinnosť**

Tento dokument nadobúda účinnosť dňom schválenia. Vlastník ho preskúma najmenej raz ročne a vždy pri zmene predpisov, organizácie alebo činnosti spoločnosti.

|  | Meno | Funkcia | Dátum | Podpis |
| :---- | :---- | :---- | :---- | :---- |
| Vypracoval | …………………… | CISO | …………………… | …………………… |
| Preskúmal (advokát) | …………………… | externý advokát | …………………… | …………………… |
| Schválil | …………………… | predstavenstvo | …………………… | …………………… |
| Účinnosť od |  |  | …………………… |  |

| Verzia | Dátum | Zmena |
| :---- | :---- | :---- |
| 1.0 | 20\. 10\. 2026 | Prvé vydanie (NÁVRH) |

