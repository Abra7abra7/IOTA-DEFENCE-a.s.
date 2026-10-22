# **04 · Policy-as-code – princípy**

IOTA Defence a.s. · IČO 00000000 (FIKTÍVNE — pred zápisom do ORSR)1.0NÁVRH

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

## **1\. Cieľ**

Flowcharty (FC) a politiky 15–25 sa prekladajú na strojovo vyhodnotiteľné pravidlá

## **2\. Životný cyklus pravidla**

* Zdroj  
* Návrh pravidla  
* Review  
* Publish  
* Enforceevaluate(action, context)  
* Audit

## **3\. Príklad pravidla (ilustrácia, nie produkčný kód)**

## **4\. Povinné vlastnosti**

| Vlastnosť | Požiadavka |
| :---- | :---- |
| Fail-closed | Pri chybe engine → DENY / ESCALATE, nie ALLOW |
| Žiadne tiché continue | silent\_continue: false vždy |
| Traceability | Každý verdikt odkazuje na Doc ID \+ kapitolu |
| Testy | Min. 1 positive \+ 1 negative case na pravidlo |
| Zmena limitu | Len L4 (Predstavenstvo); agent limity nemení |

## **5\. Mapovanie FC → pravidlá (štart)**

| FC / politika | Pravidlá (príklady ID) |
| :---- | :---- |
| FC-13 / Limity | PAY-L1…L4, P2P-RISK-MIN-L3 |
| FC-09 / Pol. 18 | SANCTIONS-HIT-STOP, EXPORT-LICENSE-GATE |
| FC-10 / Pol. 22 | WB-INTAKE-HUMAN, WB-NO-RETALIATION |
| Pol. 24 AML | AML-HIT-DUAL, KYC-BEFORE-PAY |
| Pol. 16 ABAC | GIFT-500-CAP, GIFT-REGISTER |
| FC-16 | AGENT-GATED-ALWAYS-HUMAN |

Implementačný stack policy engine: \[DOPLNIŤ — napr. OPA / interný service\]. Do schválenia Predstavenstvom platí tento dokument ako NÁVRH prevádzkových pravidiel.

IOTA Defence a.s. · 07\_AI-Governance · 04\_Policy-as-code-principles · NÁVRH v1.0 · 6\. 10\. 2026 · Márian Stančík · Interné – Dôverné