# ROLE REGISTER — SÚHRNÁ REGISTRA KLÚČOVÝCH FUNKCIÍ

**IOTA Defence a.s. · Vlastník: CEO · Spravuje: CCO · Klasifikácia: Interné – Dôverné · Stav: NÁVRH v1.0 (22.10.2026)**
**Účel:** Jediný prehľad všetkých klúčových roli v systéme — **kto je kto, čo sie od neho očakuje, za čo zodpovedá**. Použi pri onboarding, akvizícii, novom gestorovi alebo do prehľadu org.
**Úźmedzenie:** Toto NIE je právna rada a NIE nahradzá RACI maticu (`raci.md`) — RACI má záväzné R/A/C/I ku každej úlohe. Tento register dáva *popis a zodpovednosti* každej funkcie.

> ⚠️ NÁVRH. Pred schválením overiť advokátom a vyplniť `[DOPLNIŤ]`.

---

## Ako čítať (legenda)

| Stĺpec | Význam |
|:--|:--|
| **Línia** | 1L = prevádzka (vlastní riziko) · 2L = dohľad/compliance (STOP-right) · 3L = audit (nezávislé). Po FC-02: 1L+2L u jednej osoby = STOP. |
| **Reportuje** | Komu zodpovedá (štvrťročne / operatívne). |
| **Vlastní workflow** | Ktoré procesy (FC-nn) daná rola vedie (A v RACI). |
| **STOP-right** | Právo stopovať akciu (2L). Prelomí len Predstavenstvo (zápis + info DR). |

---

## A. ORGÁNY & VEDENIE (statuárne)

### VZ — Valné zosťavanie (akcionári)
- **Popis:** Najvyšší orgán firmy. Volí a odvoláva DR a Predstavenstvo, schvaľuje stanovy, ročné výsledky.
- **Zodpovednosti:** Schválenie stanovy · volenie orgánov · ročná správa · lát správ. Rozhodnutia o zmene stanovy.
- **Reportuje:** — (najvyšší) · **Línia:** — · **Vlastní:** stanovy, orgány.

### DR — Dozorná rada
- **Popis:** Kontrolný orgán (3. línia nad jednak 2. línia). Dohľadá fungovanie 2. línii a Predstavenstva.
- **Zodpovednosti:** Priamy prístup CCO/Bezp.riaditeľa · schválenie štatútu interného auditu · dohľad nad Predstavenstvom · prijíme správy IA · menovacia role pri whistleblowingu proti Predstavenstvu · report 2. línii.
- **Reportuje:** VZ · **Línia:** 3L (kontrola) · **Vlastní:** štatút IA, odvolacia orgánov.

### PREDSTAVENSTVO
- **Popis:** Štatutárny výkonný orgán (mín. 1 člen). Schvaľuje systém compliance a bezpečnosti, limity L4, org poriadok, BCP/DR.
- **Zodpovednosti:** Schválenie manuálov a politík · menovanie gestorov compliance/bezp. (CCO, ECO, CISO, Bezp.riaditeľ) · odvolanie s oznámením DR vopred · limity L4 (nad 50k EUR, rizikové) · konzorciá, US, plná moc · úver · jediné môže prelomiť veto 2. línii · dary >500 EUR/verejný funkci · sponzoring.
- **Reportuje:** VZ/DR · **Línia:** vedenie · **STOP-right:** 2L veto prelomí len ono.

---

## B. 2. LÍNIA — DOHĽAD / COMPLIANCE / BEZPEČNOSŤ (STOP-right)

### CCO — Chief Compliance Officer
- **Popis:** Gestor compliance a protikorupcie. Vlastník replikačného testu, kódexu, ABAC, TPP, whistleblowingu, konfliktov záujmov.
- **Zodpovednosti:** Compliance program & štatút CCO · kódex správania · protikorupčná politika (ABAC) · register darov & pohostenia · register konfliktov záujmov · whistleblowing (nadzír zodp. osobu) · interné vyšetrovanie · AML/KYC · program pre tretie strany & agentov · due diligence partnera · spravuje tento manuál. STOP-right na compliance.
- **Reportuje:** Predstavenstvo (+ priamy prístup predseda DR) · **Línia:** 2L · **STOP-right:** áno.
- **Vlastní:** FC-02,04,06,07,10,11,12,14,16.

