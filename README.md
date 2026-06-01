#  SupKonQuest

> Projet de fin d'année 2025-2026 — **Supinfo Paris** — Équipe de 4

**SupKonQuest** est un jeu de stratégie en temps réel inspiré de Risk, développé entièrement en **C++ avec SFML**. Les joueurs conquièrent des camps sur une carte, produisent des unités, gèrent leur territoire et s'affrontent en multijoueur en ligne.

---

##  Fonctionnalités

###  Cartes & Gameplay
- 3 cartes jouables avec configurations variées
- Génération aléatoire de carte
- **Éditeur de cartes** intégré (bonus)
- Gestion des camps, régions et revenus
- Camps neutres passifs avec tourelles défensives

###  7 types d'unités
| Unité | Description |
|---|---|
|  Infanterie | Unité de base, combat au corps à corps |
|  Soutien | Boost vitesse d'attaque / déplacement / dégâts |
|  Soin | Sort de soin avec temps de recharge |
|  Portée | Unité à distance de base |
|  Lourd | Dégâts élevés, beaucoup de PV, lent |
|  Anti-Armure | Efficace uniquement contre les unités Lourdes |
|  Motar | Attaques à distance avec dégâts de zone |

###  3 types de navires
- **Transport** — Déplace des troupes sur l'eau
- **Frégate** — Unité de portée navale
- **Destroyer** — Unité lourde avec dégâts de zone

###  Multijoueur & IA
- Multijoueur en ligne (création / rejoindre un lobby)
- Matchmaking classé (ranked)
- **3 niveaux d'IA** (stratégique, agressif, dispersé)
- Classement en ligne

###  Internationalisation
- Disponible en **3 langues** : Français 🇫🇷 · Anglais 🇬🇧 · Espagnol 🇪🇸

---

##  Technologies utilisées

![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![SFML](https://img.shields.io/badge/SFML-8CC445?style=flat&logo=sfml&logoColor=white)
![C++17](https://img.shields.io/badge/C++17-standard-blue?style=flat)

---

##  Structure du projet

```
SupKonQuest/
├── main.cpp
├── compile.sh          # Script de compilation Linux/macOS
├── compile.ps1         # Script de compilation Windows
├── src/
│   ├── core/
│   │   ├── game_manager.cpp    # Moteur principal du jeu
│   │   ├── map_config.hpp      # Configuration des cartes
│   │   └── perlin_noise.hpp    # Génération procédurale
│   ├── gameplay/
│   │   ├── ai.cpp              # Intelligence artificielle
│   │   ├── troupes.cpp         # Gestion des unités
│   │   ├── structures.cpp      # Gestion des camps
│   │   ├── groupes.cpp         # Groupes d'unités
│   │   └── player.cpp          # Gestion du joueur
│   ├── network/
│   │   └── network.hpp         # Multijoueur en ligne
│   ├── ui/
│   │   ├── pages/              # Menus (menu principal, lobby, ranked...)
│   │   ├── map/                # Carte, minimap, caméra
│   │   ├── overlays/           # HUD, pause, game over, paramètres
│   │   ├── vfx/                # Effets visuels
│   │   └── audio/              # Gestion audio
│   └── languages.csv           # Traductions FR / EN / ES
├── assets/
│   ├── music/
│   └── troops/
└── docs/
    ├── SupKonQuest_Docu_Technique.pdf
    └── SupKonQuest_Guide_Utilisateur.pdf
```

---

##  Installation

### Prérequis
- **C++17** ou supérieur
- **SFML 3.0.2**

### Windows
1. Installer [MSYS2](https://www.msys2.org/) avec les paramètres par défaut
2. Télécharger SFML 3.0.2 depuis [sfml-dev.org](https://www.sfml-dev.org/download/sfml/3.0.2/) :
   - "WinLibs UCRT 14.2.0 (64-bit)"
   - "GCC 14.2.0 MinGW (SEH) (UCRT)"
3. Lancer le script de compilation :
```powershell
.\compile.ps1
```

### Linux / macOS
1. Installer `g++` et SFML 3.0.2
2. Lancer le script :
```bash
chmod +x compile.sh
./compile.sh
```

---

##  Documentation

Le projet inclut une documentation complète dans le dossier `docs/` :
-  **Guide Utilisateur** — Comment jouer
-  **Documentation Technique** — Architecture, IA, pathfinding, réseau, choix d'implémentation

---

##  Équipe

Projet réalisé par une équipe de **4 étudiants** à Supinfo Paris.

---

##  Licence

Vous êtes libres de modifier et distribuer ce jeu **gratuitement**. La redistribution commerciale n'est pas autorisée.

---

*Projet de fin d'année — Supinfo Paris 2025-2026*
