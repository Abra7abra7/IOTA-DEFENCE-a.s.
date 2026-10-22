# **Komplexná správa o vývoji a integrácii autonómnych systémov pre UAV na platforme Apple Silicon 2025**

Súčasný rozvoj technológií bezpilotných lietajúcich prostriedkov (UAV) v roku 2025 dosiahol bod, kedy sa hranica medzi simuláciou a realitou stáva čoraz tenšou. Pre vývojárov pracujúcich na platforme Apple Silicon, konkrétne na najnovšom modeli MacBook Air 2025 s čipmi rodiny M3 alebo M4, predstavuje integrácia komplexného softvérového zásobníka (stacku) výzvu, ktorá si vyžaduje hlboké porozumenie architektúre ARM a špecifikám operačného systému macOS.1 Táto správa poskytuje vyčerpávajúci pohľad na najefektívnejšie metódy prepojenia systémov ArduPilot, MAVLink, MAVSDK a simulačného prostredia Gazebo s primárnym zameraním na prípravu prostredia pre pokročilú integráciu umelej inteligencie (AI).

## **Architektúra a hardvérový kontext MacBook Air 2025**

MacBook Air 2025 postavený na čipe M4 prináša do sféry robotiky bezprecedentný pomer výkonu na watt, čo je pre vývojárov simulácií kľúčové. Zjednotená architektúra pamäte (Unified Memory Architecture) umožňuje procesoru (CPU) a grafickému akcelerátoru (GPU) pristupovať k rovnakým dátovým blokom bez potreby nákladného kopírovania medzi RAM a VRAM.3 Tento mechanizmus je fundamentálnym predpokladom pre beh neurónových sietí v reálnom čase, kde vizuálne dáta zo simulátora musia byť okamžite spracované modelmi počítačového videnia.

Pri vývoji autonómnych systémov na zariadení bez aktívneho chladenia, akým je MacBook Air, je však nevyhnutné brať do úvahy tepelný manažment. Dlhotrvajúce simulácie v prostredí Gazebo Harmonic, ktoré využívajú fotorealistický rendering, môžu viesť k tepelnému škrteniu (thermal throttling), čo následne ovplyvňuje presnosť fyzikálneho modelovania v ArduPilot SITL.5

| Komponent | Špecifikácia pre rok 2025 | Význam pre UAV vývoj |
| :---- | :---- | :---- |
| CPU | Apple M4 (10-jadrový) | Zabezpečuje beh letového algoritmu (SITL) a logiky MAVSDK bez latencie.7 |
| GPU | 10-jadrový GPU s Ray Tracingom | Umožňuje hardvérovo akcelerovanú simuláciu senzorov v Gazebo.8 |
| Neural Engine | 16-jadrový (38 TOPS) | Kľúčový pre inferenciu AI modelov mimo hlavného GPU.3 |
| Pamäť | Minimálne 16 GB Unifikovanej pamäte | Nevyhnutná pre súčasný beh simulátora, IDE a AI tréningu.4 |

## **Softvérové základy a správa prostredia**

Prvým krokom k úspešnej inštalácii je nastavenie robustného základu pomocou správcu balíkov Homebrew a izolovaných prostredí Python. Na platforme Apple Silicon sa Homebrew inštaluje do adresára /opt/homebrew, čo odlišuje súčasné postupy od starších manuálov určených pre procesory Intel.9

### **Inštalácia Homebrew a systémových nástrojov**

Proces začína v termináli, kde je potrebné spustiť inštalačný skript a následne nakonfigurovať premenné prostredia pre shell Zsh.

Bash

/bin/bash \-c "\$(curl \-fsSL https\://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"  
echo 'eval "\$(/opt/homebrew/bin/brew shellenv)"' \>\> \~/.zshrc  
source \~/.zshrc

Tento krok sprístupní príkazy potrebné pre kompiláciu ArduPilotu a správu knižníc MAVLink. Je dôležité zdôrazniť, že pre správnu funkciu Xcode Command Line Tools, ktoré sú integrálnou súčasťou vývojového prostredia, je potrebné spustiť príkaz xcode-select \--install ešte pred inštaláciou Homebrew.7

### **Konfigurácia Pythonu pre AI a MAVSDK**

