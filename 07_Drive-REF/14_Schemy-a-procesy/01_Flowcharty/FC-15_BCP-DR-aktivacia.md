# **FC-15 · BCP/DR – aktivácia krízového štábu**

IOTA Defence a.s. · IČO: \[DOPLNIŤ\] · Verzia 1.0 · 6\. 10\. 2026 · Vypracoval: Márian Stančík · Interné – Dôverné

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

**Mapovanie:** GAP FILL · Proces 05\_BCP-DR · väzba FC-08

**Narušenie kritického procesu**Kyber · výpadok IT · lokalita · kľúčová osoba/dodávateľ

**↓**

**Hlásenie**Service desk \+ CISO (US → Bezp. manažér) · telefón, nie len e-mail

**↓**

**Klasifikácia dopadu**RTO/RPO z BIA \[DOPLNIŤ\] · P1?

**↓**

**Aktivácia krízového štábu**Vedúci \= gestor bezpečnosti

**↓**

**DR runbook podľa scenára**Ransomvér / IdP / ERP / BEC / lokalita

**↓**

**Obnova podľa priority**1 IdP → komunikácia → platby → ERP → ostatné

**↓**

**Poincidentná správa**Predstavenstvo \+ DR · nápravy · test obnovy

## **Kroky (tabuľka)**

| Krok | Činnosť | Kto | Výstup / STOP |
| :---- | :---- | :---- | :---- |
| 1 | Detekcia narušenia | Kdokoľvek | Hlásenie |
| 2 | Aktivácia štábu | Gestor bezpečnosti | Zvolanie |
| 3 | Izolácia / náhradný postup | CISO/IT/Výroba | Runbook |
| 4 | Obnova podľa priorít | IT \+ vlastníci | RTO/RPO |
| 5 | Lessons learned | Štáb | Report |

> **Rozhodovacie body (diamanty):**

> * Utajované prostredie? → mimo tohto BCP (Bezp. manažér / NBÚ)  
> * Počas krízy zmena IBAN? → STOP (len 4 oči \+ overenie mimo pásma)

---

IOTA Defence a.s. · 09\_Flowcharts · NÁVRH v1.0 · 6\. 10\. 2026 · Limity EUR a IČO: \[DOPLNIŤ\]