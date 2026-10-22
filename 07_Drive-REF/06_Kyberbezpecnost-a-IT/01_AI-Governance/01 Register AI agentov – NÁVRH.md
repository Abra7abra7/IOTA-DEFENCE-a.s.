# **01 · Agent register**

IOTA Defence a.s. · IČO 00000000 (FIKTÍVNE — pred zápisom do ORSR)1.0NÁVRH

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

Kanónická tabuľka je aj ako Google Sheet

Zmena riadku (scope / max level / status) \= gated akcia → L4 Predstavenstvo (Mino) alebo delegácia \[DOPLNIŤ\]. Ukážkový riadok EXAMPLE zmazať pred ostrým použitím.

## **Register (v1.0 NÁVRH)**

| agent\_id | role | scope | max | owner human | status |
| :---- | :---- | :---- | :---- | :---- | :---- |
| iota-cos-orchestrator | CoS orchestrator | Drive compliance; Gmail drafts; dispatch | L1 | Márian Stančík | NÁVRH |
| iota-inbox-01 | Inbox triage | Gmail read/label/draft | L1 | Márian Stančík | NÁVRH |
| iota-legal-01 | Legal QC | Compliance Docs read; Legal drafts | L1 | \[DOPLNIŤ\] | NÁVRH |
| iota-payments-01 | Payments | P2P drafts; never bank alone | L1 | \[DOPLNIŤ Financie\] | NÁVRH |
| iota-compliance-01 | Compliance | Policies 15–25; registre; SOP | L1 | CCO \[DOPLNIŤ\] | NÁVRH |
| iota-security-01 | InfoSec / NIS2 | InfoSec; logging; incident drafts | L1 | CISO \[DOPLNIŤ\] | NÁVRH |
| iota-aml-01 | AML/KYC | Screening drafts; KYC checklist | L1 | CCO \[DOPLNIŤ\] | NÁVRH |
| iota-export-01 | Export/sankcie | SOP 29 drafts | L1 | ECO \[DOPLNIŤ\] | NÁVRH |
| iota-hr-onboard-01 | Onboarding | Access request drafts | L1 | HR \[DOPLNIŤ\] | NÁVRH |
| EXAMPLE-DO-NOT-USE | Príklad | — | L1 | — | PRÍKLAD |

## **Polia (povinné)**

| Pole | Popis |
| :---- | :---- |
| agent\_id | Stabilný ID (kebab-case); viaže sa na audit |
| role | Funkčná rola v 1\. línií |
| scope | Systémy / Docs / API v rozsahu |
| max\_approval\_level | Default L1; vyššie len výslovne Predstavenstvom |
| owner\_human | Ľudský vlastník zodpovedný za správanie agenta |
| status | NÁVRH / AKTÍVNY / POZASTAVENÝ / VYRADENÝ |

IOTA Defence a.s. · 07\_AI-Governance · 01\_Agent-register · NÁVRH v1.0 · 6\. 10\. 2026