Pre rok 2025 sa odporúča používať Python verzie 3.10 alebo novšej, pričom správa verzií cez pyenv alebo conda (Miniconda pre Apple Silicon) sa ukazuje ako najstabilnejšia pre projekty integrujúce AI.1 Natívna podpora pre arm64 architektúru v knižniciach ako mavsdk a torch je kritická pre dosiahnutie maximálneho výkonu.10

| Nástroj | Účel | Odporúčaná verzia |
| :---- | :---- | :---- |
| Python | Základný jazyk pre AI a MAVSDK | 3.11+ 12 |
| Pip | Správca balíkov | Najnovšia |
| PyEnv | Správa verzií Pythonu | 2.3+ 7 |
| Virtualenv | Izolácia projektových závislostí | 20.0+ |

## **ArduPilot SITL: Jadro simulovaného autopilotu**

ArduPilot SITL (Software In The Loop) umožňuje spustiť kompletný kód letového kontrolóra ako natívnu aplikáciu na macOS. Pre MacBook Air 2025 je najlepším spôsobom natívna kompilácia, ktorá plne využíva možnosti čipu M4 a minimalizuje latenciu pri komunikácii s externými AI modulmi.11

### **Príprava zostavovacieho prostredia**

Inštalácia závislostí pre ArduPilot na macOS vyžaduje inštaláciu špecifických knižníc a kompilátorov pre architektúru ARM.

Bash

brew update  
brew install gcc-arm-none-eabi genromfs ninja gawk  
python3 \-m pip install empy==3.3.4 pyserial mavproxy

Použitie verzie empy 3.3.4 je kritické, nakoľko verzie 4.x menia API, ktoré zostavovací nástroj waf v ArduPilote nemusí plne podporovať.11 Po príprave nástrojov nasleduje klonovanie hlavného repozitára so všetkými submodulmi.

Bash

git clone \--recursive https\://github.com/ArduPilot/ardupilot.git  
cd ardupilot  
./waf configure \--board sitl  
./waf copter

Kompilácia na Apple Silicon prebieha vďaka vysokému počtu výpočtových vlákien mimoriadne rýchlo. Výsledný binárny súbor sa nachádza v adresári build/sitl/bin/, kde je pripravený na spustenie v spojení so simulátorom fyziky.5

## **Gazebo Harmonic: Pokročilá fyzika a vizualizácia**

Gazebo Harmonic predstavuje v roku 2025 vrchol simulácie pre robotiku, nahrádzajúc staršie verzie Gazebo Classic. Pre macOS je táto verzia optimalizovaná na využitie rendering engine-u Ogre2 a Metal API, čo umožňuje plynulú simuláciu aj na zariadeniach bez dedikovanej grafickej karty.5

### **Inštalácia a konfigurácia pluginu**

Prepojenie ArduPilotu a Gazebo sa realizuje cez plugin ardupilot\_gazebo, ktorý prenáša dáta o stave drona a príkazy pre motory pomocou JSON protokolu cez UDP sockety.5 Tento plugin je kľúčový pre simuláciu v reálnom čase s podporou pre "lock-step" synchronizáciu, ktorá zabezpečuje, že fyzikálny čas simulátora a čas letového kontrolóra zostávajú v dokonalej zhode.8

Inštalácia pluginu na macOS vyžaduje nastavenie verzie Gazeba pred kompiláciou:

Bash

export GZ\_VERSION=harmonic  
git clone https\://github.com/ArduPilot/ardupilot\_gazebo.git  
cd ardupilot\_gazebo  
mkdir build && cd build  
cmake.. \-DCMAKE\_BUILD\_TYPE=RelWithDebInfo  
make \-j4

Pre korektné načítanie modelov a pluginov v Gazebo je nevyhnutné pridať cesty do .zshrc. Tieto premenné informujú simulátor, kde hľadať modely drona Iris alebo Zephyr a kde sa nachádzajú skompilované knižnice pluginu.5

Bash

export GZ\_SIM\_SYSTEM\_PLUGIN\_PATH=\$HOME/ardupilot\_gazebo/build:\$GZ\_SIM\_SYSTEM\_PLUGIN\_PATH  
export GZ\_SIM\_RESOURCE\_PATH=\$HOME/ardupilot\_gazebo/models:\$HOME/ardupilot\_gazebo/worlds:\$GZ\_SIM\_RESOURCE\_PATH

