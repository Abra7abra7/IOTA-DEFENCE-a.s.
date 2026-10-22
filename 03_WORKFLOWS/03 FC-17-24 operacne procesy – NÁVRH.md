# WORKFLOWS DOPLNKOVÉ (FC-17 až FC-24) — Prevádzkové procesy

**IOTA Defence a.s. · 22.10.2026 · NÁVRH v1.0 · Interné – Dôverné · Každý proces: workflow → RACI → log → KPI. Diagramy: .archify/*.html + PNG.**

> Status priority P1: FC-17..FC-23; P2: FC-24. Kompletné diagramy v `03-WORKFLOWS/.archify/` (Archify all-gates-pass).

---

## FC-17 · VYTVORENIE KONTA UŽÍVATEĽA V SYSTÉME (IT Onboarding)

**Účel:** Nový človek dostane konto, MFA, roly a prístupy presne podľa svojej funkcie a štátnej príslušnosti — bezpečne, rýchlo, auditovateľne.

**Právny základ:** z. 215/2004 (prístup k utajovaným), 2021/821 čl. 2(2)(d) a čl. 8 (deemed export pri cudzincoch), GDPR čl. 32, ISO 27001 A.9.

**Zodpovednosti:** HR (R, iniciuje), CISO (A, schvaľuje prístupy), IT prevádzka (R, vytvorí konto), ECO (C, ak cudzinec / kontrolovaná technológia), manažér línie (C).

**Workflow (kroky):**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Onboarding request (osoba, funkcia, nástup) | HR | Ticket IT |
| 2 | Kontrola: previerka, občianstvo, ECO consent (cudzinci) | HR + ECO | Schválenie / STOP |
| 3 | Vytvorenie identity + MFA seed | IT prevádzka | Účet aktívny |
| 4 | Priradenie rolí/zón (Z0-Z3 podľa FC-05) | CISO | Access matrix |
| 5 | Oboznámenie: kódex, NDA, IPR, školenia (FC-03) | HR/CCO | Podpis |
| 6 | Log do registra prístupov + register školení | CISO/HR | Log entry |
| 7 | Odovzdanie pomôcok (FC-19) a príručiek | HR | Protokol |

**STOP:** bez schválenia ECO (cudzinec) = konto neaktívne; bez podpisu NDA/IPR = žiadne Z2/Z3 prístupy.

**Log:** access log (imutable), register prístupov, register školení, register pomôcok.
**KPI:** 100% kont do 24h od nástupu; 100% MFA aktívnych; 0 kont bez role.

---

## FC-18 · NÁKUP KOMPONENTOV (P2P + KLASIFIKÁCIA BOM)

**Účel:** Každý komponent nakúpený cez schválený proces: požiadavka → výber dodávateľa → klasifikácia pôvodu/exportného zaradenia → objednávka → príjemka → platba → evidencia. Zadanie súčasne pokrýva "nákup komponentov".

**Právny základ:** z. 392/2011 (VOP), 2021/821 (dual-use), ITAR/EAR (ak US obsah — 15 CFR 734.4 de minimis), AQAP 2110 (kvalita dodávateľov).

**Zodpovednosti:** Nákup (R), CFO (A schválenie podľa L1-L4), ECO (C klasifikácia), CCO (C tretia strana), manažér kvality (C kritické komponenty).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Request (komponent, špec, množstvo, deadline) | žiadateľ | PR ticket |
| 2 | Klasifikácia: je to VOP/dual-use/USML/EAR99? | ECO | Klasifikačná karta |
| 3 | Výber dodávateľa (DD FC-07, tretia strana) | Nákup/CCO | Schválený dodávateľ |
| 4 | Vyžiadanie vyhlásenia o pôvode + exportnom zaradení | Nákup | Deklarácia |
| 5 | Objednávka (schválenie L1-L4) | Nákup/CFO | PO |
| 6 | Príjemka + vstupná kontrola + SHN (ak kvalita) | Sklad/Kvalita | Príjemka |
| 7 | Platba (4-eyes, proti faktúre) | Financie | Platba |
| 8 | Zápis do BOM + register klasifikácie + majetok (ak pomôcka) | Nákup/ECO | Register |

**STOP:** komponent bez exportného zaradenia sa neobjednáva; dodávateľ neschválený DD = STOP; cena nad limit bez schválenia = STOP.
**Log:** nákup register, register tretích strán, register klasifikácie BOM, majetková evidencia (FC-19).
**KPI:** 100% PO s klasifikáciou pred objednaním; 100% dodávateľov s DD; cyklus P2P < 10 dní.

---

## FC-19 · EVIDENCIA PRACOVNÝCH POMÔCOK (Majetok / Inventár)

**Účel:** Každá pomôcka/majetok (IT, náradie, PPE, mobil, auto, stoj) evidovaný: kto má na starosti, kde je, stav, servis, vyradenie. Zodpovednosť + audit trail + daňové.

**Právny základ:** Zákonník práce (zodpovednosť za zverené hodnoty § 179), z. 431/2002 (účtovníctvo — inventarizácia), daňové odpisy.

**Zodpovednosti:** HR/Facility (R evidencia), CFO (A inventarizácia), vedúci útvaru (C), CISO (C IT majetok).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Prijatie pomôcky (nákup FC-18 / dar / presun) | príjemca | Príjemka |
| 2 | Zápis do majetkovej evidencie (ID, kat., hodnota, zodp.) | HR/Facility | Evidencia |
| 3 | Odovzdanie zamestnancovi (protokol) | HR | Protokol |
| 4 | Servis/údržba/oprava (podľa plánu) | Facility/IT | Servisný záznam |
| 5 | Ročná inventarizácia (kontrola fyzicky) | CFO/HR | Inventúra |
| 6 | Vyradenie/odpredaj/škoda (rozhodnutie) | CFO | Vyraďovací protokol |

**STOP:** pomôcka bez evidencie = nepoužívať; škoda sa hlási do 48h; inventarizačné rozdiely → vyšetrenie.
**Log:** majetková evidencia, servisný register, inventúra, register škôd.
**KPI:** 100% pomôcok v evidencii; inventúra 2×/rok; 0 neevidovaných zariadení.

---

## FC-20 · SLUŽOBNÉ CESTY (vrátane export-control / deemed export)

**Účel:** Služobná cesta schválená, náklady riadené, riziká kontrolované — najmä cesty mimo EÚ a s technológiami (deemed export: čo si vezmem, koho stretnem, čo ukážem).

**Právny základ:** Zákonník práce (cestovné náhrady), z. 392/2011 a 2021/821 (prenos technológií na ceste = vývoz), ITAR/EAR (ak US tech, 22 CFR 120.50/120.51, 15 CFR 734.14).

**Zodpovednosti:** cestujúci (R), manažér línie (A schválenie), CFO (C rozpočet), ECO (C, ak mimo EÚ / kontrolovaná tech), HR (R evidencia).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Žiadosť (krajina, účel, termín, rozpočet, čoho sa to týka) | cestujúci | Cestovný príkaz |
| 2 | ECO review: krajina, embargá, technológie, víza | ECO | Schválenie / STOP |
| 3 | Schválenie lídra + rozpočet | manažér/CFO | Schválený príkaz |
| 4 | Rezervácia (v rámci pravidiel, preddavok) | HR/Financie | Lístky/ubytovanie |
| 5 | Cesta (pravidlá: laptop zámok, žiadne zdieľanie, režim) | cestujúci | — |
| 6 | Vyúčtovanie do X dní + doklady | cestujúci | Vyúčtovanie |
| 7 | Zápis do evidencie ciest + report insightov (obchod/dev) | HR/CTO | Záznam |

**STOP:** cesta do embargovanej krajiny bez výnimky = NOT; technológie Z2/Z3 bez ECO = nepovolené; vyúčtovanie po lehote = pozastavenie preddavkov.
**Log:** evidencia ciest, vyúčtovanie, ECO log (ak control tech), register insightov.
**KPI:** 100% ciest schválených ECO pri mimo EÚ; vyúčtovanie < 14 dní; 0 ciest do zakázaných krajín.

---

## FC-21 · KOMUNIKÁCIA S KLIENTMI (CRM, ponuky, tendre)

**Účel:** Jedna pravda o každom klientovi/obchode: kontakt, ponuky, tendre, zmluvy, faktúry, stav — od prvého kontaktu po delivery a servis.

**Právny základ:** z. 392/2011 (každý vývoz cez ECO), Obchodný zákonník (zmluvy), GDPR (osobné údaje kontaktu), 2008/944 (kritéria obchodov).

**Zodpovednosti:** Obchod (R), Riaditeľ stratégie (A pipeline), ECO (C clearance), CCO (C DD/red flags), Financie (I fakturácia), Legal (C zmluvy).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Registrácia kontaktu/klienta v CRM | Obchod | CRM záznam |
| 2 | DD + screening klienta (FC-07, FC-09) | CCO/ECO | Schválený |
| 3 | Ponuka (klasifikácia tovaru, cena, EXW/DAP...) | Obchod + ECO | Ponuka |
| 4 | Tender/ponukové konanie (ak verejný) | Obchod/Prog. | Podanie |
| 5 | Zmluva (Legal review, doložky FC-22) | Legal + CCO | Podpísaná |
| 6 | Realizácia + dodanie (FC-09 clearance, logistika) | Obchod/Log. | Delivery |
| 7 | Fakturácia a after-sales | Financie/Obchod | Faktúra |
| 8 | CRM update + spätná väzba, KPI | Obchod | Report |

**STOP:** klient bez DD = nekomunikovať ponuky; ponuka bez klasifikácie tovaru = STOP; zmluva bez legal review = STOP.
**Log:** CRM, register tretích strán, register licencií, zmluvy register, faktúry.
**KPI:** 100% klientov v CRM; 100% ponúk s klasifikáciou; pipeline review mesačne.

---

## FC-22 · PRÁVNE ODDELENIE (Legal pipeline)

**Účel:** Všetky právne otázky, zmluvy, doložky, vzory, spory a registre cez jeden proces: príjem → posúdenie → review → schválenie → spis.

**Právny základ:** Obchodný zákonník, z. 392/2011, GDPR, z. 91/2016, vzorové doložky (IOTA-CON), advokátska kontrola.

**Zodpovednosti:** Legal (R), CCO (C compliance), ECO (C export doložky), CFO (C finančné), predstavenstvo (A pri nadlimitných).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Právny request (zmluva, doložka, otázka, spor) | ktorýkoľvek útvar | Legal ticket |
| 2 | Kategorizácia: zmluva/šablóna/posúdenie/spor | Legal | Priorita |
| 3 | Review (kontraktačné, compliance, export, IP) | Legal + CCO/ECO | Návrh |
| 4 | Vzorové doložky (IOTA-CON-01/02) — kontrola advokátom | Legal | Šablóna |
| 5 | Schválenie podľa limity (L1-L4) | podľa limitu | Sign-off |
| 6 | Podpis a archivácia | Legal | Spis |
| 7 | Evidencia (zmluvný register, termíny, obnovy) | Legal | Register |

**STOP:** ústna dohoda = nie; doložka mimo vzorus = advokát; schválenie pod hranicou limitu = STOP.
**Log:** právna agenda (register zmlúv), zmluvný register, register sporov, deadline tracker.
**KPI:** 100% zmlúv cez legal review; 0 ústnych dohôd; 100% dodržaných termínov.

---

## FC-23 · VÝVOJ PRODUKTU (Dev lifecycle + IPR + design gate)

**Účel:** Od nápadu po výrobu: fázy, design gate (klasifikácia BOM!), IP ochrana, verzie, dokumentácia. Bez tohto procesu nie je vývoj riadený.

**Právny základ:** 2021/821 (dual-use), 392/2011 (VOP), IPR (autorské právo §263 ZP, trade secrets, NDA), AQAP 2110 (riziká, konfigurácia), ML list EÚ.

**Zodpovednosti:** CTO (A), projektový manažér (R), ECO (C klasifikácia pri design gate), Legal/IP (C IPR), manažér kvality (C).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Nápad/požiadavka (product brief) | Obchod/CTO | Brief |
| 2 | Fáza 0: feasibilita + IP search + klasifikácia BOM | CTO + ECO | Go/No-Go |
| 3 | Návrh (CAD, elektronika, softvér) v izolovanom úložisku | dev tím | Revízie |
| 4 | Design gate: klasifikácia každého komponentu (BOM), pôvod | ECO | Gate PASS/STOP |
| 5 | Prototyp + test (výroba, EMC, environment) | Výroba/Kvalita | Test report |
| 6 | Dokumentácia (TD, kusovník finálne) | CTO | Docs |
| 7 | IPR: patent/návrh/trade-secret rozhodnutie | Legal/IP | Registrácia |
| 8 | Transfer do výroby (BOM release, QMS) | CTO/Výroba | Release |

**STOP:** design gate bez klasifikácie = STOP; komponent USML bez stratégie = STOP; prototyp bez test reportu = nie do výroby; dev v nezabezpečenom repozitári = STOP.
**Log:** vývojový register (fázy), BOM version history, design gate log, test reports, IPR register, dokumentácia register.
**KPI:** 100% design gate pass; 100% BOM klasifikovaný; každý release má kompletnú dokumentáciu.

---

## FC-24 · RIADENIE DOKUMENTÁCIE (verzovanie, schvaľovanie, archivácia)

**Účel:** Každý dokument má vlastníka, stav (NÁVRH→PLATNÉ→ARCHÍV), verziu, schvalovaciu trasu a miesto uloženia. **Toto je proces, ktorý drží replikačný test.**

**Právny základ:** ISO 9001/AQAP 2110 (riadené dokumenty), GDPR (retencia), z. 392/2011 (záznamy), interné pravidlo "nič sa nemaže".

**Zodpovednosti:** CCO (A riadenie dokumentov), dokument-control (R), vlastníci dokumentov (C), predstavenstvo (A schválenie politík).

**Workflow:**
| Krok | Činnosť | Kto | Výstup/STOP |
|:--|:--|:--|:--|
| 1 | Nový/revízia dokumentu (šablóna: NN Názov – STAV) | vlastník | Draft |
| 2 | Kontrola: RACI, právny základ, KPI | CCO | Review |
| 3 | Schválenie (podľa matice, predstavenstvo pre politiky) | schvaľovateľ | PODPÍSANÉ |
| 4 | Publikácia (PLATNÉ, jedno miesto pravdy) | doc-control | Published |
| 5 | Školenie/oznam (ak dopad) | HR/CCO | Notice |
| 6 | Archív neplatných verzií → 99_Archiv | doc-control | Archivácia |
| 7 | Retencia a lehoty (podľa registrov) | CCO | Schedule |

**STOP:** dokument bez vlastníka/schválenia = nie PLATNÉ; dve verzie v pracovnom priečinku = chyba (archivovať); citlivosť Z2/Z3 mimo úložiska = STOP.
**Log:** register dokumentov, version history, change log, archív.
**KPI:** 100% dokumentov má vlastníka+schválenie; 0 duplicit v pracovných priečinkoch; retencia podľa registrov.

---

IOTA Defence a.s. · 03-WORKFLOWS/FC-17..24 · NÁVRH v1.0 · 22.10.2026 · Interné – Dôverné