# **FC-04 · Nákup → Objednávka → Platba (P2P)**

IOTA Defence a.s. · IČO: \[DOPLNIŤ\] · Verzia 1.0 · 6\. 10\. 2026 · Vypracoval: Márian Stančík · Interné – Dôverné

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

**Mapovanie:** Schéma 04 · Proces 03\_Nakup · Limity 06\_Limity

**1\. Požiadavka**Žiadateľ: čo, prečo, koľko, kategória

**↓**

**2\. Schválenie podľa limitu**L1 manažér / L2+Financie / L3+CCO / L4 Predstavenstvo

**↓**

**3\. Objednávka (PO)**Nákup · len preverený dodávateľ

**↓**

**4\. Príjem / akceptácia**Žiadateľ / sklad / kvalita

**↓**

**5\. Faktúra · 3-way match**PO \= príjem \= faktúra · Financie

**↓**

**6\. Platba 4 oči**Zadávateľ ≠ autorizátor · zamknutý IBAN

**↓**

**STOP podmienky**Bez PO · zmena IBAN bez overenia · hotovosť agentovi · sankčná zhoda · konflikt · delenie nákupu

## **Kroky (tabuľka)**

| Krok | Činnosť | Kto | Výstup / STOP |
| :---- | :---- | :---- | :---- |
| 1 | Požiadavka | Žiadateľ | Formulár/ERP |
| 2 | Schválenie limitu / ABAC | Manažér / Financie / CCO | E-schválenie |
| 3 | PO preverenému dodávateľovi | Nákup | Číslo PO |
| 4 | Príjem / akceptácia | Žiadateľ/sklad | Príjemka |
| 5 | 3-way match | Financie | Zaúčtovanie |
| 6 | Platba 4 oči | Financie | Výpis banky |

> **Rozhodovacie body (diamanty):**

> * Hodnota → ktorá úroveň L1–L4? (pozri FC-13)  
> * Nový dodávateľ? → vendor onboarding pred PO  
> * Dar/pohostenie verejnému funkcionárovi? → vždy CCO vopred  
> * Zmena IBAN? → spätné telefonické overenie \+ 4 oči

---

IOTA Defence a.s. · 09\_Flowcharts · NÁVRH v1.0 · 6\. 10\. 2026 · Limity EUR a IČO: \[DOPLNIŤ\]