

| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. |
| :---: |

# **01 · IT štruktúra a identity – defence SME (\~30 osôb)**

IOTA Defence a.s. · IČO 00000000 (FIKTÍVNE — pred zápisom do ORSR) · Verzia 1.0 · 7\. 10\. 2026 · Márian Stančík · Interné – Dôverné · Stav: NÁVRH  
Mapovanie: 07\_AI-Governance (ABAC, L1–L4, 02\_Audit-schema) · FC-07 Due diligence partnera · FC-09 Sankcie a export control · FC-15 BCP/DR · Politika InfoSec / NIS2

## **1\. Účel a výhrada**

> * **Účel:** navrhnúť cieľový model IT a správy identít pre \~30 interných zamestnancov \+ externistov (freelanceri, partneri) v defence / dual-use prostredí tak, aby bol prevádzkovateľný malým tímom a obhájiteľný voči GDPR, NIS2 (SK: zákon č. 69/2018 Z. z. v znení novely transponujúcej NIS2) a exportnej kontrole (nariadenie (EÚ) 2021/821).  
> * **Rozsah:** identita, prístupy, dáta, audit, procesy. **Mimo rozsahu:** utajované skutočnosti podľa zákona č. 215/2004 Z. z. – tie patria výhradne do certifikovaného systému podľa NBÚ (žiadna z variantov A–D ich nenahrádza).  
> * **Výhrada:** NÁVRH na diskusiu. Nie je právna rada ani licenčné posúdenie. Licencie, ceny a zaradenie pod NIS2 overiť s Legal, CISO a dodávateľom pred rozhodnutím.

## **2\. Cieľový model – vrstvy**

| Vrstva | Čo rieši | Minimálny štandard pre IOTA |
| :---- | :---- | :---- |
| **1 · IdP (identita)** | Jeden zdroj pravdy pre osoby, skupiny, servisné účty a AI agentov | Jeden tenant v EÚ; SSO (SAML/OIDC) pre všetky SaaS; MFA pre všetkých, phishing-resistant (FIDO2/passkey) pre adminov a zónu Controlled; 2 break-glass účty v trezore |
| **2 · Kolaborácia** | Mail, chat, dokumenty, videohovory | Firemné účty, žiadne súkromné úložiská; externé zdieľanie len cez pozvaných hostí s expiráciou |
| **3 · Dátové zóny** | Kde smú byť aké dáta | Public / Internal / Project / Controlled (kap. 5); označenie (label) \+ technické vynútenie |
| **4 · RBAC \+ ABAC** | Kto čo smie | RBAC \= roly (Obchod, Výroba, Financie, ECO, CISO…). ABAC \= atribúty: *employment\_type* (int/ext), *project\_ids*, *zone\_clearance*, *export\_screening* (výstup FC-07/FC-09), *device\_compliant*, *location=EU*, *contract\_end*. Rovnaký princíp ako ABAC pre agentov v 07\_AI-Governance (default max L1, fail-closed) |
| **5 · PAM** | Privilegované účty | Oddelené admin účty (bez mailu), just-in-time elevácia s časovým limitom, 4 oči na zmeny tenant politík; max. 2–3 globálni admini |
| **6 · Zariadenia** | Endpointy | MDM, šifrovanie disku, EDR, automatické záplaty; prístup do Project/Controlled len zo spravovaného zariadenia |
| **7 · Audit / SIEM** | Dôkazy a detekcia | Centrálny log (IdP, kolaborácia, endpointy, AI agenti podľa 02\_Audit-schema), append-only, alerty na kap. 7 |
| **8 · Procesy** | Ľudská vrstva | JML, externé prístupy, exportná brána, mesačná revízia, tabletop (kap. 6\) |

## **3\. Varianty A–D**

