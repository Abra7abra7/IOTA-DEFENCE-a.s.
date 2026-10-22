# IP & BEZPEČNOSTŤ — Princípy a zodpovednosti

**IOTA Defence a.s. · Vlastník: CCO (IP) / CISO (IT-sec) / Bezp. riaditeľ (utajované) · Klasifikácia: Dôverné · Stav: NÁVRH v1.0 (22.10.2026)**

> **Účel:** Zabetpečiť dve najhodnotnejšie aktíva firmy: **intelektuálna vlastnosť (IP) a bezpečnosť** (dát, ľudí, infra, utajovaných skutočností). Kompletny priečinok: `04-IP-SECURITY/`.

---

## 1. KLASIFIKÁCIA DÁT — 4 ZÓNY (FC-05)

| Zóna | Úroveň | Príklady | Prístup | Skladovanie |
|:--|:--|:--|:--|:--|
| **Z0 Verejné** | public | Web, marketing | ktokoľvek | verejný web |
| **Z1 Interné** | internal | Politiky, org | všetci zamestnanci | Google Drive (interné) |
| **Z2 Dôverné** | confidential | BOM, licencie, registre, IP | need-to-know | oddelené, DLP, access log |
| **Z3 Utajované** | classified z.215/2004 | utajované skutočnosti, evidencia výbušnín | osobitné pracovisko | **MIMO verejného úložiska** |

**Pravidlá:**
- `Z2` a `Z3` **nikdy** na verejných cloud/ChatGPT/kopierky bez DLP.
- Least-privilege: prístup iba na potrebu (`need-to-know`), access log vždy.
- Utajované doklady a evidencia výbušnín → **mimo** Google Drive (z.215/2004, z.58/2014).
- Bunneboarding: revokácia prístupov do 24h; audit po odchode.

---

## 2. INTELEKTUÁLNA VLASNOSŤ (IP)

### 2.1 IPR zmluvy (vývoj)
- Kútikód (hardware+software) je **trade-secret** firmy. Všetci zamestnanci, konzulatni, subcontractori, agenti → **IPR/NDA zmluva** pred prístupom k Z1+.
- Verejné: WDO (work for hire), §263 Zákonníka práce (autorské právo na výsledok tvorivej činnosti vytvoravej pracovným poměrom — overiť) a **explicitná IPR doložka** k.Vz.
- Odmienka: IPR firmy vs osobná. Každá IPR zmluva overená advokátom.

### 2.2 Komerciálne tajemstvo (trade secrets)
- Právny základ: GDPR nie; TP z.300/2005 §263, §380; smernica (EÚ) 2016/943 (Trade Secrets Directive), transpozycia do z. .
- Zmluvné doložky: NDA, non-disclosure, non-dealing, non-poaching, non-compete; dožiowanie konfidenciality po odchode.
- Technologie control (TCP) — podľa n.ú.s.2021/821 čl.2 bod 2 písm.d; §3 písm.c z.392/2011; 15 CFR 734.14(b).
- Register trade-secrets: čo je trade-secret, kto má prístup, kde je logované.

### 2.3 Kusovníky (BOM) & klasifikácia
- BOM = klasifikovaný podľa ML listu EÚ / 2021/821 príl.I / MTCR.
- ECO + CTO riadia klasifikáciu (IOTA-EXP-02; register klasifikácie BOM IOTA-REG-05).
- Americký obsah → ITAR/EAR (22 CFR 120, 123; 15 CFR 730-774); postoj kompletne ITAR-free n.vrh (Politika IOTA-EXP-05).

---

## 3. KYBERBEZPEČNOSŤ & IT (ZÁVÄZNÉ)

