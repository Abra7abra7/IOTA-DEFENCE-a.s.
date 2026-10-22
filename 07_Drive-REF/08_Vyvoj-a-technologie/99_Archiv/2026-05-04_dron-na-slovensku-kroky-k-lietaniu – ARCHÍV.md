# **Komplexná analýza regulačného rámca a prevádzkových postupov pre podomácky vyrobené bezpilotné systémy na Slovensku v roku 2026**

Prudký rozvoj bezpilotných technológií a ich dostupnosť pre širokú verejnosť viedli k potrebe harmonizácie pravidiel v rámci celého európskeho priestoru. Pre konštruktéra, ktorý si dronom s hmotnosťou približne 1,5 kg postavil svojpomocne z komponentov zakúpených u predajcov ako Rototrama, Alza či RpiShop, predstavuje rok 2026 obdobie plnej integrácie do európskeho legislatívneho rámca spravovaného Agentúrou Európskej únie pre bezpečnosť letectva (EASA) a implementovaného na národnej úrovni Dopravným úradom Slovenskej republiky.1 Táto analýza poskytuje vyčerpávajúci pohľad na všetky administratívne, technické a prevádzkové kroky potrebné na legálne lietanie s takýmto zariadením na verejných priestranstvách a lúkach v Slovenskej republike.

## **Legislatívna architektúra a kategorizácia podomácky vyrobených UAS**

Základným kameňom regulácie dronov v Európskej únii je vykonávacie nariadenie Komisie (EÚ) 2019/947, ktoré definuje pravidlá a postupy pre prevádzku bezpilotných lietadiel.2 Na Slovensku je táto legislatíva integrovaná do národného práva prostredníctvom zákona č. 143/1998 Z. z. o civilnom letectve (letecký zákon), ktorý bol v roku 2024 novelizovaný s cieľom zaviesť poplatkové štruktúry a jasné sankčné mechanizmy.3

### **Definícia privátne postaveného bezpilotného lietadla**

V kontexte súčasnej legislatívy sa drony rozdeľujú na dve základné skupiny: drony so štítkom triedy (C0 až C6) a drony bez takéhoto štítku, kam patria aj „privátne postavené“ (privately built) drony.2 Privátne postavený dron je zariadenie, ktoré si operátor zostavil pre vlastnú potrebu z jednotlivých komponentov a ktoré nebolo uvedené na trh ako hotový komerčný produkt pod konkrétnou značkou triedy.2 Pre zariadenie s hmotnosťou 1,5 kg to znamená, že nemôže požívať výhody certifikovaných dronov triedy C2, ktoré by mu umožňovali lietanie v blízkosti ľudí v podkategórii A2.6

| Parameter | Špecifikácia pre 1,5 kg DIY dron | Klasifikácia podľa EASA |
| :---- | :---- | :---- |
| **Hmotnosť (MTOW)** | 1,5 kg | Nad 250 g, do 25 kg |
| **Kategória prevádzky** | Otvorená (Open) | Nízkoriziková prevádzka |
| **Podkategória** | A3 (Lety ďaleko od ľudí) | Prevádzka mimo osídlenia |
| **Certifikácia** | Žiadna (Legacy / DIY) | Privátne postavený systém |

Keďže podomácky vyrobený dron s váhou nad 250 g nedisponuje certifikačným štítkom, je podľa platných prechodných ustanovení automaticky zaradený do podkategórie A3 v rámci otvorenej kategórie.2 Toto zaradenie striktne definuje priestorové obmedzenia letu, kde pilot nesmie prelietavať nad nezúčastnenými osobami a musí udržiavať bezpečnú horizontálnu vzdialenosť minimálne 150 metrov od obytných, obchodných, priemyselných alebo rekreačných oblastí.2

### **Fyzikálne aspekty a kinetická energia dopadu**

Dôvod pre zaradenie 1,5 kg drona do podkategórie A3 s prísnymi vzdialenostnými limitmi vychádza z fyzikálneho rizika, ktoré takéto teleso predstavuje v prípade poruchy. Kinetická energia ![][image1], ktorú objekt nadobudne pri voľnom páde z maximálnej povolenej výšky 120 metrov, sa vypočíta podľa vzorca:

![][image2]  
kde ![][image3] je hmotnosť (![][image4]) a ![][image5] je rýchlosť dopadu. Rýchlosť dopadu pri páde z výšky ![][image6] (bez započítania odporu vzduchu) je ![][image7]. Pri výške ![][image8] a gravitačnom zrýchlení ![][image9] dosahuje rýchlosť dopadu približne ![][image10] (![][image11]). Výsledná kinetická energia dopadu je približne ![][image12].6 Táto energia je mnohonásobne vyššia ako prahová hodnota pre vážne zranenia alebo úmrtie, čo odôvodňuje požiadavku na prevádzku výhradne v neobývaných oblastiach, ako sú polia alebo lúky vzdialené od ľudí.6

## **Administratívne požiadavky: Registrácia prevádzkovateľa UAS**

Prvým nevyhnutným krokom k legálnemu lietaniu na Slovensku nie je registrácia samotného dronu, ale registrácia jeho prevádzkovateľa.4 Prevádzkovateľom je osoba (fyzická alebo právnická), pod ktorej menom a zodpovednosťou sa dron používa.5

### **Proces registrácie na Dopravnom úrade SR**

Registrácia je povinná pre každého, kto prevádzkuje dron s hmotnosťou 250 g a viac, alebo dron vybavený kamerou či iným senzorom schopným zachytiť osobné údaje.11 Pre 1,5 kg drona s komponentmi z Rototramy je tento úkon povinný bez ohľadu na účel letu.5

| Spôsob registrácie | Správny poplatok (e-kolok) | Kód e-kolku |
| :---- | :---- | :---- |
| **Elektronicky cez slovensko.sk** | 17,50 EUR | 7605 (znížená sadzba) |
| **Listinne (poštou alebo osobne)** | 35,00 EUR | 7605 (plná sadzba) |

Proces registrácie vyžaduje vyplnenie žiadosti o zápis do registra prevádzkovateľov UAS, kde sa uvádzajú identifikačné údaje, kontaktné údaje a informácie o poistení zodpovednosti.4 Od 15\. júla 2024 je tento proces spoplatnený podľa nového sadzobníka.3 Po úspešnom spracovaní žiadosti, čo trvá štandardne 30 dní, pridelí Dopravný úrad prevádzkovateľovi unikátne 12-miestne registračné číslo prevádzkovateľa.5

### **Označovanie a správa registračného čísla**

Získané registračné číslo musí byť fyzicky a trvanlivo umiestnené na každom drone, ktorý daný prevádzkovateľ vlastní.5 V prípade podomácky vyrobeného dronu sa odporúča použiť gravírovaný štítok alebo odolnú nálepku umiestnenú na ráme. Okrem viditeľného označenia je prevádzkovateľ povinný toto číslo nahrať do systému diaľkovej identifikácie (Remote ID), ak to technické vybavenie drona umožňuje.5

## **Poistenie zodpovednosti za škodu**

Lietanie s dronom o hmotnosti 1,5 kg nesie so sebou značnú zodpovednosť za prípadné škody na zdraví alebo majetku tretích osôb. Slovenská legislatíva, konkrétne § 35 leteckého zákona, ukladá prevádzkovateľom vybraných kategórií dronov povinnosť uzavrieť poistenie zodpovednosti.16

### **Povinnosť poistenia pre kategóriu A3**

