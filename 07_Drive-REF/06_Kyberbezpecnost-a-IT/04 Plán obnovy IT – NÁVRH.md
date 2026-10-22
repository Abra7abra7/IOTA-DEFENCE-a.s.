**BCP / DR – kontinuita činností a obnova**

*IOTA Defence a.s. · rámec plánu kontinuity, obnovy po havárii, zálohovania a krízového riadenia*

IOTA Defence a.s. · Verzia 1.0 · Dátum: 6\. 10\. 2026 · Vypracoval: Márian Stančík · Klasifikácia: Interné – Dôverné · Stav: NÁVRH

| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. Rámec kontinuity činností (BCP) a obnovy po havárii (DR). Hodnoty RTO, RPO, MTPD, retencie, frekvencie a kontakty sú \[DOPLNIŤ\] – určí ich BIA a schváli predstavenstvo (rozhodnutie R9, uznesenie U-13). Referenčný rámec: ISO 22301, ISO/IEC 27001 (A.5.29–A.5.30, A.8.13). Utajované prostredie sa týmto dokumentom neriadi (kap. 9). |
| :---- |

 

# **1\. Účel, rozsah a vlastníctvo**

| Položka | Obsah |
| :---- | :---- |
| Účel | Zabezpečiť, aby kritické procesy IOTA Defence a.s. (výroba, dodávky, zmluvné záväzky v konzorciách, platby) pokračovali alebo boli obnovené v schválenom čase po narušení (kybernetický útok, výpadok IT, požiar, výpadok energie, nedostupnosť kľúčových osôb alebo dodávateľa). |
| Vlastník BCP | Predstavenstvo – gestor bezpečnosti \[DOPLNIŤ meno\] |
| Vlastník DR (IT) | CISO (A – štandard, test, dohľad); IT prevádzka (R – výkon zálohovania a obnovy) podľa U-06 |
| Rozsah | Lokality \[DOPLNIŤ\]; bežné IT (Google Workspace / M365 \[DOPLNIŤ\], ERP, CRM/register partnerov, internetbanking, súborové úložiská, koncové zariadenia); výrobné a OT systémy (CNC, PLC, testovacie zariadenia) \[DOPLNIŤ zoznam\]; kľúčoví dodávatelia; kľúčové osoby. |
| Mimo rozsahu | Utajované prostredie a utajované skutočnosti – samostatný plán v bezpečnostnej dokumentácii podľa NBÚ (kap. 9). |
| Revízia | Najmenej raz ročne, po každom cvičení, incidente alebo zásadnej zmene. |

 

# **2\. Analýza dopadov (BIA) – metodika**

> 1. Zoznam procesov a ich vlastníkov (workshop s Výrobou, Obchodom, Financiami, Nákupom, HR).  
> 2. Pre každý proces: dopady v čase (finančné, zmluvné – pokuty v konzorciách, regulačné, reputačné, bezpečnostné) pri výpadku 4 h / 1 deň / 3 dni / 1 týždeň \[časové pásma DOPLNIŤ podľa potreby\].  
> 3. Určenie MTPD (maximálne prípustné obdobie narušenia), RTO (cieľový čas obnovy) a RPO (maximálna prípustná strata dát).  
> 4. Závislosti: systémy, dáta, dodávatelia, osoby, priestory.  
> 5. Schválenie hodnôt predstavenstvom; ich premietnutie do štandardu záloh (kap. 4\) a zmlúv s dodávateľmi (SLA).

# **3\. Kritické procesy a systémy – ciele obnovy**

Zámerne bez čísel. Hodnoty vyplní BIA; stĺpec „Priorita obnovy“ je návrh poradia, ktorý BIA potvrdí alebo zmení.

| Proces / systém | Vlastník | Priorita obnovy (návrh) | MTPD | RTO | RPO | Závislosti |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Identita a prístup (IdP, MFA) | IT prevádzka | 1 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Bez IdP nefunguje nič; break-glass účty |
| E-mail a komunikácia | IT prevádzka | 1 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | IdP, DNS, mobilné telefóny |
| Internetbanking a platby | Financie | 2 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Token/podpisové zariadenia, 4-eyes, IBAN lock |
| ERP (objednávky, sklad, fakturácia) | Financie / Výroba | 2 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Databáza, licencie, dodávateľ ERP |
| Výroba – OT/CNC/PLC konfigurácie | Výroba | 2 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Zálohy konfigurácií, servis dodávateľa |
| Register partnerov / CRM / DD záznamy | CCO / Obchod | 3 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | SaaS dodávateľ, exporty |
| Exportné záznamy a licencie | ECO | 3 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Úložisko, registratúra |
| Súborové úložiská (zóny Interné, Dôverné) | IT prevádzka | 3 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Workspace / M365, SaaS záloha |
| eSchránka / slovensko.sk, komunikácia s úradmi | Legal / Financie | 3 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | KEP/eID čítačky, oprávnené osoby |
| Mzdy a HR | HR | 4 | \[DOPLNIŤ\] | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Externý mzdový dodávateľ \[DOPLNIŤ\] |
| Utajované prostredie | Bezpečnostný manažér | samostatne | podľa NBÚ | podľa NBÚ | podľa NBÚ | Kap. 9 – nikdy nie z bežných záloh |

 

