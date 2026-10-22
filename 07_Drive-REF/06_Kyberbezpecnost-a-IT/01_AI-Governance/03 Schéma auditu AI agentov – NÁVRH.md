# **02 · Audit schema (immutable event log)**

IOTA Defence a.s. · IČO 00000000 (FIKTÍVNE — pred zápisom do ORSR)1.0NÁVRH

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

Účel:

## **1\. Princípy**

* Append-onlycorrection  
* Pred akciou  
* Hash vstupuinput\_hash  
* Retencia  
* Úložisko

## **2\. Povinné polia eventu**

| Pole | Typ | Popis |
| :---- | :---- | :---- |
| event\_id | UUID | Unikátny identifikátor riadku |
| timestamp | ISO-8601 UTC+2 label | Čas vzniku (Europe/Bratislava v reporte) |
| agent\_id | string | Z Agent register (napr. iota-inbox-01) |
| agent\_version | string | Verzia promptu / build (semver alebo git SHA) |
| actor\_human | string \| null | Ľudský schvaľovateľ / initiator (email/meno) ak je |
| action | enum | draft \| search \| classify \| send\_mail \| payment \| merge \| register\_write \| policy\_change \| escalate \| deny \| … |
| target\_id | string | Doc ID, thread ID, ticket, IBAN-hash, PR URL… |
| purpose | string | Krátky účel (max 280 znakov) |
| input\_hash | SHA-256 | Hash normalizovaného vstupu |
| result | enum | ok \| denied \| escalated \| error \| pending\_human |
| policy\_decision | ALLOW \| DENY \| ESCALATE | Verdikt policy engine pred akciou |
| escalation\_ref | string \| null | Ticket / chat ID / Doc ID eskalácie |
| approval\_level | L1–L4 \| null | Úroveň použitá / požadovaná |
| amount\_eur | number \| null | Ak relevantné (platba, nákup, dar) |
| correlation\_id | UUID | Zoskupenie krokov jedného behu |

## **3\. Zakázané**

Tiché pokračovanie po DENY. Mazanie auditu. Spustenie gated akcie bez actor\_humanagent\_id

## **4\. Príklad (ilustrácia)**

| Pole | Hodnota |
| :---- | :---- |
| action | send\_mail |
| policy\_decision | ESCALATE |
| result | pending\_human |
| actor\_human | null → po ÁNO: Márian Stančík |
| escalation\_ref | ticket-AI-2026-0042 |

IOTA Defence a.s. · 07\_AI-Governance · 02\_Audit-schema · NÁVRH v1.0 · 6\. 10\. 2026 · Márian Stančík · Interné – Dôverné