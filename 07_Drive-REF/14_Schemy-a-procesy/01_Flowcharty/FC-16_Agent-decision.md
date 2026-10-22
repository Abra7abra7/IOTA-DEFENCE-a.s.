# **FC-16 · Agent decision (AI gated flow)**

IOTA Defence a.s. · IČO 00000000 (FIKTÍVNE)

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

Mapovanie:

1\. RequestÚloha \+ agent\_id \+ purpose \+ correlation\_id

↓

Agent v registri a v scope?01\_Agent-register · status AKTÍVNY/NÁVRH

↓ Nie → DENY

DENY \+ ticketAudit · žiadne tiché continue

↓ Áno

2\. Policy engineevaluate(action, context) → ALLOW | DENY | ESCALATE

↓

Gated akcia?send · payment · merge · sanctions write · policy change · AML/export hit

↓ Nie (search/draft/classify)

3a. Auto / draftVykonaj v scope · max L1 · zapíš audit

↓ Áno gated

3b. Eskaláciapending\_human · ticket · owner / L2–L4 podľa matice

↓

Ľudské ÁNO?actor\_human \+ čas v audite

↓ Nie / timeout

DENY / holdŽiadny execute

↓ Áno

4\. Audit log (immutable)input\_hash · policy\_decision · escalation\_ref · result

↓

5\. Execute alebo DenyVýsledok \+ replay fingerprint

## **Kroky (tabuľka)**

| Krok | Činnosť | Kto | Výstup / STOP |
| :---- | :---- | :---- | :---- |
| 1 | Request \+ agent\_id | Agent / ľudský initiator | correlation\_id |
| 2 | Register \+ scope check | Runtime | DENY ak mimo |
| 3 | Policy evaluate | Policy engine | ALLOW/DENY/ESCALATE |
| 4 | Auto draft ALEBO human gate | Agent / owner / L2–L4 | ÁNO event |
| 5 | Immutable audit | Audit store | event\_id |
| 6 | Execute / Deny | Runtime | result \+ replay |

* DENY → vždy ticket; nikdy silent continue  
* Platba / send / merge / sanctions write / policy change → vždy ľudské ÁNO  
* AML / export / whistleblowing citlivé → dual control (05)  
* Suma podľa L1 1 000 / L2 10 000 / L3 50 000 / L4 Predstavenstvo; dary 500 EUR samostatne

IOTA Defence a.s. · 09\_Flowcharts · FC-16 · NÁVRH v1.0 · 6\. 10\. 2026 · 07\_AI-Governance