## **Komunikačná infraštruktúra: MAVLink a MAVProxy**

MAVLink je chrbticou komunikácie v ekosystéme ArduPilot. Pre efektívne prepojenie viacerých komponentov súčasne – simulátora, riadiaceho skriptu a pozemnej stanice – sa ako najjednoduchší a najlepší nástroj javí MAVProxy.15 MAVProxy funguje ako inteligentný router, ktorý dokáže duplikovať dátové toky pre viacerých klientov.16

### **Smerovanie dát pre AI a monitoring**

V prostredí MacBooku Air 2025 chceme typicky dosiahnuť nasledujúcu topológiu:

1. **ArduPilot SITL** generuje telemetriu.  
2. **MAVProxy** prijíma dáta a posiela ich ďalej.  
3. **QGroundControl** (GCS) vizualizuje stav na porte 14550\.  
4. **MAVSDK-Python** (AI skript) spracováva dáta na porte 14540\.16

Príkaz na spustenie SITL s takýmto smerovaním:

Bash

sim\_vehicle.py \-v ArduCopter \-f gazebo-iris \--model JSON \--map \--console \--out=udp:127.0.0.1:14550 \--out=udp:127.0.0.1:14540

Použitie prepínača \--model JSON je kľúčové pre komunikáciu s moderným pluginom Gazebo.5 Každý parameter \--out vytvára nový UDP stream, čo umožňuje, aby AI skript bežal nezávisle od vizuálneho monitoringu v QGroundControl.16

## **QGroundControl: Inštalácia a konfigurácia**

QGroundControl (QGC) je primárna stanica pre plánovanie misií a konfiguráciu parametrov. Na macOS 12 a novšom (vrátane macOS 15 v roku 2025\) je QGC vysoko optimalizovaný pre Apple Silicon.18

### **Riešenie bezpečnostných povolení**

Keďže QGC často nie je podpísaný oficiálnym certifikátom Apple pre každý beta build, používatelia na macOS Monterey a novších sa stretávajú s blokovaním aplikácie. Najjednoduchším riešením je kliknúť pravým tlačidlom na aplikáciu v priečinku Applications a vybrať "Open", čím sa vytvorí trvalá výnimka v systéme Gatekeeper.20

Pre potreby AI integrácie je dôležité nastaviť QGC tak, aby automaticky prijímal video stream zo simulátora Gazebo. V nastaveniach videa (Application Settings \-\> Video) sa nastavuje:

* **Video Source:** UDP h.264 Video Stream.  
* **UDP Port:** 5600\.5

Tento stream je generovaný pluginom v Gazebo a umožňuje operátorovi vidieť vizuálny vstup, ktorý zároveň spracováva neurónová sieť v MAVSDK skripte.5

## **MAVSDK-Python: Most k umelej inteligencii**

MAVSDK predstavuje moderné programové rozhranie, ktoré nahrádza nízkoúrovňový pymavlink pre väčšinu úloh spojených s autonómiou. Jeho asynchrónna povaha (asyncio) je ideálna pre integráciu s AI frameworkami, ktoré bežia vo vlastných výpočtových slučkách.13

### **Inštalácia a základné pripojenie**

Inštalácia na MacBook Air 2025 prebieha jednoducho cez pip, pričom balík už obsahuje binárny súbor mavsdk\_server skompilovaný pre architektúru arm64.13

Bash

pip3 install mavsdk

Základný skript pre pripojenie k simulátoru vyzerá nasledovne:

Python

import asyncio  
from mavsdk import System

async def run():  
    drone \= System()  
    \# Pripojenie k portu, ktorý sme definovali v MAVProxy  
    await drone.connect(system\_address="udp://:14540")

    print("Čakám na pripojenie drona...")  
    async for state in drone.core.connection\_state():  
        if state.is\_connected:  
            print(f"Dron pripojený\!")  
            break

if \_\_name\_\_ \== "\_\_main\_\_":  
    asyncio.run(run())

Tento kód tvorí základ pre akýkoľvek autonómny systém. Vďaka MAVSDK môžeme jednoducho pristupovať k telemetrii, ovládať misie alebo prepínať do režimu Offboard, ktorý je pre AI integráciu najdôležitejší.22

