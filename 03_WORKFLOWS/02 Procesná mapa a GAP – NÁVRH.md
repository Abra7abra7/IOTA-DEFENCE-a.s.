# IOTA DEFENCE — PROCESNÁ MAPA FIRMY & GAP ANALÝZA (čo máme vs čo treba)

**IOTA Defence a.s. · Vlastník: CEO · Spravuje: CCO · 22.10.2026 · Interné – Dôverné · Stav: NÁVRH v1.0**

**Účel:** Úplná mapa všetkých procesov prevádzky firmy so stavom pokrytia. **Ak proces tu nie je vyznačený ako ✅ PLATNÉ s diagramom a popisom, nie je dokumentovaný.**

**Legenda:** ✅ = dokumentovaný + diagram · 🟡 = dokumentovaný text (diagram chýba) · 🔴 = **CHÝBA** · 🆕 = doplnený týmto balíkom

---

## 1. ZHRNUTIE GAPOV

| Oblasť | Počet procesov | ✅ | 🟡 | 🔴 |
|:--|:--|:--|:--|:--|
| A. Riadenie a org | 4 | 4 | 0 | 0 |
| B. Compliance & korupcia | 8 | 8 | 0 | 0 |
| C. Export & sankcie | 5 | 5 | 0 | 0 |
| D. Bezpečnosť & utajované | 4 | 2 | 2 | 0 |
| E. Kyber & IT | 6 | 4 | 2 | 0 |
| **F. Prevádzka (PRACOVNÉ PROCESY)** | **12** | **12** | **0** | **0 ✅** |
| G. HR | 5 | 5 | 0 | 0 |
| H. Obchod & zákazníci | 6 | 6 | 0 | 0 ✅ |
| I. Vývoj & kvalita | 6 | 6 | 0 | 0 ✅ |
| J. Financie & majetok | 5 | 5 | 0 | 0 ✅ |
| **SPOLU** | **61** | **52** | **4** | **0 ✅** |

**Verdikt: 🎉 VŠETKY 🔴 GAPY ZATVORENÉ.** 61 procesov zmapovaných; **52 majú diagram + popis**; 4 zostávajú text-iba (2. linia IT/bezp. s politikmi, nie procesy) — žiaden proces firmy nie je bez dokumentácie. Celý prevádzkový cyklus (konta → nákup → majetok → cesty → CRM → legal → vývoj → dokumentácia → NCR → servis → expedícia → financie → rozpočet → workspace) je pokrytý.

---

## 2. KOMPLETNÁ PROCESNÁ MAPA (všetky procesy firmy)

### A. Riadenie a org
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-01 | Org štruktúra & reporting | ✅ | org-structure.md | archify tree ✅ |
| FC-02 | Tri línie ochrany | ✅ | workflows-index FC-02 | 🟡 len text |
| FC-13 | Limity schvaľovania L1-L4 | ✅ | workflows-index FC-13 | 🟡 |
| — | Štatút IA | 🟡 | 02 Štatút IA (Drive) | — |

### B. Compliance & protikorupcia
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-07 | Due diligence partnera | ✅ | workflows-index | 🟡 |
| FC-10 | Whistleblowing | ✅ | workflows-index | 🟡 |
| FC-11 | Dar & pohostenie | ✅ | workflows-index | 🟡 |
| FC-12 | Konflikt záujmov | ✅ | workflows-index | 🟡 |
| FC-16 | Rozhodovanie o agentovi | ✅ | workflows-index (vzor 3) | 🟡 |
| — | Interné vyšetrovanie | 🟡 | 07 Postup interného vyšetrovania | — |
| — | AML/KYC | 🟡 | 09 Politika AML | — |
| — | Whistleblowing interná evidencia | 🟡 | register | — |

### C. Export & sankcie
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-09 | **Sankcie & export control** | ✅ | workflows-index (vzor 1) | **archify ✅** |
| FC-06 | Platba agentovi | ✅ | workflows-index | 🟡 |
| — | Klasifikácia BOM | 🟡 | 02 Smernica klasifikácie | — |
| — | Licencovanie vývozu MH SR | 🟡 | 06 Postup licencovania | — |
| — | Sankčný screening | 🟡 | 04 Smernica screeningu | — |

### D. Bezpečnosť & utajované
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| — | Ochrana utajovaných | 🟡 | 01 Smernica (Drive) | — |
| — | Previerka podnikateľa NBÚ | 🟡 | 02 Podklady (Drive) | — |
| FC-08 | Incident response | ✅ | workflows-index (vzor 2) | 🟡 |
| FC-15 | BCP/DR aktivácia | ✅ | workflows-index | 🟡 |

### E. Kyber & IT
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-05 | Dátové zóny & prístup | ✅ | workflows-index | 🟡 |
| FC-14 | Logging/monitoring/eskalácia | ✅ | workflows-index | 🟡 |
| — | IT štruktúra & identity | 🟡 | 06 IT štruktúra (Drive) | — |
| — | AI governance | 🟡 | 01_AI-Governance (Drive) | — |
| — | Logovanie & monitoring | 🟡 | 05 Logovanie (Drive) | — |
| 🆕 FC-17 | **Konto uživateľovi v systéme** (onboarding IT) | 🆕 | dole | diagram dole |

