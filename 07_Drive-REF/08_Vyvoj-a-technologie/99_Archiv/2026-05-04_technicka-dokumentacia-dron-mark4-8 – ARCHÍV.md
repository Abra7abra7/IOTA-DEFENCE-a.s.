# **Technická dokumentácia: GEPRC Mark4-8 UAS**

Tento dokument slúži ako podklad pre technický opis a registráciu bezpilotného leteckého systému (UAS) na Dopravnom úrade. Obsahuje podrobné špecifikácie komponentov, výkonové charakteristiky a bezpečnostné prvky.

## **1\. Základné technické parametre**

| Parameter | Hodnota / Špecifikácia |
| :---- | :---- |
| Dĺžka (rám) | 367 mm (diagonálne motor-to-motor) |
| Šírka (rám) | Cca 280 mm |
| Hmotnosť (MTOM) | \~1 650 g (vstavaná váha \+ 6S 5500mAh batéria) |
| Operačný dolet | 5 \- 8 km (v závislosti od terénu a rušenia) |
| Maximálna doba letu | 18 \- 25 minút (podľa štýlu letu) |

## **2\. Pohonný systém a efektivita**

Pre účely registrácie a posúdenia letovej spôsobilosti uvádzame pomer ťahu k hmotnosti (Thrust-to-Weight Ratio), ktorý určuje manévrovateľnosť a rezervu výkonu.

> * **Motory:** iFlight XING2 2809 1250Kv  
> * **Vrtule:** HQprop LR8X4.2X3 (8-palcové, trojlisté)  
> * **Statický ťah (jeden motor):** Cca 2 600 g (pri 100% plyne na 6S)  
> * **Celkový maximálny ťah (4 motory):** 10 400 g  
> * **Hmotnostný koeficient (Pomer ťah/hmotnosť):** **6.3 : 1**

*Poznámka: Pomer nad 2:1 je považovaný za bezpečný pre stabilný let; pomer 6.3:1 indikuje vysoký prebytok výkonu vhodný pre náročnejšie operácie a AI stabilizáciu.*

## 

## 

## **3\. Detailný rozpis komponentov**

### **3.1 Rám a pohon**

> * **Rám:** GEPRC Mark4-8 (odolný uhlíkový rám pre 8" vrtule)  
> * **Regulátory (ESC):** AM60 AM32 (podpora vysokého prúdu)  
> * **Akumulátor:** GNB 5500mAh 6S 70C (XT60 konektor)

### **3.2 Riadiaca elektronika**

> * **Riadiaca jednotka (FC):** Skystars H7 Dual Gyro (vysoký výpočtový výkon pre stabilitu)  
> * **Rádiové spojenie (RX):** Radiomaster XR1 Nano ELRS (868MHz/2.4GHz)  
> * **Navigácia:** FlyfishRC M10QMC-5883L GPS s integrovaným kompasom  
> * **Filtrácia:** Kondenzátor 1000uF 50V pre elimináciu napäťových špičiek

### **3.3 AI Modul a Autopilot**

Dron je vybavený palubným počítačom pre pokročilé spracovanie obrazu a autonómne funkcie.

> * **Palubný počítač:** Raspberry Pi 5 (8GB RAM) s aktívnym chladením  
> * **Napájanie AI modulu:** BEC 2-13S 5V 5A  
> * **Senzor obrazu:** Raspberry Pi Camera 3  
> * **Prídavné systémy:** Micro Servo MG90S (mechanizmus pre zhadzovanie nákladu)

### **3.4 FPV (First Person View)**

> * **Kamera:** Caddx Ratel 2 Micro (vynikajúca citlivosť v šere)  
> * **Video vysielač (VTX):** Axisflying Smurfs 25-1600mW  
> * **Antény:** Foxeer Lollipop 4 Plus (vysoký zisk)

## **4\. Vyhlásenie k bezpečnosti**

Dron je vybavený systémom GPS Fail-safe. V prípade straty riadiaceho signálu alebo kritického poklesu napätia batérie je aktivovaný režim "Return to Home" (RTH), ktorý zabezpečí autonómny návrat na miesto vzletu a bezpečné pristátie.  
Zariadenie spĺňa požiadavky pre kategóriu Open A3 podľa nariadení EASA, pričom vyžaduje registráciu prevádzkovateľa a označenie identifikačným číslom.