## **Príprava na AI integráciu: Využitie Metal Performance Shaders (MPS)**

Najväčšou výhodou MacBook Air 2025 pri vývoji autonómnych dronov je prítomnosť výkonného GPU a Neural Engine. Pre tréning a inferenciu modelov (napr. detekcia objektov pomocou YOLO alebo riadenie cez Reinforcement Learning) je kľúčové použiť PyTorch s backendom MPS.1

### **Konfigurácia PyTorch pre Apple Silicon**

Tradičné návody pre AI často predpokladajú prítomnosť NVIDIA CUDA. Na macOS je však potrebné explicitne definovať zariadenie mps.

Python

import torch  
if torch.backends.mps.is\_available():  
    device \= torch.device("mps")  
    print("GPU akcelerácia cez Metal je aktívna.")  
else:  
    device \= torch.device("cpu")

MPS backend mapuje výpočtové grafy PyTorch priamo na vysoko optimalizované jadrá v čipe M4.1 To umožňuje spracovávať video stream z Gazebo s frekvenciou 30+ snímok za sekundu priamo na MacBooku Air, čo by na CPU bolo nereálne.25

| AI Úloha | Backend | Výkon na M4 Air |
| :---- | :---- | :---- |
| Detekcia objektov (YOLOv11) | MPS (GPU) | \~25 ms / snímok 26 |
| Spracovanie telemetrie (LSTM) | CPU / MPS | \< 1 ms |
| Reinforcement Learning (Inferencia) | MPS | \~10 ms |

## **Prepojenie AI cyklu: Od senzora k akcii**

Kompletný autonómny systém na MacBooku Air 2025 funguje v uzatvorenej slučke, kde simulátor poskytuje dáta, AI model ich vyhodnocuje a MAVSDK vykonáva príkazy.25

### **Mechanizmus prenosu dát**

1. **Gazebo** simuluje prostredie a kameru drona. Obraz je kódovaný do formátu h.264 a streamovaný cez UDP.5  
2. **OpenCV** v Python skripte zachytáva tento stream a konvertuje ho na tenzory pre PyTorch.  
3. **PyTorch (MPS)** vykoná inferenciu (napr. identifikuje cieľ pre pristátie).  
4. **Riadiaca logika** vypočíta potrebný vektor rýchlosti v súradnicovom systéme NED (North-East-Down).  
5. **MAVSDK** pošle príkaz offboard.set\_velocity\_ned() do ArduPilot SITL.25

Tento proces si vyžaduje synchronizáciu časových pečiatok, aby AI model nereagoval na staré dáta. ArduPilot SITL v režime lock-step s Gazebom zabezpečuje, že simulácia "počka", kým AI výpočet neskončí, čím sa eliminuje drift v simulácii.8

### **Optimalizácia dátových tokov**

Pre minimalizáciu latencie na MacBooku Air 2025 je vhodné použiť zdieľanú pamäť tam, kde je to možné. Hoci medzi procesmi (Gazebo a Python) prebieha komunikácia cez sockety, použitie efektívnych kodekov a nízkych rozlíšení (napr. 640x480 pre AI videnie) výrazne znižuje vyťaženie CPU a zahrievanie zariadenia.25

## **Dynamika letu a fyzikálne modelovanie**

Pri simulácii drona v prostredí Gazebo Harmonic je nevyhnutné správne definovať aerodynamické sily. ArduPilot SITL preberá zodpovednosť za stabilitu (PID regulátory), zatiaľ čo Gazebo modeluje odpor vzduchu, gravitáciu a kolízie.8

Regulačná slučka pre stabilitu polohy drona v ArduPilote sa dá matematicky popísať ako:

![][image1]  
Kde ![][image2] je odchýlka od požadovanej polohy generovanej AI modelom. Vývojár v roku 2025 môže tieto parametre ladiť priamo v QGroundControl, zatiaľ čo simulácia beží, a sledovať vplyv na výkonnosť AI agenta v reálnom čase.8

## **Pokročilé simulačné scenáre: Swarming a AI kooperácia**

