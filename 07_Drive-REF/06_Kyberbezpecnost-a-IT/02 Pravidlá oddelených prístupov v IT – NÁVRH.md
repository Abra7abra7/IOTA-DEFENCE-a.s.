**Pravidlá oddelených prístupov v IT**

IOTA Defence a.s. · Číslo: IOTA-IT-02 · Verzia 1.0 · 20\. 10\. 2026 · Vlastník: CISO · Schvaľuje: predstavenstvo · Klasifikácia: Interné · Stav: NÁVRH

# **1\. Účel**

Technicky zabezpečiť, aby k dátam mal prístup len ten, kto ho má schválený podľa roly, štátnej príslušnosti, licencie a previerky.

# **2\. Rozsah**

Identity, skupiny, repozitáre, úložiská, vývojové prostredia, e-mail a vzdialený prístup.

# **3\. Právny základ a štandardy**

| Predpis alebo štandard | Ustanovenie | Čo z neho vyplýva |
| :---- | :---- | :---- |
| [15 CFR 734.14](https://www.ecfr.gov/current/title-15/section-734.14) | (b) | Deemed reexport pri sprístupnení americkej technológie cudzincovi. |
| [22 CFR 120.56](https://www.ecfr.gov/current/title-22/section-120.56) | celý paragraf | Sprístupnenie prístupových údajov môže byť odovzdaním. |
| [22 CFR 126.18](https://www.ecfr.gov/current/title-22/section-126.18) | (c) | Preverenie zamestnancov a plán bezpečnosti technológií. |
| [nariadenie (EÚ) 2021/821](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0821) | čl. 2 bod 2 písm. d) | Sprístupnenie osobám mimo EÚ je vývoz. |

# **4\. Zodpovednosti**

| Funkcia | Úloha | Reportuje |
| :---- | :---- | :---- |
| CISO | Navrhuje a kontroluje model prístupov. | predstavenstvu |
| IT prevádzka | Nastavuje prístupy len podľa schválenej žiadosti. | CFO |
| ECO | Schvaľuje zónu Controlled. | predstavenstvu |
| HR | Hlási nástupy, zmeny a odchody v deň zmeny. | CFO |

# **5\. Postup**

| Zóna | Technické opatrenie | Schvaľuje |
| :---- | :---- | :---- |
| Internal | firemný účet, MFA | vedúci |
| Project | skupina projektu, oddelený repozitár | vedúci projektu |
| Controlled | samostatná skupina, oddelené repozitáre a úložisko v EÚ, šifrovanie, záznam prístupov, zákaz externého zdieľania | ECO |
| Utajované | certifikovaný systém mimo bežnej siete | Bezpečnostný riaditeľ |

> 1. Žiadosť o prístup cez IT systém s uvedením zóny a dôvodu.  
> 2. Schválenie podľa tabuľky; pri zóne Controlled ECO overí krajinu a licenciu.  
> 3. IT nastaví prístup a zapíše ho.  
> 4. Odchod alebo zmena: prístup odobratý v deň zmeny.  
> 5. Štvrťročná kontrola prístupov; odchýlky odstránené do 5 pracovných dní.

# **6\. Evidencia a lehoty**

| Záznam | Kto vedie | Lehota alebo uchovávanie |
| :---- | :---- | :---- |
| Žiadosti a schválenia prístupov | IT prevádzka | 5 rokov |
| Výsledky štvrťročných kontrol | CISO | 5 rokov |

# **7\. Kontrola a sankcie**

> * CISO a ECO štvrťročne kontrolujú prístupy do zóny Controlled.

Porušenie tohto dokumentu zamestnancom je porušením povinnosti dodržiavať predpisy vzťahujúce sa na vykonávanú prácu, s ktorými bol riadne oboznámený (§ 81 písm. c) [Zákonníka práce](https://static.slov-lex.sk/static/SK/ZZ/2001/311/20260901.html)), a môže viesť k pracovnoprávnym opatreniam vrátane skončenia pracovného pomeru. Pri obchodných partneroch je porušenie dôvodom na pozastavenie plnenia a ukončenie zmluvy. Ak porušenie môže byť trestným činom alebo správnym deliktom, predstavenstvo na návrh príslušného gestora rozhodne o oznámení orgánu činnému v trestnom konaní alebo príslušnému úradu.

# **8\. Súvisiace dokumenty**

> * Plán kontroly technológií  
> * Politika informačnej bezpečnosti

# **9\. Schválenie a účinnosť**

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