| Oblasť | Norma/Súlad | Štandard | Zodpovedný |
|:--|:--|:--|:--|
| Informačná bezpečnosť | Politika info-sec | ISO/IEC 27001 | CISO |
| Kyber bezpečnosť regulácia | NIS2 (z.69/2018) | súlad povinný subjekt | CISO |
| AI | AI Act 2024/1689 | risk mgmt, log, governance | CISO/CCO+CTO |
| Dátová ochrana | GDPR čl.32 | encryption, access, incident | CISO/DPO |
| Klasifikované IT | z.215/2004, NATO | SSP, delegované| Bezp.riaditeľ/CISO |
| Export/súlad | TCP, ITAR-alignment | access control 22 CFR 120.56 | ECO/CISO |

**IT baseline (minimum):**
1. **2FA/MFA** všade (identity per user — bez shared accounts).
2. **Least-privilege access** + oddelené zóny (FC-05).
3. **Immutable logging** (SIEM): všetky prístupy, zmluvy, platby, decision → log; log nie editovateľný.
4. **Backup 3-2-1** + BCP/DR test (FC-15).
5. **Incident response** (FC-08): triáž P1-P4, SLA, eskalácia.
6. **AI agents register** + AI governance (AI Act).
7. **Endpoint hardening** + patch mgmt + antivírus/EDR.
8. **Copilot/AI tools** — zakáz pre Z2/Z3 bez DLP review.

**ITIL/Identity:** Google Workspace (identity), oddelené prístupy na Z2/Z3; CISO cieľová architektúra — pozri `06_IT-struktura-a-identity-defence-SME` (z pričinok).

---

## 4. UTJAVANÉ SKUTOČNOSTI & BEZPEČNOSTNÁ PREVIERKA (z.215/2004)

### 4.1 Bezpečnostná previerka podnikateľa (biznis)
- **Podnikateľská bezpečnostná previerka** — NBÚ potvrdenie (§45 z.215/2004): firma overená na úroveň utajovania, ktore skutočnosti firma potrebuje pre zákazky (tajné / prísne tajné).
- Proces: bezpečnostný projekt podnikateľa (§45(2,3),(8) z.215/2004), osobitný pracovisko, audit NBÚ.
- Konzultácia s NBÚ pred projektom (adyvokát/Bezp.riaditeľ).

### 4.2 Osobná previerka zamestnancov
- Osôby s prístupom k utajovaným → osobná bezpečnostná previerka (stupeň tajné/prísne tajné).
- Osobitný pracovisko skontroluje personel; inkorporovať do onboarding (FC-03) a HR.
- Evidencia v Z3 (mimo verejného).

### 4.3 Objektová bezpečnosť
- Fyzické zabezpečenie skladov výbušnín (§18,19 z.58/2014; HBÚ) + kancelárie/IT (Z2/Z3).
- Alarm, CCTV, access control, log návštevu, SOC.

---

## 5. IT INFRA — CIELOVÁ ARCHITEKTÚRA (VYCHOD)

Cieľová IT architektúra (z pričinok `06_IT-struktura-a-identity-defence-SME` + `08 Úvodné zistenie`):

| Vrstva | Systém | Klasifikácia | Náza |
|:--|:--|:--|:--|
| Identity | Google Workspace + SSO/MFA | Z1 | CISO |
| KB (ERP/CRM)| oddelené Z2 | Z2 | CISO/CFO |
| SiS/fortress | Z3 izolovaná (offline/air-gap) | Z3 | Bezp.riaditeľ |
| Logging/SIEM | immutable, WORM | Z2 | CISO |
| Backup | 3-2-1 + off-site + DR site | Z2 | CISO/IT |
| AI agents | sandbox, policy-as-code | Z2 | CISO/AI-governance |

---

## 6. AUDIT & OVERENIE

- **3. línia (externý IA)** ročne overí: prístupy, log, registre, IPR zmluvy, NIS2/GDPR súlad, BCP test.
- **2. línia** štvrťročne self-audit.
- **CCO** štvrťročne skontroluje úplnosť registrov.
- **Incident post-mortem** po každej eskalácii P1/P2.

---

IOTA Defence a.s. · 04-IP-SECURITY · NÁVRH v1.0 · 22.10.2026 · Dôverné