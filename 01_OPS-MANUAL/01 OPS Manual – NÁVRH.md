# IOTA Defence a.s. — OPS MANUAL (Operating Manual / Manuál fungovania)

**IČO: [DOPLNIŤ] · Vlastník: CEO · Spravuje: CCO · Klasifikácia: Interné – Dôverné · Stav: NÁVRH (v1.0, 22.10.2026)**
**Účel:** Jediný autoritatívny manuál, podla ktorého firma funguje. **Ak toto dáš hocikomu (nový CCO, nový CEO, akvizícia, nový shareholder, regulátor), musí byť schopný zreplikovať a overovať celé fungovanie firmy.**

> **⚠️ NIE JE PRÁVNA RADA.** NÁVRH na schválenie predstavenstvom. Všetky konkrétne právne povinnosti overiť advokátom + aktuálnymi predpismi (Slov-Lex / Eur-Lex). Všetky čísla ([DOPLNIŤ]) vyplniť pred schválením.

---

## 0. JAK PRACOVAŤ S TÝMTO MANUÁLOM

- **Zásada replikácie:** Každý subjekt, proces, úloha a register v tejto firme má 4 atribúty: (1) **vlastník** (RACI kto odpovedá), (2) **workflow** (aký dokument/flowchart ho riadi), (3) **logging** (kde a čo sa loguje), (4) **KPI/overenie** (ako vieme že funguje).
- **Replikačný test (The Replication Test):** Pred schválením každej zmeny odpovedz na 4 otázky: *Kto je vlastník? Aký je workflow? Kde je log? Ako to overím?* Ak hocikto z nich nemá odpoveď, proces nie je hotový.
- **Stav dokumentov:** NÁVRH → NA-PODPIS → PODPÍSANÉ → PLATNÉ → ARCHÍV. V pracovnom priečinku **len jedna platná verzia**; staré idú do `99_Archiv`. Nič sa nemaže natrvalo.
- **Zodpovednosti (RACI) sú záväzné.** Kto datú sign-off, overuje že výstup je úplný a platný v čase podpisu.
- **Každá zmiena mení 2 súbory:** tento manuál + zodpovedný dokument procesu (a register).

---

## 1. KONTROLNÁ ARCHITEKTÚRA: TRI LÍNIE OCHRANY

Firma funguje na modeli **3 línií ochrany** (3 Lines of Defence, ISO 37301 / UK Bribery Act s.7 alignment).

| Línia | Úloha | Kto | Reportuje |
|:--|:--|:--|:--|
| **1. Línia** — prevádzka | Vlastní riziká, denne kontroluje, vykonáva | Obchod, Nákup, Výroba, Financie, HR, IT prevádzka, Kvalita | Predstavenstvo (operatívne) |
| **2. Línia** — dohľad/compliance/bezpečnosť | Politiky, monitoring, limity, screening, **STOP-right** | CCO, ECO, Legal, DPO, Bezp. riaditeľ, CISO | **Predstavenstvo** (nie 1. línii!) |
| **3. Línia** — interný audit | Nezávislé testovanie účinnosti | Externý IA | Dozorná rada (funkčné) / Predstavenstvo (admin.) |

**Záväzné pravidlá (z FC-02, Rámec v1.1):**
1. **Kumulácia 1.+2. línii u jednej osoby = STOP.** Výnimka: len Predstavenstvo.
2. **Gestor (CCO/ECO/CISO/Bezp.) nesmie byť zodpovedný za predaj.**
3. CISO je **oddelený** od IT prevádzky (kumulácia len dočasne so súhlasom Predstavenstva, U-06).
4. Odvolanie CCO/CISO/Bezp.riaditeľa/ECO → Predstavenstvo oznámi DR **vopred**.
5. **Priamy prístup** CCO a Bezp. riaditeľa → predseda DR (štvrťročný report aj DR, U-02/U-03).

---

## 2. ORG STRUKTÚRA & REPORTING

Diagram: `02-ORG-VIZ/org-structure.md` (Mermaid). Reporting frekvencia a kanály:

