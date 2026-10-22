**Smernica o klasifikácii výrobkov a kusovníku (BOM)**

IOTA Defence a.s. · Číslo: IOTA-EXP-02 · Verzia 1.0 · 20\. 10\. 2026 · Vlastník: ECO · Schvaľuje: predstavenstvo · Klasifikácia: Interné · Stav: NÁVRH

# **1\. Účel**

Zabezpečiť, aby každý výrobok, súčiastka, softvér a technológia mali exportné zaradenie už pri návrhu, a aby kusovník (BOM) obsahoval pôvod a zaradenie každej položky. Bez zaradenia nemožno určiť potrebnú licenciu ani americký obsah.

# **2\. Rozsah**

Všetky vlastné výrobky, ich súčiastky a podzostavy, firmvér a softvér, technická dokumentácia a výrobné technológie; nakupované položky a softvér tretích strán.

# **3\. Pojmy**

| Pojem | Význam v tomto dokumente |
| :---- | :---- |
| Kusovník (BOM) | Zoznam všetkých položiek výrobku s množstvom, dodávateľom, pôvodom a exportným zaradením. |
| Zaradenie EÚ | Položka Spoločného zoznamu vojenského materiálu (VM 1 až 22), kód prílohy I nariadenia 2021/821 alebo „nekontrolované“. |
| Zaradenie USA | Kategória USML (ITAR), ECCN alebo EAR99 (EAR), alebo „nepodlieha“. |
| Kontrolný bod v návrhu | Bod v procese vývoja, v ktorom ECO potvrdí zaradenie pred schválením návrhu alebo zmeny. |

# **4\. Právny základ a štandardy**

| Predpis alebo štandard | Ustanovenie | Čo z neho vyplýva |
| :---- | :---- | :---- |
| [Spoločný zoznam vojenského materiálu EÚ (C/2026/1640)](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=OJ:C_202601640) | VM 3, VM 4, VM 10, VM 11, VM 21, VM 22 | Munícia; bomby, rakety a nálože; UAV; elektronika; softvér; technológia. |
| [nariadenie (EÚ) 2021/821](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32021R0821) | čl. 2 a príloha I | Položky s dvojakým použitím. |
| [delegované nariadenie (EÚ) 2025/2003](https://eur-lex.europa.eu/legal-content/SK/TXT/?uri=CELEX:32025R2003) | príloha | Nové znenie prílohy I od 15\. 11\. 2025 (napr. 9A012, 9A112, 5A002, 5D002, kategória 4). |
| [MTCR – usmernenia a príloha](https://www.mtcr.info/en/mtcr-guidelines) | kategória I a II | UAV s doletom aspoň 300 km (s užitočným zaťažením 500 kg kategória I). |
| [15 CFR 734.3](https://www.ecfr.gov/current/title-15/section-734.3) | (a)(2) | Americké položky podliehajú EAR kdekoľvek. |
| [15 CFR 734.4](https://www.ecfr.gov/current/title-15/section-734.4) | (c), (d), (a), (b) | De minimis 10 % alebo 25 % a výnimky. |
| [22 CFR 120.11](https://www.ecfr.gov/current/title-22/section-120.11) | (c) | Položka z USML zostáva pod ITAR aj po zabudovaní. |
| [15 CFR 748.3](https://www.ecfr.gov/current/title-15/section-748.3) | celý paragraf | Žiadosť o určenie ECCN úradom BIS. |
| [22 CFR 120.4](https://www.ecfr.gov/current/title-22/section-120.4) | celý paragraf | Určenie, či položka patrí do USML (commodity jurisdiction). |

# **5\. Zodpovednosti**

| Funkcia | Úloha | Reportuje |
| :---- | :---- | :---- |
| ECO | Rozhoduje o zaradení; môže zablokovať zaradenie položky do kusovníka. | predstavenstvu |
| Špecialista klasifikácie | Pripravuje zaradenie, vedie register klasifikácie a kusovníky. | ECO |
| CTO a vývojári | Dodajú technické parametre, navrhujú alternatívy pri problémových položkách. | CEO |
| Nákup | Vyžiada vyhlásenie dodávateľa o pôvode a zaradení pred objednávkou. | CFO |

# **6\. Postup**

> 1. Nová položka: vývojár zapíše položku do návrhu kusovníka so stavom „nezaradené“.  
> 2. Nákup vyžiada od dodávateľa vyhlásenie o krajine pôvodu, ECCN alebo USML, a pri softvéri o šifrovaní.  
> 3. Špecialista klasifikácie posúdi zaradenie podľa EÚ a USA; pri pochybnosti konzultuje externého poradcu.  
> 4. ECO schváli zaradenie a stav sa zmení na „zaradené“. Bez toho Nákup nesmie vystaviť objednávku.  
> 5. Pri americkom obsahu sa vypočíta podiel podľa 15 CFR 734.4 a zapíše do registra.  
> 6. Kontrolný bod v návrhu: pred schválením návrhu a pred každou zmenou ECO potvrdí zaradenie celého výrobku, jeho softvéru a technickej dokumentácie.  
> 7. Pri zmene dodávateľa, verzie softvéru alebo právnych predpisov sa zaradenie preskúma.

## **6.1 Údaje v kusovníku**

| Pole | Príklad |
| :---- | :---- |
| Číslo položky / názov | P-0001 letový kontrolér |
| Výrobca a dodávateľ | …………………… |
| Krajina pôvodu | …………………… |
| Zaradenie EÚ (VM / dual-use / nekontrolované) | …………………… |
| Zaradenie USA (USML / ECCN / EAR99 / nepodlieha) | …………………… |
| Hodnota (pre de minimis) | …………………… |
| Zdroj informácie a dátum | …………………… |
| Schválil ECO (dátum) | …………………… |

# **7\. Evidencia a lehoty**

| Záznam | Kto vedie | Lehota alebo uchovávanie |
| :---- | :---- | :---- |
| Register klasifikácie a kusovníky | ECO | pri každej zmene; počas životnosti výrobku a 10 rokov |
| Vyhlásenia dodávateľov | Nákup | pred objednávkou; 10 rokov |
| Výpočty de minimis | ECO | pri každom výrobku a zmene; 10 rokov |

# **8\. Kontrola a sankcie**

> * ECO štvrťročne overí, či žiadna objednávka nebola vystavená na nezaradenú položku.  
> * Interný audit raz ročne preverí vzorku kusovníkov.

Porušenie tohto dokumentu zamestnancom je porušením povinnosti dodržiavať predpisy vzťahujúce sa na vykonávanú prácu, s ktorými bol riadne oboznámený (§ 81 písm. c) [Zákonníka práce](https://static.slov-lex.sk/static/SK/ZZ/2001/311/20260901.html)), a môže viesť k pracovnoprávnym opatreniam vrátane skončenia pracovného pomeru. Pri obchodných partneroch je porušenie dôvodom na pozastavenie plnenia a ukončenie zmluvy. Ak porušenie môže byť trestným činom alebo správnym deliktom, predstavenstvo na návrh príslušného gestora rozhodne o oznámení orgánu činnému v trestnom konaní alebo príslušnému úradu.

# **9\. Súvisiace dokumenty**

> * Politika amerického obsahu a návrhu bez ITAR  
> * Plán kontroly technológií  
> * Register klasifikácie (13\_Registre-a-evidencie)

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

