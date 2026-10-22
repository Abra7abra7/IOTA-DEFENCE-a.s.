# WORKFLOWS DOPLNKOVÉ V2 (FC-25 až FC-35) — Zostávajúce procesy firmy

**IOTA Defence a.s. · 22.10.2026 · NÁVRH v1.0 · Interné – Dôverné · Každý proces: workflow → RACI → log → KPI. Diagramy: .archify/*.html + PNG.**

> Kompletné zatvorenie gap analýzy — po týchto 11 procesoch je **mapa 61/61 procesov pokrytá** (text + diagram).

---

## FC-25 · ODMENOVANIE A VÝPLATY

**Účel:** Odmena, zrážky, výplata a evidencia miezd — v súlade so Zákonníkom práce, daňami a limitmi schvaľovania. Komisia mzdy je dôvernejší proces (Z2).

**Právny základ:** z. 311/2001 (mzda, §118-126), z. 595/2003 (daň), z. 461/2003 (sociálne a zdravotné poistenie), z. 91/2016 (dokumentácia miezd = register).

**Zodpovednosti:** HR (R), mzdová účtovníčka (R), CFO (A), manažéri línie (C), CCO (C kontrola odmien gestorov — nesmú závisieť od obratu).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Podklady: dochádzka, odmeny, príplatky, výdavky | HR/IT | Podklad |
| 2 | Výpočet mzdy + odvodov | mzdy | Mzdový list |
| 3 | Schválenie mzdového listu (CFO) | CFO | Sign-off |
| 4 | Kontrola CCO (len pre gestorov 2.línie: odmena nezávisí od obratu) | CCO | OK |
| 5 | Výplata (bankový prevod, 4-eyes) | Financie | Výplata |
| 6 | Evidencia (mzdový register, potvrdenia) | HR | Register |

**STOP:** mzda nad limit bez sign-off = STOP; odmiana gestora naviazaná na obrat = STOP (Rámec v1.1); výplata hotovosti = nepovolené.

**Log:** mzdový register, register potvrdení, sign-off log.
**KPI:** 100% výplat do konca mesiaca; 0 odchýlok pri kontrole CCO; 100% nadčasov v podkladoch.

---

## FC-26 · ODHOD ZAMESTNANCA (Offboarding)

**Účel:** Odchod zamestnanca bezpečne a úplne: výpoveď/koniec zmluvy, odovzdanie agendy, revokácia prístupov, pomôcky, IP a mlčanlivosť.

**Právny základ:** z. 311/2001 (skončenie PP), z. 215/2004 (koniec previerky, obmedzenia), 2021/821 (prístup ku kontrolovaným tech po odchode), GDPR (výmaz/mylé zníženie).

**Zodpovednosti:** HR (R), CISO (R revokácia), manažér línie (A), CCO (C odchodové interview), CFO (C vyúčtovanie).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Oznámenie/rozhodnutie o skončení PP | manažér/HR | Dohoda/výpoveď |
| 2 | Odovzdanie agendy + dokumentov (handover) | odchádzajúci | Spis |
| 3 | Odovzdanie pomôcok + majetkové vyrovnanie (FC-19) | HR/CFO | Protokol |
| 4 | Revokácia prístupov (do 24h), MFA, kľúče, zóny | CISO/IT | Revokácia |
| 5 | Odchodový rozhovor + IPR/NDA + prehlásenie | HR/CCO | Podpis |
| 6 | Vyúčtovanie mzdy + potvrdenie zamestnania | mzdy/HR | Zápočtový list |

**STOP:** bez revokácie prístupov sa odchádzajúci nesmie dostať k Z2/Z3 po poslednom dni; bez odovzdania pomôcok = pozastavenie zápočtového listu.

**Log:** offboarding check, access log (revokácia), register pomôcok, register potvrdení.
**KPI:** 100% revokácií do 24h; 100% handoverov dokončených; 0 prístupov po odchode.

---

## FC-27 · NEZHODY / NCR / CAPA (Kvalita)

**Účel:** Každá nezhoda (reklamácia, výrobná chyba, audit finding, dodávateľská chyba) → identifikácia → náprava → preventívne opatrenie (CAPA) → uzavretie.

**Právny základ:** AQAP 2110 (kap. 5.4 — kontrola nezhody), ISO 9001 §8.7, §10.2, z. 58/2014 (bezpečnostné incidenty pri munícii), zákaznícke zmluvy.

**Zodpovednosti:** manažér kvality (A), zúčastnený útvar (R), CCO (C pri compliance nálezoch), ECO (C pri exportných nezhodách).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Registrácia nezhody (NCR číslo) | ktokoľvek | NCR |
| 2 | Triáž: výrobná/procesná/audit/dodávateľská/bezpečnostná | Kvalita | Klasifikácia |
| 3 | Izolácia (zastavenie dávky, karanténa) | Výroba/Kvalita | Karanténa |
| 4 | Root cause analýza (5-Why / Ishikawa) | vlastník procesu | RCA |
| 5 | Nápravné opatrenie (CA) + termín + zodpovedný | Kvalita | CA |
| 6 | Preventívne opatrenie (PA) → proces/doc update | Kvalita | PA |
| 7 | Overenie účinnosti + uzavretie | Kvalita | Uzavreté |
| 8 | Log + eval (dodávateľ: FC-18, sťažnosť zákazníka: FC-21) | Kvalita | Register |

**STOP:** nezhoda s vplyvom na bezpečnosť ≤ hlášené bezodkladne (HSE, 58/2014); dodávka z karantény bez rozhodnutia = STOP; uzavretie bez overenia účinnosti = STOP.

**Log:** register nezhôd (NCR register), CAPA register, karanténny register.
**KPI:** 100% NCR uzavretých do 30 dní; 0 nezhôd bez RCA; trend ≤ 2 % výroby.

---

## FC-28 · PROTOTYP A TESTOVANIE (Vývojová fáza)

**Účel:** Prototypové kusy, testovanie (funkčné, EMC, enviro) a overenie pred release — riadene, bezpečne, s dokumentáciou vstupujúcou do release FC-23.

**Právny základ:** 2021/821 (klasifikácia prototypu), z. 58/2014 (skúšanie výbušnín — pyrotechnik), AQAP 2110 (prototypy), SORA/prevádzkové povolenie (testovacie lety UAV).

**Zodpovednosti:** CTO (A), vedúci testovania (R), Výroba (R prototyp), HSE (C pri nebezpečných testoch), Kvalita (C), ECO (C).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Test plan (cieľ, rozsah, vybavenie, riziká) | CTO | Test plan |
| 2 | Postavenie prototypu (FC-23 fáza 5) | Výroba | Prototyp |
| 3 | Testy: funkčné/EMC/enviro/lety | testovanie | Test report |
| 4 | Kontrola HSE (ak výbušniny/let) | HSE | Povolenie testu |
| 5 | Analýza výsledkov (pass/fail) | CTO/Kvalita | Zhrnutie |
| 6 | Iterácia (návrat FC-23) alebo release spôsob | CTO | Rozhodnutie |
| 7 | Dokumentácia testov → kvalifikácia | Kvalita | Register |

**STOP:** test výbušnín bez pyrotechnika = STOP; let bez prevádzkového povolenia = STOP; test report bez podpisu = neplatný.

**Log:** test register, prototyp register, letový register (UAS), HSE log.
**KPI:** 100% testov podľa plánu; 0 testov bez povolenia; doba kvalifikácie < 30 dní od posledného testu.

---

## FC-29 · POŠTOVÁ KOREŠPONDENCIA A REGISTRE (Doručená/odoslaná pošta)

**Účel:** Všetka pošta (fyzická, e-mail, úradná, súdna) evidovaná, triedená a doručená správnemu gestorovi s termínmi.

**Právny základ:** správny/občiansky súdny poriadok (lehoty), z. 305/2013 (e-Government), GDPR (dôvernosť), interné pravidlá.

**Zodpovednosti:** Podateľňa/Facility (R), CCO (A kontrola registrov), gestori (C).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Príjem (fyzická/e-mail/úradná) | Podateľňa | Pečiatka/scan |
| 2 | Evidencia (dátum, odosielateľ, typ, termín) | Podateľňa | Poštový register |
| 3 | Triedenie → gestor | Podateľňa | Rozdelenie |
| 4 | Vybavenie (gestor v lehote) | gestor | Vybavené |
| 5 | Odpoveď → odoslaná pošta (evidencia odoslania) | Podateľňa | Register odoslanej |
| 6 | Archív + retencia | Podateľňa/CCO | Archív |

**STOP:** úradná/súdna pošta bez evidencie termínu = STOP; nevybavené v lehote = eskalácia.

**Log:** poštový register, register odoslanej, register termínov.
**KPI:** 100% pošty evidovaná; 100% termínov splnených; 0 stratených zásielok.

---

## FC-30 · BUDOVA A OBJEKTOVÁ ÚDRŽBA (Facility)

**Účel:** Prevádzka budov, údržba, bezpečnosť objektu, energetika, úklid, revízie (elektro, požiarna), havarijné stavy — vrátane chránených priestorov (z. 215/2004).

**Právny základ:** z. 215/2004 §53 (chránené priestory), stavebný zákon, z. 124/2006 (BOZP), požiarna ochrana, revízie.

**Zodpovednosti:** Facility (R), Bezp. riaditeľ (C chránené priestory), CFO (A rozpočet), HSE (C BOZP).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Plán údržby + revízií (ročný) | Facility | Plán |
| 2 | Havária/požiadavka (tiket facility) | ktokoľvek | Ticket |
| 3 | Triáž (priorita, riziko chránených priestorov) | Facility/Bezp. | Priorita |
| 4 | Oprava/údržba + zápis | Facility | Záznam |
| 5 | Revízie (elektro, PO, výťahy) v termínoch | Facility | Revízne správy |
| 6 | Kontrola chránených priestorov | Bezp. riaditeľ | Audit |
| 7 | Kvartálny report nákladov | Facility/CFO | Report |

**STOP:** revízia po termíne = zariadenie odstaviť; prístup do chránených priestorov bez kontroly = STOP.

**Log:** facility register, revízny register, havarijný denník, energetický register.
**KPI:** 100% revízií v termíne; 0 nevybavených P1; náklady v rozpočte.

---

## FC-31 · DOPRAVA, LOGISTIKA A EXPEDÍCIA

**Účel:** Expedícia tovaru (vr. munície a VOP) — balenie, prepravné doklady, export clearance, dopravca schválený ECO, sledovanie dodávky až po doručenie a certifikát overenia dodávky.

**Právny základ:** z. 392/2011 (§18 — certifikát overenia dodávky; §16 EUC), z. 58/2014 (preprava výbušnín — ADR), 2021/821 (dual-use), sankčné pravidlá dopravcov.

**Zodpovednosti:** Logistika (A), ECO (C clearance), Sklad (R), CFO (C), Obchod (I).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Požiadavka expedície (objednávka, termín, cieľ) | Obchod | Expedičný list |
| 2 | Export clearance (FC-09), EUC platné | ECO | Clearance |
| 3 | Výber dopravcu (DD + sankčný screening) | Logistika | Schválený dopravca |
| 4 | Balenie + ADR/embaláž (ak výbušniny) | Sklad | Balené |
| 5 | Prepravné doklady (CMR/faktúra/certifikáty) | Logistika | Doklady |
| 6 | Expedícia + tracking | Logistika | Vyslané |
| 7 | Potvrdenie doručenia (POD) + certifikát overenia dodávky | Logistika/ECO | POD |
| 8 | Spis + hlásenia MH SR | ECO | Spis |

**STOP:** zásielka bez clearance = STOP; dopravca bez screeningu = STOP; výbušniny bez ADR/embaláže = STOP.

**Log:** expedičný register, dopravný register, certifikáty overenia dodávky, spis MH SR.
**KPI:** 100% expedícií s clearance; 100% POD doložených; 0 deviácií ADR.

---

## FC-32 · PO-PREDAJNÁ PODPORA A SERVIS

**Účel:** Záručný/pozáručný servis, technická podpora, aktualizácie softvéru, náhradné diely — so zachovaním exportných a bezpečnostných pravidiel (servis na diaľku = prenos technológie).

**Právny základ:** z. 392/2011 (§3 písm. c — vzdialený servis ako služba = vývoz), 2021/821 čl. 2(2)(d) (prenos), zmluvy so zákazníkmi.

**Zodpovednosti:** Obchod/Servis (A), CTO (C technická), ECO (C clearance servisu), Kvalita (C záruka), Logistika (R diely).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Servisný tiket (zákazník, popis, záruka?) | zákazník/Obchod | Ticket |
| 2 | Triáž + SLA | Servis | Priorita |
| 3 | Ak vzdialený servis/aktualizácia → ECO clearance | ECO | Clearance |
| 4 | Diagnostika + náhradné diely (FC-18/31) | Servis/Log | Plán |
| 5 | Realizácia servisu (on-site/remote) | Servis | Report |
| 6 | Overenie + zákazník sign-off | Servis/Obchod | Podpis |
| 7 | Zápis do servisného registra + záruka | Kvalita | Register |

**STOP:** vzdialený servis k VOP/dual-use bez ECO = STOP; diel bez klasifikácie = STOP; servis bez zákazníckeho sign-off = neuzavretý.

**Log:** servisný register, register aktualizácií, ECO servisný log, register náhradných dielov.
**KPI:** 100% servisov v SLA; 100% vzdialených servisov s clearance; CSAT ≥ 90 %.

---

## FC-33 · ÚČTOVNÍCTVO A CONTROLLING

**Účel:** Účtovná osnova, závierka, DPH, controlling nákladov a marží, dohľad nad hotovosťou (AML), podpora reportingu — so 4-eyes a audit trail.

**Právny základ:** z. 431/2002 (účtovníctvo), z. 222/2004 (DPH), z. 595/2003 (daň z príjmov), z. 297/2008 (AML — hotovosť), Obchodný zákonník.

**Zodpovednosti:** účtovníčka (R), CFO (A), CCO (C AML/limity), audítor (I), predstavenstvo (I).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Príjem dokladov (faktúry, banka, pokladňa) | účtovníčka | Doklad |
| 2 | Zaúčtovanie + kontrola (HPP) | účtovníčka | Záznam |
| 3 | Mesačná uzávierka + DPH | účtovníčka/CFO | Report |
| 4 | Kvartálny controlling (marže, náklady, backlog) | CFO | Controlling |
| 5 | AML kontrola (hotovosť, 4-eyes) | CCO/CFO | AML log |
| 6 | Ročná závierka + audit | CFO/audítor | Závierka |
| 7 | Archív dokladov (retencia) | účtovníčka | Archív |

**STOP:** doklad bez podkladu = nezaúčtovať; hotovosť > 10 000 € = STOP (vnútorný zákaz); deň uzávierky posun = eskalácia.

**Log:** účtovný register, DPH register, AML log, controlling report.
**KPI:** 100% dokladov zaúčtovaných do uzávierky; 0 AML odchýlok; závierka do zákonom určenej lehoty.

---

## FC-34 · ROZPOČET A CASHFLOW

**Účel:** Ročný rozpočet, sledovanie plnenia, cashflow projekcia, investičné rozhodnutia a riziko likvidity — schvaľované podľa limitov a reportované predstavenstvu.

**Právny základ:** Obchodný zákonník (povinnosť riadenia), z. 431/2002, stanovy, limity schvaľovania.

**Zodpovednosti:** CFO (A), controlling (R), útvary (C), predstavenstvo (A schválenie rozpočtu), DR (I).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Požiadavka na rozpočet (návrh útvarov) | útvary | Návrh |
| 2 | Konsolidácia + cashflow projekcia | controlling/CFO | Rozpočet návrh |
| 3 | Review + škrtanie/priorita | CFO | Finalizácia |
| 4 | Schválenie rozpočtu (predstavenstvo) | Predstavenstvo | Schválené |
| 5 | Mesačný controlling plnenia | controlling | Report |
| 6 | Cashflow (týždenne) a riziko | CFO | Cashflow |
| 7 | Kvartálny report DR | CFO | Report |

**STOP:** čerpanie nad rozpočet bez schválenia = STOP; cashflow v riziku → eskalácia CEO; investícia nad limit bez predstavenstva = STOP.

**Log:** rozpočtový register, controlling, cashflow register, sign-off.
**KPI:** 100% čerpania podľa rozpočtu; cashflow projekcia 13+ týždňov; 0 prekročení limitov.

---

## FC-35 · WORKSPACE A VYBAVENIE (Kancelária / Pracovisko)

**Účel:** Zariadenie kancelárií a pracovísk (nábytok, kancelárske potreby, IT periférie, PPE) — obstaranie, evidencia, údržba, bezpečnosť, ergonómia.

**Právny základ:** Zákonník práce (BOZP, ergonómia), z. 124/2006 (BOZP), interné pravidlá podpory.

**Zodpovednosti:** Facility (A), HR (C), CFO (C), IT prevádzka (C periférie), HSE (C ergonómia).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Požiadavka (vybavenie, nábytok, PPE) | zamestnanec/Facility | Ticket |
| 2 | Schválenie (podľa kategórie a limitu) | Facility/CFO | OK |
| 3 | Obstaranie (FC-18 nákup) | Nákup | Dodanie |
| 4 | Evidencia majetku (FC-19) + odovzdanie | Facility/HR | Evidencia |
| 5 | Ergonómia/BOZP kontrola | HSE | OK |
| 6 | Údržba/obnova podľa plánu | Facility | Záznam |

**STOP:** vybavenie nad limit bez schválenia = STOP; uvoľnenie zariadenia bez evidencie = STOP; ergonomicky nevhodné pracovisko = nahlásiť HSE.

**Log:** registr vybavenia/workspace, facility register, BOZP záznamy.
**KPI:** 100% vybavenia evidovaného; doba obstarania < 5 dní; 0 BOZP odchýlok.

---

IOTA Defence a.s. · 03-WORKFLOWS/FC-25-35 · NÁVRH v1.0 · 22.10.2026 · Interné – Dôverné