Hoci európske nariadenie 785/2004 striktne vyžaduje poistenie pre drony nad 20 kg, Slovensko využilo svoju kompetenciu a zaviedlo povinnosť poistenia aj pre ľahšie drony prevádzkované v podkategóriách A2, A3 a v osobitnej kategórii.16 Pre podomácky vyrobený 1,5 kg dron je teda poistenie zákonnou podmienkou legálnej prevádzky.4

| Poskytovateľ poistenia | Orientačná cena (ročne) | Charakteristika |
| :---- | :---- | :---- |
| **CoverDrone** | Cca 17 – 20 EUR | Medzinárodne uznávané, akceptované DÚ SR |
| **Premium Poisťovňa** | Od 30 EUR | Domáci poskytovateľ, spolupráca s Mám Dron |
| **UNIQA** | V rámci poistenia majetku | Krytie rekreačných letov do 4 kg MTOW |

Pri výbere poistenia je dôležité sledovať limit poistného krytia. Štandardom pre medzinárodné uznanie je krytie vo výške približne ![][image13] (čo zodpovedá limitom v jednotkách SDR – Special Drawing Rights).4 Číslo poistnej zmluvy je nevyhnutné uviesť už pri registrácii prevádzkovateľa na Dopravnom úrade.4

## **Certifikácia vzdialeného pilota: Skúška A1/A3**

Aby bolo možné s dronom legálne vzlietnuť, musí osoba, ktorá ho reálne ovláda (vzdialený pilot), preukázať svoju spôsobilosť. Pre drony nad 250 g je povinné získať „Doklad o absolvovaní online výcviku“ pre podkategórie A1 a A3.5

### **Proces vzdelávania a online skúška v roku 2026**

V roku 2026 je na Slovensku plne funkčný systém online preskúšania cez portál letectvo.nsat.sk.11 Proces pozostáva z nasledujúcich fáz:

1. **Online výcvik:** Pilot absolvuje bezplatný vzdelávací kurz pokrývajúci témy ako bezpečnosť letov, obmedzenia vzdušného priestoru, letecké predpisy, ľudská výkonnosť, ochrana súkromia a GDPR, a vedomosti o UAS.11  
2. **Online test:** Po úspešnom preštudovaní materiálov nasleduje test so 40 otázkami. Na úspešné absolvovanie je potrebná správnosť aspoň 75 % (30 otázok) v časovom limite 60 minút.11  
3. **Vydanie preukazu:** Po úspešnom zložení testu systém vygeneruje elektronický preukaz vzdialeného pilota s celoeurópskou platnosťou na 5 rokov.10

Za vykonanie skúšky na slovenskom portáli sa platí správny poplatok 30 EUR (e-kolok kód 7616).3 Alternatívou, ktorú využívajú mnohí piloti, je vykonanie skúšky v inom členskom štáte EÚ (napr. Luxembursko), kde je tento úkon bezplatný a preukaz je v SR plne akceptovaný.4

## **Technické požiadavky: Diaľková identifikácia (Remote ID)**

Od 1\. januára 2024 sú všetky drony prevádzkované v otvorenej kategórii (s výnimkou triedy C0) povinné vysielať údaje o svojej polohe a identite v reálnom čase.5 Pri podomácky vyrobenom drone z komponentov z Alzy či Rototramy je splnenie tejto požiadavky technickou výzvou, ktorú legislatíva rieši prostredníctvom externých modulov.5

### **Externé moduly pre DIY drony**

Keďže privátne postavené drony zvyčajne nedisponujú integrovaným certifikovaným systémom vysielania, prevádzkovateľ musí dron vybaviť externým modulom diaľkovej identifikácie (Direct Remote ID).5 Tieto moduly, vyrábané spoločnosťami ako Dronetag alebo Aerobits, majú hmotnosť len niekoľko gramov a vysielajú údaje cez Bluetooth alebo Wi-Fi.5

| Vysielaný údaj | Popis a význam |
| :---- | :---- |
| **ID prevádzkovateľa** | 12-miestne číslo pridelené Dopravným úradom |
| **Poloha drona** | GPS súradnice a nadmorská výška v reálnom čase |
| **Poloha pilota** | GPS súradnice miesta vzletu alebo ovládača |
| **Vektor pohybu** | Rýchlosť a smer letu zariadenia |

Tento systém umožňuje bezpečnostným zložkám a verejnosti identifikovať legálnosť letu prostredníctvom mobilných aplikácií, čo zvyšuje transparentnosť a bezpečnosť vzdušného priestoru.15 Pre 1,5 kg dron v podkategórii A3 je aktívne Remote ID nevyhnutnou podmienkou legálneho letu od roku 2024\.5

## **Operačné pravidlá a geografické zóny na Slovensku**

Samotný akt lietania na verejných priestranstvách alebo lúkach podlieha prísnym pravidlám definujúcim, kde je let povolený a za akých podmienok. Pre 1,5 kg DIY dron v podkategórii A3 sú kľúčové nasledujúce limity 2:

* **Vzdialenosť od zastavaných oblastí:** Minimálne 150 metrov od obytných, komerčných alebo priemyselných zón.2  
* **Vzdialenosť od osôb:** Let sa smie vykonávať len v priestore, kde sa neočakáva prítomnosť nezúčastnených osôb. Ak sa v blízkosti objaví osoba, pilot musí zachovať bezpečnú vzdialenosť.2  
* **Maximálna výška:** Limit je stanovený na 120 metrov nad úrovňou zemského povrchu (![][image14]).2  
* **Vizuálny kontakt (VLOS):** Pilot musí mať dron neustále v priamom vizuálnom dohľade bez pomôcok (okrem dioptrických okuliarov).2

### **Kontrola vzdušného priestoru cez aplikáciu MamDron**

Pred každým vzletom je pilot povinný overiť, či sa nenachádza v obmedzenom alebo zakázanom vzdušnom priestore. Najefektívnejším nástrojom na tento účel na Slovensku je aplikácia **MamDron**, vyvinutá spoločnosťou R-SYS v spolupráci s národnými autoritami.5 Aplikácia integruje dáta o:

1. **Riadených okrskoch letísk (CTR):** V blízkosti letísk (zvyčajne rádius 5,6 km) je lietanie bez koordinácie povolené len do výšky 30 m.4  
2. **Vojenských priestoroch a TSAs:** Oblasti so špeciálnym režimom, kde môže byť let zakázaný.5  
3. **Chránených územiach:** Lety v národných parkoch (3. až 5\. stupeň ochrany) podliehajú súhlasu orgánov ochrany prírody.5

## **Komponenty a technická zhoda pri stavbe drona**

Pri nákupe komponentov z webov ako Rototrama či RpiShop pilot nadobúda súčiastky, ktoré majú individuálne CE označenie (napr. rádiové moduly alebo regulátory napätia).1 Avšak ako celok podomácky vyrobený dron nespĺňa požiadavky na produktovú certifikáciu triedy C pod dohľadom notifikovanej osoby.1

### **Zodpovednosť konštruktéra**

Z právneho hľadiska preberá konštruktér plnú zodpovednosť za technickú bezpečnosť zariadenia. Je nevyhnutné, aby dron pred prvým letom na verejnom priestranstve prešiel dôkladnými testami stability a núdzových funkcií (napr. Fail-Safe pri strate signálu).12 Odporúča sa viesť si technický denník a zoznam použitých komponentov s ich technickými listami pre prípad kontroly alebo riešenia poistnej udalosti.12

## **Sled krokov k legálnemu letu: Praktický manuál**

Pre úspešnú legalizáciu 1,5 kg drona na Slovensku v roku 2026 je potrebné dodržať nasledujúcu sekvenciu úkonov:

1. **Technická finalizácia a váženie:** Zvážte hotový dron vrátane batérie a vrtúľ. Ak je hmotnosť ![][image15], fixne spadáte do A3.2  
2. **Uzatvorenie poistenia:** Vyberte si poistku zodpovednosti (napr. CoverDrone) a stiahnite si certifikát.4  
3. **Registrácia prevádzkovateľa:** Cez slovensko.sk podajte žiadosť na Dopravný úrad (poplatok 17,50 EUR), priložte informáciu o poistení.4  
4. **Získanie pilotnej licencie:** Absolvujte online test A1/A3 na portáli NSAT (poplatok 30 EUR) alebo v zahraničí (zadarmo).8  
5. **Fyzické označenie:** Po obdržaní registračného čísla ho nalepte na dron.5  
6. **Inštalácia Remote ID:** Vybavte dron externým modulom (napr. Dronetag BS) a vložte doň svoje registračné číslo.5  
7. **Predletová príprava:** Stiahnite si aplikáciu MamDron, skontrolujte lokalitu lúky a uistite sa, že ste aspoň 150 m od najbližšej budovy či cesty.5  
8. **Let:** Lietajte bezpečne, v dohľade a mimo ľudí.2

## **Záverečná syntéza a výhľad do budúcnosti**

Prechod na európsky model regulácie v roku 2026 definitívne ukončil éru „anonymného“ lietania s podomácky vyrobenými dromi nad 250 g.4 Pre majiteľa 1,5 kg drona to znamená počiatočnú administratívnu a finančnú investíciu vo výške približne 100 až 150 EUR (vrátane modulu Remote ID a poistenia), ktorá je však nevyhnutná pre zákonnú ochranu a bezpečnosť spoločného vzdušného priestoru.4

Systém poplatkov zavedený v júli 2024 a prísne pokuty až do výšky 5 000 EUR pre fyzické osoby signalizujú jasný postoj štátu k dodržiavaniu pravidiel.3 Zároveň však otvorenie online skúšobného portálu a akceptácia medzinárodných certifikátov uľahčuje nadšencom vstup do tohto odvetvia pri zachovaní vysokých štandardov bezpečnosti. Budúci vývoj smerujúci k plnej implementácii U-space bude klásť ešte väčší dôraz na digitálnu konektivitu dronov, čím sa drony stanú plnohodnotnými a monitorovanými účastníkmi letovej prevádzky.15

#### **Citované práce**

