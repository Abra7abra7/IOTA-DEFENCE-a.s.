# IOTA Defence a.s. — Organizačná štruktúra & reporting (Org-Chart)

Vizualizácia org-struktúry. Primárny artefakt: **interaktívny Archify diagram** (`iota-org-tree-archify.html` — zoom/search/chapters, dark+light téma, PNG export). Alternatíva: Mermaid (`org-structure-A.png`, `org-reporting-B.png`). Zdroj: FC-01 z pričinok (NÁVRH v1.0, 6.10.2026).

> **Archify skill** (tt-a1i/archify v3.2) inštalovaný cez `npx skills add tt-a1i/archify -g`. Candidate: `iota-org-tree.candidate.json`; render: `iota-org-tree-archify.html` (all 4 gates pass, SHA-256 receipt v `.archify/`).

---

## A) Org-Tree — čistá verzia

```mermaid
flowchart TD
    VZ["VZ<br/>Valné zosťavanie<br/>(akcionári)"] --> DR
    VZ --> PS
    DR["DOZORNÁ RADA<br/>kontrolný orgán"] --> PS

    subgraph GOV["VEDENIE"]
        PS["PREDSTAVENSTVO<br/>štatutár · gestor compliance + bezpečnosť"]
    end

    subgraph L2["2. LÍNIA — dohľad / compliance (reportujú Predstavenstvu)"]
        CCO["CCO"]
        ECO["ECO"]
        LEG["Legal"]
        DPO["DPO (ext.)"]
        BEZ["Bezp. riaditeľ"]
        CIS["CISO"]
    end

    subgraph L1["1. LÍNIA — prevádzka"]
        OBD["Obchod"]; NAK["Nákup"]; VYR["Výroba"]; FIN["Financie"]
        HR["HR"]; IT["IT"]; KVL["Kvalita"]
    end

    L3["3. LÍNIA<br/>Interný audit (ext.)"]

    PS --> L1
    PS --> L2
    L3 --> DR
```

---

## B) Reporting & rozhodovacie väzby (čisté)

```mermaid
flowchart LR
    L1["1. LÍNIA<br/>vlastník rizík · RACI"]
    L2["2. LÍNIA<br/>CCO · ECO · CISO · Bezp. · Legal · DPO<br/>STOP-right"]
    L3["3. LÍNIA<br/>Interný audit"]
    PS["PREDSTAVENSTVO<br/>štatutár"]
    DR["DOZORNÁ RADA<br/>kontrolný"]

    L1 -->|"riziko/incident/eskalácia"| L2
    L2 -->|"politiky · monitoring · STOP"| L1
    L2 -->|"štvrťročný report U-03"| PS
    L3 -->|"správa IA"| DR
    PS -->|"uznesenia"| L2
    DR -->|"dohľad"| PS
```

---

**Pravidlo kumulácie (FC-02):** 1.+2. línia u jednej osoby → STOP (výnimka: Predstavenstvo). Gestor nesmie zodpovedať za predaj. CISO oddelený od IT prevádzky.

---
IOTA Defence a.s. · 02-ORG-VIZ · NÁVRH v1.0 · 22.10.2026 · Interné – Dôverné