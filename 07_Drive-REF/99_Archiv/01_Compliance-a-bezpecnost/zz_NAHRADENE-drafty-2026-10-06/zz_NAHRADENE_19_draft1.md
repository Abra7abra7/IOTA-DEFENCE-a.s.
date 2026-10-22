**Politika informačnej bezpečnosti**

*Delta Defence a.s. · ISMS v duchu ISO/IEC 27001 · povedomie o NIS2 · klasifikácia informácií · MFA*  
Delta Defence a.s. · Verzia 1.0 · Dátum: 6\. 10\. 2026 · Vypracoval: Márian Stančík · Klasifikácia: Interné – Dôverné · Stav: **NÁVRH**

| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. Text je úplným návrhom politiky na schválenie predstavenstvom. Limity, mená, lehoty a sumy sú zámerne \[DOPLNIŤ\] / \[DOPLNIŤ EUR\]. Citácie predpisov overí advokát podľa znenia účinného ku dňu schválenia. Politika je súčasťou systému podľa [Rámca v1.1](https://docs.google.com/document/d/1tREEdndg7Vqy-VBGkGJrPrB0vI7eSF62PHuHcuDjaNs/edit). Pôsobnosť zákona č. 69/2018 Z. z. o kybernetickej bezpečnosti v znení zákona č. 366/2024 Z. z. (transpozícia NIS2) sa posúdi v úlohe D05; politika je navrhnutá tak, aby obstála v oboch prípadoch. Utajované skutočnosti sa riadia osobitne Politikou 20\. |
| :---- |

# **Základné údaje**

---

| Položka | Hodnota |
| :---- | :---- |
| Číslo dokumentu | DD-POL-19 |
| Vlastník politiky | CISO (A); IT prevádzka vykonáva (R) podľa U-06 |
| Schvaľuje | Predstavenstvo Delta Defence a.s. uznesením č. \[DOPLNIŤ\] |
| Na vedomie | Dozorná rada (štvrťročný report 2\. línie podľa [Rámca v1.1](https://docs.google.com/document/d/1tREEdndg7Vqy-VBGkGJrPrB0vI7eSF62PHuHcuDjaNs/edit) kap. 1.4) |
| Účinnosť | Dňom \[DOPLNIŤ\] (po schválení predstavenstvom) |
| Revízia | Najmenej raz ročne a pri podstatnej zmene právnej úpravy, obchodného modelu alebo po závažnom incidente |
| Klasifikácia | Interné – určené všetkým zamestnancom a dotknutým tretím stranám |

# **1\. Účel**

---

Chrániť dôvernosť, integritu a dostupnosť informácií a systémov spoločnosti, zákazníkov a partnerov; stanoviť minimálne záväzné bezpečnostné pravidlá a vytvoriť základ systému riadenia informačnej bezpečnosti (ISMS) podľa ISO/IEC 27001:2022.

# **2\. Rozsah**

---

Všetky informácie v akejkoľvek forme, informačné a komunikačné systémy, cloudové služby, koncové zariadenia (vrátane súkromných zariadení používaných na prácu – BYOD), výrobné a OT systémy, priestory a všetky osoby s prístupom (zamestnanci, externisti, dodávatelia, externý IT správca).Rozsah ISMS na účely certifikácie určí predstavenstvo (U-13, R7).

# **3\. Definície**

---

| Pojem | Význam |
| :---- | :---- |
| Aktívum | Informácia, systém, zariadenie alebo služba s hodnotou pre spoločnosť; má určeného vlastníka. |
| MFA | Viacfaktorová autentifikácia – minimálne dva nezávislé faktory; uprednostňujú sa faktory odolné voči phishingu (FIDO2/kľúče, passkeys). |
| Privilegovaný účet | Účet s administrátorskými právami; spravuje sa v režime PAM/JIT, break-glass účty sú zapečatené a monitorované. |
| Bezpečnostný incident | Udalosť, ktorá ohrozuje alebo narušila dôvernosť, integritu alebo dostupnosť informácií (podrobne [dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit)). |
| Zóna | Logické prostredie podľa [schémy 05 Dátové zóny](https://drive.google.com/file/d/18dzCOe1RYn7n4GpjySAi9Sz7gk9bVeQf/view) (napr. Verejné, Interné, Dôverné, Prísne dôverné / technické dáta). |

# **4\. Pravidlá**

## ---

**4.1 Klasifikácia informácií (neutajované)**

| Trieda | Príklady | Minimálne pravidlá |
| :---- | :---- | :---- |
| VEREJNÉ | Web, katalóg schválený na zverejnenie | Zverejniť len so schválením marketingu a ECO (technické údaje) |
| INTERNÉ | Interné predpisy, organizačné informácie | Len pre zamestnancov a zmluvných partnerov; firemné nástroje |
| DÔVERNÉ | Ponuky, ceny, zmluvy, osobné údaje, finančné dáta, dáta zákazníkov | Need-to-know, šifrovanie pri prenose a uložení, zákaz súkromných úložísk, označenie dokumentu, zdieľanie len s menovitými osobami |
| PRÍSNE DÔVERNÉ | Technická dokumentácia kontrolovaných položiek, know-how, bezpečnostná architektúra, M\&A | Ako DÔVERNÉ \+ osobitná zóna, schválený zoznam osôb, DLP, logovanie prístupov, posúdenie ECO pred sprístupnením zahraničnej osobe |

**Utajované skutočnosti** (Vyhradené až Prísne tajné, NATO/EÚ) nie sú triedou tejto schémy a **nesmú sa spracúvať v bežných IT systémoch** – výlučne podľa [Politiky 20](https://drive.google.com/drive/folders/1KR6yWpbcPSXMf7ShKL2XWJjclu36Obr0). Vlastník informácie určí triedu pri vzniku; pri pochybnosti sa použije vyššia trieda.

## **4.2 Riadenie prístupu a MFA**

**4.2.1** Prístupy sa prideľujú podľa princípu najnižších oprávnení a need-to-know, na základe žiadosti schválenej vlastníkom aktíva; zriadenie a zrušenie vykonáva IT prevádzka ([Onboarding a prístupy](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit)).  
**4.2.2** **MFA je povinná** pre: všetky účty v cloude a e-maile, vzdialený prístup (VPN, VDI), privilegované účty, ERP, internetbanking, prístupy externých dodávateľov. Pre privilegované účty a zónu PRÍSNE DÔVERNÉ sa vyžaduje phishing-odolná MFA.  
**4.2.3** Zdieľané účty sú zakázané (okrem technických so schválením CISO a trezorom hesiel). Heslá: min. \[DOPLNIŤ\] znakov, správca hesiel, žiadne opakovanie.  
**4.2.4** Privilegované prístupy len cez PAM/JIT so záznamom relácií; break-glass účty podľa [dok. 09 kap. 3–4](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit).  
**4.2.5** Preskúmanie prístupov: bežné ročne, privilegované štvrťročne; zrušenie prístupov pri odchode v deň ukončenia.

## **4.3 Koncové zariadenia a prijateľné používanie**

**4.3.1** Len spravované zariadenia so šifrovaním disku, EDR, aktualizáciami a uzamknutím obrazovky; BYOD len pre e-mail/kalendár cez MDM s oddelením firemných dát.  
**4.3.2** Zakázané: inštalácia neschváleného softvéru, vypínanie bezpečnostných nástrojov, USB médiá bez schválenia, ukladanie DÔVERNÝCH dát do súkromných úložísk, vkladanie firemných dát do neschválených AI nástrojov.  
**4.3.3** Pri ceste do vysokorizikových krajín \[DOPLNIŤ\] sa používajú „cestovné“ zariadenia bez citlivých dát podľa pokynu CISO.

## **4.4 Bezpečnosť prevádzky**

**4.4.1** Záplaty: kritické do \[DOPLNIŤ\] dní, ostatné do \[DOPLNIŤ\] dní; výnimky schvaľuje CISO.  
**4.4.2** Zálohy podľa pravidla 3-2-1-1-0 a pravidelné testy obnovy – [dok. 08 BCP/DR](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit).  
**4.4.3** Logovanie a monitoring (SIEM, P1–P4) – [dok. 09](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit); logy sú chránené proti zmene.  
**4.4.4** Segmentácia sietí; OT/výrobné systémy oddelené od kancelárskej siete; vzdialený prístup dodávateľov len cez schválený kanál.  
**4.4.5** Zmeny v produkčných systémoch len cez riadený proces zmien so schválením.

## **4.5 Dodávatelia a cloud**

**4.5.1** Dodávateľ s prístupom k dátam DÔVERNÉ a vyššie alebo k systémom prechádza posúdením CISO (súčasť DD podľa [Politiky 17](https://drive.google.com/drive/folders/1KR6yWpbcPSXMf7ShKL2XWJjclu36Obr0)); zmluva obsahuje bezpečnostné požiadavky, hlásenie incidentov, audit, umiestnenie dát a exit.  
**4.5.2** Dáta PRÍSNE DÔVERNÉ sa ukladajú len v EÚ/EHP a len u schválených poskytovateľov \[DOPLNIŤ\].

## **4.6 Vývoj a technické dáta**

**4.6.1** Bezpečný vývoj (code review, správa tajomstiev, skenovanie závislostí) pre interný softvér a firmvér; repozitáre s technickými dátami v zóne PRÍSNE DÔVERNÉ.

## **4.7 Incidenty a hlásenia**

**4.7.1** Každý zamestnanec hlási podozrenie na incident (phishing, strata zariadenia, neobvyklé správanie systému) **okamžite** na \[DOPLNIŤ\]. Neohlásenie je porušením politiky; nahlásenie vlastnej chyby sa nesankcionuje.  
**4.7.2** Postup a lehoty: [schéma 08b](https://drive.google.com/file/d/1J_0XgArJD_RQPz1hAMeNjCR0-6LrbqpU/view) a jednotná tabuľka lehôt [dok. 09 kap. 9](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit) (NBÚ 24 h / 72 h / 1 mesiac, ak je spoločnosť v pôsobnosti NIS2; ÚOOÚ 72 h pri osobných údajoch).

## **4.8 NIS2 a zodpovednosť vedenia**

**4.8.1** Ak spoločnosť spadá do pôsobnosti zákona č. 69/2018 Z. z. (posúdenie D05), predstavenstvo schvaľuje opatrenia riadenia kybernetických rizík, dohliada na ich zavedenie a jeho členovia absolvujú školenie z kybernetickej bezpečnosti; spoločnosť si splní registračné a oznamovacie povinnosti voči NBÚ.  
**4.8.2** Bez ohľadu na pôsobnosť sa minimálne opatrenia (riadenie rizík, MFA, zálohy, incident management, bezpečnosť dodávateľského reťazca, školenia, kryptografia) zavedú ako dobrá prax a požiadavka zákazníkov z obranného sektora.

# **5\. Školenia a povedomie**

---

Povinné úvodné školenie pri nástupe a ročné školenie; phishingové simulácie najmenej \[DOPLNIŤ\]-krát ročne; osobitné školenie pre administrátorov a predstavenstvo.

# **6\. Role a zodpovednosti**

---

| Rola | Zodpovednosť |
| :---- | :---- |
| Predstavenstvo | Schvaľuje politiku, rizikový apetít a zdroje; pri pôsobnosti NIS2 nesie zodpovednosť za opatrenia riadenia rizík. |
| CISO (2. línia, A) | Vlastník politiky a ISMS; štandardy, posúdenie rizík, dohľad, testovanie kontrol, výnimky, vedenie incidentu a hlásenia; nemá trvalé privilegované účty (U-06). |
| IT prevádzka / externý správca (1. línia, R) | IAM, MFA, zálohy, záplaty, EDR, logovanie, segmentácia, zmeny. |
| Vlastníci aktív | Klasifikácia, schvaľovanie prístupov, ročné preskúmanie. |
| Bezpečnostný manažér | Rozhranie na utajované skutočnosti a fyzickú bezpečnosť. |
| DPO | Rozhranie na osobné údaje. |
| Každý používateľ | Dodržiava pravidlá, hlási incidenty. |

# **7\. Kontroly a monitoring**

---

| Kontrola | Frekvencia | Vlastník | Dôkaz / záznam |
| :---- | :---- | :---- | :---- |
| Pokrytie MFA (cieľ 100 % povinných systémov) | Mesačne | IT prevádzka / CISO | Report IAM |
| Preskúmanie prístupov | Ročne / privilegované štvrťročne | Vlastníci aktív, IT prevádzka; dohľad CISO | Podpísané protokoly |
| Stav záplat a EDR | Mesačne | IT prevádzka | Report |
| Test obnovy zo záloh | Podľa dok. 08 | IT prevádzka / CISO | Protokol testu |
| Phishingová simulácia | \[DOPLNIŤ\]× ročne | CISO | Výsledky |
| Skenovanie zraniteľností / penetračný test | Štvrťročne / ročne | CISO | Správa |
| Interný audit ISMS | Ročne | Interný audit / CISO | Správa |

# **8\. Porušenie politiky a sankcie**

---

Porušenie tejto politiky sa posudzuje podľa závažnosti, úmyslu, opakovania, spôsobenej škody a súčinnosti dotknutej osoby. Skutočnosť, že porušenie bolo „v záujme spoločnosti“ alebo na pokyn nadriadeného, nie je ospravedlnením.

| Osoba | Možné opatrenia |
| :---- | :---- |
| Zamestnanec | Porušenie pracovnej disciplíny podľa zákona č. 311/2001 Z. z. Zákonník práce: písomné upozornenie, zníženie alebo nepriznanie pohyblivej zložky mzdy podľa vnútorného predpisu \[DOPLNIŤ\], výpoveď alebo pri závažnom porušení okamžité skončenie pracovného pomeru; náhrada spôsobenej škody v rozsahu Zákonníka práce. |
| Vedúci zamestnanec | Ako zamestnanec; navyše zodpovednosť za nedostatočný dohľad, ak porušenie umožnil, toleroval alebo neohlásil. |
| Člen predstavenstva | Posúdenie dozornou radou a valným zhromaždením podľa stanov \[DOPLNIŤ\]: odvolanie z funkcie, zodpovednosť za škodu podľa Obchodného zákonníka (§ 194), nepriznanie odmeny. |
| Externý spolupracovník, agent, dodávateľ, partner | Zmluvné sankcie podľa compliance doložky: pozastavenie plnenia a platieb, zmluvná pokuta \[DOPLNIŤ EUR\], odstúpenie od zmluvy alebo jej okamžité ukončenie, zaradenie do stavu ZAMIETNUTÝ v registri partnerov. |
| Všetci | Ak porušenie môže napĺňať znaky trestného činu alebo správneho deliktu, Legal posúdi oznámenie orgánom činným v trestnom konaní alebo príslušnému orgánu; spoločnosť si vyhradzuje uplatnenie nároku na náhradu škody. |

> * Úmyselné obchádzanie bezpečnostných opatrení (vypnutie EDR, zdieľanie hesla, export dát) je závažné porušenie; CISO môže okamžite pozastaviť prístup.

Disciplinárne opatrenie navrhuje vedúci zamestnanec s HR po stanovisku CCO (pri utajovaných skutočnostiach Bezpečnostný manažér, pri IT CISO); o opatrení voči členovi predstavenstva rozhoduje orgán podľa stanov. **Za porušenie sa nepovažuje** odmietnutie konania, ktoré by porušilo túto politiku, ani oznámenie podozrenia v dobrej viere – takáto osoba je chránená podľa [Politiky 22 Whistleblowing](https://drive.google.com/drive/folders/1KR6yWpbcPSXMf7ShKL2XWJjclu36Obr0).

# **9\. Súvisiace dokumenty a právny rámec**

---

| Dokument | Väzba |
| :---- | :---- |
| [08 BCP/DR](https://docs.google.com/document/d/1HNOq-cDTeJ6m0i8S75VeGqGTrc4RIMG1eRolCfBneXE/edit) · [09 Logovanie a monitoring](https://docs.google.com/document/d/1ECV6dK_5veXzHxN8O4KrBGDjn1X4-zTx9jDDlvBH7Qs/edit) · [Schéma 08b Incident response](https://drive.google.com/file/d/1J_0XgArJD_RQPz1hAMeNjCR0-6LrbqpU/view) | Prevádzkové štandardy |
| [Technologický stack](https://docs.google.com/document/d/1kF7lRDtN74uFgo2XYpCqU7BDmXPNpXKKjMfddlxgK0w/edit) · [Onboarding a prístupy](https://docs.google.com/document/d/1yhK0ReIa0lRzAhsshYqiuY_QenGatRn964p4MYRBHCw/edit) · [Schéma 05 Dátové zóny](https://drive.google.com/file/d/18dzCOe1RYn7n4GpjySAi9Sz7gk9bVeQf/view) | Nástroje a prístupy |
| [20 Utajované skutočnosti](https://drive.google.com/drive/folders/1KR6yWpbcPSXMf7ShKL2XWJjclu36Obr0) · [23 GDPR](https://drive.google.com/drive/folders/1KR6yWpbcPSXMf7ShKL2XWJjclu36Obr0) · [07 JD CISO](https://docs.google.com/document/d/1dGiRAkzxfogUno00VR0eU2j5EbKVYDfLaq16odA1LgY/edit) | Súvisiace |
| Zákon č. 69/2018 Z. z. v znení zákona č. 366/2024 Z. z.; smernica (EÚ) 2022/2555 (NIS2); ISO/IEC 27001:2022, ISO/IEC 27002:2022 | Právny a normatívny rámec |
| [11 Rámec organizácia, compliance, bezpečnosť v1.1](https://docs.google.com/document/d/1tREEdndg7Vqy-VBGkGJrPrB0vI7eSF62PHuHcuDjaNs/edit) | Nadradený rámec – organizácia, 3 línie, RACI, osnova politík (kap. 5\) |
| [26 INDEX politík](https://drive.google.com/drive/folders/1KR6yWpbcPSXMf7ShKL2XWJjclu36Obr0) | Zoznam všetkých politík a ich stav |

# **10\. Schválenie a účinnosť**

---

| Funkcia | Meno | Podpis | Dátum |
| :---- | :---- | :---- | :---- |
| Predseda predstavenstva | \[DOPLNIŤ\] |  |  |
| Člen predstavenstva – gestor compliance | \[DOPLNIŤ\] |  |  |
| Člen predstavenstva – gestor bezpečnosti | \[DOPLNIŤ\] |  |  |
| Na vedomie: predseda dozornej rady | \[DOPLNIŤ\] |  |  |

Výklad politiky poskytuje vlastník politiky. Výnimky z politiky môže udeliť len predstavenstvo písomne, na dobu určitú a s kompenzačnými opatreniami; každá výnimka sa eviduje v registri výnimiek CCO a reportuje dozornej rade.

# **Správa dokumentu**

---

| Verzia | Dátum | Autor | Popis zmeny | Stav |
| :---- | :---- | :---- | :---- | :---- |
| 1.0 | 6\. 10\. 2026 | Márian Stančík | Prvý úplný návrh textu politiky (úloha D04 podľa [14 P0 STATUS](https://docs.google.com/document/d/1Av6agRJX-ekdOGWSkGOKlRhQrmUKUUypTWc4NG102VY/edit)) | NÁVRH – na právnu revíziu a schválenie predstavenstvom |