| Variant | Čo to je | Výhody | Nevýhody | EÚ / NIS2 fit | Fit pre 30-člennú dual-use firmu | Náklady / zložitosť |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **A · M365 \+ Entra ID (EU)** | Microsoft 365 (napr. Business Premium) s EU Data Boundary; Entra ID ako IdP; Intune, Defender, Purview labels | Všetko v jednom: IdP, MDM, EDR, DLP, labely, Conditional Access; veľa SK dodávateľov; štandard u obranných zákazníkov | US poskytovateľ (CLOUD Act); pokročilé funkcie (PIM, access reviews) vyžadujú vyššie licencie; riziko „klikania“ bez dokumentácie | Dobrý – dáta v EÚ, bohatý audit, hotové kontroly pre NIS2 opatrenia; suverenita kľúčov obmedzená | **Vysoký** – najrýchlejšia cesta k funkčnému štandardu | Licencie stredné; zložitosť nízka–stredná |
| **B · Google Workspace \+ Okta** | Workspace (vyššia edícia s data regions EU) na kolaboráciu; Okta (EU cell) ako IdP; MDM/EDR tretej strany | Jednoduchá kolaborácia; Okta silná v SSO a lifecycle; dobré pre firmy „cloud-native“ | Dvaja (až traja) US dodávatelia; MDM/EDR/DLP treba skladať; slabšia akceptácia u časti obranných zákazníkov (Office formáty) | Dobrý pri správnej edícii; viac zmlúv a DPA na správu | Stredný | Licencie stredné–vyššie (Okta navyše); zložitosť stredná |
| **C · Hybrid: EÚ cloud \+ Keycloak / on-prem pre citlivé** | Bežná práca v A alebo B; zóna Controlled na EÚ/on-prem infraštruktúre (napr. Nextcloud/súborový server \+ Keycloak, vlastné kľúče) | Kontrola nad kľúčmi a lokalitou pre exportne citlivé dáta; zníženie rizika CLOUD Act pre Controlled | Dva svety \= dve sady politík, logov, záloh; potrebná interná/externá prevádzka 24/7 pre on-prem | Veľmi dobrý pre Controlled; NIS2 vyžaduje preukázať rovnakú úroveň bezpečnosti aj pre on-prem časť | **Vysoký**, ak zákazník/licencia vyžaduje kontrolu kľúčov alebo EÚ-only prevádzku | Stredné–vyššie; zložitosť stredná–vysoká |
| **D · Plne suverénne EÚ (VPS / minimum US SaaS)** | EÚ hosting (VPS/privátny cloud); Keycloak, Nextcloud, Matrix/Element, open-source mail, vlastný SIEM | Maximálna suverenita a kontrola; žiadna závislosť na US poskytovateľoch | Prevádzku, záplaty, zálohy, EDR a detekciu nesiete sami; vyššie riziko chyby pri malom tíme; horšia UX | Suverenita výborná; NIS2 súlad závisí úplne od vlastnej prevádzky (najťažšie preukázať) | Nízky–stredný pre 30 osôb bez dedikovaného IT tímu | Licencie nízke, ľudské náklady vysoké; zložitosť vysoká |

## **4\. Odporúčanie (predvolené)**

| Predvolene variant A – „Entra first“. Jeden EÚ tenant M365, Entra ID ako jediný IdP (aj pre externistov ako hostí a pre AI agentov ako servisné identity), Intune \+ Defender, Purview labely mapované na dátové zóny. Pre \~30 osôb dáva najlepší pomer bezpečnosti, nákladov a prevádzkovateľnosti. |
| :---- |

**Kedy prejsť na C:** zákazník, licencia alebo ECO vyžaduje EÚ-only spracovanie a vlastné kľúče pre technické dáta; objem Controlled dát rastie; zmluvy s MO/NATO dodávateľmi obsahujú požiadavky na suverenitu. Postup: A ostáva pre Public/Internal/Project, Controlled sa presunie do C (federácia Entra ↔ Keycloak).  
**Kedy D:** len pri explicitnej požiadavke „bez US poskytovateľa“ a s rozpočtom na dedikovanú prevádzku (interný admin \+ zmluvný SOC). Pre 30 osôb neodporúčané ako štart.  
**Kedy B:** ak už firma beží na Google Workspace a migrácia by bola drahšia než prínos – vtedy Okta ako IdP a doplniť MDM/EDR.

## **5\. Dátové zóny**

| Zóna | Príklady | Kto | Externisti | Technické pravidlá | Schvaľuje prístup |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **Public** | Web, marketing, verejné katalógy (po kontrole ECO) | Všetci | Áno | Bez obmedzení; zverejnenie technických údajov len po ECO kontrole | Vlastník obsahu |
| **Internal** | Smernice, HR oznamy, interné procesy | Zamestnanci | Nie (výnimka cez projekt) | Label Internal; zákaz anonymných odkazov | Automaticky pri nástupe (JML) |
| **Project** | Ponuky, zmluvy, projektová dokumentácia bez exportne kontrolovaných technických dát | Členovia projektu (need-to-know) | Áno – menovite, s expiráciou, po FC-07 | Samostatný site/tím na projekt; hosť s expiráciou ≤ 90 dní; len spravované zariadenie alebo webový prístup bez sťahovania | Vlastník projektu (L2) |
| **Controlled** | Exportne kontrolovaná technológia a technické dáta (dual-use, vojenský materiál), dáta zákazníka so zmluvnými obmedzeniami | Menovite určené osoby s *export\_screening \= OK* | Len po exportnej bráne (FC-09) a ECO ÁNO | Šifrujúci label; phishing-resistant MFA; spravované zariadenie; prístup len z EÚ; zákaz preposielania/sťahovania na nespravované zariadenia; plný audit čítania | Vlastník dát \+ ECO (analogicky L3 z 03\_Escalation-matrix) |

