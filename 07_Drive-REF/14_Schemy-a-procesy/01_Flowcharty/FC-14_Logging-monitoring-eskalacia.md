# **FC-14 · Logging / monitoring – eskalácia alertov**

IOTA Defence a.s. · IČO: \[DOPLNIŤ\] · Verzia 1.0 · 6\. 10\. 2026 · Vypracoval: Márian Stančík · Interné – Dôverné

**NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM.**

**Mapovanie:** GAP FILL · Proces 06\_Logging · väzba na FC-08

**Alert zo SIEM / EDR / IdP / ERP**Use-case detekcia

**↓**

**Priorita P1–P4**P1 kritická · P2 vysoká · P3 stredná · P4 nízka

**↓**

**P1**CISO ihneď → gestor → krízový štáb (FC-08)

**P2**CISO \+ incident owner · izolácia

**↓**

**P3**IT prevádzka · denný prehľad CISO

**P4**Týždenný prehľad

**↓**

**Väzba na incident response**Ak potvrdený incident → FC-08 kroky 2–6

## **Kroky (tabuľka)**

| Krok | Činnosť | Kto | Výstup / STOP |
| :---- | :---- | :---- | :---- |
| 1 | Detekcia alertu | SIEM/SOC/IT | Ticket |
| 2 | Triáž P1–P4 | SOC/IT/CISO | Priorita |
| 3 | Reakcia podľa SLA \[DOPLNIŤ\] | CISO/IT | Opatrenie |
| 4 | Eskalácia na IR / BCP | CISO/gestor | FC-08 / FC-15 |

> **Rozhodovacie body (diamanty):**

> * Break-glass použitie / nový globálny admin / zmena IBAN bez 4 očí / ransomvér? → P1  
> * Výpadok zberu logov kritického zdroja? → P2

---

IOTA Defence a.s. · 09\_Flowcharts · NÁVRH v1.0 · 6\. 10\. 2026 · Limity EUR a IČO: \[DOPLNIŤ\]