# **4\. Politika zálohovania**

| Pravidlo | Požiadavka |
| :---- | :---- |
| Princíp | 3-2-1-1-0: najmenej 3 kópie dát, 2 rôzne médiá/platformy, 1 kópia mimo primárnej lokality, 1 kópia offline alebo nemenná (immutable), 0 chýb pri overení obnovy. |
| Rozsah | Servery a databázy (ERP), SaaS (Google Workspace / M365 – e-mail, disky; SaaS nezálohuje dáta za zákazníka v potrebnom rozsahu), CRM/register partnerov (export), konfigurácie sieťových prvkov, firewallov, IdP, OT/CNC/PLC, kľúčové koncové zariadenia podľa potreby. |
| Frekvencia | Podľa RPO z BIA: \[DOPLNIŤ\] pre každý systém v kap. 3\. |
| Retencia | \[DOPLNIŤ\] – podľa BIA, právnych požiadaviek (účtovné, daňové, exportné záznamy – lehoty prevziať z aktuálneho znenia predpisov) a GDPR (minimalizácia). |
| Šifrovanie | Zálohy šifrované pri prenose aj v pokoji; kľúče uložené oddelene od záloh; postup obnovy kľúčov zdokumentovaný (štandard šifrovania D17). |
| Oddelené prístupy | Zálohový systém mimo domény / tenantu produkcie; samostatné účty s MFA (FIDO2); žiadny bežný administrátor nesmie mazať nemennú kópiu; zmena retencie len 4-eyes. |
| Monitoring | Denná kontrola úspešnosti úloh; neúspešná záloha \= incident úrovne P3 (dokument 09 kap. 7), opakovaná \= P2. |
| Dodávatelia | Zmluva so správcom / poskytovateľom zálohovania obsahuje RPO/RTO, lokalitu dát (EÚ/EHP \[DOPLNIŤ\]), právo auditu, hlásenie incidentov. |
| Zakázané | Zálohy utajovaných skutočností v bežnom IT; zálohy na súkromné úložiská; zálohy bez šifrovania mimo areálu. |

 

# **5\. Testovanie obnovy – kadencia (návrh na schválenie)**

| Typ testu | Rozsah | Návrh frekvencie | Vykonáva / dohľad | Záznam |
| :---- | :---- | :---- | :---- | :---- |
| Kontrola úspešnosti záloh | Všetky úlohy | denne (automaticky) | IT prevádzka / CISO (mesačná kontrola) | Report zálohovacieho systému |
| Vzorová obnova súborov / poštových schránok | Náhodný výber | \[DOPLNIŤ\] (návrh: mesačne) | IT prevádzka / CISO | Záznam o teste obnovy |
| Obnova kritického systému | Systémy priority 1–2 rotačne | \[DOPLNIŤ\] (návrh: štvrťročne) | IT prevádzka / CISO | Záznam \+ dosiahnuté RTO/RPO |
| Úplný DR test / obnova z nemennej kópie | Scenár ransomvér | \[DOPLNIŤ\] (návrh: ročne) | IT prevádzka \+ CISO \+ vlastníci procesov | Správa z testu \+ nápravy |
| Tabletop cvičenie krízového štábu | Kyber \+ GDPR \+ utajované \+ výpadok lokality | \[DOPLNIŤ\] (návrh: ročne) | Gestor bezpečnosti | Zápis, poučenia |
| Test po zásadnej zmene | Dotknutý systém | po každej zmene | IT prevádzka | Záznam v change managemente |

 

**Záznam o teste obnovy obsahuje:** dátum, systém, zdroj zálohy (dátum zálohy), kto vykonal, dosiahnutý čas obnovy vs. RTO, strata dát vs. RPO, overenie integrity vlastníkom dát, odchýlky, nápravné opatrenia s termínom, podpis CISO.

# **6\. Krízové riadenie – roly**