Pozn.: Sprístupnenie technológie osobe mimo EÚ (aj cez cloud, e-mail alebo zdieľanú obrazovku) môže byť vývozom podľa nariadenia 2021/821 alebo prevodom podľa zákona č. 392/2011 Z. z. GDPR: namiesto ukladania štátnej príslušnosti v IdP používať odvodený atribút *export\_screening* (OK / STOP / v preverovaní); podklady drží ECO.

## **6\. Procesné checklisty**

### **6.1 Joiner – Mover – Leaver (JML)**

> * ☐ **Joiner:** žiadosť od HR/manažéra cez formulár (nie e-mail) → účet z HR záznamu, rola podľa pozície, zóna Internal; MFA registrácia v deň nástupu; spravované zariadenie; podpis NDA a IT pravidiel; prístup do Project/Controlled len samostatnou žiadosťou.  
> * ☐ **Mover:** pri zmene pozície/projektu sa staré roly *odoberajú* (nie len pridávajú nové); vlastník projektu potvrdí do 5 pracovných dní.  
> * ☐ **Leaver:** deaktivácia účtu v deň odchodu (pri konflikte okamžite), revokácia relácií a tokenov, odobratie zariadenia / remote wipe firemných dát, prevod vlastníctva súborov na manažéra, zmena zdieľaných hesiel v trezore, záznam do auditu.  
> * ☐ Všetky kroky majú ticket a sú dohľadateľné.

### **6.2 Externí a partneri**

> * ☐ Partner je v stave **SCHVÁLENÝ** podľa FC-07 (due diligence, sankčný screening) pred prvým prístupom.  
> * ☐ Zmluva / NDA s doložkami o bezpečnosti, exporte a GDPR (DPA, ak spracúva osobné údaje).  
> * ☐ Menovitý hosťovský účet (žiadne zdieľané účty), MFA povinná, expirácia ≤ 90 dní, interný sponzor zodpovedný za predĺženie.  
> * ☐ Prístup len do konkrétneho projektového priestoru; Internal a Controlled defaultne zakázané.  
> * ☐ Pri ukončení zmluvy alebo strate stavu SCHVÁLENÝ okamžité odobratie prístupu.

### **6.3 Exportná / sankčná brána (väzba na FC-09)**

> * ☐ Pred udelením prístupu do Controlled alebo zdieľaním technických dát navonok: ECO overí klasifikáciu dát (dual-use / vojenský materiál / bez kontroly).  
> * ☐ Screening osoby a organizácie (sankčné zoznamy, krajina, konečné použitie) – výstup *export\_screening* \= OK / STOP.  
> * ☐ Ak je potrebná licencia: bez platnej licencie prístup **STOP** (výnimky neexistujú – zhodne s FC-09).  
> * ☐ Udelenie prístupu \= ECO ÁNO zaznamenané v audite (kto, komu, aké dáta, licencia/odkaz, expirácia).  
> * ☐ AI agenti nesmú do Controlled zapisovať ani z nej exportovať bez ľudského ÁNO (03\_Escalation-matrix).

### **6.4 Mesačná revízia prístupov / audit**

> * ☐ Vlastníci projektov potvrdia členov a hostí (odobrať nepotrebných).  
> * ☐ ECO potvrdí zoznam osôb v Controlled a platnosť screeningov/licencií.  
> * ☐ CISO: zoznam adminov, break-glass test (štvrťročne), neaktívne účty \> 30 dní, účty bez MFA, zariadenia mimo súladu.  
> * ☐ Kontrola externého zdieľania (anonymné odkazy, zdieľanie na súkromné adresy).  
> * ☐ Kontrola AI agentov oproti Agent registru (scope, max L1).  
> * ☐ Výstup: krátky záznam (dátum, zistenia, nápravy) → štvrťročne do reportu 2\. línie Predstavenstvu (FC-01).

### **6.5 Incident tabletop (light, 60–90 min, polročne)**

