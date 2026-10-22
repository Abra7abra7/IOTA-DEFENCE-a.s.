# IOTA Defence a.s. — START HERE (vstupná mapa celého package)

**IČO: [DOPLNIŤ] · 22.10.2026 · Interné – Dôverné · NÁVRH**
**Účel:** Toto je **jediný vstupný bod**. Začni tu → celá firma fungovanie je prehľadné v 5 logických krokách. Každý dokument je link v package a zrkadlo na Google Drive.

> ⚠️ NIE JE PRÁVNA RADA. Overiť advokátom + aktuálnymi predpismi; čísla [DOPLNIŤ] vyplniť pred schválením.

---

## JEDNOODSTAVKOVÝ ZOZNAM (model)

**"Firma = 3 línie ochrany (prevádzka + dohľad + audit) nad riadeným systémom procesov (každý: vlastník → workflow → log → KPI), s rolámi, registriami a legislatívou všetko logované a trackovatelné."**

Celý package odpovedá na 6 otázok:

| # | Otázka | Dokument | Vizual |
|:--|:--|:--|:--|
| 1 | **Kto je kto?** (role, popis, zodpovednosti) | `01_OPS-MANUAL/02 ROLES register – NÁVRH.md` | roles-register archify |
| 2 | **Aká je org štruktúra + kompetencie?** | `02_ORG-VIZ/01 Org štruktúra – NÁVRH.md` | org-competencies.html |
| 3 | **Aké sú záväzné procesy?** (35× workflow) | `03_WORKFLOWS/01 WF index – NÁVRH.md` | 35 FC diagramy |
| 4 | **Ako riadiame IP a bezpečnosť?** | `04_IP-SECURITY/01 IP a bezpečnosť – NÁVRH.md` | ip-security-zones.html |
| 5 | **Aká je legislatíva (licencie, NBÚ, IT)?** | `05_REGULATORY/01 Regulatory mapa – NÁVRH.md` | regulatory-map.html |
| 6 | **Kto je konkurencia (Anduril/CSG)?** | `06_COMPETITIVE/` | competitive-map.html |

---

## LOGICKÁ ŠTRUKTÚRA (ako riešiame problémy)

```
A) LŪDIA (roles.md)            — KTO: rolá, zodpovednosti, línii
B) ORG & VEDENIE (02-ORG-VIZ)  — AKÁ: organizačná štruktúra, 3 línie, reporting
C) PROCESY (03-WORKFLOWS)      — AKO: 35 záväzných procesov (FC-01..35)
    každý: owner → workflow → log → KPI  (replikačný test)
D) IP & KYBER (04-IP-SECURITY) — ČO CHRÁNIME: zóny Z0-Z3, utajované, IT
E) ZÁKONY (05-REGULATORY)      — ČO MUSME: licencie, previerky NBÚ, sankcie
F) TRH (06-COMPETITIVE)        — KDE STOJÍME: vs Anduril, CSG
```

---

## NAJLEPŠÁ CESTA ČÍTANIA (20 min)

1. **`01_OPS-MANUAL/02 ROLES register – NÁVRH.md`** (3 min) — kto je kto.
2. **`02_ORG-VIZ/org-competencies.html`** (2 min) — org + kompetencie (Archify).
3. **`01_OPS-MANUAL/01 OPS Manual – NÁVRH.md`** sekcie 1–3 (5 min) — 3 línie + registre.
4. **`03_WORKFLOWS/02 Procesná mapa a GAP – NÁVRH.md`** (3 min) — celý procesný sladky.
5. **`04_IP-SECURITY/01 IP a bezpečnosť – NÁVRH.md`** + vizual (2 min).
6. **`05_REGULATORY/01 Regulatory mapa – NÁVRH.md`** + vizual (3 min).

---

## KĽÚČOVÉ PRAVIDLÁ (pitfalls — NEPORUŠIŤ)

1. **RACI:** každá úloha má **presne jednu A** (dvojitý A = STOP). → `raci.md`
2. **Tri línie:** 1L+2L u jednej osoby = STOP; gestor nesmie zodpovedať za predaj. → FC-02
3. **Bez workflow + log = proces nevydržá.** Žiadny výnimok.
4. **STOP-right (2L):** CCO/ECO/CISO/Bezp. môžu STOP — prelomí len Predstavenstvo (zápis + info DR).
5. **Limity L1-L4:** platba vždy 4-eyes; rizikový prípad → min L3; delenie pod limit = STOP. → FC-13
6. **IP:** utajované a evidencia výbušnín NIKDY na Google Drive. Z3 → osobitné pracovisko. → z.215/2004, z.58/2014
7. **Export:** bez clearance/ITAR-free žiadny prenos, expedícia, vzdialený servis. → FC-09,31,32

---

## REŠTOVANIE PROBLÉMOV (troubleshooting)

| Máme otázku... | Čítame... |
|:--|:--|
| Kto zodpoveda za X? | `roles.md` → `raci.md` (nájdi funkciu, potom A) |
| Aký je postup pri Y? | `workflows-index.md` (ID) → konkrétny FC diagram + text |
| Musme licenciu na Z? | `regulatory-map.md` (povolenia) |
| Je to utajované? | `ip-security.md` (klasifikácia Z0-Z3) |
| Vidím incident / riziko? | FC-08 (incident) / FC-14 (alert) / FC-15 (BCP) |
| Chceme platba/nákup? | FC-04 → limity FC-13 |
| Nový človek? | FC-03/17 onboarding → FC-26 offboarding |

---

## GOOGLE DRIVE ZRKADLO

- **Package:** My Drive > `01_PROJEKTY_A_SUBJEKTY` > `IOTA DEFENCE a.s.`.
- **Zdrojové pôvodné dokumenty:** zrkadlo v `07_Drive-REF/` (pôvodné texty 01_Spolocnost… 14_Schemy).
- **Pomenovávanie:** dokumenty `NN Názov – STAV`, priečinky `NN_Nazov-bez-diakritiky`, 99_Archiv.

---

IOTA Defence a.s. · 00-START-HERE · NÁVRH v1.0 · 22.10.2026 · Interné – Dôverné