> 1. EU drone regulations are crazy confusing : r/fpv \- Reddit, otvorené mája 4, 2026, [https\://www\.reddit.com/r/fpv/comments/1ixf56f/eu\_drone\_regulations\_are\_crazy\_confusing/](https://www.reddit.com/r/fpv/comments/1ixf56f/eu_drone_regulations_are_crazy_confusing/)  
> 2. Open Category — Low Risk — Civil Drones \| EASA \- European Union, otvorené mája 4, 2026, [https\://www\.easa.europa.eu/en/domains/drones-air-mobility/operating-drone/open-category-low-risk-civil-drones](https://www.easa.europa.eu/en/domains/drones-air-mobility/operating-drone/open-category-low-risk-civil-drones)  
> 3. Nové poplatky a pokuty v bezpilotnom letectve \- Lety Dronom, otvorené mája 4, 2026, [https\://www\.letydronom.sk/nove-poplatky-v-bezpilotnom-letectve/](https://www.letydronom.sk/nove-poplatky-v-bezpilotnom-letectve/)  
> 4. Drony Legislatíva 2026 \| zákon na drony \- aktuálne informácie \- Xtreme.sk, otvorené mája 4, 2026, [https\://www\.xtreme.sk/clanok/14/drony-legislativa-2026/](https://www.xtreme.sk/clanok/14/drony-legislativa-2026/)  
> 5. LEGISLATÍVA \- Mám Dron, otvorené mája 4, 2026, [https\://mamdron.sk/legislativa/](https://mamdron.sk/legislativa/)  
> 6. Can You Fly a Drone Over People? (2026 Regulations & Safety Guide) \- JOUAV, otvorené mája 4, 2026, [https\://www\.jouav.com/blog/can-you-fly-a-drone-over-people.html](https://www.jouav.com/blog/can-you-fly-a-drone-over-people.html)  
> 7. Pravidlá pre drony 2026: Komplexný sprievodca pre Česko, Nemecko a Rakúsko :: www\.fpvvideo.cz, otvorené mája 4, 2026, [https\://www\.fpvvideo.cz/l/pravidla-pre-drony-2026-komplexny-sprievodca-pre-cesko-nemecko-a-rakusko/](https://www.fpvvideo.cz/l/pravidla-pre-drony-2026-komplexny-sprievodca-pre-cesko-nemecko-a-rakusko/)  
> 8. Nová legislatíva pre drony v roku 2024 \- Datacomp.sk, otvorené mája 4, 2026, [https\://datacomp.sk/legislativa-drony\_a915.html](https://datacomp.sk/legislativa-drony_a915.html)  
> 9. Pravidlá na lietanie s dronmi 2025 (LEGISLATÍVA) \- Alza.sk, otvorené mája 4, 2026, [https\://www\.alza.sk/pravidla-na-drony-legislativa](https://www.alza.sk/pravidla-na-drony-legislativa)  
> 10. everything you need to know in 2026 \- A1/A3 Drone License, otvorené mája 4, 2026, [https\://www\.dronelicense.eu/blogs/popular/a1-a3-drone-license](https://www.dronelicense.eu/blogs/popular/a1-a3-drone-license)  
> 11. Skúška pilota dronu A1/A3 \- Dronisti.sk, otvorené mája 4, 2026, [https\://www\.dronisti.sk/drony/skuska-pilota-dronu-a1-a3/](https://www.dronisti.sk/drony/skuska-pilota-dronu-a1-a3/)  
> 12. Large Foam Drone Guide: How to Choose & Use One \- ElectronicsHub, otvorené mája 4, 2026, [https\://electronics.alibaba.com/buyingguides/large-foam-drone-guide-build-vs.-buy,-size-vs.-stability](https://electronics.alibaba.com/buyingguides/large-foam-drone-guide-build-vs.-buy,-size-vs.-stability)  
> 13. Poplatky \- Civilné letectvo \| NSAT \- Dopravný úrad, otvorené mája 4, 2026, [https\://letectvo.nsat.sk/bezpilotne-letectvo/poplatky/](https://letectvo.nsat.sk/bezpilotne-letectvo/poplatky/)  
> 14. Remote ID 2026: What it means for UK drone pilots \- Heliguy, otvorené mája 4, 2026, [https\://www\.heliguy.com/blogs/posts/remote-id-what-it-means-for-uk-drone-pilots/](https://www.heliguy.com/blogs/posts/remote-id-what-it-means-for-uk-drone-pilots/)  
> 15. A Practical Guide to Drone Remote ID Requirements in 2026 (EU & US) \- SPH Engineering, otvorené mája 4, 2026, [https\://www\.sphengineering.com/news/drone-remote-id-requirements](https://www.sphengineering.com/news/drone-remote-id-requirements)  
> 16. Drone Laws in Latvia (April 2026): Rules and Regulations Guide \- Propel RC, otvorené mája 4, 2026, [https\://www\.propelrc.com/drone-laws-in-latvia/](https://www.propelrc.com/drone-laws-in-latvia/)  
> 17. Máte dron? Pozor na zákony a poistenie\! \- A-FinAdvice, otvorené mája 4, 2026, [https\://afinadvice.sk/drony-na-slovensku/](https://afinadvice.sk/drony-na-slovensku/)  
> 18. Ako si vybaviť poistenie dronov na Slovensku \- UNIQA, otvorené mája 4, 2026, [https\://www\.uniqa.sk/poistenie-dronov-na-slovensku/](https://www.uniqa.sk/poistenie-dronov-na-slovensku/)  
> 19. Poistenie dronov \- Mám Dron, otvorené mája 4, 2026, [https\://mamdron.sk/poistenie-dronov/](https://mamdron.sk/poistenie-dronov/)  
> 20. Online skúšky pre pilotov dronov už fungujú aj na Slovensku \- DroneRepublic.sk, otvorené mája 4, 2026, [https\://www\.dronerepublic.sk/blog/dockali-sme-sa--skusky-pre-pilotov-dronov-uz-funguju-aj-na-slovensku/](https://www.dronerepublic.sk/blog/dockali-sme-sa--skusky-pre-pilotov-dronov-uz-funguju-aj-na-slovensku/)  
> 21. EASA Drone Regulations \| 2026 Updated \- Grupo One Air, otvorené mája 4, 2026, [https\://www\.grupooneair.com/new-easa-drone-regulations/](https://www.grupooneair.com/new-easa-drone-regulations/)  
> 22. Remote ID Regulations Explained: EASA vs UK Rules from 2026 \| AirHub, otvorené mája 4, 2026, [https\://www\.airhub.app/resources/news/remote-id-easa-vs-uk-2026](https://www.airhub.app/resources/news/remote-id-easa-vs-uk-2026)  
> 23. Licencia pilota dronu A1/A3 na Slovensku – online kurz s PROAVIATE, otvorené mája 4, 2026, [https\://proaviate.sk/blog/licencia-pilota-dronu-a1a3-na-slovensku-online-kurz-s-proaviate.html](https://proaviate.sk/blog/licencia-pilota-dronu-a1a3-na-slovensku-online-kurz-s-proaviate.html)  
> 24. Poistenie dronov pre hobby aj profesionálne použitie \- DroneRepublic.sk, otvorené mája 4, 2026, [https\://www\.dronerepublic.sk/poistenie-dronov/](https://www.dronerepublic.sk/poistenie-dronov/)

[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABcAAAAYCAYAAAARfGZ1AAABd0lEQVR4Xu2UyytFURSHl7zCSBmImUw8BoqSDExIKcnEgJnHBEMZGOAvMGeqKCkppUvkUTJiLnlkREaEifD7Wfves9pd2vceZXK/+uqstc9Zd92z1z4iOf6bTngR6IB7Jpg8WAoT8BN2wWJY5PKVcBK+wz73TMbcw2dY6C84zmCTnwyhXrTrbS/faq53YbmJgxkXLT5tchVwx8Qz5joj1kSL98Ma2AYP4Zy9KVse4Bs8hqfwTvTHOuxN2dAgWmjL5Mrgo+jUkALR10S4DydwxcW/wjFj8SmT43humHgCjph4UQL3YF20eIu/4OBonovOfBIeqHYTp4Ud8u8/wXxvLck8XDBxNXwVPWRsiOt1Zj1Fs6Sfb1IFl+EHrDX5QbgHu2EPPIBjZv17Cq5EO2BxTsotvIY3otPDojzym/pIiiV4CYdczK654X8C3/co3Bev47jwI/YiusnDcFV0Y2OfB9Ir0XlohEdwNlqOBzsuMTHH86cpyxHxBURxSyTri/s/AAAAAElFTkSuQmCC>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAmwAAAArCAYAAADFV9TYAAACgklEQVR4Xu3dT6hOaRwH8GdiGoqxmhh/YtiMoqREITakLGSlZmdJTbJRUsrev2wom0E2ygYLC/mzoIRYkDRqahJNLJjs+T2d5+193tOlq8t13ns/n/r2/Du9t7v7dZ5znpMSAAAAAAAAAAAAAAAAAAAAAAAAAAAAADCudrYnAADohj8jWyMf2gsAAHSLgg0AoOMUbAAAHadgAwDoOAUbAEDHfYuC7dfIvsjP7QUAAEbvauR55F3k78jBweUxeVTa9wOzAAB0xpbSvhmYBQAYYhtTszU5PTItMityp75gCM2O/NaeBAAYVhdS/1myeZH5kbX95aFzJrI5sqO9AAAwrP6L/F/6RyMbIiv6y9/F8tIuicwp/V4xWfu96q8sbS4+ewEAmBByYfMs8jByo7V2OH2+eNsduVXlZmp+43rkWP+yUcvbsZcir1L/Lt/91H+BIP/my9I/UtrzkR8j/5QxAMCE8kNq3tScUsZrSnu7tH+UdrzVd8dyf0/pv46crdZyQZmLvGxXNQ8AMGEsi1xpT4b9pT2dmrtX+WPtI1kc2fSJrKqu+1Jvq34u2Hp3+XJ/W7WWjwbpGen/AAAYepcjq6vx9tRsR2ZzU1MgzYws6l0wDvLf3VuNL1b9vF2a7wb+VMb3SptfnOg96wYAMGmcjByI/Fvar2195FB7MkxtT1R+icxozS1sjQEAJo0HqdnW/CuybnBpzPKzZ+cixyPXUnP+GwAAHZK3Wk9V/RfVGgAAHZMLthPtSQAAuiMf2ru0PQkAQDf0DsEFAKBjFqTmawhZPuftbrUGAEAHPIk8Ts1nrJ6mwbPWAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACagj7A9V9LF+jx/AAAAAElFTkSuQmCC>

[image3]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAAYCAYAAAAcYhYyAAABEElEQVR4Xu3SvyuFcRTH8ePHJFeRieiWQVJks7Ew3PIH3MFAVgvDrWtjUCaDgbJISRYGufJPWCXFaCElk4H3cc73cfpORsPzqVc9z+f7fE/PL5EyZf6eTsxh0M87MIV5dKeLyDhq6AldkVMc4E1s2AWa2McrhrGDXTTwgVndmDKDTYziC4/o9zW9C+1eMO2d5hYn4VxWMIZFsQ06NGXEu43QaZ5xnHU/ORR7nPbQLYkNmQzdhHfLoSvygMusOxJ7J3HwFj7l95GL6FfR6etZ/4TzrLvHtR/voS8t1MWG6GdNqXq3GjrdoN2a2Ps6C2uyjTu0hW4B72IXx1yhhRsMxIUKumLh6c0Lz5DYD1rm3+cbWwYurM1cW5kAAAAASUVORK5CYII=>

[image4]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADUAAAAXCAYAAACrggdNAAACtElEQVR4Xu2XWahNURjH/+YhU+YkU4aUZJ6JJKUoKaR0yxQS3igPJEqGB8MDT24JryhTkpInkQeKkClDPFCUMvv/+9bqrr3u3vdue18n6vzq97C//Z1z1rf3+tZaB6hSpQrpRNvHwaZiAK2JgznpTzfRqbQDHUgX0+VhUsR++o3+oiuie6UYTvfQ2/QnPZ+8nZtZsMGFvqKTwqQU5uMvFDUB9oVj6RcUL2omfUlv0nN0G+0dJmSgh9rkRYWUKWoGrY2DORiKf7io6ShW1BAki+pB+9BetC9t6+KiBR1NZ9N2tCPdSFcHOfUoU9Q0epYeoldhPapCG8MXtdJdH3TXvidHuPggep8ep1voE3oHVpDG3c3l1aNMUZPpezrOXQ+j72C91RC+qFXuWsWpL+fB3oznDKwIz3rYeLs6M1HShTiYE00HLesheqrf6eAoHuKL0hOXF2HfFfMJds+zAPa5hUEsFRUVfrAsu9H4IuCL0nT9TO/RNokM4wpsOno2w/a47kEslTJF3aC3aPMgthM24A1BLMYXdQS2p+nN7ktkGNrPXtNr9AB9Q5cmMjJQUZfioEPzNmvfaQZ7ig9oyyB+FDZgnTKyUO8pZ5G73kV/wLaIkMN0ImxlVP/mOla1ol/pdSQH5nkKm9faV9LYC2tuTxf6gl4OYmmMgRXlj1OtYW/hGe3nYmIHbApqQamBHcFGBvcTaCCPYK/2o/MtfUg7B3mnYUX5pTdGb1FLeS3dTu/CFp2eQU6MjmcfUPe72hLU+OotXeuetggxF3VLfahWSu1nhdHTWRMHI9Qjy+io+EYJtBioSG26fhZp+umI95iecLFCHIOdviuNZocGn8ZW2KwqxHh6Mg5WCL2p57C+Va8KLU5zYK2y1sX+mCVo4ChSAdTf62Arqv4FnILtg1PCpCr/C78BCYWZaYlqPGYAAAAASUVORK5CYII=>

[image5]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAYCAYAAADDLGwtAAAAmklEQVR4XmNgGAXUBhpArI0mZgTEQsgCmUDcA8TPgTgDKiYHxP+AeANMkRQQ90LZ94F4KZTNCuUfh/IZ4oBYF4gNgfg/lA8D2UA8G4kPBiCrfwIxP5IYyEmRSHwwuAPEO9DEtgAxN7IAiAOythlJTBmI5yPx4eA0EHdC2SCPrAJiCYQ0AvgB8SUgngTEi4HYCVUaE8ijC4xcAABA1xdmxtZaVwAAAABJRU5ErkJggg==>

[image6]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAsAAAAYCAYAAAAs7gcTAAAA10lEQVR4Xu3SLQ9BcRQG8MNQvCTzknwMpkqawkxnEzSbICuaTaDoZjrBFEGlmE3xBRQ2M4Hn3nPvnHv8P4Dg2X7hPue5Jlyin00UwrrU6cMDXtBWN2MaxOOcPpgyhisE9MGUIyx0aUqa+C90IAFFyHgWIlXi8RRm0IQT9OTIzYh43BWdNbyAX3R2DrBR3YR47EmSvn/VyhnmqqMK8TgvuqzT1URnZwg3CIpuAHeIQBlK7mEPS/fByRZW4IM1Od9LCJ5Q/+zstGBH/EJBHlLyQSQOMV3+Y+UNkPQmuk3Ojm8AAAAASUVORK5CYII=>

[image7]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFMAAAAYCAYAAACGLcGvAAADRElEQVR4Xu2YWciMURjHH/uWSNkL2VIiS7LcGKSQRLnghkiylxsk6ZULZItEtiTLBSVlzfrJVriShJQbS3EhWYps//8858w872lmvvm+bzLTa371y3ue57zv+znznGVGpEqVAkRlNFFEzlSZTBR/wkCJaQnbh8EkEjk97eBiuBWugF1Nrq5Mh59FP6zzQS6R2KrsDx/A5XAhfAK/iA5KfeEz+Y41YSJpRE5PDZxr2h3hT/jVXdeH2aKDOSpMJA1blY3hD/gbdjPxG6L9FphYXdgvOtWbholcDIADg9gw2CGIVRqR07IXXpD4f5wxDuZ8E7P0gJMl/wbzHF6CbeA4ODyezsKFeht8Bxe5GB/OT/es71ShFLuDPxSd6uE0Z/ui6NKwDN6FV+BK04ebF99zTXRA2e8qvGP6pOFU2O6uX8ET7rqZa9937XwsgbfyWOO8KTrNrsOdvKlERM7amCg6GIeCeGv4Ah4TXR4I11r2nec7gVkuxoFs4mL+mUN8JzIHDoJDXZJtz1J40LT/NZEUPgwXU5Vt4TN4BjYPcjtEn9HLxFgcjPU1sX2imxePWx6OE/sNNrEMnObfJX4Dpz93sXLAauYfy39zETkLwTWT1XRYshVleQsfBbFT8E0Qeyo6rS1H4QfYKIineQkvBzEeULngFqK3aMkX6wi9rSAppx9QXocUU5UcxC2mzRnIzYP0EX3G7mw6PTDv4UkT6yTab62JtYAf4QETy8AB4w0bTYwvO2La+ZgE19VBuxbVRkpyV2fkLMQGuDqIcUBmuuvO8Jfo7PNw/eP7eND3sD9jY0xshotNgD3hJpNLw93Of4rcfFjuXbLpspGrOiNznQsOBs+EvJcbXw28Bz+JVqeHcS5vpLvo2sp39fMdRCuX3544Jp7N8JvoGrxHchzkp8HHojdzdxsfT5eNlMSrM3Lmo5XoEYj3hLIS+WOFh5sui4gnFm60/Ar62uTJbXg8iI0UXVdPw1VBLgbLttKw1RnFMqXDr5csJAvXTH9ssvBDa8iPJ2UjJdnqimKZ+sHB4fo5xcTGij5/qoklFl+dpWC06LP8hstfhPh1cX2mR8JJSWmqknDj4A7Mg/w5uEv+k4qsUqVKg/gLAGXV9ZtxC20AAAAASUVORK5CYII=>

[image8]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAXCAYAAABJXhw0AAACjUlEQVR4Xu2WS6hNYRTHFyHJayBxQwZueQ8IlxAy8MjAwCMGYiBGUmJCkQgZoLxNPBKFpDwGXskjA/KMuCXySFEihbz+/9b6Tuuss/ep223P9q9+3bv/e52zv7X39337iJSUlLSU/nBRDB0T4AZzRjiXaAtnwU1wJexdfbo4BsEt8B78C89Xn66wHR6FC+EO+Adehh1dTQd4SvQ7JsLV8B0c62oKYzRcAkfCn5LdyCT4AHZ12U74D25z2TL4EXZyGZ/MS9jOZYWT18ha0UHvcxnvOLO3LrsPz7ljMlW0bnzICyWvkVHwLpztsp6iA3xjx93t+HClQhlh+bqQJ3rAMaJrbgBsAwfDaaLfmRgGp8MuLsslr5EsZooOcJcdN9rx/kqFMsTyvSFPLIavRWu4iZyFG0VvyA84zv4/ANfD73ABP1iPljRyC34V3SwIF3TWgHme+cmQe/qI1nDg/Szj7vcB/oJzLCNn4DN3nAkbuRDDDJbCb3CKy5qkdh2R1MjxkHvStDwR8qeiT4tNJfjEWVsXNnIxhoHJ8L3ouvFwfvMCB0M+1PI0BbPgbsgabvGex/B2yPjEW90IFxy/fKDLVtjfzvC31E4hznFeeE3IPVzArNka8ofwZsh2i9ZyU8iFjVyKodEXXrW/ifaiu1niOrzjjsl80QsPD7mnm2Q38kh0LXr2iNb66VYFB8WFdUNqX16cw5yvT+AVeE20jovutKubJ7qrNLjsiGiD9WA9B8e77Xku+ovDD/qQaC1nQBXcv/nm5bznLkT5dn4heqcI3878cJabrSbBrZMNcsodE53j/hdBZBX8LHpdbiBc3NxEXllGOTZmzfCLZZ/gcimYXnCu6JbMJ11SUlLSev4D9mmgDosC9fEAAAAASUVORK5CYII=>

[image9]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAHcAAAAZCAYAAAALx7GgAAAFhUlEQVR4Xu2ad4glRRCHy5yzmBVzjoeY9VYx/GHALAa8EzNmzBhRBHOOmNZTERUT/mP2VETFnBXTmXPOiuH3Ua/Zmr6ZebPLuvuevA9+sFPd772e7uqq6pk169HNzCTtIR0qLZy19ehippCulFaWdpd+lZYv9OjRtawn/S7N27p+QLptoLlHJzKNNH1uLGFmaTfzHQws7HUDzT06kROlTXNjGxaQvpLWzhs6lVnMi4VzzT106mJzY/iebaVTpY3Nd0YVFCiH58YR5kmrH2POVNId0uZ5Q6eytPSOdIl5brlGekKaLnZqwJzSY9Jp0prmC/yGNFvoM4d0jHnO+k36ObSNNOtKF+fGNpxl7rSwTmzoRKaVnpMeDzZ27fvSmcHWhOulXTMbk3F1uJ5HOkgaKz1qo7u4V0hr5cYacMr9pNXMP3dRsXn4mFGaNTeWQBipo0/6R7ogs1MwfGwDBUQT3paOy2xbS69mtsS9NnqLS1R6OjfW0Gc+T1Enh/ZS2DkbSGPyhgqo7E6X/pB+kZ6Rdin0GIAKD2+rY1/zgZ6R2ftb9hUyex3koh+lccE2wbxoKaPp4s5gPj+b2EARs5B53lskdQq2BYOtiu2lk3Kj+fzuIO0pLSdtWWxuDovyqXSsdIN0i/SW1Sd4+hIul5GmlDaT7jPPYflCnGe+c+rY2cp37q0te8ovTaDq5CzI51g4vpNQjQOX0XRxWdgXzL/3Tul86SrzxcHJD5COku6SjpQ+MK8f6qDvEpltQ/NUwZyhh6RXCj0asrf5RKzUuib8vStNSh0q4ClJGXgiRdFE8xsjFN5u7c9wi0t/2uRnNgohJnOnzN4O+qew9Zd0cLG5QNPFTRD2+U4cMsGGYIHjYvKb3BM7uYy5zecph8jDo8UEc/NyuG4EYYPwdW1m/9x8B9eRe1uEPEJIIQxulbXVQZj/3vymYQvpW/MFGswZcFXpdfOjEPeWFploUwaLS2ppCrv3IyvWESwqv7FksKVoNDbYIgdK++dG8aD0tXkqW8V8w61Y6NGAfcx/nElM8JwSG23t4Eao9PrN8xvnxSqalutHSy+Zh70TzHcE41k2dqqBvPiFeZpI8DdF2d9WngdZXJ7RNoWqnhojQsXKOGPoT9GjL9gihF6ObTlUwYT05JT8vVGhRwPIQ3w4/gB5AxtnzjrwRvIyN0UxdLf0npXnVooLzppD4WHpM6vP/xHqB9JCDpPDfbGbcwa7uM9KT2U28jrfH8dJ9MJGDs1hfklXZRD5cFKckgITZ/1Omj12agcHZ0JwhB3zSWYro98m9zp2/UTzsLKdeZVH2GEymgyMsHxhuKbKJm3kjkEOqsrhOFfZ4sI35g8MclhcHmQ05XmbfHEZd764O7ZsZbvuFGmb3NiCyBWPl0uZR50yJ6mkzzzhp4k/wnwwN6YONYzPDQEG/Yh5XqKaXL3YXAlFA+ETqMDPMa8SoxMtZn6jbwZbBIfAy3GuCEeJF628YiY6UAzx2XaQZ8nnLABjTFxuPnfRiXl8ii2mPSCHEtbLxgKTzNNTYlHzonf+YGsLg+PJDRXt/dLZ5oPZK3YaQcabH6U4RjAeCpf5Ygdzj35N+smqizpyFqGcp10UJRPMdxo7IDGXeVohlfzQEsUb1XnM15H1zY+MqT9/syupnnEobDzIp1DiiPNly0aRGE8BPFq9LFznMAb604eIQN0xrtBjCKR8WzVpIwGVMrmq3QvoS62+LiBvrWH+QptQPNQXEP8F7PK6AjO9q2XMuXM3Yoz5mxcmIUF4GsyjsNGCsHZPbuwSCMV5vh52KCIIbbwpIY8cL31o5UeFTuMwKz8fdgOc+6segw4bvE2gFCc33CwdYt3zz1Ys7GBeJHQSN5kXhT3+h1As9ujRo0fGv8WhJNDpaJ4WAAAAAElFTkSuQmCC>

[image10]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEwAAAAXCAYAAACh3qkfAAAD9ElEQVR4Xu2YZ4hVVxSFtzU21Gjs4ogBiWIFFRvOYEUQkhjFxJ4QMCi2gKIRcRQUFLuIHeeHEEMKYgF7CTEaIiL6Q8UyUUERSyyIBSxrsc9h9j3vPuddhnnOj/fBgrnrnnfLPvvss++I5MiRo/ypGxo50tMPWhKaSfkI2gvlhSdAC+h7aB7UNTiXKeOgEVAbqDbUB5oBtbKDssQ2qEtoJmUp9BZqF/jdoH+hKVAv6GdoV2REZpwQvb7VBqi6HZQFakJ/h2ZSekDPJD5gxZKadQwgMyYJx0Uf9LRooD6PnM0e30BzQjMJXIqc/eWSGrCWzuPysayG1gdeaRyFWofmB2CflLEMLIZGQ7MlNWCVofvQFain82pBl0QLZxKOSPKAdYQKoGHuuD40COoEVXJePWiw6NjSaAodDk3Ra+WLlp3e0FDRREqBBfx393dcwMgC57+G1kD7oamREZnBB50MHYDOQGtF60k6qkJ/QS9FJ20CtAeaBd2AfoWGiF6Xz34SOgdV4Y/TMBP6LvAaQBdErz8A2iL6vp/YQYQPdAxq7o7TBYyw5vAcdRfqHz2dEQwUd6dqovdeBV2U0rNuK/QG2mg8Bp7PclZKMo1ZR2+UHxQDa2jYf02X6CbG6xVLTMDYInxrjtMFjMWdD8bZ5A055pVoCiehregS9+SJXqvIeHGwXnLcZ8Yb6Ty2Op5mzltgPEsH6JfQBPNFJ4T3YSJw1+a9IpnKoOy2hsQHrDv0P9TYHfOFf4ReQJf9oAzxmeBhpvF+NwM/ZKXouDrG+8p5rF2eJs4rNJ6FbZOvhZaPoT+lZAU9FV26EZjSrAP/QdedHov+4Jbo1k+4nrmMQhaJjuX6zwQ+6CPRzPBwBjmzrE/vY4XovWy9+9J53AA8jZy30HgeTjRXCUtBCDOK59lazYXOi16nwIyJZZ2kZhjTNC5gnaHnEn2A9ubvkEmim8Z44/kldMh4cbDWhQEb7jwbMK4CepzMEC41blhx8P1Y7D18p2KJD3wEFlXekMHw5EMPoU+NRzjr3Ag8E0V/u8l4FmYi2wouQw+XNoPY13hxbBa9NjPI87XzvjCe7xnZT4ZsF/1iiaNI9JPQ11eWjquin3GxsAe7JrpknogG6JQ5z6zgVwDbD6bsQWinaD/mYe9yR7RfS8c00W6/UHTnewCNMedDuFRYNlhT+Fwcz2/PP6B7zqN2QD9Bt90xx/OFPczMf8xxSBH0m2hQmQj89FsmqTU3EWwOB4oGl7tNOuKaQksN0XrGxjDT+ldWmI0MaDq4WXj4T4aswZtxlioa7AbK9ClUXrDztvWvItBQtGGucLB7HhuaFYAfRDekHBnCgNmGN0c2eAfqNtNCIMyJVAAAAABJRU5ErkJggg==>

[image11]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGMAAAAXCAYAAAAfiPFCAAAExElEQVR4Xu2Yd4gkRRTGP3PAjAHjrTkrBlSMIByoqGAOIIsRDCiC+I+CigFFEcxZENNhwqyIAcV4p5hzuDUjmHPW99vXtVP9pruvd8Ddm3N+8MH06+rq8FXVezXSgAEDBkwEi8bA/53FTAvH4ATxgGmR7HgB05LZ8bgYMg3HYMFtpgNMm5s2Mm1QaH3Tylm7HB7mXtOUeKIl85qmmk4z7WCau3y6xHmmP0z/mA4J5yYC3vGO4ve2ph/kz/LQWIsWrGs62/SC6W/TfeXToyxo+kveeZUu7zQtcY78PPcYL6uaZppONm1vut90QqlFN7tp8sw4ybR3dswM/UzjNGML+cNvZvpN1WYwAz4xXWO61HSR6QLTTfIbLtNpOgb9/qTezOBFXjMdVBzPJ3+2F8daVMN9JsuM5+SDNucVjdOMnDoz9lT3qJzLdI9pxxAHlqfH5UtHL2ZgMuazTCW4/z7ZcRVraXLM2NJ0dQwaL+k/MIOZMRRix5rODLEE8QNNJ6o3M74x3Vn8XkHtE/KaKpvBjOX65UwryUfu0vKPt4tpDfmgWs+0k2kJv2yUDU07q12FdLE8p0WYycmMKfJ7LN453UydGZF15FMwH7mJTUy3F797MWN1+TU3mm42XWX6yHStaZ6sXRXJjEOLY5bSlNc+lQ+qg00fFjEKA0w/3XSd6VfT1sXvK02nypdaBlYdLKHkW0yNEH9UvkIwc06R9zecN6qjrRksT8fEoNycx+SjEXoxY1/5Nb/IRywsJP+Y5KsmkhmHFceYMl0+C3IjmSW04+OvUsSo1D43/a7yckiF9GZ2HNnddFYMFmAG96EKTdxiejc7rgUzqFqa4ANRda0YT8grCkZeohczjpZf83CIT5N/vKVCPCeZcXgh6n6MjLAc0Y4+c16Xz5q8hL5C3raOW1X/fphB7ssHwiXy/mY1y0fN4AWa4OFY0yM80N0h1osZjEquYZnIYZoTb0riyQw+ws/yioxiIkK1RjuWj5xXTU+H2GWqNwNTn4zBDJ7j+RCjEqW/qiW+RBszPjDNiEHjKPmoGpG3Qd/Jb/yx6dmxls2wqeSaC0Oc3EF8/xDPSWaQULcy/Wk6t9TCISnTjn1Qzsvq/rhpJFflhCNMx8VgBgmckjcn5TFyTSOY8WAMZiwv7+iReKKGNArizFhN3TV5gpdm73JDiJPM8zW+irXl99urOD5Dvlll05hDRVNlBkXJUyFGnqJt1e6f5LxsDGZgbjSDQTZLMzhJ8npC9VNoqrwjEngb2JnTfuMsxs6anPN2Fouw68aQVAbyPCPq/niRTeX3S5vF+eVJeURlEykwaMeoz3lLvrTkHz4tj/l/TjCk5u9ATiDxY3DeX/omlSUulQbZnZf/vtAXpnfUfcE28o6uD/EIpeD7pm/l/X1teqY4x3r9hulHeRlbBQ9P1cF6S/lJX5SbTTU/f+mQy9I73GXaQ547OOYco5LN41dFjP+PWFrZuM7MruVbEHtPnXf40nSkOjBg9suOc7aTD4LUH7+r+quqSFvDErKrmqdmW5j+7Jib4A9JylT+qpndYPmpqtT6Dkxtyk2zOwyOqr8/+pLjVZ7y/cb56i4K+haMqCoV+wHyGRVXvz7/HAV/Pg7H4IA5iH8BRNgmThC9tbcAAAAASUVORK5CYII=>

[image12]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGMAAAAXCAYAAAAfiPFCAAAExklEQVR4Xu2YV4glVRCGyyzmnMMYMWMOiLgoijmsOcOCCQwPioqoD4piQEHEjCjqrj4YEOOD4qooRsScXROKopgxh//bOoepW9t95zLeWVT6g5+ZrtN9uk9Xnarqa9bR0dHR8T9hPmmJbJxoRqSjsrFwh3SItLm0kbRB0frSyuG8ysbS2dL+0gJpLHORNDkbWzhXekN6R3pbek+aIU0K5wyLraTvpb+kR9PYhLCudKH0gvSndH/v8Ezml/4wf6gmXTN66swo4sFvknY0n/veMJ7Z1XyO4/PAGPDcXPeBtGjv0FBZWPrYZpMztpSmSJtJv1izM9gBn0g3SFdJV0iXS9OkT6WlR0+1m8t5FRaBIxcPtgov8V0bnzOWNb/u9TwwATxns8kZkTZnkEJOTbY5zCN+h2A7xvwFEbWVPczTVRPXS2fa+JyxlPl1r+WBCeAZ+xc5g50xkmwnSecn293SN+V/op4X1sZO0rXmO3M8zljS+juDOkZwHCGtlsZGpG2lPaXli20Z82fZRdqw2CpPW7MzFpEOko41zywRsgVzs4NXsNEGANtK0irlnFbanJFZR3pZmjvZya1vmjuJdPWi9JT5QiMLSU+YL2bYzmDHUuSfN39RB5sX+DPCOddJP5tfz8uHo6WPii0HWZMz9jafF0fg1OnSbdKCZfw083fBfD+YBwbcWGzUZ7JCK4M6g/R0QrLxwrnJ7+YLA17MXdIr0pzFBtSc3cr/w3bGidKP0mLBNsm8buGcyqHW6wxgNw3ijE3M17lzsLH+z6Srg43ijyNwUoX3QNBuEWyN4IwHsjGxnrlXV0x2WlwWwhxzBftxxb57Od7OPDoq/9QZrwYbC/3amgPqWen9cLyPzeoMmoxBnHGP9J31rhMuNr9+1WBjrT/ZaHCQHqPDWuFFPpiNCfI8C86Q/3gQev/I4cV+pXmL/Jj1fkCN1xn1ftEZaxbbrcFWedh8rHZ1e5VjWuvKoM6gs0SZs8yv3zfYCL64PpoWvtXGZBBnEF20ehmikmihlkQOM38YvkXY3h8WzTCf6/My/mU5zsW2spz1bu3a2pICK6sX253BVnnSfKzWL3Yqx3XHAkEyiDOoLV+F4wrXcf0Byf6WeQ3j4/fxNNYKzngoGwN0AtzskTxQuN1mjZja7h6Y7JX9rDdy2sBRnLd1OaYb4ZhFVggIXhQpKcKOpGDH9EV64nqKb6Wm2guCDZhvejhm51GDqAkRdj3BVYt45XTzeS8zr2ljMo/0q7nncpdUoR1l0rYv6u3NH5LUU5lqHlkU8ybodpjz5DyQYMd9Ia1RjuliuC5/w1AL+AmD3Fw50vy5Ng22taTfzAt55VLzOeNHKw7m3qyhNiE8A0EXOzTmw+FN62BXcy9qR9/fuOhq+J2HL2nSDMK75P78MwML5GFvSfbIKeZRfJ55+0prSyucYUHcl+3OPb+1/mmKe5MqcAK7iOcl9TUFztrmjQidHDuHAOO3ssw50kvSJebtLu+C9SE6o23K3/peuCepFng31E+yxH3mv5FNLmNNUPT5xWJoEN18UefvhgyRMMV8cW07YjzMa75gUguppx/clxoykuwZOiIKf/0xkw9c0vFY81dYK84ns/QD5+W01tHR0dHR0fFf5m8u/DF52+w3dQAAAABJRU5ErkJggg==>

[image13]: <data:image/png;base64,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>

[image14]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGEAAAAXCAYAAAAbfSF/AAAEqklEQVR4Xu2Yd4glRRCHSzFn0RPzneKBWVSMmAMmDgwYUPBQUPQPUcGAoGBAUfEPA2aRNZ9g4gynGBEDIooRs2JWDJhz+n1U9269upn39h2yy8F88GN3quvN65nqrqp+Zh0dHR0dk8AC0inS0nlgAItKO0gzpJWDfbl0/b8xTZqZjYHtpbOK9k5jlQXNJ3yudKK0Su/wpLGt9K90eB5oYRnpMulr6QVpRLpFukCaIt0rHVR8F5Hekd4tf6veknYtPn1ZTzrf/Iv+ke7vHR7lIukm6TDpYulv6RFpseDDZO4wvwerh5X3qbRN8JksmDNBaHu+yHTpTfOXul0aO0D6yvxeNQiVtYqdwMX3MpAtpSOlzaXfrXmSO0kvma+OyiXmX3hhsB0jfSktEWzsCFbFQsE20ZCKmMP30h/S8r3DPSwsvSL9JW2YxirspqYgrFjsnyX7ULQF4XTzm18VbKx0bJ8E24vS7HANu5n75RU1kZBG75RuMJ8Li66N08x9rsgDgaWkX609COz+eaYtCFtIz0n7BdtK5l/4UbmmUHHNg0Y2K/Yzkr3CxLcyrzHrmK/a9aU9ze9Z2Ujay4YvrEBuP0Tax3wuD/UO9/CquQ91rR8EtS0IcWEOTVsQmqgPdGm5Jo9yffWoh7NBsV+Z7JUjpA/NfSj490jnmAfzN/OCyv/XSGdKP0uH8sFxQqPwnvnqJdV8K/0prRCdCjQRzAO1paIKi3DZZKtB+DjZh2KYIDwt/WBe2IHi2/SyGcd+e7JHVjf34aWvWWy8vM/Nc/iBxQZ3SW+E60HsaN4sVK43/66jgq2yiY0FIda/8VKDULPDPEEQHsjGBo6WfpR2CbatzScQ6wbUINya7JGaymYl++vmu4SAVNhp+I6Xy603iHuYf/7hYKusYWNBWDuNAbsdn9WKplrvWWFQEBY39+kLQZiTjYmdzas/dSJCPmcC1yY72xp7TVtNsOrwoQ2OkJ+fSTZ22niDQPC+MO/X6XheNg8sn6f7mTLmOgq7jPHd84C4z7wt/8Xch516chgfFISDpeOyMTMoCBRHXsy6wXZ8+UvO5cFy2qmHpFOTPUKxxYeDUISX9lSysbLxpYAPggVzt/ncokbM70FLnTnbfIyzUxsj5j65Ng2qCdQ1zhl9IQgPZmOBbfhY+Vuh0NE1VZ6Qng3XQFfCxDZO9ggFrikIrF5qT4TWEd+Yotpg17D6MjUl8TwZzjgc0mhBp/UOjXKb+efzvfsFgYMsTQGLshVeKEXwSZv7YEXOZhu/Jj0qPW7ux9alVaswKbqXVYPtRvPg9AN/Js8qj3Bq5SQfX/h15r6s6H4QdB666XzCCyGlcOqfmsZgU/Nen2emWEeoBaQh5pBb1Npd5cMac3m+jHGqngv6c06TfJBuB3HqfdvGWjBOvdygSecVnwrtJcEhTd1sntP7dRonSd+Yfy/FnkJMwf+g2BBzw8YK/a7Y+GngWGuGB+Ze+P0knRDGZprfr46j96Ulgw9QcEmtnLLJDqQn6h27k5fPrt2/+BLUOt/6Xvhpg0Ayz2rjZyF+EJwQeAAmStvKDpufIQvsa36e4eQ9aAd2dHR0dHR0zK/8B5fRLxpgs+0oAAAAAElFTkSuQmCC>

[image15]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADoAAAAXCAYAAABaiVzAAAADRUlEQVR4Xu2WWahNURjH/2aJDCEPHgyRmxciU3hQZHggL+YuLsqQhMxJIlOGFOFFlCgeyPhAN9ODB0KZCZmHPJC58P/71t5n7XX2Oe7p3pej86tf965vrfY+317fGoASJUoUG+1oeRjMw2I6lLamLd3/ioU0o5PoBjqVNkh2x/Smy+kK2j3oqzZldD29Sn/Rk8nunNSivwO/0Wn+INKW3qabaV+6i96hLfxBZCG9RUfTcfQ+nZMYUU16wb5yD/odVU9UfKEXaSVsttJm4RA9EcQu071euwvsQ/X0YkNgv6ezF6sxCk30cRgIaAV75vwgvoZ+RqaEt9CPme6/1IdVmMq4xik00UdhIGAUbKamBHElrvgA175On2a6Y5T8uTCYgj7oMNrRtQfSlbRTPCKg0ESf0Hn0LL1JZyR6gemwhLTmfGa7+BjXfkHvZbpj3sHWcz6WwT641vhhWJXtpkfodm9cgkIT/Uor3P/aXC7Q47Suiy1FMqGImS6uv0LvTUvojTMX3WDPGenaeu9LuglW+o1dPAu98FQYzIM2EZ9y2Isnu/YS1x4bDXBEiUYVoN36bqY7Rknqh+diAew5OpYirtEbXjsVJXo6DOZBR4zPYNiL97u2jhq1J8QjDB0biusoEc/pg0x3zHvYkshFf9hztESENjd9nG3xiBwUkuha+pZ28GKDYC/W+hDaIPwSjdC68mfiCrJLVB+xKr/nPGxdboVtXJW0eWJECnrwmTCYg4P0E5LlqxJVArrdiEawY2RdPMLQpUEfqY5rr4IdJQ2jAaQN7FlzvViIbmQ6o7U2+9D2ye506tEfsA0l2kzyMQJ2SYjQDByjr5C89eyErZvarq1N4iEsuQgdC/poOo4idIl5DUs4F03oB9hxpfFaIvpdqZvQcNj60KLXuSVVRrqCNfXGhWg29tGjsBlUiemI0A3LR4np+JEq4Ut0R2KEoTLXR1oNu5LqyOiaGJGNJkcTo5n3VQ46bmoUXeZVstoY/NILUYnrPC0LOzw0E/rwSlqz9S82wo4zTYgqSpWoctbN6yeyT4Wi5RmdGAZhM62lMD7sKFYWwXbcfl5M18E9sKWXulaLFd2XVaoHYJuhkpyF/yzJEj5/AHY7undZmYpEAAAAAElFTkSuQmCC>