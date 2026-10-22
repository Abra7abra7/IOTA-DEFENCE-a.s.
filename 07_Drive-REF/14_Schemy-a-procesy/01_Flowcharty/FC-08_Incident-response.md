# **FC-08 · Incident response**

IOTA Defence a.s. · IČO: \[DOPLNIŤ\] · Verzia 1.0 · 6\. 10\. 2026 · Vypracoval: Márian Stančík · Interné – Dôverné

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

**Mapovanie:** Schéma 08b · Logging kap. 8–9 · BCP/DR

**1\. Detekcia**SIEM P1–P4 · hlásenie zamestnanca · dodávateľ

**↓**

**2\. Klasifikácia**Kyber / GDPR / Utajované / ABAC-sankcie · závažnosť

**↓**

**3\. Interná notifikácia**CISO / Bezp. manažér / CCO · krízový štáb pri P1

**↓**

**4\. Izolácia a dôkazy**Blokácia účtov · EDR · zachovanie logov

**↓**

**5\. Hlásenie orgánom**NIS2 NBÚ 24h/72h/1 mes. · ÚOOÚ 72h · US NBÚ bezodkladne · Legal

**↓**

**6\. Obnova \+ poučenie**DR runbook · nápravy · report Predstavenstvu/DR

## **Kroky (tabuľka)**

| Krok | Činnosť | Kto | Výstup / STOP |
| :---- | :---- | :---- | :---- |
| 1 | Detekcia | IT/SOC/kdokoľvek | Čas zistenia |
| 2 | Klasifikácia | Incident owner | Typ+severita |
| 3 | Notifikácia | CISO/gestor | Strom kap.7 BCP |
| 4 | Izolácia | IT+CISO | Opatrenia |
| 5 | Hlásenie orgánom | CISO/DPO/Bezp./Legal | Potvrdenia |
| 6 | Obnova \+ lessons learned | Krízový štáb | Report |

> **Rozhodovacie body (diamanty):**

> * P1 (ransomvér, break-glass, IBAN bez 4 očí, exfiltrácia)? → ihneď CISO \+ krízový štáb  
> * Osobné údaje? → DPO · ÚOOÚ do 72 h  
> * Utajované? → Bezp. manažér · NBÚ bezodkladne

---

IOTA Defence a.s. · 09\_Flowcharts · NÁVRH v1.0 · 6\. 10\. 2026 · Limity EUR a IČO: \[DOPLNIŤ\]