### ECO — Export Control Officer (zodp. zástupca §8 z.392/2011)
- **Popis:** Gestor exportných kontrol. Klíčová rolá zbrojného segmentu — odpovedá za licencie, klasifikáciu, sankcie.
- **Zodpovednosti:** ICP (vnútorná súlad) · klasifikácia výrobkov & BOM · TCP (kontrola technológií) · sankčný screening · americký obsah (ITAR-free návrh) · licencie vývozu & hlásenia MH SR · EUC + red flags · register licencií · clearance expedícií/servisov/vzdialených prenosov.
- **Reportuje:** Predstavenstvo · **Línia:** 2L · **STOP-right:** áno (export).
- **Vlastní:** FC-09, schválenie FC-18,20,31,32.

### CISO — Chief Information Security Officer
- **Popis:** Gestor informačnej bezpečnosti. Oddelený od IT prevádzky (kumulácia iba dočasne s súhlasom Predstavenstva, U-06).
- **Zodpovednosti:** Politika info-sec · oddelené prístupy (least-privilege) · logging & monitoring & eskalácia · incident response · IT štruktúra & identity · AI governance (register agentov) · NIS2 / z.69/2018 súlad · klasifikácia dátových zón · GDPR technické opatrenia.
- **Reportuje:** Predstavenstvo · **Línia:** 2L · **STOP-right:** áno (IT/kyber).
- **Vlastní:** FC-05,08,14,17.

### Bezp. riaditeľ (Security Officer)
- **Popis:** Gestor utajovaných skutočností a objektovej bezpečnosti. Klíčová rolá pre previerky NBÚ (z.215/2004).
- **Zodpovednosti:** Ochrana utajovaných skutočností · bezpečnostný projekt podnikateľa (NBÚ) · previerky osôb · chránené priestory · objektová bezpečnosť (FC-30) · evidencia utajovaných · hlásenia NBÚ pri incidentoch.
- **Reportuje:** Predstavenstvo (+ priamy prístup DR) · **Línia:** 2L · **STOP-right:** áno (utajované).
- **STOP:** utajované v bežnom cloude = STOP (FC-05).

### Legal (Legální)
- **Popis:** Právna podpora a dohľad — zmluvy, doložky, CR/ORSR, súlad.
- **Zodpovednosti:** Zmluvy + doložky (export, IPR, NDA, COI) · ORSR/CR administraciu · právny dohľad dokumentov pred schválením · konzorciá · whistleblowing podpora · procesy cudzincov.
- **Reportuje:** Predstavenstvo · **Línia:** 2L · **Vlastní:** FC-22 (legal pipeline).

### DPO — Data Protection Officer (externý)
- **Popis:** Gestor GDPR / ochrany osobných údajov.
- **Zodpovednosti:** GDPR súlad · záznamy spracovateľských činností (čl.30) · DPIA · hlásenie incidentov ÚOOÚ (72h) · register obvyklých činností.
- **Reportuje:** Predstavenstvo · **Línia:** 2L.

### Zodpovedná osoba pre oznamovateľov (whistleblowing)
- **Popis:** Nezávislá rolá (z.54/2019 §7). Stranná k CCO.
- **Zodpovednosti:** Prijatie podnetu · potvrdenie ≤7 dní · preverenie ≤90 dní · ochrana pred odvetou · štvrťročný anonymizovaný report · register oznámení (3 r.).
- **Reportuje:** Predstavenstvo/DR · **Línia:** 2L · **Vlastní:** FC-10.
- **STOP:** podnet proti Predstavenstvu → DR (nie Predstavenstvo).