Pre MacBook Air 2025 s čipom M4 nie je problém simulovať ani viacero dronov súčasne (swarming). ArduPilot SITL podporuje multi-vehicle simuláciu pomocou prepínača \--count v skripte sim\_vehicle.py.30

Bash

sim\_vehicle.py \-v ArduCopter \-f gazebo-iris \--count 3 \--auto-sysid

V tomto prípade MAVProxy automaticky priradí každému dronu unikátne systémové ID (SysID). AI integrácia pre swarm vyžaduje, aby MAVSDK skript manažoval viaceré inštancie System() objektov, pričom každý sa pripája na vlastný UDP port.31 Toto je ideálne prostredie pre vývoj algoritmov kolektívnej inteligencie, kde sa drony musia vyhýbať nielen prekážkam, ale aj sebe navzájom.

## **Riešenie bežných problémov na platforme Apple Silicon**

Vývoj na architektúre ARM v roku 2025 prináša špecifické chyby, ktorým sa vývojár musí vyhnúť pre zachovanie "najjednoduchšieho a najlepšieho" spôsobu práce.

### **Architektúra knižníc (x86\_64 vs arm64)**

Častou chybou je inštalácia Python balíkov cez emuláciu Rosetta 2\. To vedie k dramatickému poklesu výkonu v AI úlohách, pretože Rosetta nepodporuje priamy prístup k MPS (Metal) backendu.4 Vždy je potrebné overiť, či Python beží natívne:

Python

import platform  
print(platform.machine()) \# Musí vrátiť 'arm64'

Ak sa zobrazí x86\_64, je potrebné preinštalovať Python a jeho prostredie pomocou natívneho inštalátora pre Apple Silicon.2

### **Problémy s verziou CMake a Protobuf**

Pri kompilácii pluginov Gazebo alebo MAVSDK zo zdroja sa môžu vyskytnúť nekompatibility medzi verziami protobuf a abseil. Na macOS sa odporúča inštalovať tieto knižnice výhradne cez Homebrew a v prípade pretrvávajúcich chýb prekompilovať CMake priamo zo zdrojových kódov pre verziu 3.31+.34

## **Budúcnosť: AI generované jadrá a ANE integrácia**

Vývoj v roku 2025 smeruje k využívaniu Apple Neural Engine (ANE) pre nízkoenergetickú inferenciu. Zatiaľ čo GPU (MPS) je výkonnejšie pre masívne paralelné úlohy, ANE je ideálne pre bežiace filtre a jednoduchšie detekčné modely.3 Experimentálne nástroje začínajú umožňovať generovanie Metal jadier (kernels) pomocou veľkých jazykových modelov (LLM), čo urýchľuje optimalizáciu špecifických operácií potrebných pre spracovanie dát z lidaru alebo hĺbkových kamier v simulácii.36

## **Záverečné zhrnutie a odporúčaný postup**

Pre dosiahnutie najlepšieho a najjednoduchšieho nastavenia na MacBook Air 2025 pre autonómne drony je kľúčová postupnosť krokov, ktorá minimalizuje konflikty závislostí.

1. **Systémový základ:** Xcode CLT, Homebrew (v /opt/homebrew) a natívny Python 3.11+.2  
2. **ArduPilot:** Natívna kompilácia SITL cez waf na macOS pre maximálny výkon simulácie.11  
3. **Simulátor:** Gazebo Harmonic s pluginom ardupilot\_gazebo pre fyzikálne presnú 3D simuláciu.8  
4. **Komunikácia:** MAVProxy ako centrálny uzol smerujúci dáta do QGroundControl a MAVSDK.16  
5. **AI Engine:** PyTorch s MPS akceleráciou pre spracovanie dát zo simulátora na GPU.1  
6. **Riadenie:** MAVSDK-Python pre asynchrónne ovládanie drona z AI skriptov.13

Tento ekosystém poskytuje kompletnú vývojovú platformu, ktorá na jednom zariadení (MacBook Air) dokáže simulovať let drona, vykresľovať zložité 3D prostredie a v reálnom čase trénovať modely umelej inteligencie. Vďaka unifikovanej architektúre pamäte a vysokej efektivite čipov M3/M4 ide o momentálne najvýkonnejšie mobilné riešenie pre inžinierov v oblasti UAV autonómie. Správna konfigurácia, ako je popísaná v tejto správe, zabezpečí stabilitu systému a pripravenosť na nasadenie algoritmov do reálneho hardvéru bez nutnosti rozsiahlych zmien v kóde.

