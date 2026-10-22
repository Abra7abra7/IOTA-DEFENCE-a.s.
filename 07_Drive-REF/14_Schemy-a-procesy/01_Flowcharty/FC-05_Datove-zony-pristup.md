# **FC-05 · Dátové zóny – rozhodovací tok prístupu**

IOTA Defence a.s. · IČO: \[DOPLNIŤ\] · Verzia 1.0 · 6\. 10\. 2026 · Vypracoval: Márian Stančík · Interné – Dôverné

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

**Mapovanie:** Schéma 05 · Tech-stack kap. 3 · Onboarding kap. 4

**Žiadosť o prístup k dátam**Systém / priečinok / projekt

**↓**

**Ktorá zóna?**Verejné / Interné / Dôverné / Utajované

**↓**

**Verejné**Bez schválenia (publikovanie: Marketing+ECO)

**Interné**Vlastník vzťahu · freelancer \= len projekt

**↓**

**Dôverné**Vlastník dát \+ CISO · need-to-know

**Utajované**Len Bezp. manažér · previerka NBÚ

**↓**

**Pridelenie cez role skupiny \+ MFA**Recertifikácia: bežné ročne · Dôverné polročne · Freelancer pri predĺžení

## **Kroky (tabuľka)**

| Krok | Činnosť | Kto | Výstup / STOP |
| :---- | :---- | :---- | :---- |
| 1 | Určiť zónu obsahu | Vlastník dát | Klasifikácia |
| 2 | Schválenie podľa matice | Vlastník / CISO / Bezp. manažér | Áno/Nie |
| 3 | Pridelenie skupiny IAM | IT | Audit trail |
| 4 | Recertifikácia / offboarding | Vlastník \+ IT | Odobratie |

> **Rozhodovacie body (diamanty):**

> * Freelancer \+ Dôverné so sťahovaním? → STOP  
> * Utajované v bežnom cloude? → STOP  
> * AI nástroje s Dôvernými/Utajovanými? → STOP

---

IOTA Defence a.s. · 09\_Flowcharts · NÁVRH v1.0 · 6\. 10\. 2026 · Limity EUR a IČO: \[DOPLNIŤ\]