---

## C. 1. LÍNIA — PREVÁDZKA (vlastní riziko denne)

### CEO
- **Popis:** Najvyšší výkonný (predseda Predstavenstva). Vlastní org poriadok, krízový plán, plán licencií, BCP/DR.
- **Zodpovednosti:** Org poriadok · krízový & kontinuitný plán (BCP/DR) · plán licencií · schválenie org-struktúry · replikačný test synergia · vedie nábor a gestorov.
- **Reportuje:** Predstavenstvo · **Línia:** 1L · **Vlastní:** FC-01,15.

### CFO — Chief Financial Officer
- **Popis:** Gestor financií, limitov, platieb.
- **Zodpovednosti:** Limity schvaľovania L1-L4 (návrh) · nákup P2P & platby · register platieb agentom (10 r.) · register tretích strán (10 r.) · rozpočet & cashflow (FC-34) · účtovníctvo (FC-33) · AML finančný dohľad · 4-eyes autorizácia.
- **Reportuje:** CEO · **Línia:** 1L · **Vlastní:** FC-04,06,13,33,34.
- **STOP:** platba nad limit / hotovosť >10 k EUR = STOP.

### Vedúci HSE (vedúci bezpečnosti výroby / pyrotechnik)
- **Popis:** Gestor výroby a skladu výbušnín (z.58/2014). Osvedčenie NBÚ/HBÚ.
- **Zodpovednosti:** Bezpečnosť výroby & skladu výbušnín · munícia & činnosti (z.58/2014) · evidencia výbušnín (min. 10 r.) · BOZP · skúšanie výbušnín (pyrotechnik) · ADR expedícia výbušnín.
- **Reportuje:** CEO · **Línia:** 1L · **Vlastní:** evidencia munície, FC-28 (testy).
- **STOP:** výbušniny bez osvedčenia/pyrotechnika = STOP.

### Manažér kvality
- **Popis:** Gestor kvality a AQAP 2110.
- **Zodpovednosti:** Príručka kvality / AQAP 2110 · NCR/CAPA (FC-27) · overenie účinnosti náprav · prototyp/testovacie overenie (FC-28) · vstupná kontrola dodávok.
- **Reportuje:** CEO · **Línia:** 1L · **Vlastní:** FC-27,28.

### HR — Human Resources
- **Popis:** Gestor ľudí, prístupov, pľánov.
- **Zodpovednosti:** Onboarding & prístupy (FC-03,17) · plán školení · popisy pracovných miest (JD) · cudzinci (pobyty/povolenia na zák. 404/2011) · evidencia pracovných pomôcok (FC-19) · odmeňovanie (FC-25) · offboarding/odchod (FC-26) · register školení (5 r.).
- **Reportuje:** CEO · **Línia:** 1L · **Vlastní:** FC-03,17,19,25,26.

### IT prevádzka (IT Operations)
- **Popis:** Obstaranie a údržba IT infra. **Oddelená od CISO.**
- **Zodpovednosti:** IT infra prevádzka · backup 3-2-1 · identity provisioning (IAM+MFa podľa FC-03/05/17) · príjemka tech · servis/údržba.
- **Reportuje:** CEO/CISO · **Línia:** 1L · **Vlastní:** FC-17 (technická časť), FC-14 (prevádzka).

### Obchod (Sales)
- **Popis:** Predaj, tendre, ponuky, klienti.
- **Zodpovednosti:** Komunikácia s klientmi (FC-21) · ponuky & tendre · expedičný input · servisná podpora (FC-32) · požiadavky vývoja (FC-23) · EUC red flags initial.
- **Reportuje:** CEO · **Línia:** 1L · **Vlastní:** FC-21,32.
- **STOP:** gestor nesmie zodpovedať za predaj (FC-02).