#### **Citované práce**

> 1. Accelerated PyTorch training on Mac \- Metal \- Apple Developer, otvorené marca 11, 2026, [https\://developer.apple.com/metal/pytorch/](https://developer.apple.com/metal/pytorch/)  
> 2. Installation \- Homebrew Documentation, otvorené marca 11, 2026, [https\://docs.brew.sh/Installation](https://docs.brew.sh/Installation)  
> 3. Unleashing Apple Silicon's AI Power: A Deep Dive into MPS-Accelerated Image Generation \- Medium, otvorené marca 11, 2026, [https\://medium.com/@michael.hannecke/unleashing-apple-silicons-hidden-ai-superpower-a-technical-deep-dive-into-mps-accelerated-image-9573ba90570a](https://medium.com/@michael.hannecke/unleashing-apple-silicons-hidden-ai-superpower-a-technical-deep-dive-into-mps-accelerated-image-9573ba90570a)  
> 4. MPS training (basic) — PyTorch Lightning 2.6.1 documentation, otvorené marca 11, 2026, [https\://lightning.ai/docs/pytorch/stable/accelerators/mps\_basic.html](https://lightning.ai/docs/pytorch/stable/accelerators/mps_basic.html)  
> 5. Using SITL with Gazebo — Dev documentation \- ArduPilot, otvorené marca 11, 2026, [https\://ardupilot.org/dev/docs/sitl-with-gazebo.html](https://ardupilot.org/dev/docs/sitl-with-gazebo.html)  
> 6. Gazebo Sim with UTM VM on M4 Mac makes CPU very hot : r/ROS \- Reddit, otvorené marca 11, 2026, [https\://www\.reddit.com/r/ROS/comments/1lb7m2r/gazebo\_sim\_with\_utm\_vm\_on\_m4\_mac\_makes\_cpu\_very/](https://www.reddit.com/r/ROS/comments/1lb7m2r/gazebo_sim_with_utm_vm_on_m4_mac_makes_cpu_very/)  
> 7. macOS Development Environment \| PX4 Guide (main), otvorené marca 11, 2026, [https\://docs.px4.io/main/en/dev\_setup/dev\_env\_mac](https://docs.px4.io/main/en/dev_setup/dev_env_mac)  
> 8. Plugins and models for vehicle simulation in Gazebo Sim with ArduPilot SITL controllers \- GitHub, otvorené marca 11, 2026, [https\://github.com/ArduPilot/ardupilot\_gazebo](https://github.com/ArduPilot/ardupilot_gazebo)  
> 9. Install Homebrew on Mac · 2026 · Step by Step, otvorené marca 11, 2026, [https\://mac.install.guide/homebrew/3](https://mac.install.guide/homebrew/3)  
> 10. MAVSDK verson on macOS aarch64 · Issue \#1989 \- GitHub, otvorené marca 11, 2026, [https\://github.com/mavlink/MAVSDK/issues/1989](https://github.com/mavlink/MAVSDK/issues/1989)  
> 11. Setting up the Build Environment (MacOSX) — Dev documentation \- ArduPilot, otvorené marca 11, 2026, [https\://ardupilot.org/dev/docs/building-setup-mac.html](https://ardupilot.org/dev/docs/building-setup-mac.html)  
> 12. Python Releases for macOS, otvorené marca 11, 2026, [https\://www\.python.org/downloads/macos/](https://www.python.org/downloads/macos/)  
> 13. mavlink/MAVSDK-Python \- GitHub, otvorené marca 11, 2026, [https\://github.com/mavlink/MAVSDK-Python](https://github.com/mavlink/MAVSDK-Python)  
> 14. Compile, Deploy and Fly — ArduPilot on Mac OS X. \| by Varun Sarwal \- Medium, otvorené marca 11, 2026, [https\://medium.com/@varunsarwal/compile-deploy-and-fly-ardupilot-on-mac-os-x-cdbed57b5262](https://medium.com/@varunsarwal/compile-deploy-and-fly-ardupilot-on-mac-os-x-cdbed57b5262)  
> 15. Startup Options — MAVProxy documentation \- ArduPilot, otvorené marca 11, 2026, [https\://ardupilot.org/mavproxy/docs/getting\_started/starting.html](https://ardupilot.org/mavproxy/docs/getting_started/starting.html)  
> 16. Telemetry Forwarding — MAVProxy documentation \- ArduPilot, otvorené marca 11, 2026, [https\://ardupilot.org/mavproxy/docs/getting\_started/forwarding.html](https://ardupilot.org/mavproxy/docs/getting_started/forwarding.html)  
> 17. How to Set Up ArduPilot SITL with Gazebo for Drone Simulation \| by Sanjana Kumari, otvorené marca 11, 2026, [https\://medium.com/@sanjana\_dev9/how-to-set-up-ardupilot-sitl-with-gazebo-for-drone-simulation-a0d15e19b8e3](https://medium.com/@sanjana_dev9/how-to-set-up-ardupilot-sitl-with-gazebo-for-drone-simulation-a0d15e19b8e3)  
> 18. Download and Install \- QGC Guide \- QGroundControl, otvorené marca 11, 2026, [https\://docs.qgroundcontrol.com/master/en/qgc-user-guide/getting\_started/download\_and\_install.html](https://docs.qgroundcontrol.com/master/en/qgc-user-guide/getting_started/download_and_install.html)  
> 19. Download and Install \| QGC Guide (v5.0), otvorené marca 11, 2026, [https\://docs.qgroundcontrol.com/Stable\_V5.0/en/qgc-user-guide/getting\_started/download\_and\_install.html](https://docs.qgroundcontrol.com/Stable_V5.0/en/qgc-user-guide/getting_started/download_and_install.html)  
> 20. Download and Install \| QGC Guide (4.3), otvorené marca 11, 2026, [https\://docs.qgroundcontrol.com/Stable\_V4.3/en/qgc-user-guide/getting\_started/download\_and\_install.html](https://docs.qgroundcontrol.com/Stable_V4.3/en/qgc-user-guide/getting_started/download_and_install.html)  
> 21. Getting started with MAVSDK-Python \| mavsdk.mavlink.io, otvorené marca 11, 2026, [https\://mavsdk.mavlink.io/develop/en/python/quickstart.html](https://mavsdk.mavlink.io/develop/en/python/quickstart.html)  
> 22. MAVSDK-Python/examples/mission.py at main \- GitHub, otvorené marca 11, 2026, [https\://github.com/mavlink/MAVSDK-Python/blob/main/examples/mission.py](https://github.com/mavlink/MAVSDK-Python/blob/main/examples/mission.py)  
> 23. MAVSDK-Python/examples/goto.py at main \- GitHub, otvorené marca 11, 2026, [https\://github.com/mavlink/MAVSDK-Python/blob/main/examples/goto.py](https://github.com/mavlink/MAVSDK-Python/blob/main/examples/goto.py)  
> 24. Add GPU Acceleration for tabular model using pytorch MPS (Metal Performance Shaders) for macOS · Issue \#62 · mostly-ai/mostlyai-engine · GitHub, otvorené marca 11, 2026, [https\://github.com/mostly-ai/mostlyai-engine/issues/62](https://github.com/mostly-ai/mostlyai-engine/issues/62)  
> 25. MAVSDK: Human Tracking Drone \- PURA UAV, otvorené marca 11, 2026, [https\://www\.purauav.com.tr/blog7.html](https://www.purauav.com.tr/blog7.html)  
> 26. Optimization of Drone Detection Models Through TorchScript Conversion,... \| Download Scientific Diagram \- ResearchGate, otvorené marca 11, 2026, [https\://www\.researchgate.net/figure/Optimization-of-Drone-Detection-Models-Through-TorchScript-Conversion-Data-Flow-Graph\_fig3\_382891706](https://www.researchgate.net/figure/Optimization-of-Drone-Detection-Models-Through-TorchScript-Conversion-Data-Flow-Graph_fig3_382891706)  
> 27. Telemetry · MAVSDK Guide \- MAVLink, otvorené marca 11, 2026, [https\://mavsdk.mavlink.io/v1.4/en/cpp/guide/telemetry.html](https://mavsdk.mavlink.io/v1.4/en/cpp/guide/telemetry.html)  
> 28. How to use mavsdk-python to takeoff without GPS · Issue \#704 \- GitHub, otvorené marca 11, 2026, [https\://github.com/mavlink/MAVSDK-Python/issues/704](https://github.com/mavlink/MAVSDK-Python/issues/704)  
> 29. Script Setup and Use Examples — Dev documentation \- ArduPilot, otvorené marca 11, 2026, [https\://ardupilot.org/dev/docs/common-scripting-step-by-step.html](https://ardupilot.org/dev/docs/common-scripting-step-by-step.html)  
> 30. Using SITL — Dev documentation \- Simulation \- ArduPilot, otvorené marca 11, 2026, [https\://ardupilot.org/dev/docs/using-sitl-for-ardupilot-testing.html](https://ardupilot.org/dev/docs/using-sitl-for-ardupilot-testing.html)  
> 31. alireza787b/mavsdk\_drone\_show: All in one Drone Show and Smart Swarm Solutin for PX4, otvorené marca 11, 2026, [https\://github.com/alireza787b/mavsdk\_drone\_show](https://github.com/alireza787b/mavsdk_drone_show)  
> 32. FAQ · MAVSDK Guide, otvorené marca 11, 2026, [https\://mavsdk.mavlink.io/v2.0/en/faq.html](https://mavsdk.mavlink.io/v2.0/en/faq.html)  
> 33. Windows laptop vs Mac M4 for docker in corporate environment \- Reddit, otvorené marca 11, 2026, [https\://www\.reddit.com/r/docker/comments/1rit1rw/windows\_laptop\_vs\_mac\_m4\_for\_docker\_in\_corporate/](https://www.reddit.com/r/docker/comments/1rit1rw/windows_laptop_vs_mac_m4_for_docker_in_corporate/)  
> 34. Tuto: compiling PX4 v1.12 with MacOS with Apple Silicon \- Guides, otvorené marca 11, 2026, [https\://discuss.px4.io/t/tuto-compiling-px4-v1-12-with-macos-with-apple-silicon/46981](https://discuss.px4.io/t/tuto-compiling-px4-v1-12-with-macos-with-apple-silicon/46981)  
> 35. PX4 SITL refuses to build on macOS (Intel \+ M-Series), otvorené marca 11, 2026, [https\://discuss.px4.io/t/px4-sitl-refuses-to-build-on-macos-intel-m-series/47858](https://discuss.px4.io/t/px4-sitl-refuses-to-build-on-macos-intel-m-series/47858)  
> 36. Speeding up PyTorch inference on Apple devices with AI-generated Metal kernels, otvorené marca 11, 2026, [https\://gimletlabs.ai/blog/ai-generated-metal-kernels](https://gimletlabs.ai/blog/ai-generated-metal-kernels)

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB8AAAAYCAYAAAACqyaBAAABlklEQVR4Xu2VTysFURjGX6KUrKzkC7AgshFKNhSlZHMXVpIoKzaSlJKslE8gK1mIhSyUlX8bCylbX8DGRknE+9zzzr3Hc89p7szd3l89dc7vPe/M3DtnZkTqZGeWRYQuFrVyrBlhGeFR08MyL5OaK5Yp/GpaWeYBB4rxrPlhqYxrPlhmZUPzxNIDF3bO0kCtk2UWcIBBlkaDuHofFwzc+1uWzJTmTDPKBQn/5d3i9sG+uPq0zZmChPuLbIorjtl8T3NQLhcPGGpe1qxpvsXVVy0hQv2lEzd6rl1z7823JdJsoHbKkgj2Q77YuFmzaM7nKOASkvvdywUCa1p8gXucXPWuZkncr2YOJX7yFYnXfLCmzRdbJtNYl/i6N4nXfCrW4DVZIY05bzwj8XXwF9783Rv7BPsh58lhD0yQCzaL8ws2fhW6rwY+RMF+7PJPcUXk+n+5BGoDLKX8DCMdVEvAk/PAMguXmjuWVYILw5NUE8G/LoVhzRfLPOxoTlimgC9dE8u83Ej6CyUB+6efZa3gZVQNQyzq/AEoilnbeRmahgAAAABJRU5ErkJggg==>