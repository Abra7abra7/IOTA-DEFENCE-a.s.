

| NÁVRH – NIE JE PRÁVNA RADA. NA SCHVÁLENIE PREDSTAVENSTVOM. |
| :---: |

# **02 · Slovník pojmov – IT, identita a prístupy**

IOTA Defence a.s. · IČO 00000000 (FIKTÍVNE — pred zápisom do ORSR) · Verzia 1.0 · 7\. 10\. 2026 · Márian Stančík · Interné – Dôverné · Stav: NÁVRH  
Nadväzuje na: 01\_IT-struktura-a-identity-defence-SME-30\_NAVRH (https\://docs.google.com/document/d/1H83T1Oa3hwzx7FhapHuClGH\_09tSdpYuPbE1hJeW9o8/edit) · Priečinok 08\_IT-a-identita

## **Ako slovník čítať**

> * **Pre koho:** predstavenstvo a kolegovia bez IT vzdelania. Cieľom je, aby ste rozumeli dokumentu 01 a vedeli o ňom rozhodovať.  
> * **Štruktúra:** pojmy sú rozdelené do 6 skupín (Identita · Prístupy · Dáta · Audit · Regulácia · Dodávatelia). Anglický názov je v zátvorke, lebo sa tak objavuje v ponukách a v nastaveniach systémov.  
> * **Príklady** sú ilustračné pre firmu s \~30 ľuďmi v dual-use / defence oblasti; nie sú záväzným popisom súčasného stavu.  
> * **Výhrada:** právne pojmy (GDPR, NIS2, export, CLOUD Act) sú zjednodušené. Pri konkrétnom rozhodnutí platí znenie predpisov a stanovisko Legal / ECO.

## **10 pojmov, ktoré by mal poznať každý člen predstavenstva**

IdP (jedno miesto pre všetky účty) · MFA (heslo nestačí) · Least privilege (len nevyhnutné práva) · JML (nástup – zmena – odchod) · Dátové zóny (Public / Internal / Project / Controlled) · ECO a exportná kontrola · Sankčný screening · Audit log (dôkaz, kto čo urobil) · NIS2 (hlásenie incidentov v lehotách) · CLOUD Act (vedome prijaté riziko US poskytovateľa).

## **1\. Identita – kto ste v systéme**

| Pojem | Čo to znamená (jednoducho) | Príklad v IOTA (\~30 osôb) |
| :---- | :---- | :---- |
| **Digitálna identita (Identity)** | Váš „elektronický preukaz“ vo firme: účet s menom, rolou a údajmi, podľa ktorých systémy vedia, kto ste. | *Príklad:* Nová účtovníčka dostane účet jana.novakova@iota…, ktorý ju identifikuje v e-maile, dokumentoch aj v účtovnom systéme. |
| **IdP – poskytovateľ identity (Identity Provider)** | Jedno centrálne miesto, kde sú vedené všetky účty a kde sa overuje, či ste to naozaj vy. Ostatné aplikácie sa ho „pýtajú“. | *Príklad:* Entra ID je pre IOTA jediný IdP: keď niekto odíde, vypne sa jeden účet a prístup stratí do všetkých aplikácií naraz. |
| **SSO – jednotné prihlásenie (Single Sign-On)** | Prihlásite sa raz a ďalšie firemné aplikácie vás pustia bez ďalšieho hesla. Menej hesiel \= menej chýb a menej phishingu. | *Príklad:* Obchodník sa ráno prihlási do notebooku a bez nového hesla otvorí e-mail, CRM aj cestovné náhrady. |
| **MFA – viacfaktorové overenie (Multi-Factor Authentication)** | Okrem hesla treba ešte druhý dôkaz – napr. potvrdenie v mobile alebo bezpečnostný kľúč. Ukradnuté heslo samo nestačí. | *Príklad:* Útočník vyláka heslo technika podvodným e-mailom, ale prihlásiť sa nedokáže, lebo nemá jeho telefón. |
| **Adaptívne MFA (Adaptive MFA)** | Systém žiada druhé overenie podľa rizika: v známej situácii menej často, pri nezvyčajnej (nová krajina, nové zariadenie) vždy a prísnejšie. | *Príklad:* Člen predstavenstva sa prihlasuje z kancelárie bez otázok; keď sa ten istý účet prihlasuje o 3:00 z inej krajiny, systém si vyžiada kľúč alebo prístup zablokuje. |
| **Phishing-odolné MFA (FIDO2, passkey)** | Najsilnejší druh MFA – fyzický kľúč alebo prístupový kľúč v zariadení, ktorý sa nedá „vylákať“ cez falošnú stránku. | *Príklad:* Správcovia IT a ľudia so zónou Controlled majú USB/NFC kľúč; bežní zamestnanci aplikáciu v mobile. |
| **Hosťovský účet (Guest)** | Účet pre človeka mimo firmy (partner, freelancer) s obmedzeným prístupom a dátumom vypršania. | *Príklad:* Konzultant partnerskej firmy dostane hosťovský účet len do jedného projektového priestoru na 90 dní. |
| **Servisný účet (Service account)** | Účet, ktorý nepatrí človeku, ale programu alebo automatizácii. Musí mať vlastníka a čo najmenšie práva. | *Príklad:* Účet, cez ktorý fakturačný systém posiela PDF faktúry e-mailom; jeho vlastníkom je finančná manažérka. |
| **Núdzový účet (Break-glass)** | Záložný administrátorský účet „za sklom“ na prípad, že bežné prihlasovanie zlyhá. Používa sa len v núdzi a každé použitie sa preveruje. | *Príklad:* IOTA má 2 také účty, heslá a kľúče sú v trezore; štvrťročne sa skúša, či fungujú. |
| **Onboarding / Offboarding** | Onboarding \= všetko, čo treba pri nástupe (účet, zariadenie, školenie). Offboarding \= všetko pri odchode (vypnúť účet, vrátiť notebook, odovzdať súbory). | *Príklad:* Pri odchode konštruktéra sa v posledný deň vypne účet, notebook sa vráti a jeho súbory prevezme vedúci. |
| **Životný cyklus identity / JML (Joiner–Mover–Leaver)** | Pravidlá pre tri situácie: nástup (Joiner), zmena pozície či projektu (Mover), odchod (Leaver). Cieľom je, aby prístupy vždy zodpovedali aktuálnej práci. | *Príklad:* Technička prejde z výroby na projekt pre zákazníka: dostane prístup k projektu a **zároveň** sa jej odoberú staré výrobné práva. |
| **Identity Governance (správa a dohľad nad prístupmi)** | Pravidelná kontrola a schvaľovanie, kto má k čomu prístup a prečo – s dôkazmi pre audit. Nie technológia, ale „poriadok v prístupoch“. | *Príklad:* Raz mesačne vedúci projektu potvrdí zoznam členov a hostí; nepotrebných odstráni a záznam sa uloží. |
| **Revízia prístupov (Access review)** | Konkrétny krok Identity Governance: vlastník dát prejde zoznam ľudí s prístupom a potvrdí alebo odoberie. | *Príklad:* ECO každý mesiac skontroluje 6 osôb v zóne Controlled a zistí, že jeden externista už nemá platnú zmluvu – prístup sa odoberie. |
| **Federácia identít (Federation)** | Dôvera medzi dvoma systémami identít – človek sa prihlási „doma“ a druhý systém to akceptuje bez nového účtu. | *Príklad:* Ak by IOTA mala citlivé dáta v Keycloak, zamestnanci by sa tam prihlasovali svojím Entra ID účtom. |

## **2\. Prístupy – kto čo smie**

| Pojem | Čo to znamená (jednoducho) | Príklad v IOTA (\~30 osôb) |
| :---- | :---- | :---- |
| **Princíp najmenších oprávnení (Least privilege)** | Každý má len tie práva, ktoré nevyhnutne potrebuje na svoju prácu – nie „pre istotu“ viac. | *Príklad:* Asistentka predstavenstva vidí zmluvy, ale nemá prístup k technickým výkresom ani k nastaveniam IT. |
| **Need-to-know (potreba vedieť)** | K citlivej informácii má prístup len ten, kto ju potrebuje na konkrétnu úlohu – ani vysoká funkcia sama nestačí. | *Príklad:* Člen predstavenstva nemá automaticky prístup k výkresom exportne kontrolovaného dielu, ak na projekte nepracuje. |
| **RBAC – prístup podľa roly (Role-Based Access Control)** | Práva sa prideľujú podľa pracovnej roly, nie každému zvlášť. Zmena roly \= zmena práv. | *Príklad:* Rola „Financie“ automaticky otvára účtovníctvo a bankové výpisy; rola „Výroba“ nie. |
| **ABAC – prístup podľa vlastností (Attribute-Based Access Control)** | Rozhoduje sa podľa viacerých vlastností naraz: kto ste, aké máte zariadenie, odkiaľ sa pripájate, či prešiel screening a pod. Jemnejšie než samotné roly. | *Príklad:* Do zóny Controlled sa dostane len interný zamestnanec, s výsledkom screeningu „OK“, zo spravovaného notebooku a z EÚ. |
| **Privilegovaný prístup (Privileged access)** | Mimoriadne silné práva – napr. správa celého IT, mazanie účtov, zmena bezpečnostných pravidiel. Zneužitie by malo veľký dopad. | *Príklad:* Globálny administrátor Microsoft 365 môže vypnúť MFA celej firme – preto majú tento prístup max. 2–3 ľudia. |
| **PAM – správa privilegovaných prístupov (Privileged Access Management)** | Pravidlá a nástroje na stráženie privilegovaných účtov: oddelené admin účty, prístup len na čas, schvaľovanie, záznam všetkých krokov. | *Príklad:* IT správca pracuje bežne s obyčajným účtom; admin práva si „požičia“ na 2 hodiny so zdôvodnením a všetko sa zaznamená. |
| **Just-in-time prístup (JIT)** | Práva sa udelia len na nevyhnutný čas a potom automaticky zaniknú. | *Príklad:* Dodávateľ servisu dostane admin prístup k serveru v utorok od 9:00 do 12:00, potom sa sám zruší. |
| **Princíp štyroch očí (4-eyes)** | Dôležitú zmenu musí schváliť ešte druhá osoba. | *Príklad:* Zmenu bezpečnostného pravidla pre celú firmu navrhne IT správca a schváli CISO. |
| **Podmienený prístup (Conditional Access)** | Pravidlá typu „ak–potom“, ktoré pri každom prihlásení vyhodnotia situáciu a prístup povolia, sťažia alebo zablokujú. | *Príklad:* „Ak sa niekto pripája k projektovým dátam zo súkromného počítača, môže ich len čítať v prehliadači, nie sťahovať.“ |
| **Súlad zariadenia (Device compliance)** | Overenie, že počítač alebo mobil spĺňa firemné pravidlá: šifrovaný disk, aktuálne záplaty, antivírus, firemná správa. | *Príklad:* Notebook bez aktuálnych bezpečnostných aktualizácií sa nedostane do zóny Project, kým sa neaktualizuje. |
| **MDM – správa zariadení (Mobile Device Management)** | Nástroj, ktorým IT na diaľku nastavuje, zabezpečuje a pri strate vymaže firemné zariadenia. | *Príklad:* Stratený firemný telefón obchodníka sa na diaľku uzamkne a firemné dáta sa z neho zmažú. |
| **VPN (Virtual Private Network)** | Šifrovaný „tunel“ cez internet do firemnej siete. Chráni prenos, ale sám neoveruje, či je zariadenie bezpečné. | *Príklad:* Technik v hoteli sa cez VPN pripojí k súborovému serveru vo firme; bez VPN by server z internetu nebol dostupný. |
| **Zero Trust (nulová dôvera)** | Prístup: „nikomu automaticky neverím – ani vo firemnej sieti“. Každé prihlásenie a zariadenie sa overuje vždy znova. | *Príklad:* Aj počítač pripojený vo firemnej kancelárii musí prejsť MFA a kontrolou zariadenia, ak ide do citlivých dát. |
| **Bezpečný prístup partnerov (Secure Partner Access)** | Kontrolovaný spôsob, ako pustiť externých partnerov k firemným dátam: preverený partner, menovitý účet, MFA, obmedzený priestor, dátum konca. | *Príklad:* Subdodávateľ obrábania má prístup len k výkresom svojho dielu v jednom projekte, a len po schválení due diligence (FC-07). |
| **Clearance (oprávnenie / previerka pre zónu)** | Potvrdenie, že osoba smie pracovať s určitou úrovňou citlivých dát. V tomto balíku ide o **interné** oprávnenie pre zónu (napr. Controlled), nie o bezpečnostnú previerku NBÚ. | *Príklad:* Inžinier má atribút „clearance \= Controlled“ až po exportnom screeningu a súhlase ECO. |
| **Politika ako kód (Policy-as-code)** | Pravidlá prístupu sú zapísané ako presný, strojovo čitateľný predpis (nie len v PDF smernici), takže sa dajú automaticky vynucovať, testovať a porovnávať verzie. | *Príklad:* Pravidlo „externisti nesmú do zóny Controlled“ je zapísané v nastaveniach ako kód; každá zmena prechádza schválením a je dohľadateľná. |
| **AI agent (v kontexte prístupov)** | Softvérový asistent, ktorý samostatne vykonáva úlohy (číta dokumenty, píše e-maily, pracuje v systémoch). Pre IT je to ďalšia „identita“ – musí mať vlastný účet, vlastníka, obmedzené práva a záznam činností. | *Príklad:* AI agent na triedenie dopytov smie čítať schránku obchod@ (úroveň L1), ale nesmie odosielať e-maily ani otvoriť zónu Controlled bez ľudského schválenia. |

## **3\. Dáta – kde a ako sú uložené**

| Pojem | Čo to znamená (jednoducho) | Príklad v IOTA (\~30 osôb) |
| :---- | :---- | :---- |
| **Dátové zóny** | Rozdelenie firemných dát podľa citlivosti do 4 „priečinkov dôvery“. Čím citlivejšia zóna, tým prísnejšie pravidlá prístupu. | *Príklad:* Ponuka pre zákazníka patrí do Project, technický výkres dual-use dielu do Controlled. |
| **Zóna Public (verejné)** | Informácie, ktoré smú byť zverejnené. Technické údaje sa zverejňujú až po kontrole ECO. | *Príklad:* Firemný web, leták z veľtrhu, verejný produktový katalóg. |
| **Zóna Internal (interné)** | Informácie pre zamestnancov; mimo firmy sa nezdieľajú. | *Príklad:* Smernica o cestovných náhradách, interné oznamy, organizačná štruktúra. |
| **Zóna Project (projektové)** | Dokumenty konkrétneho projektu, prístupné len členom projektu (vrátane menovite schválených externistov). | *Príklad:* Zmluva, harmonogram a cenová ponuka pre zákazníka X v samostatnom projektovom priestore. |
| **Zóna Controlled (kontrolované)** | Najcitlivejšie dáta – najmä exportne kontrolovaná technológia a dáta so zmluvnými obmedzeniami. Prístup len menovite, po exportnom screeningu a so súhlasom ECO. | *Príklad:* Výrobná dokumentácia dielu zaradeného ako dual-use; otvoriť ju možno len z firemného notebooku v EÚ s bezpečnostným kľúčom. |
| **Označenie citlivosti (Label)** | „Nálepka“ na dokumente alebo e-maile, ktorá hovorí, do ktorej zóny patrí, a automaticky zapne ochranu (šifrovanie, zákaz preposlania). | *Príklad:* Dokument s labelom Controlled sa nedá otvoriť, ak ho niekto omylom pošle na súkromný Gmail. |
| **DLP – prevencia úniku dát (Data Loss Prevention)** | Automatická kontrola, ktorá zachytí alebo zablokuje pokus poslať citlivé dáta von. | *Príklad:* Systém zastaví e-mail s prílohou označenou Controlled adresovaný mimo firmu a upozorní ECO. |
| **Šifrovanie (Encryption)** | Dáta sa „zamknú“ tak, že bez správneho kľúča sú nečitateľné – pri strate notebooku aj pri prenose. | *Príklad:* Ukradnutý firemný notebook so šifrovaným diskom zlodejovi neodhalí žiadne výkresy. |
| **Lokalita dát (Data residency)** | Kde – v ktorej krajine/regióne – sú dáta fyzicky uložené a spracúvané. Dôležité pre GDPR, zmluvy so zákazníkmi a export. | *Príklad:* IOTA si zvolí ukladanie dát v dátových centrách v EÚ a túto voľbu zdokumentuje pre zákazníkov. |
| **EU Data Boundary (dátová hranica EÚ)** | Záväzok Microsoftu, že dáta zákazníkov z EÚ sa ukladajú a spracúvajú prevažne v EÚ. Výrazne pomáha, ale **neruší** pôsobnosť amerického práva (pozri CLOUD Act). | *Príklad:* M365 tenant IOTA je v EÚ; e-maily a dokumenty sú uložené v európskych dátových centrách. |

## **4\. Audit a bezpečnostná prevádzka – dôkazy a reakcia**

| Pojem | Čo to znamená (jednoducho) | Príklad v IOTA (\~30 osôb) |
| :---- | :---- | :---- |
| **Auditný záznam (Audit log)** | Automatický „denník“, kto čo kedy v systéme urobil (prihlásenie, otvorenie súboru, zmena práv). Slúži ako dôkaz a na vyšetrovanie. | *Príklad:* Pri podozrení na únik vieme presne povedať, kto a kedy otvoril výkres v zóne Controlled. |
| **Nemenný záznam (Immutable / append-only log)** | Denník, do ktorého sa dá iba pridávať, ale nič v ňom nemožno zmeniť ani zmazať – ani administrátor. Preto je dôveryhodným dôkazom. | *Príklad:* Ani IT správca nemôže dodatočne „vygumovať“ záznam o tom, že si sám pridal admin práva. |
| **Retencia (Retention)** | Ako dlho sa záznamy alebo dokumenty uchovávajú, kým sa zmažú. Musí byť vyvážená medzi dôkazmi a GDPR (neuchovávať zbytočne dlho). | *Príklad:* Záznamy o prihláseniach 12 mesiacov; záznamy o exportných rozhodnutiach min. 5 rokov (overiť s ECO). |
| **SIEM (Security Information and Event Management)** | Centrálny systém, ktorý zbiera záznamy zo všetkých systémov na jedno miesto, hľadá v nich podozrivé vzorce a spúšťa poplach. | *Príklad:* SIEM upozorní, že ten istý účet sa za 10 minút prihlásil z Bratislavy aj z Ázie. |
| **EDR (Endpoint Detection and Response)** | Moderný „antivírus“ na počítačoch, ktorý sleduje podozrivé správanie a vie zariadenie izolovať. | *Príklad:* EDR zastaví na notebooku program, ktorý začal hromadne šifrovať súbory (ransomware). |
| **Bezpečnostný incident** | Udalosť, ktorá ohrozila alebo poškodila bezpečnosť dát či systémov – napr. napadnutý účet, únik, výpadok. | *Príklad:* Omylom zdieľaný kontrolovaný dokument s osobou mimo EÚ je incident (aj možný neoprávnený vývoz). |
| **Eskalácia (Escalation)** | Posunutie problému alebo rozhodnutia na vyššiu úroveň podľa vopred dohodnutých pravidiel – kto, kedy a do akého času. | *Príklad:* Podozrenie na exportný incident ide okamžite na ECO a Legal; pri vážnom dopade do 24 h na predstavenstvo (podľa 03\_Escalation-matrix). |
| **Cvičenie „pri stole“ (Tabletop exercise)** | Krátke (60–90 min) nacvičenie incidentu formou diskusie: prejde sa scenár a overí, kto čo robí a koho volá. Nič sa reálne nevypína. | *Príklad:* Polročne si vedenie a IT prejdú scenár „napadnutý účet externistu“ a zapíšu, čo treba zlepšiť. |
| **BCP / DR (kontinuita a obnova)** | Plán, ako firma funguje počas vážneho výpadku (BCP) a ako obnoví IT systémy (DR). | *Príklad:* Pri výpadku prihlasovania sa použije núdzový účet a obnova prebehne v poradí: identita → komunikácia → platby → ERP (FC-15). |

## **5\. Regulácia a právo – čo od nás vyžaduje zákon**

| Pojem | Čo to znamená (jednoducho) | Príklad v IOTA (\~30 osôb) |
| :---- | :---- | :---- |
| **GDPR** | Nariadenie EÚ o ochrane osobných údajov. Určuje, ako smieme zbierať, používať a uchovávať údaje o ľuďoch. | *Príklad:* V IT systéme sa neukladá štátna príslušnosť zamestnanca; namiesto toho len výsledok screeningu „OK / STOP“. |
| **DPO – zodpovedná osoba (Data Protection Officer)** | Osoba, ktorá dohliada na dodržiavanie GDPR a je kontaktom pre úrad. Povinná len v určitých prípadoch – posúdiť s Legal. | *Príklad:* IOTA určí, či DPO potrebuje; ak áno, môže to byť aj externá služba \[DOPLNIŤ\]. |
| **Zmluva o spracúvaní (DPA)** | Zmluva s dodávateľom, ktorý pre nás spracúva osobné údaje – určuje, čo s nimi smie robiť. | *Príklad:* S poskytovateľom mzdového softvéru IOTA podpíše DPA pred nahratím údajov zamestnancov. |
| **NIS2** | Smernica EÚ o kybernetickej bezpečnosti (na Slovensku cez zákon č. 69/2018 Z. z. v znení novely). Ukladá vybraným firmám bezpečnostné opatrenia a hlásenie incidentov v krátkych lehotách. | *Príklad:* Ak IOTA spadá pod NIS2 \[DOPLNIŤ\], vážny incident treba nahlásiť včasným varovaním do 24 h a hlásením do 72 h (overiť podľa SK zákona). |
| **CLOUD Act (poznámka k riziku)** | Zákon USA, podľa ktorého môžu americké úrady za určitých podmienok žiadať dáta od amerických poskytovateľov – aj keď sú uložené v EÚ. **Riziko:** malá pravdepodobnosť, ale pri citlivých technických dátach ho treba vedome prijať alebo zmierniť. | *Príklad:* Bežné e-maily IOTA ostávajú v M365 (riziko prijaté); pre zónu Controlled sa zvažuje variant C s vlastnými kľúčmi v EÚ. |
| **Exportná kontrola (Export control)** | Pravidlá, ktoré obmedzujú vývoz citlivého tovaru a technológií. Za vývoz sa môže považovať aj poslanie výkresu e-mailom alebo zdieľanie obrazovky osobe v zahraničí. | *Príklad:* Pred zdieľaním výkresov s partnerom mimo EÚ ECO overí, či je potrebná licencia; bez nej STOP. |
| **ECO – zodpovedný za exportnú kontrolu (Export Control Officer)** | Osoba vo firme, ktorá rozhoduje o exportných otázkach: zaradenie tovaru/dát, licencie, schválenie prístupu do zóny Controlled. | *Príklad:* ECO dá „ÁNO“ k prístupu nového inžiniera do Controlled a rozhodnutie sa zapíše do auditu. |
| **Dual-use (dvojaké použitie)** | Tovar, softvér alebo technológia, ktoré majú civilné aj vojenské využitie. V EÚ upravuje nariadenie (EÚ) 2021/821. | *Príklad:* Špeciálny senzor pre priemysel, ktorý sa dá použiť aj v zbraňovom systéme – jeho dokumentácia patrí do Controlled. |
| **Sankčný screening (Sanctions screening)** | Kontrola, či osoba, firma alebo krajina nie je na sankčných zoznamoch a či konečné použitie nie je zakázané. | *Príklad:* Pred založením hosťovského účtu pre nového partnera prebehne screening; výsledok STOP \= žiadny prístup. |
| **Utajované skutočnosti (NBÚ)** | Štátom utajované informácie podľa zákona č. 215/2004 Z. z. Patria **výhradne** do certifikovaného systému podľa NBÚ – nie do bežného cloudu ani do zón v tomto balíku. | *Príklad:* Ak IOTA dostane utajovaný dokument od zákazníka, nesmie ho uložiť do M365 ani do zóny Controlled. |

## **6\. Dodávatelia a architektúra – na čom to beží**

| Pojem | Čo to znamená (jednoducho) | Príklad v IOTA (\~30 osôb) |
| :---- | :---- | :---- |
| **Tenant** | Vlastné, oddelené „firemné prostredie“ u cloudového poskytovateľa – s vlastnými účtami, nastaveniami a dátami. | *Príklad:* IOTA má jeden tenant Microsoft 365 v EÚ; firma od vedľa má svoj, navzájom sa nevidia. |
| **SaaS vs. on-prem** | SaaS \= softvér ako služba v cloude, platený predplatným, prevádzku rieši dodávateľ. On-prem \= vlastný server vo firme alebo v prenajatom dátovom centre; prevádzku riešime sami. | *Príklad:* E-mail v M365 je SaaS; súborový server v serverovni IOTA je on-prem. |
| **Hybrid** | Kombinácia cloudu a vlastnej infraštruktúry – bežné veci v cloude, najcitlivejšie u seba. | *Príklad:* Bežná práca v M365, výkresy zóny Controlled na serveri v EÚ s vlastnými kľúčmi (variant C). |
| **Microsoft Entra ID** | Služba Microsoftu na správu identít a prihlasovania (predtým „Azure Active Directory“). V odporúčanom variante A je to IdP celej IOTA. | *Príklad:* Všetci zamestnanci, hostia aj AI agenti majú účet v Entra ID; tam sa nastavuje aj MFA a podmienený prístup. |
| **Okta** | Samostatný americký poskytovateľ správy identít a SSO, často používaný s Google Workspace. | *Príklad:* Variant B: ak by IOTA pracovala v Google Workspace, Okta by zabezpečila prihlasovanie a JML. |
| **Keycloak** | Bezplatný open-source systém na správu identít a SSO, ktorý si firma prevádzkuje sama (napr. na serveri v EÚ). | *Príklad:* Variant C/D: Keycloak stráži prístup k serveru so zónou Controlled; prevádzku a záplaty si IOTA zabezpečuje sama alebo cez dodávateľa. |
| **Microsoft 365 / Google Workspace** | Balíky kancelárskych cloudových služieb: e-mail, kalendár, dokumenty, chat, videohovory. | *Príklad:* Variant A: M365 (Outlook, Teams, SharePoint); variant B: Google Workspace (Gmail, Drive, Meet). |

## **7\. Často zamieňané pojmy**

> * **VPN vs. Zero Trust:** VPN chráni „cestu“, Zero Trust overuje „kto a z čoho“ pri každom prístupe.  
> * **RBAC vs. ABAC:** RBAC \= podľa funkcie; ABAC \= podľa funkcie *a* ďalších okolností (zariadenie, krajina, screening).  
> * **Clearance (interné) vs. previerka NBÚ:** interné oprávnenie pre zónu Controlled nie je štátna bezpečnostná previerka.  
> * **EU Data Boundary vs. suverenita:** dáta v EÚ ≠ úplná nezávislosť od práva USA.  
> * **Audit log vs. SIEM:** audit log je samotný denník; SIEM ich zbiera dohromady a vyhodnocuje.

**Otvorené body \[DOPLNIŤ\]:** potvrdiť zaradenie pod NIS2, menovanie CISO / ECO / DPO, voľbu variantu (A predvolene). Slovník sa aktualizuje spolu s dokumentom 01\. Počet hesiel vo verzii 1.0: 67\.

| IOTA Defence a.s. · 08\_IT-a-identita · 02\_Slovník pojmov · NÁVRH v1.0 · IČO 00000000 (FIKTÍVNE) · Nie je právna rada |
| :---: |