| Rola | Kto (návrh) | Zástupca | Zodpovednosti |
| :---- | :---- | :---- | :---- |
| Vedúci krízového štábu | Gestor bezpečnosti (člen predstavenstva) | \[DOPLNIŤ\] | Aktivácia BCP, rozhodnutia o prioritách, výdavkoch v rámci limitu \[DOPLNIŤ\], komunikácia s dozornou radou a akcionármi. |
| Koordinátor obnovy IT | Vedúci IT prevádzky | \[DOPLNIŤ\] | Výkon DR runbookov, koordinácia dodávateľov IT. |
| Incident owner – kyber | CISO | \[DOPLNIŤ\] | Analýza, izolácia, zachovanie dôkazov, hlásenie NBÚ (ak v pôsobnosti). |
| Bezpečnosť utajovaných | Bezpečnostný manažér | \[DOPLNIŤ\] | Ochrana utajovaných skutočností, hlásenie NBÚ, samostatný plán. |
| Compliance / GDPR | CCO / DPO | \[DOPLNIŤ\] | Posúdenie porušenia ochrany osobných údajov (72 h), sankčné a zmluvné dopady. |
| Právo | Legal | \[DOPLNIŤ\] | Zmluvné povinnosti voči konzorciám a zákazníkom, poistenie, OČTK. |
| Prevádzka / Výroba | Vedúci výroby | \[DOPLNIŤ\] | Náhradné postupy výroby, priority zákaziek. |
| Financie | Finančný riaditeľ | \[DOPLNIŤ\] | Núdzové platby (len 4-eyes, žiadna zmena IBAN počas krízy bez overenia mimo pásma). |
| Komunikácia | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Interná a externá komunikácia, schválené vyhlásenia. |
| HR | Vedúci HR | \[DOPLNIŤ\] | Bezpečnosť a dostupnosť zamestnancov, náhradné pracovné režimy. |
| Zapisovateľ | \[DOPLNIŤ\] | \[DOPLNIŤ\] | Časová os, rozhodnutia, dôkazová stopa. |

 

# **7\. Komunikačný strom a eskalácia**

| Krok | Kto informuje | Koho | Kanál | Lehota |
| :---- | :---- | :---- | :---- | :---- |
| 1 | Ktokoľvek, kto zistí udalosť | Service desk / IT prevádzka a CISO; pri utajovaných Bezpečnostný manažér | Telefón \[DOPLNIŤ číslo\], nie len e-mail | Ihneď |
| 2 | CISO / Bezpečnostný manažér | Vedúci krízového štábu (gestor bezpečnosti) | Telefón, záložný kanál \[DOPLNIŤ – napr. Signal skupina mimo tenantu\] | Do \[DOPLNIŤ\] od klasifikácie |
| 3 | Vedúci krízového štábu | Krízový štáb (kap. 6); predseda predstavenstva | Konferenčný hovor / zvolanie | Do \[DOPLNIŤ\] |
| 4 | Vedúci krízového štábu | Predseda dozornej rady | Telefón | Pri incidente úrovne P1 bezodkladne |
| 5 | CISO / DPO / Bezp. manažér / Legal | Orgány: NBÚ (kyber, utajované), ÚOOÚ SR (osobné údaje), OČTK (trestný čin) | Podľa predpisov (dokument 09 kap. 9\) | Zákonné lehoty |
| 6 | Legal / Obchod | Zákazníci, konzorciá, dodávatelia podľa zmlúv | Podľa zmlúv | Zmluvné lehoty \[DOPLNIŤ\] |
| 7 | Komunikácia | Zamestnanci, médiá (len schválené vyhlásenie) | Intranet / SMS / tlačové vyhlásenie | Podľa rozhodnutia štábu |

 

**Kontaktný list** (mená, mobilné čísla, zástupcovia, dodávatelia IT, banka, poisťovňa, NBÚ, ÚOOÚ SR) sa vedie v zóne Dôverné a **v tlačenej podobe** u členov krízového štábu – musí byť dostupný aj pri výpadku e-mailu a cloudu. Aktualizácia \[DOPLNIŤ frekvencia\].

# **8\. Postupy obnovy bežného IT (DR runbooky – osnova)**

## **8.1 Ransomvér / rozsiahla kompromitácia**

> 1. Izolovať: odpojiť postihnuté segmenty a zariadenia od siete (nevypínať, ak sa zachovávajú dôkazy – rozhodne CISO).  
> 2. Zablokovať kompromitované účty, resetovať privilegované heslá a tokeny (break-glass účty overiť).  
> 3. Aktivovať krízový štáb, posúdiť hlásenia (NBÚ, ÚOOÚ SR, OČTK) a lehoty.  
> 4. Zachovať dôkazy: logy (dokument 09), obrazy diskov, vzorky; reťazec dôkazov.  
> 5. Overiť čistotu záloh (nemenná kópia, dátum pred kompromitáciou), pripraviť čisté prostredie.  
> 6. Obnoviť v poradí priorít (kap. 3): IdP → sieť/DNS → e-mail → platby → ERP → ostatné.  
> 7. Overiť integritu dát s vlastníkmi; pred návratom do prevádzky skenovanie a monitoring zvýšenej úrovne.  
> 8. Poincidentná analýza, nápravné opatrenia, report predstavenstvu a DR.