| Kto | Komu | Čo | Frekvencia | Dokument |
|:--|:--|:--|:--|:--|
| VZ | volí/odvoláva | orgány | podľa stanovy | Stanovy |
| DR | dohľad 2. línie | štvrťročný report | štvrťročne | U-03 |
| Predstavenstvo | gestori compliance/bezp. | menovanie | ustanovenie | U-02 |
| 2. línia | Predstavenstvu | report + STOP/eskalácia | štvrťročne | U-03 |
| CCO/Bezp. | predseda DR | priamy prístup | štvrťročne | U-02, U-03 |
| Interný audit | DR | správa IA | ročne/výnimočne | Štatút IA |

---

## 3. REGISTRE & EVIDENCIE — TRACKOVATEĽNOSŤ

Všetko v tej firme musí byť **logované a trackovatelné**. Register = "kniha pravdy". Zoznam záväzných registrov (IOTA-REG-00):

| Register | Správca | Lehota uchovania | Právny základ |
|:--|:--|:--|:--|
| Register darov & pohostenia | CCO | 5 r. | TZ §328-336c |
| Register konfliktov záujmov | CCO | 5 r. po skončení | §196 OBZ, §10 z.54/2019 |
| Register tretích strán | CCO | 10 r. po skončení | OECD / ABAC |
| Register platieb agentom | CFO | 10 r. | z.54/2019 §11 |
| Register licencií & povolení | ECO | 10 r. po skončení | z.392/2011, 2021/821 |
| Register oznámení (whistleblowing) | zodpovedná osoba | 3 r. (§11 z.54/2019) | z.54/2019 §11 |
| Register klasifikácie (BOM) | ECO | min. 5 r. | 2021/821, ML list |
| Register školení | HR | 5 r. po skončení | z.311/2001 §81c |
| Evidencia výbušnín & munície | vedúci HSE | min. 10 r. | z.58/2014 §12(5) |
| Evidencia utajovaných skutočností | osobitné pracovisko | podľa predpisov | z.215/2004 |
| Záznamy o spracovateľských činnostiach | DPO | priebežne | GDPR čl.30 |
| Register AI agentov | CISO/AI-governance | priebežne | AI Act |

**Pravidlo: každý register má > 1 evidencia, kontroluje ju CCO štvrťročne (úplnosť).**

---

## 4. ZÁVÄZNÉ PROCESY & WORKFLOW (index)

Kompletny proces sa nevykonáva bez workflow dokumentu. Každý workflow má RACI, STOP-bod, log a overenie. Index záväzných procesov (FC):

| ID | Proces | Workflow | Kto (lead) | Log |
|:--|:--|:--|:--|:--|
| FC-01 | Org štruktúra & reporting | org-structure.md | CEO | U-záznamy |
| FC-02 | Tri línie ochrany | FC-02 | CCO | Compliance register |
| FC-03 | Onboarding & prístupy | FC-03 | HR/CISO | Access log, register školení |
| FC-04 | Nákup P2P | FC-04 | Financie | Nákup register |
| FC-05 | Dátové zóny & prístup | FC-05 | CISO | Access/DLP log |
| FC-06 | Platba agentovi | FC-06 | CFO/CCO | Register platieb agentom |
| FC-07 | Due diligence partnera | FC-07 | CCO | Register tretích strán |
| FC-08 | Incident response | FC-08 | CISO | Incident log |
| FC-09 | Sankcie & export control | FC-09 | ECO | Register licencií, screening log |
| FC-10 | Whistleblowing | FC-10 | zodp. osoba | Register oznámení |
| FC-11 | Dar & pohostenie | FC-11 | CCO | Register darov |
| FC-12 | Konflikt záujmov | FC-12 | CCO | Register konfliktov |
| FC-13 | Limity schvaľovania L1-L4 | FC-13 | CFO | Sign-off log |
| FC-14 | Logging/monitoring/eskalácia | FC-14 | CISO | Alert log, triáž P1-P4 |
| FC-15 | BCP/DR aktivácia | FC-15 | CEO/CISO | BCP register |
| FC-16 | Rozhodovanie o agentovi | FC-16 | CCO/ECO | Register tretích strán |
| — | Replikačný test (sekcia 0) | tento manuál | CEO | Change log |

---

## 5. IP & BEZPEČNOSTŤ (jahrom)

Detailnyj vec v `04-IP-SECURITY/`. Tu: princípy.