> * ☐ Scenár 1: kompromitovaný účet externistu s prístupom do Project.  
> * ☐ Scenár 2: omylom zdieľaný Controlled dokument mimo EÚ (potenciálny neoprávnený vývoz).  
> * ☐ Scenár 3: výpadok IdP / ransomware (väzba na FC-15, obnova IdP → komunikácia → platby → ERP).  
> * ☐ Overiť: kto rozhoduje, kontakty, NIS2 lehoty (včasné varovanie do 24 h, hlásenie do 72 h, záverečná správa do 1 mesiaca – overiť podľa SK zákona), GDPR hlásenie do 72 h, oznámenie ECO/Legal pri exportnom incidente.  
> * ☐ Zapísať lessons learned a úlohy s vlastníkmi.

## **7\. Minimálne auditné udalosti (retencia)**

| Udalosť | Zdroj | Alert | Návrh retencie |
| :---- | :---- | :---- | :---- |
| Prihlásenia (úspešné/neúspešné), MFA zlyhania, rizikové prihlásenia | IdP | Áno pri anomálii | 12 mes. |
| Zmeny MFA metód, resety hesiel | IdP | Áno | 12 mes. |
| Vytvorenie/zmena/zrušenie účtu, zmena skupín a rolí | IdP | Áno pre admin/Controlled | 24 mes. |
| Privilegovaná elevácia, zmeny tenant politík (Conditional Access, retencia, logovanie) | IdP / admin log | Áno (vždy) | 24 mes. |
| Pozvanie/odobratie hosťa, externé a anonymné zdieľanie | Kolaborácia | Áno | 24 mes. |
| Prístup, sťahovanie a zdieľanie v zóne Controlled; zníženie/odstránenie labelu | Kolaborácia / DLP | Áno (vždy) | min. 5 rokov (súvisí s evidenciou podľa čl. 27 nar. 2021/821 – overiť s ECO) |
| Rozhodnutia exportnej brány (ÁNO/STOP, licencia, expirácia) | Ticket / register ECO | — | min. 5 rokov |
| Hromadné sťahovanie / mazanie, DLP zásahy | Kolaborácia / DLP | Áno | 12 mes. |
| Stav zariadení (nesúlad, EDR detekcie, wipe) | MDM / EDR | Áno pri detekcii | 12 mes. |
| Akcie AI agentov (polia podľa 02\_Audit-schema) | Agent log | Áno pri deny/escalate | podľa 02\_Audit-schema |

Logy sú append-only, prístup k nim má len CISO/IT bezpečnosť (oddelene od bežných adminov). Retencia je návrh – vyvážiť s GDPR minimalizáciou a zmluvnými požiadavkami zákazníkov.

## **8\. Ďalších 30 dní**

| Týždeň | Kroky | Vlastník | Výstup |
| :---- | :---- | :---- | :---- |
| **1** | Rozhodnúť variant (A predvolene); inventúra používateľov, externistov, SaaS, zariadení a adminov; určiť vlastníkov dát; vytvoriť 2 break-glass účty; MFA pre všetkých | Predstavenstvo / CISO / IT | Rozhodnutie \+ inventár |
| **2** | Tenant v EÚ, skupiny a roly (RBAC), ABAC atribúty, Conditional Access baseline (MFA, blokovanie legacy auth, spravované zariadenie pre Project/Controlled), MDM \+ EDR na všetky notebooky; oddelené admin účty | IT / CISO | Baseline konfigurácia (zdokumentovaná) |
| **3** | Dátové zóny: labely \+ priestory pre Internal/Project/Controlled; politika hostí (expirácia, sponzor); JML formulár; prepojenie exportnej brány s FC-09 a stavu partnera s FC-07 | IT / ECO / CCO | Zóny v prevádzke; JML a brána |
| **4** | Centrálne logovanie a alerty (kap. 7); prvá revízia prístupov; light tabletop (scenár 2); registrácia AI agentov ako servisných identít podľa Agent registra; predloženie na schválenie | CISO / ECO / Márian Stančík | Audit report v1 \+ návrh na schválenie Predstavenstvom |

**Otvorené body \[DOPLNIŤ\]:** zaradenie IOTA pod NIS2 (významný/kľúčový subjekt?), menovanie CISO/ECO/DPO, aktuálny stav IT (existujúci tenant?), zákaznícke požiadavky na suverenitu dát, rozpočet licencií.

| IOTA Defence a.s. · 08\_IT-a-identita · NÁVRH v1.0 · IČO 00000000 (FIKTÍVNE) · Nie je právna rada |
| :---: |