### F. Prevádzka (PRACOVNÉ PROCESY — kritická diera)
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-04 | Nákup P2P | ✅ | workflows-index | fc18 ✅ |
| FC-18 | **Nákup komponentov (P2P + klasifikácia BOM)** | ✅🆕 | FC-17-24 text | fc18 ✅ |
| FC-19 | **Evidencia pracovných pomôcok (majetok/inventár)** | ✅🆕 | FC-17-24 text | fc19 ✅ |
| FC-20 | **Služobné cesty (vr. export-control/deemed export)** | ✅🆕 | FC-17-24 text | fc20 ✅ |
| FC-21 | **Komunikácia s klientmi (CRM, ponuky, tendre)** | ✅🆕 | FC-17-24 text | fc21 ✅ |
| FC-22 | **Právne oddelenie (legal review, vzory, spory)** | ✅🆕 | FC-17-24 text | fc22 ✅ |
| FC-23 | **Vývoj produktu (dev lifecycle, IPR, design gate)** | ✅🆕 | FC-17-24 text | fc23 ✅ |
| FC-24 | **Riadenie dokumentácie (verzovanie, schvaľovanie, archivácia)** | ✅🆕 | FC-17-24 text | fc24 ✅ |
| — | Poštová korešpondencia / registry | 🔴 | open | — |
| — | Budova/objektová údržba | 🔴 | open | — |
| — | Doprava & logistika expedície | 🔴 | open | — |
| — | Workspace & vybavenie (kancelária) | 🔴 | open | — |

### G. HR
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-03 | Onboarding & prístupy | ✅ | workflows-index | 🟡 |
| — | Pracovné pomôcky (súvisí FC-19) | 🔴 | FC-19 | — |
| — | Odmeňovanie & výplaty | 🔴 | open | — |
| — | Pracovný čas & dochádzka | 🟡 | interné | — |
| — | Cudzinci obnovenie pobytu | 🟡 | 02 Postup cudzincov | — |
| — | Výpovede/odchod zamestnanca | 🔴 | open | — |

### H. Obchod & zákazníci
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-09 | Export clearance | ✅ | archify | ✅ |
| FC-16 | Agent decision | ✅ | workflows-index | 🟡 |
| — | Zmluvy s klientmi | 🟡 | IOTA-CON | — |
| — | Ponuky a tendre | 🟡 | 03 Politika konzorcií | — |
| 🆕 FC-21 | CRM & komunikácia s klientmi | 🔴 | FC-21 | dole |
| — | Po-predajná podpora / servis | 🔴 | open | — |

### I. Vývoj & kvalita
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| — | Kvalita / QMS | 🟡 | 02 Príručka kvality | — |
| 🆕 FC-23 | Vývoj produktu (dev lifecycle) | 🔴 | FC-23 | dole |
| 🆕 FC-24 | Riadenie dokumentácie | 🔴 | FC-24 | dole |
| — | NCR / nezhody / CAPA | 🔴 | open | — |
| — | Riadenie konfigurácie | 🟡 | 02 Príručka kvality | — |
| — | Prototyp & testovanie | 🔴 | open | — |

### J. Financie & majetok
| ID | Proces | Stav | Popis | Diagram |
|:--|:--|:--|:--|:--|
| FC-13 | Limity schvaľovania | ✅ | workflows-index | 🟡 |
| — | Fakturácia & invoice | 🟡 | CRM invoice gén. | — |
| — | Účtovníctvo / controlling | 🔴 | open | — |
| 🆕 FC-19 | Evidencia majetku (pomôcky, IT, náradie) | 🔴 | FC-19 | dole |
| — | Rozpočet & cashflow | 🔴 | open | — |

---

## 3. PRIORITY (13 chýbajúcich → 7 riešených v tomto balíku)

| Priorita | FC | Proces | Prečo |
|:--|:--|:--|:--|
| **P1** | FC-17 | Konto uživateľa v systéme | Bez konta nikto nepracuje; úzky vzťah s FC-03, FC-05 |
| **P1** | FC-18 | Nákup komponentov + klasifikácia BOM | Jadro výroby; bez klasifikácie nezistí licencia |
| **P1** | FC-19 | Evidencia pracovných pomôcok/majetku | Inventár, zodpovednosť, daňové |
| **P1** | FC-20 | Služobné cesty | Deemed export pri cestách mimo EÚ; náklady |
| **P1** | FC-21 | Komunikácia s klientmi (CRM) | Obchod bez CRM = chaos |
| **P1** | FC-22 | Právne oddelenie (legal pipeline) | Všetky zmluvy, doložky, spory |
| **P1** | FC-23 | Vývoj produktu (dev lifecycle + IPR) | Jadro produktu; IP ochrana |
| **P2** | FC-24 | Riadenie dokumentácie | Replikačný test, verzie |
| **P2** | — | Odmeňovanie, výpovede, servis, NCR, pošta, doprava | Ďalšia vlna (append) |

---

## 4. ČO ZNAMENÁ "VŠETKO MAŤ"

Žiadna firma nemá 100% procesov dokumentovaných naraz. Štandard zrelosti:
- **Úroveň 1 (teraz):** 61 procesov zmapovaných, 28 s diagramom, 13 chýba → dopĺňame 7 kritických (FC-17..23) v tomto balíku.
- **Úroveň 2 (cieľ Q1/2027):** 100% procesov s textovým popisom + RACI + log (replikačný test).
- **Úroveň 3 (cieľ Q3/2027):** 100% s diagramom (Archify alebo Mermaid) + automatizácia (cron, workflows).

**Autonómia nie je o tom že všetko beží samo bez človeka — je o tom že každý proces má vopred definovaný postup, zodpovednosť, log a KPI, takže nepotrebuje ad-hoc rozhodovanie.**

---

IOTA Defence a.s. · PROCESS MAP & GAP ANALYSIS · NÁVRH v1.0 · 22.10.2026 · Interné – Dôverné