1. **Klasifikácia dát (zóny):** Verejné / Interné / Dôverné / Utajované (z.215/2004). Dátové zóny oddelené (FC-05); prístup podla least-privilege.
2. **Utajované skutočnosti (z.215/2004):** osobitné pracovisko, evidencia výbušnín MIMO verejného úložiska. Utajované doklady NIKDY do Google Drive.
3. **Komerciálne tajemstvo (§5 z.392/2011, WDO protokol):** NDA, non-compete, non-disclosure, technologie control (TCP), access control.
4. **IT:** ISO/IEC 27001, NIS2 (z.69/2018), CMMC/ITAR-alignment (ak US obsah), SSP, max privilege, 2FA, log všetkých prístupov (immutable), backup 3-2-1 + BCP/DR (FC-15).
5. **IPR (vývoj):** zamestnanci + outsideri podpíšú IPR zmluvy; kusovníky (BOM), technická dokumentácia, trade-secret register, NDA pre každého tretieho partnera.

---

## 6. ZODPOVEDNOSTI (RACI) — KLÚČOVÉ FUNKCIE

Komplet v `01-OPS-MANUAL/raci.md` (RACI) a **`01-OPS-MANUAL/roles.md` (ROLE REGISTER — popis + zodpovednosti + línii každého klíčového role)**. Zhrnutie:

| Funkcia | Hlavné zodpovednosti | Reportuje | Gestor |
|:--|:--|:--|:--|
| **CEO** | Org poriadok, krízový plán, plán licencií, BCP | Predstavenstvo | gestor compliance+bezp. |
| **CCO** | Compliance program, kódex, protikorupcia, TPP, whistleblowing, registre CCO | Predstavenstvo | 2. línia |
| **ECO** | ICP, klasifikácia BOM, TCP, screening, licencie MH SR, americký obsah | Predstavenstvo | 2. línia |
| **Legální** | Zmluvy, doložky, CR/ORSR, právny dohľad | Predstavenstvo | 2. línia |
| **DPO (ext.)** | GDPR, záznamy čl.30 | Predstavenstvo | 2. línia |
| **Bezp. riaditeľ** | Utajované, NBÚ previerka, objektová bezpečnosť | Predstavenstvo | 2. línia |
| **CISO** | Info-sec, prístupy, logging, incident, NIS2/AI | Predstavenstvo | 2. línia |
| **CFO** | Financie, limity, register platieb agentom, register partnerov | CEO | 1. línia |
| **Vedúci HSE** | Výbušniny, sklad, BOZP | CEO | 1. línia |
| **Manažér kvality** | QMS/AQAP 2110 | CEO | 1. línia |
| **HR** | Onboarding, školení, cudzinci, prístupy | CEO | 1. línia |
| **IT prevádzka** | Infra prevádzka, backup | CEO/CISO | 1. línia |
| **Interný audítor** | Nezávislé overenie 3. línia | DR | 3. línia |

---

## 7. SCHVÁLENIE & REVIZIA

- Tento manuál schvaľuje **predstavenstvo**; vlastník **CEO**, spravuje **CCO**.
- Revizia: **ročná** + pri každej zmene predpisov/org/činnosti.
- **Replikačný test** (sekcia 0) pred každou zmenou.
- Advokát kontrola pred schválením (najmä prístup k z.54/2019, GDPR, NIS2, americké predpisy).

---

## 8. ČO EŠTE TREBA (GAP LIST — z PREHĽADU 5.)

**Povolenia:** živnosť výroby (§4 z.392/2011) · povolenie obchodovania (§5,8 z.392/2011) · činnosti s muníciou (§41,42 z.58/2014) · sklad (§18,19 z.58/2014) · potvrdenie §45 z.215/2004 NBÚ · zbrojná licencia A (§29 z.190/2003) · licencie vývozu/dual-use/EUC (MH SR) · pobyty cudzincov · prevádzkové povolenie UAS (NSAT/SORA) · register partnerov verejného sektora (>z.315/2016).

**Ľudia:** CCO + analytik · ECO (zodp. zástupca §8 z.392/2011) + 2 analytici · Bezp. riaditeľ + osobitné pracovisko · CISO · vedúci HSE s osvedčením HBÚ + pyrotechnici · manažér kvality · DPO (ak povinný) + zodp. osoba pre oznamovateľov · externý IA.

---
IOTA Defence a.s. · 01-OPS-MANUAL · NÁVRH v1.0 · 22.10.2026 · Interné – Dôverné