### Nákup (Procurement)
- **Popis:** Obstaranie komponentov a služieb.
- **Zodpovednosti:** Nákup komponentov (FC-18) · DD dodávateľov (s CCO) · vstupná kontrola · balenie vstupov · logistická požiadavka.
- **Reportuje:** CEO/CFO · **Línia:** 1L · **Vlastní:** FC-04,18,31 (vstup).

### Výroba (Production)
- **Popis:** Fyzická výroba a montáž.
- **Zodpovednosti:** Montáž/postavenie podľa BOM · vstupná kontrola (s kvalita) · karanténa nezhôd (FC-27) · prototypy (FC-28) · balenie/ADR (s HSE) · bezpečnosť výroby.
- **Reportuje:** CEO/vedúci HSE · **Línia:** 1L.

### Financie (Finance Ops)
- **Popis:** Účtovanie a výplaty (1L operatíva pod CFO).
- **Zodpovednosti:** Faktúry · výplaty 4-eyes · register platieb · DPH · mesačná uzávierka · AML operatívny check.
- **Reportuje:** CFO · **Línia:** 1L · **Vlastní:** FC-06 (výkon), FC-33.

---

## D. 3. LÍNIA — NEZÁVISLÁ KONTROLA

### Interný audítor (externý / IA)
- **Popis:** Nezávislé overenie účinnosti celého systému (3. línia).
- **Zodpovednosti:** Štatút IA (schvaľuje DR) · ročné overenie · výnimočné audity · správa IA → DR · overenie tri línii fungovanie.
- **Reportuje:** DR · **Línia:** 3L · **Vlastní:** štatút IA, FC-02 (overenie).

---

## E. PREVÁDKOVÉ FUNKCIE (doplnkové z FC-25..35)

| Funkcia | Popis | Zodpovednosti (výber) | Línia |
|:--|:--|:--|:--|
| **Logistika / dopravca** | Expedícia tovaru, dopravca, ADR | Expedičný register · výber dopravcu + screening · balenie/ADR · certifikát overenia dodávky (FC-31) | 1L |
| **Facility (objektová údržba)** | Budovy, údržba, revízie | Plán údržby · revízie (elektro/PO) · chránené priestory (s Bezp.) · workspace vybavenie (FC-30,35) | 1L |
| **Podateľňa (pošta/registry)** | Príjem a evidencia pošty | Poštový register · termíny · triedenie → gestor · archív (FC-29) | 1L |
| **Mzdy (payroll)** | Výpočet miezd | Mzdový register · odvody · výplaty (pod HR/CFO, FC-25) | 1L |
| **Servis (after-sales)** | Po-predajná podpora | Servisný register · vzdialené servisy s ECO clearance · diely (FC-32) | 1L |
| **Kvalita operatíva** | Nezhody, NCR | Register NCR/CAPA · RCA · karanténa (FC-27) | 1L |

---

## F. MINIMÁLNA OBSADENOSŤ PO ZÁKONOCH (GAP z OPS-MANUAL 8.)

| Rolá | Zákon / povinnosť |
|:--|:--|
| CCO + analytik | compliance (FC-02) |
| ECO + 2 analytici | zodp. zástupca §8 z.392/2011 |
| Bezp. riaditeľ + osobitné pracovisko | z.215/2004 NBÚ |
| CISO | info-sec/NIS2 |
| Vedúci HSE s osvedčením NBÚ + pyrotechnici | z.58/2014 |
| Manažér kvality | AQAP 2110 |
| DPO (ak povinný) | GDPR |
| Zodp. osoba pre oznamovateľov | z.54/2019 |
| Externý IA | 3. línia |

---

**Zhrnutá matica:** kompletná RACI po úlohach v `raci.md`; tu si nájdeš popis + zodpovednosti + línii každého klíčového funkcie. Replikačný test: hocikto, kto prečíta ROLES.md + RACI + OPS-MANUAL, vie kto je kto a za čo zodpovedá v celej firme.

IOTA Defence a.s. · 01-OPS-MANUAL/ROLES.md · NÁVRH v1.0 · 22.10.2026 · Interné – Dôverné