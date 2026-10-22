**FC-14 · Logging / monitoring – eskalácia**  
IOTA Defence a.s. · IČO: \[DOPLNIŤ\] · Verzia 1.0 · 6\. 10\. 2026 · Márian Stančík · Interné – Dôverné  
**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**  
**Mapovanie:** GAP FILL · Proces 06\_Logging · FC-08  
**Tok:** **1** Detekcia alertu **→** **2** Triáž P1–P4 **→** **3** Reakcia podľa SLA \[DOPLNIŤ\] **→** **4** Eskalácia na IR/BCP

| Krok | Činnosť | Kto | Výstup / STOP |
| :---- | :---- | :---- | :---- |
| 1 | Detekcia alertu | SIEM/SOC/IT | Ticket |
| 2 | Triáž P1–P4 | SOC/IT/CISO | Priorita |
| 3 | Reakcia podľa SLA \[DOPLNIŤ\] | CISO/IT | Opatrenie |
| 4 | Eskalácia na IR/BCP | CISO/gestor | FC-08 / FC-15 |

**Rozhodovacie body:**

> * Break-glass / globálny admin / IBAN bez 4 očí / ransomvér → P1  
> * Výpadok zberu logov kritického zdroja → P2

*IOTA Defence a.s. · 09\_Flowcharts · NÁVRH v1.0 · EUR/IČO: \[DOPLNIŤ\]*