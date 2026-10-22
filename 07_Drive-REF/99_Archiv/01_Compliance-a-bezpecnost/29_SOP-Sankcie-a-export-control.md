**SOP – Sankčný screening a exportná kontrola**

*IOTA Defence a.s. · štandardný operačný postup pre preverenie obchodu pred uzavretím, klasifikáciu položiek, end-user kontrolu, red flags a export clearance · vykonáva Politiku 18*  
IOTA Defence a.s. · IČO: \[DOPLNIŤ\] · Verzia 1.0 · Dátum: 6\. 10\. 2026 · Vypracoval: Márian Stančík · Klasifikácia: Interné – Dôverné · Stav: **NÁVRH**

| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. Postup je úplným návrhom vykonávacieho predpisu k [Politike 18 Sankcie a exportná kontrola](https://docs.google.com/document/d/1-BMetKsinxo-py1yhrMkOMB_5Ep7Nedzuo6O5mGEXHo/edit) (úlohy D11 ICP a D12 SOP screeningu). Nástroje, zoznamy, lehoty a kontakty sú zámerne \[DOPLNIŤ\]. Citácie predpisov (nariadenie (EÚ) 2021/821, zákon č. 39/2011 Z. z., zákon č. 392/2011 Z. z., zákon č. 289/2016 Z. z.) overí advokát podľa znenia účinného ku dňu schválenia. Postup nenahrádza individuálne posúdenie ECO ani stanovisko Ministerstva hospodárstva SR. |
| :---- |

# **Základné údaje**

---

| Položka | Hodnota |
| :---- | :---- |
| Číslo dokumentu | SOP-29 (nadväzuje na DD-POL-18; jednotné číslovanie po zmene obchodného mena \[DOPLNIŤ\]) |
| Vlastník postupu | Export Control Officer (ECO); v časti sankčného screeningu spoločne s Chief Compliance Officer (CCO) |
| Schvaľuje | Predstavenstvo IOTA Defence a.s. uznesením č. \[DOPLNIŤ\] |
| Na vedomie | Dozorná rada (štvrťročný report 2\. línie podľa [Rámca v1.1](https://docs.google.com/document/d/1fsKntU4A8GR40fjTRc5AxB8Z0OV1pydM5Vauuq9Z1ik/edit)) |
| Účinnosť | Dňom \[DOPLNIŤ\] (po schválení predstavenstvom a zaškolení dotknutých útvarov) |
| Revízia | Najmenej raz ročne; mimoriadne pri zmene sankčných režimov, kontrolných zoznamov, licenčných podmienok alebo po incidente |
| Adresáti | Obchod, Nákup, Logistika / Expedícia, Výroba a technický útvar (R\&D), Financie, Legal, ECO, CCO, CISO, Predstavenstvo |

# **1\. Účel a vzťah k ďalším dokumentom**

---

**1.1** Tento postup určuje záväzné kroky, ktoré musí spoločnosť vykonať **pred** každým obchodom, odoslaním, platbou alebo sprístupnením technológie, aby nedošlo k porušeniu medzinárodných sankcií alebo pravidiel exportnej kontroly výrobkov obranného priemyslu a položiek s dvojakým použitím.  
**1.2** Postup vykonáva [Politiku 18](https://docs.google.com/document/d/1-BMetKsinxo-py1yhrMkOMB_5Ep7Nedzuo6O5mGEXHo/edit) (najmä kap. 5.2 Klasifikácia, 5.3 Sankčný screening, 5.4 Licencie, 5.5 Koncový užívateľ, 5.6 Red flags a 5.7 Evidencia), nadväzuje na [Politiku 17 Third-Party Due Diligence](https://docs.google.com/document/d/1WNQSZZp4E0p_K-tCxHX7EyCVKdaGAE8rQB_cUFRpmLI/edit) a na poradie krokov v [schéme 07b Due diligence partnera v1.1](https://drive.google.com/file/d/1cV-uOqbk4XuPqQpVLUZ-7Gk8KWT2IMxl/view). Organizačné zaradenie ECO a CCO vychádza z [Rámca organizácie, compliance a bezpečnosti v1.1](https://docs.google.com/document/d/1fsKntU4A8GR40fjTRc5AxB8Z0OV1pydM5Vauuq9Z1ik/edit) a z [opisov pracovných miest 2\. línie (dok. 07\)](https://docs.google.com/document/d/1KvYwlYO2e6qD5Y4YOaPD4w4L_IaYZBQU-MjV3SWdBmU/edit); podpisové oprávnenia z [dok. 12 Limity schvaľovania a podpisový poriadok](https://docs.google.com/document/d/1EusiYKQM2AQxMK3GE3kIYbBa9b-zG0eCSZvQnh9cfi4/edit).  
**1.3** Pri rozpore medzi týmto postupom a Politikou 18 platí Politika 18; pri rozpore s právnym predpisom alebo podmienkou licencie platí predpis alebo licencia.

# **2\. Rozsah a spúšťače postupu**

---

**2.1** Postup sa uplatní vždy, keď nastane niektorá z týchto udalostí (ďalej „spúšťač“):

| \# | Spúšťač | Minimálne kroky SOP |
| :---- | :---- | :---- |
| S1 | Nový obchodný partner (zákazník, distribútor, agent, dodávateľ, subdodávateľ, partner v konzorciu) | Kroky 1–3 (zápis, screening, krajinové riziko) |
| S2 | Dopyt, ponuka alebo cenová kalkulácia pre zahraničného odberateľa alebo s dodaním mimo SR | Kroky 2–7 pred odoslaním ponuky |
| S3 | Uzavretie alebo zmena zmluvy, objednávky alebo rámcovej dohody | Kroky 2–9 (vrátane rozhodnutia ECO a zmluvných doložiek) |
| S4 | Fyzické odoslanie tovaru vrátane vzoriek, náhradných dielov, dočasného vývozu (výstava, test, oprava) a tranzitu | Krok 10 (pre-shipment kontrola) – 100 % zásielok |
| S5 | Prijatie alebo odoslanie platby, záloha, záruka, akreditív | Krok 11 (kontrola platby) |
| S6 | Nehmotný prenos technológie (e-mail, cloud, výkresy, softvér, technická pomoc, prístup zahraničnej osoby alebo návštevníka) | Kroky 4, 5 a 8 pred sprístupnením |
| S7 | Aktualizácia sankčných zoznamov, nový sankčný balík EÚ, zmena vlastníckej štruktúry alebo KUV partnera | Re-screening (krok 2\) celej databázy partnerov |
| S8 | Nový výrobok, zmena konštrukcie alebo nový dodávateľ komponentu s pôvodom mimo EÚ | Krok 4 (nová klasifikácia pred prvou ponukou) |

**2.2** Postup platí rovnako pre **predaj aj nákup**. Žiadna z udalostí S2 až S6 nesmie prebehnúť bez platného záznamu „export clearance“ v systéme \[DOPLNIŤ\].

# **3\. Definície a skratky**

---

| Pojem | Význam v tomto postupe |
| :---- | :---- |
| ECO | Export Control Officer – vlastník ICP a tohto postupu; má právo zastaviť transakciu (STOP-right). |
| CCO | Chief Compliance Officer – zodpovedá za sankčný screening spoločne s ECO a za integráciu s due diligence. |
| Export clearance | Písomný záznam ECO v systéme \[DOPLNIŤ\], že transakcia, zásielka alebo prenos môže pokračovať (SCHVÁLENÉ / SCHVÁLENÉ S PODMIENKAMI / STOP). |
| Strany transakcie | Zákazník, koncový užívateľ, príjemca tovaru (consignee), sprostredkovatelia, agent, prepravca a špeditér, banky, platiteľ, dodávateľ, ich KUV a osoby, ktoré ich vlastnia alebo ovládajú. |
| Potenciálna zhoda | Výsledok screeningu, keď sa meno, adresa alebo iný identifikátor zhoduje alebo podobá so záznamom na sankčnom zozname a zhodu nemožno hneď vylúčiť. |
| Potvrdená zhoda | Zhoda overená na základe ďalších identifikátorov (dátum narodenia, registračné číslo, adresa, štát), alebo vlastníctvo či kontrola sankcionovanou osobou. |
| Pravidlo 50 % | Subjekt vlastnený z 50 % alebo viac, alebo inak ovládaný sankcionovanou osobou sa posudzuje ako sankcionovaný (výklad EÚ aj OFAC – rozsah overí Legal). |
| EUC | End-User Certificate / vyhlásenie o konečnom použití a koncovom užívateľovi. |
| Catch-all | Povinnosť licencie aj pre nezaradenú položku, ak spoločnosť vie alebo bola informovaná, že položka je alebo môže byť určená na zakázané koncové použitie. |
| STOP-right | Oprávnenie ECO (a v sankčnej časti CCO) okamžite pozastaviť transakciu; zrušiť ho môže len predstavenstvo podľa kap. 8\. |
| ICP | Internal Compliance Programme – súbor postupov exportnej kontroly spoločnosti (Politika 18 a tento SOP). |

# **4\. Role a zodpovednosti (RACI)**

---

R \= vykonáva, A \= zodpovedá za výsledok, C \= konzultovaný, I \= informovaný.

| Činnosť | Obchod / Nákup | ECO | CCO | Legal | Financie | Logistika | Predstavenstvo | Dozorná rada |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Zápis partnera a podkladov | R | I | A | – | – | – | – | – |
| Sankčný screening a re-screening | C | R | A | C | C | – | I (pri zhode) | – |
| Krajinové riziko a embargá | C | A/R | C | C | – | – | – | – |
| Klasifikácia položky | C (technický útvar R) | A | – | C | – | – | – | – |
| Licenčné posúdenie a žiadosť MH SR | C | A/R | – | C | – | – | I | – |
| Získanie a overenie EUC | R | A | C | C | – | – | – | – |
| Vyhodnotenie red flags | R (hlási) | A | R | C | R (platby) | R (preprava) | – | – |
| Export clearance / STOP | I | A/R | C | C | I | I | – | – |
| Výnimka z interného postupu | – | C (stanovisko) | C (stanovisko) | C | – | – | A/R | I |
| Hlásenie orgánom, dobrovoľné oznámenie | – | R | R | R | – | – | A | I |
| Pre-shipment kontrola | – | A | – | – | – | R | – | – |
| Kontrola platby | – | C | C | – | A/R | – | – | – |
| Evidencia a uchovávanie | R | A | R | – | R | R | – | – |
| Štvrťročný report | – | R | R | – | – | – | I | I |

**4.1** ECO a CCO patria do 2\. línie ochrany a reportujú predstavenstvu cez gestora compliance; nesmú byť podriadení Obchodu, Nákupu, Výrobe ani Financiám. Pri podozrení proti členovi predstavenstva informujú priamo predsedu Dozornej rady.

# **5\. Prehľad procesu**

---

| Krok | Názov | Vlastník | Výstup / dôkaz | Lehota |
| :---- | :---- | :---- | :---- | :---- |
| 1 | Iniciácia a zápis „v preverovaní“ | Obchod / Nákup | Záznam v registri partnerov, dotazník partnera | Pred prvým rokovaním o podmienkach |
| 2 | Sankčný screening strán transakcie | CCO / ECO | Report nástroja, rozhodnutie o zhode | \[DOPLNIŤ\] prac. dní |
| 3 | Krajinové riziko a embargá | ECO | Záznam krajinového posúdenia | Spolu s krokom 2 |
| 4 | Klasifikácia položky | ECO \+ technický útvar | Klasifikačný záznam v ERP | Pred ponukou |
| 5 | Licenčné posúdenie | ECO | Licenčný záznam / žiadosť MH SR | Pred zmluvou |
| 6 | Koncový užívateľ a EUC | Obchod → ECO | Overený EUC | Pred zmluvou / pred odoslaním |
| 7 | Kontrola red flags | ECO (+ všetci) | Vyplnený kontrolný zoznam (Príloha C) | Priebežne |
| 8 | Rozhodnutie ECO – export clearance | ECO | SCHVÁLENÉ / S PODMIENKAMI / STOP | Pred podpisom zmluvy |
| 9 | Zmluva a doložky | Legal \+ Obchod | Podpísaná zmluva s doložkami | Pred aktiváciou partnera |
| 10 | Pre-shipment kontrola | Logistika \+ ECO | Kontrolný list zásielky, colné vyhlásenie | Pred každým odoslaním |
| 11 | Kontrola platby | Financie | Záznam o screeningu platby | Pred zaúčtovaním / odoslaním platby |
| 12 | Po vývoze: čerpanie licencie, hlásenia, archivácia | ECO | Protokol čerpania, hlásenie MH SR | Podľa licencie / \[DOPLNIŤ\] |

Poradie krokov 1 až 9 zodpovedá [schéme 07b](https://drive.google.com/file/d/1cV-uOqbk4XuPqQpVLUZ-7Gk8KWT2IMxl/view): partner je aktivovaný v stave „schválený“ až po podpise zmluvy a kladnom export clearance; do toho času nesmie byť vystavená objednávka, prijatá záloha ani udelená plná moc.

# **6\. Postup krok za krokom**

## ---

**Krok 1 – Iniciácia a zápis do registra partnerov**

> 1. Zamestnanec Obchodu alebo Nákupu, ktorý ako prvý vstupuje do kontaktu s partnerom, založí záznam v registri partnerov \[DOPLNIŤ\] so stavom **V PREVEROVANÍ**.  
> 2. Vyžiada od partnera dotazník: obchodné meno, sídlo, registračné číslo, krajina registrácie a pôsobenia, štatutári, koneční užívatelia výhod (KUV) a vlastnícka štruktúra až po fyzické osoby, banka a krajina účtu, predmet záujmu, deklarované koncové použitie a koncový užívateľ.  
> 3. Do ukončenia kroku 8 je prípustná len výmena neutajovaných, nekontrolovaných informácií pod NDA; technické údaje kontrolovaných položiek sa neposkytujú (zóna Dôverné podľa [schémy 05](https://drive.google.com/file/d/1reIAE5pKIrCx8LSJS0O9HLgr1AkkpgTF/view)).

## **Krok 2 – Sankčný screening**

> 1. CCO alebo ECO preverí **všetky strany transakcie** (kap. 3\) v nástroji \[DOPLNIŤ\] voči týmto zoznamom:  
   * **EÚ** – konsolidovaný zoznam osôb, skupín a subjektov podliehajúcich finančným sankciám EÚ a prílohy krajinových sankčných nariadení Rady (napr. nariadenie (EÚ) č. 269/2014, č. 833/2014, nariadenie (ES) č. 765/2006);  
   * **OSN** – konsolidovaný sankčný zoznam Bezpečnostnej rady OSN;  
   * **SR** – opatrenia vykonávané podľa zákona č. 289/2016 Z. z. o vykonávaní medzinárodných sankcií \[DOPLNIŤ\];  
   * **USA (awareness)** – OFAC SDN List a ďalšie zoznamy OFAC, BIS Entity List a ďalšie zoznamy BIS – povinne pri US mene (USD), US osobách, US komponentoch alebo technológii; dosah posúdi Legal;  
   * **Spojené kráľovstvo (awareness)** – OFSI Consolidated List pri UK nexus;  
   * ďalšie zoznamy podľa nástroja a rizika: \[DOPLNIŤ\].  
> 2. Nastavenie nástroja: fuzzy matching s prahom \[DOPLNIŤ\] %, transliterácia (azbuka, arabské písmo), kontrola aliasov; zoznamy sa aktualizujú automaticky \[DOPLNIŤ\] (min. denne).  
> 3. Výsledok sa vyhodnotí takto:

| Výsledok | Postup | Kto rozhoduje |
| :---- | :---- | :---- |
| Bez zhody | Záznam reportu nástroja k partnerovi; pokračuje sa krokom 3\. | CCO / ECO |
| Falošná zhoda (false positive) | Písomné zdôvodnenie (odlišný dátum narodenia, registračné číslo, krajina); schválenie druhou osobou (4 oči). | CCO \+ ECO |
| Potenciálna zhoda | **Okamžitý STOP** transakcie; doplnenie identifikátorov od partnera; rozhodnutie do \[DOPLNIŤ\] pracovných dní. Partnerovi sa neoznamuje dôvod preverovania (tipping-off). | CCO \+ ECO, konzultácia Legal |
| Potvrdená zhoda alebo vlastníctvo / kontrola sankcionovanou osobou (pravidlo 50 %) | **STOP** a stav ZAMIETNUTÝ; žiadne sprístupnenie finančných prostriedkov ani hospodárskych zdrojov; zmrazenie podľa sankčného predpisu; eskalácia na úroveň 3 (kap. 7); oznámenie príslušnému orgánu podľa posúdenia Legal \[DOPLNIŤ\]. | Predstavenstvo na návrh CCO, ECO a Legal |

> 4. Re-screening: automaticky pri každej aktualizácii zoznamov a min. \[DOPLNIŤ\] (týždenne) celej databázy aktívnych partnerov; mimoriadne pri spúšťači S7.

## **Krok 3 – Krajinové riziko a embargá**

> 1. ECO overí, či krajina zákazníka, koncového užívateľa, tranzitu alebo banky nepodlieha **zbrojnému embargu** EÚ alebo OSN, sektorovým sankciám alebo zákazom vývozu konkrétnych položiek.  
> 2. Krajiny sa zaradia do kategórií: **ZAKÁZANÉ** (bez rozhodnutia predstavenstva sa nepokračuje), **VYSOKÉ RIZIKO** (rozšírené preverenie, povinný vládny EUC, súhlas ECO a CCO), **ŠTANDARD**. Zoznam krajín vedie ECO: \[DOPLNIŤ\].  
> 3. Pri vývoze výrobkov obranného priemyslu ECO zdokumentuje posúdenie podľa kritérií Spoločnej pozície Rady 2008/944/SZBP (ľudské práva, vnútorná a regionálna stabilita, riziko presmerovania), ktoré sú podkladom aj pre licenčné konanie.

## **Krok 4 – Klasifikácia položky**

> 1. Každá položka (výrobok, komponent, náhradný diel, softvér, technická dokumentácia, technická pomoc) musí mať pred prvou ponukou klasifikáciu v kmeňových dátach ERP \[DOPLNIŤ\]:

| Kategória | Právny základ | Dôsledok |
| :---- | :---- | :---- |
| Výrobok obranného priemyslu (vojenský zoznam) | Zákon č. 392/2011 Z. z. o obchodovaní s výrobkami obranného priemyslu; Spoločný vojenský zoznam EÚ | Povolenie na obchodovanie a licencia MH SR na vývoz, dovoz, transfer, sprostredkovanie; vládny EUC |
| Položka s dvojakým použitím | Nariadenie (EÚ) 2021/821, Príloha I (kód položky); zákon č. 39/2011 Z. z. o výrobkoch s dvojakým použitím | Licencia na vývoz mimo EÚ (individuálna, globálna alebo všeobecná licencia EÚ / národná); pri položkách z Prílohy IV aj na transfer v rámci EÚ |
| Nekontrolovaná položka | – | Platí catch-all (krok 7\) a sankčné zákazy vývozu konkrétnych tovarov (napr. podľa nariadenia (EÚ) č. 833/2014) |
| Položka s US pôvodom alebo obsahom | US EAR (ECCN) / ITAR (USML) – awareness | Posúdenie re-exportu Legal a ECO; prípadne US povolenie |

> 2. Klasifikáciu navrhuje technický útvar na základe technických parametrov a potvrdzuje ECO podpisom v systéme; pri pochybnosti ECO požiada MH SR o stanovisko \[DOPLNIŤ\].  
> 3. Zmena konštrukcie, nový dodávateľ komponentu alebo nová verzia softvéru \= nové posúdenie klasifikácie.

## **Krok 5 – Licenčné posúdenie**

> 1. ECO určí, či je potrebné povolenie alebo licencia (vývoz, dovoz, transfer v EÚ, sprostredkovanie, technická pomoc, tranzit) a jej typ; podá žiadosť príslušnému orgánu (MH SR \[DOPLNIŤ\]) a eviduje lehotu konania.  
> 2. Licencia musí byť platná v deň odoslania alebo sprístupnenia; ECO eviduje jej podmienky (množstvo, hodnota, koncový užívateľ, krajina, doba platnosti, povinnosť hlásení) a čerpanie.  
> 3. Ponuka sa môže odoslať pred udelením licencie len s výhradou „podlieha udeleniu vývoznej licencie“ a so súhlasom ECO; zmluva musí obsahovať odkladaciu podmienku udelenia licencie (krok 9).  
> 4. Dočasný vývoz (výstava, test, oprava) a opätovný dovoz podliehajú rovnakému posúdeniu.

## **Krok 6 – Koncový užívateľ a EUC**

> 1. Obchod získa EUC alebo vyhlásenie o konečnom použití pri každom vývoze mimo EÚ, pri každom výrobku obranného priemyslu a pri rizikových transferoch v EÚ; pri výrobkoch obranného priemyslu do tretích krajín sa vyžaduje vládny EUC v predpísanej forme \[DOPLNIŤ\].  
> 2. ECO overí úplnosť podľa **Prílohy B**, konzistenciu so zmluvou a licenciou, oprávnenosť podpisujúcej osoby a pravosť dokumentu (napr. cez príslušný orgán krajiny určenia alebo zastupiteľský úrad \[DOPLNIŤ\]).  
> 3. Pri vývoze do tretích krajín sa do zmluvy zaradí zákaz reexportu bez súhlasu a doložka „No Russia“ v rozsahu podľa nariadenia (EÚ) č. 833/2014 a posúdenia Legal.  
> 4. Pri vysokom riziku ECO navrhne overenie po dodaní (post-shipment verification) a jeho právo zakotví zmluva.

## **Krok 7 – Kontrola red flags**

> 1. Každý zamestnanec, ktorý zistí red flag (**Príloha C**), ho bezodkladne ohlási ECO; Financie kontrolujú platobné red flags, Logistika prepravné.  
> 2. Pri red flag sa transakcia **zastaví** až do písomného vyriešenia. Vyriešenie musí byť doložené (nie len ústne ubezpečenie partnera).  
> 3. Ak spoločnosť vie alebo bola informovaná o možnom zakázanom koncovom použití (zbrane hromadného ničenia, vojenské použitie v krajine pod zbrojným embargom, porušovanie ľudských práv, kybersledovanie), uplatní sa **catch-all**: ECO zastaví transakciu a informuje MH SR \[DOPLNIŤ\].

## **Krok 8 – Rozhodnutie ECO (export clearance) a STOP-right**

> 1. ECO na základe krokov 2 až 7 zapíše do systému jedno z rozhodnutí: **SCHVÁLENÉ**, **SCHVÁLENÉ S PODMIENKAMI** (napr. licencia, doložka, overenie po dodaní) alebo **STOP**, so zdôvodnením a odkazom na dôkazy.  
> 2. **STOP-right:** rozhodnutie ECO o zastavení je záväzné pre všetky útvary. Obchod, Výroba, Financie ani vedúci zamestnanci ho nemôžu zmeniť ani obísť (napr. rozdelením zásielky, zmenou príjemcu alebo popisu tovaru).  
> 3. Proti rozhodnutiu STOP možno podať len písomný podnet na predstavenstvo podľa kap. 8; do rozhodnutia predstavenstva platí STOP.  
> 4. Pri sankčnom STOP (krok 2\) má rovnaké oprávnenie aj CCO.

## **Krok 9 – Zmluva a zmluvné doložky**

> 1. Legal zabezpečí v zmluve najmä: sankčné a exportné vyhlásenia partnera, povinnosť súčinnosti pri licenciách a EUC, zákaz reexportu, doložku „No Russia“ (ak sa uplatní), odkladaciu podmienku udelenia licencie, právo pozastaviť plnenie a odstúpiť pri sankčnej zhode alebo porušení, právo auditu a overenia po dodaní, ABAC doložku podľa [Politiky 16](https://docs.google.com/document/d/1gd80bWUa8dIHZoYfTLlBFb28WHJeA9V3Q43InO06Q1k/edit).  
> 2. Zmluvu podpisujú osoby podľa [dok. 12](https://docs.google.com/document/d/1EusiYKQM2AQxMK3GE3kIYbBa9b-zG0eCSZvQnh9cfi4/edit); bez záznamu export clearance ju nemožno predložiť na podpis.  
> 3. Po podpise CCO zmení stav partnera na **SCHVÁLENÝ** (schéma 07b, krok 6).

## **Krok 10 – Pre-shipment kontrola (každá zásielka)**

> 1. Logistika pred odoslaním overí: platný export clearance, aktuálny re-screening príjemcu, prepravcu a špeditéra, platnosť a voľný zostatok licencie, zhodu tovaru (kód, množstvo, hodnota, výrobné čísla) s licenciou a EUC, adresu dodania.  
> 2. Vývozné colné vyhlásenie obsahuje správnu klasifikáciu a odkaz na licenciu \[DOPLNIŤ\]; tovar nesmie byť označený zavádzajúco.  
> 3. Akýkoľvek nesúlad \= zásielka sa neodošle a vec sa vráti ECO.

## **Krok 11 – Kontrola platby**

> 1. Financie pred prijatím alebo odoslaním platby overia, že platiteľ alebo príjemca je strana zmluvy, banka a krajina účtu prešli screeningom a platba nevykazuje platobné red flags (platba od tretej osoby alebo z tretej krajiny, hotovosť, rozdelené platby).  
> 2. Pri nesúlade sa platba pozastaví a vec sa postúpi CCO; potvrdená sankčná zhoda \= zmrazenie prostriedkov podľa kroku 2\.

## **Krok 12 – Po vývoze**

> 1. ECO aktualizuje čerpanie licencie, podáva hlásenia a výkazy príslušným orgánom v lehotách podľa predpisov a licencie \[DOPLNIŤ\].  
> 2. Pri overení po dodaní ECO zaznamená výsledok; zistená diverzia \= incident, eskalácia podľa kap. 7 a posúdenie dobrovoľného oznámenia.  
> 3. Kompletný spis transakcie sa archivuje podľa kap. 9\.

# **7\. Eskalácia**

---

| Úroveň | Situácia | Kto rieši | Lehota | Informovanie |
| :---- | :---- | :---- | :---- | :---- |
| 1 | Falošná zhoda, chýbajúci podklad, nejasná klasifikácia, red flag s jasným vysvetlením | ECO / CCO | Do \[DOPLNIŤ\] pracovných dní | Žiadateľ (Obchod / Nákup) |
| 2 | Potenciálna zhoda, nevyriešený red flag, nejasná potreba licencie, US / UK nexus, podozrenie na catch-all | ECO \+ CCO \+ Legal, gestor compliance | Do \[DOPLNIŤ\] pracovných dní | Gestor compliance v predstavenstve |
| 3 | Potvrdená sankčná zhoda, catch-all, zistené alebo podozrivé porušenie, žiadosť o výnimku, nesúhlas s rozhodnutím STOP, kontakt s orgánom dozoru | **Predstavenstvo** na návrh ECO, CCO a Legal | Bezodkladne, najneskôr do \[DOPLNIŤ\] hodín od zistenia | **Dozorná rada** (predseda DR) – pri každom prípade úrovne 3; pri podozrení proti členovi predstavenstva CCO informuje priamo predsedu DR |

**7.1** O dobrovoľnom oznámení porušenia orgánu rozhoduje predstavenstvo na návrh Legal a ECO (Politika 18 kap. 5.8). Zamestnanec môže podozrenie oznámiť aj cez vnútorný systém podľa [Politiky 22 Whistleblowing](https://docs.google.com/document/d/1SlYSh3SuoFi9hEXB4qgpySmxLdZMmEyOmRbjpLyrJHw/edit) a je chránený pred odvetou.

# **8\. Výnimky**

---

**8.1** Výnimku z tohto postupu môže udeliť **výlučne predstavenstvo** uznesením, písomne, na dobu určitú, so zdôvodnením, kompenzačnými opatreniami a po písomnom stanovisku ECO a CCO; nesúhlasné stanovisko ECO alebo CCO sa prikladá k uzneseniu.  
**8.2** Výnimka sa môže týkať len interných procesných požiadaviek (napr. lehoty, forma dokladu). **Nemožno** udeliť výnimku zo zákonnej povinnosti, sankčného zákazu, licenčnej povinnosti ani z podmienky licencie.  
**8.3** Každá výnimka sa zapíše do registra výnimiek CCO a **predstavenstvo o nej informuje Dozornú radu** najneskôr v najbližšom štvrťročnom reporte; výnimky úrovne 3 bezodkladne.

# **9\. Evidencia a uchovávanie záznamov**

---

| Záznam | Kde sa vedie | Vlastník | Doba uchovávania |
| :---- | :---- | :---- | :---- |
| Reporty screeningu, rozhodnutia o zhode, zdôvodnenia falošných zhôd | Nástroj \[DOPLNIŤ\] \+ spis partnera | CCO | \[DOPLNIŤ\] rokov od skončenia vzťahu |
| Klasifikačné záznamy položiek | ERP \[DOPLNIŤ\] | ECO | Po dobu výroby \+ \[DOPLNIŤ\] rokov |
| Licencie, žiadosti, korešpondencia s MH SR, čerpanie | Spis ECO \[DOPLNIŤ\] | ECO | Najmenej podľa nariadenia (EÚ) 2021/821 (najmenej 5 rokov od konca kalendárneho roka vývozu – overí Legal) a zákona č. 392/2011 Z. z. \[DOPLNIŤ\]; interne min. \[DOPLNIŤ\] rokov |
| EUC a vyhlásenia o konečnom použití | Spis transakcie | ECO | Ako licencie |
| Kontrolné zoznamy red flags, export clearance, pre-shipment kontroly | Systém \[DOPLNIŤ\] | ECO / Logistika | Ako licencie |
| Colné a prepravné doklady, faktúry, platby | Účtovníctvo / Logistika | Financie | Podľa účtovných a colných predpisov \[DOPLNIŤ\], min. ako licencie |
| Uznesenia predstavenstva k výnimkám a úrovni 3 | Register výnimiek CCO | CCO | Trvalo / \[DOPLNIŤ\] |

**9.1** Záznamy sa vedú tak, aby boli úplné, nezmeniteľné (audit trail) a dohľadateľné pre kontrolu orgánu dozoru; technické dáta kontrolovaných položiek sa ukladajú len v zóne s riadeným prístupom podľa [schémy 05](https://drive.google.com/file/d/1reIAE5pKIrCx8LSJS0O9HLgr1AkkpgTF/view) a [Politiky 19](https://docs.google.com/document/d/1hrvT-LPIT3iGBI5UG46uMVUc5GYZzKCsdvWTaehKBYc/edit). Osobné údaje sa spracúvajú podľa [Politiky 23 GDPR](https://docs.google.com/document/d/1XknQE2F5Nq94idZttkMoobVAa0TocKIWtcYCFiCBBHQ/edit).

# **10\. Školenia, kontroly a reporting**

---

| Kontrola / činnosť | Frekvencia | Vlastník | Dôkaz |
| :---- | :---- | :---- | :---- |
| Export clearance pred každým odoslaním a prenosom (100 %) | Priebežne | ECO | Záznam v systéme |
| Re-screening databázy partnerov | Pri aktualizácii zoznamov, min. týždenne | CCO / ECO | Log nástroja |
| Zosúladenie čerpania licencií s expedíciami | Mesačne | ECO | Protokol |
| Vzorková kontrola spisov transakcií (úplnosť EUC, red flags, clearance) | Štvrťročne | CCO | Protokol vzorky |
| Školenie Obchod, Nákup, Logistika, R\&D, Financie | Ročne \+ pri nástupe | ECO | Evidencia účasti, test |
| Štvrťročný report ECO/CCO predstavenstvu a Dozornej rade (počet screeningov, zhody, STOP, výnimky, incidenty) | Štvrťročne | ECO \+ CCO | Report |
| Interný audit ICP | Ročne / podľa plánu DR | Interný audit | Správa |

# **11\. Súvisiace dokumenty**

---

| Dokument | Väzba |
| :---- | :---- |
| [18 Politika sankcií a exportnej kontroly](https://docs.google.com/document/d/1-BMetKsinxo-py1yhrMkOMB_5Ep7Nedzuo6O5mGEXHo/edit) | Nadradená politika – tento SOP ju vykonáva |
| [11 Rámec organizácia, compliance, bezpečnosť v1.1](https://docs.google.com/document/d/1fsKntU4A8GR40fjTRc5AxB8Z0OV1pydM5Vauuq9Z1ik/edit) | Organizácia 2\. línie, RACI, reporting DR |
| [Schéma 07b Due diligence partnera v1.1](https://drive.google.com/file/d/1cV-uOqbk4XuPqQpVLUZ-7Gk8KWT2IMxl/view) | Poradie krokov a stavy v registri partnerov |
| [17 Politika Third-Party Due Diligence](https://docs.google.com/document/d/1WNQSZZp4E0p_K-tCxHX7EyCVKdaGAE8rQB_cUFRpmLI/edit) | Preverenie partnerov a KUV |
| [16 Politika ABAC](https://docs.google.com/document/d/1gd80bWUa8dIHZoYfTLlBFb28WHJeA9V3Q43InO06Q1k/edit) | Agenti, provízie, doložky |
| [24 Politika AML/KYC](https://docs.google.com/document/d/12sNia9tROgrfoG5RJfIREmnR3t2wpVEaG68TxKI1LKI/edit) | Identifikácia partnerov a platobné kontroly |
| [20 Ochrana utajovaných skutočností](https://docs.google.com/document/d/1Uk9yJfED0-g_YbFufawhC9B0kb3e5PTseaqZAv_4TBk/edit) | Utajované zákazky a informácie |
| [25 Konzorciá a subdodávatelia](https://docs.google.com/document/d/1Sxy-ou7zFZusixlia8PaLuQH9RSDMw_1jwjJpd0TEak/edit) | Exportná kontrola v dodávateľskom reťazci |
| [07 Job descriptions (ECO, CCO)](https://docs.google.com/document/d/1KvYwlYO2e6qD5Y4YOaPD4w4L_IaYZBQU-MjV3SWdBmU/edit) | Postavenie a právomoci ECO a CCO |
| [12 Limity schvaľovania a podpisový poriadok](https://docs.google.com/document/d/1EusiYKQM2AQxMK3GE3kIYbBa9b-zG0eCSZvQnh9cfi4/edit) | Podpis zmlúv a schvaľovanie predaja |
| [Schéma 05 Dátové zóny](https://drive.google.com/file/d/1reIAE5pKIrCx8LSJS0O9HLgr1AkkpgTF/view) | Ochrana technických dát |
| Nariadenie (EÚ) 2021/821; zákon č. 39/2011 Z. z.; zákon č. 392/2011 Z. z.; zákon č. 289/2016 Z. z.; sankčné nariadenia Rady EÚ; Spoločná pozícia 2008/944/SZBP; odporúčanie Komisie (EÚ) 2019/1318 | Právny rámec (citácie overí advokát) |

# **Príloha A – Záznam o sankčnom screeningu (vzor)**

---

| Pole | Vyplní |
| :---- | :---- |
| ID transakcie / partnera | \[DOPLNIŤ\] |
| Preverené strany (meno, krajina, identifikátor) | \[DOPLNIŤ\] |
| Použitý nástroj a verzia zoznamov (dátum aktualizácie) | \[DOPLNIŤ\] |
| Zoznamy: EÚ / OSN / SR / OFAC / BIS / OFSI / iné | áno / nie / n.a. |
| Výsledok: bez zhody / falošná / potenciálna / potvrdená | \[DOPLNIŤ\] |
| Zdôvodnenie (pri zhode) | \[DOPLNIŤ\] |
| Vlastníctvo / kontrola (pravidlo 50 %) preverené | áno / nie |
| Vykonal (meno, funkcia, dátum) | \[DOPLNIŤ\] |
| Druhá kontrola – 4 oči (meno, dátum) | \[DOPLNIŤ\] |

# **Príloha B – Minimálny obsah EUC (kontrolný zoznam)**

---

| \# | Náležitosť | Splnené |
| :---- | :---- | :---- |
| 1 | Identifikácia vývozcu (IOTA Defence a.s., IČO \[DOPLNIŤ\]) | ☐ |
| 2 | Identifikácia koncového užívateľa a príjemcu (meno, adresa, krajina) | ☐ |
| 3 | Opis položky, klasifikácia, množstvo, hodnota – zhodné so zmluvou | ☐ |
| 4 | Konkrétne koncové použitie a miesto použitia | ☐ |
| 5 | Vyhlásenie o zákaze reexportu / transferu bez súhlasu (a pri vojenských položkách súhlasu orgánu krajiny vývozu) | ☐ |
| 6 | Vyhlásenie, že položky nebudú použité v súvislosti so zbraňami hromadného ničenia ani na zakázané účely | ☐ |
| 7 | Podpis oprávnenej osoby, dátum, pečiatka; pri vládnom EUC overenie príslušným orgánom | ☐ |
| 8 | Overenie pravosti a konzistencie vykonal ECO (meno, dátum) | ☐ |

# **Príloha C – Red flags (kontrolný zoznam)**

---

| Oblasť | Red flag | Áno / Nie |
| :---- | :---- | :---- |
| Koncové použitie | Zákazník nevie alebo odmieta uviesť koncové použitie alebo užívateľa; EUC neúplný alebo nekonzistentný | ☐ |
| Profil | Profil zákazníka nezodpovedá produktu alebo množstvu; nový zákazník bez histórie; prepojenie na sankcionované osoby | ☐ |
| Trasa | Neobvyklá trasa, tranzit cez krajiny známe obchádzaním sankcií; dodanie na sklad, špeditéra alebo do voľnej zóny | ☐ |
| Platba | Platba z tretej krajiny alebo od tretej osoby, v hotovosti, rozdelená; ochota zaplatiť nadštandardnú cenu | ☐ |
| Servis | Odmietnutie inštalácie, školenia alebo záručného servisu | ☐ |
| Dokumenty | Žiadosť o odstránenie výrobných čísel, zmenu popisu tovaru alebo HS kódu, nezvyčajné balenie či označenie | ☐ |
| Vlastníctvo | Nejasná vlastnícka štruktúra, nominee štruktúry, nedávna zmena KUV | ☐ |
| Iné | \[DOPLNIŤ\] | ☐ |

# **Schválenie a účinnosť**

---

| Funkcia | Meno | Podpis | Dátum |
| :---- | :---- | :---- | :---- |
| Vypracoval: Chief of Staff | Márian Stančík |  |  |
| Preskúmal: Export Control Officer (ECO) | \[DOPLNIŤ\] |  |  |
| Preskúmal: Chief Compliance Officer (CCO) | \[DOPLNIŤ\] |  |  |
| Preskúmal: Legal / advokát | \[DOPLNIŤ\] |  |  |
| Schválil: predseda predstavenstva | \[DOPLNIŤ\] |  |  |
| Schválil: člen predstavenstva – gestor compliance | \[DOPLNIŤ\] |  |  |
| Na vedomie: predseda Dozornej rady | \[DOPLNIŤ\] |  |  |

Postup nadobúda účinnosť dňom uvedeným v uznesení predstavenstva. Výklad poskytuje ECO; výnimky len podľa kap. 8\.

# **Správa dokumentu**

---

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý úplný návrh SOP (úlohy D11/D12 podľa [14 P0 STATUS](https://docs.google.com/document/d/1C93C6KPWHPYyP6G4vgxq5AcJ5HB0-klc3RQK_ByCgHo/edit)); obchodné meno IOTA Defence a.s. | NÁVRH – na právnu revíziu a schválenie predstavenstvom |