## **8.2 Výpadok identity (IdP) / tenantu**

> 1. Overiť stav poskytovateľa (status page) a rozsah.  
> 2. Použiť break-glass účty (FIDO2, uložené v trezore, použitie zaznamenať).  
> 3. Prepnúť na záložnú komunikáciu (kap. 7).  
> 4. Po obnove: revízia logov z obdobia výpadku, rotácia break-glass poverení.

## **8.3 Výpadok ERP / internetbankingu**

> 1. Prepnúť na náhradný postup: manuálna evidencia objednávok a príjmu na formulároch \[DOPLNIŤ\].  
> 2. Platby len kritické, so 4-eyes; zákaz zmeny IBAN počas výpadku.  
> 3. Obnova podľa RTO; spätné zaúčtovanie a reconciliácia s overením Financiami.

## **8.4 Kompromitácia e-mailu (BEC)**

> 1. Zablokovať účet, odvolať relácie a tokeny, skontrolovať pravidlá presmerovania.  
> 2. Okamžite upozorniť Financie: zastaviť platby na nové / zmenené IBAN, overiť telefonicky na známom čísle.  
> 3. Zistiť, či došlo k úniku osobných údajov alebo exportne kontrolovaných technológií (ECO, DPO).  
> 4. Informovať dotknutých partnerov podľa rozhodnutia štábu.

## **8.5 Výpadok lokality / výroby**

> 1. Bezpečnosť osôb na prvom mieste (evakuácia podľa požiarneho poriadku).  
> 2. Náhradné pracovisko \[DOPLNIŤ\] / práca na diaľku pre administratívu.  
> 3. Výroba: priority zákaziek, informovanie zákazníkov a konzorcií, záložní dodávatelia (AVL).

# **9\. Utajované prostredie – osobitný režim**

| Utajované prostredie je fyzicky a logicky oddelené (air-gapped) a nie je súčasťou tohto BCP/DR. Pre utajované skutočnosti platí: kontinuita a obnova sa riadia výlučne bezpečnostnou dokumentáciou schválenou podľa zákona č. 215/2004 Z. z. a požiadaviek NBÚ (vrátane bezpečnostného projektu technického prostriedku, ak bude certifikovaný); zálohy utajovaných dát sa nikdy neukladajú v bežnom IT, cloude ani u bežného zálohovacieho dodávateľa; médiá sa evidujú a uchovávajú v chránenom priestore; bežný krízový štáb dostáva o udalosti v utajovanom prostredí len neutajovanú informáciu; riadi Bezpečnostný manažér; do certifikácie utajovaného prostredia platí, že sa utajované skutočnosti elektronicky nespracúvajú (len listinný režim); podrobnosti sa v Google Drive neuvádzajú. |
| :---- |

 

# **10\. RACI – BCP/DR**

| Činnosť | Predstavenstvo | Gestor bezp. | CISO | IT prevádzka | Vlastníci procesov | Bezp. manažér | CCO/DPO |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Schválenie BCP a RPO/RTO | A | R | C | C | C | I | I |
| BIA | I | A | R | C | R | I | C |
| Štandard zálohovania | I | I | A | R | C | — | I |
| Výkon záloh a obnovy | — | I | C (dohľad) | A/R | I | — | — |
| Testy obnovy | I | I | A | R | C (overenie dát) | — | — |
| Aktivácia krízového štábu | I | A/R | R | C | C | C | C |
| Utajované prostredie – kontinuita | I | I | — | — | — | A/R | — |
| Cvičenia | I | A | R | R | R | R | R |

 

# **11\. Otvorené body**

> * BIA a schválené hodnoty RTO/RPO/MTPD (R9).  
> * Zoznam OT/výrobných systémov a ich záloh.  
> * Kontaktný list a záložný komunikačný kanál.  
> * Zmluvy s dodávateľmi IT/zálohovania so SLA.  
> * Prvý zdokumentovaný test obnovy (podmienka uzavretia P0 – audit kap. 8, výstup 7).  
> * Náhradné pracovisko.

# **Správa dokumentu**

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý návrh rámca BCP/DR, zálohovania a testov obnovy | NÁVRH – na posúdenie predstavenstvom, právnu a bezpečnostnú revíziu |

 