# **05 · Dual control a replay**

IOTA Defence a.s. · IČO 00000000 (FIKTÍVNE — pred zápisom do ORSR)1.0NÁVRH

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

## **1\. Dual control (4 oči / 2 agenti)**

Pri kritických verdiktoch nestačí jeden agent ani jeden človek v roli „pripravil \+ schválil“.

| Scenár | 1\. kontrola | 2\. kontrola | Min. úroveň |
| :---- | :---- | :---- | :---- |
| AML hit / podozrenie | Agent draft \+ CCO | 2\. človek (Legal / Predstavenstvo) alebo 2\. agent \+ človek | L3+ |
| Export / sankcie DENY | ECO | CCO alebo Predstavenstvo | L3 / L4 |
| Whistleblowing (citlivé rozhodnutie) | Zodpovedná osoba (Pol. 22\) | CCO / Predstavenstvo (bez odhalenia identity oznamovateľa mimo potreby) | podľa Pol. 22 |
| Platba nad L2 | Financie | Manažér / CCO podľa limitu | L2–L4 |
| Zmena Agent register / policy rules | CISO/CCO návrh | Predstavenstvo (Mino) | L4 |

Tá istá osoba (ani agent s rovnakým agent\_id) nesmie byť zároveň initiator aj final approver pri dual-control scenároch.

## **2\. Replay**

* Každý beh musí byť replayovateľnýinput\_hashagent\_versionrule\_versionpolicy\_decision  
* Replay je read-only  
* Odchýlka pri replay \= incident (FC-08) \+ report 2\. línie.  
* Frekvencia vzoriek: \[DOPLNIŤ — napr. 5 % gated / 100 % DENY\] mesiaca.

## **3\. Evidence pack (pri audite / NIS2)**

* event\_id \+ correlation\_id  
* input\_hash \+ uložený snapshot vstupu (redakcia PII podľa GDPR/DPO)  
* rule\_id \+ rule\_version \+ Doc odkaz  
* Ľudské ÁNO (čas, osoba)  
* Výsledok execute / deny

## **4\. Väzba na 3 línie**

| Línia | Úloha pri AI |
| :---- | :---- |
| 1\. (agenti \+ prevádzka) | Vykonávajú podľa ABAC; logujú; eskalujú |
| 2\. (CCO, CISO, ECO, DPO, Legal) | Policy rules, dual control, monitoring výnimiek |
| 3\. (interný audit / DR) | Nezávislý test replay a súladu; report DR (Jano/Fero/Kamil) |

IOTA Defence a.s. · 07\_AI-Governance · 05\_Dual-control-a-replay · NÁVRH v1.0 · 6\. 10\. 2026 · Márian Stančík · Interné – Dôverné