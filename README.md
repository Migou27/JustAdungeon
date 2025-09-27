# Just A Dungeon

Un jeu de donjon 2D développé avec Unity, comportant des mécaniques de combat, de l'IA pour monstres, des combats de boss et des éléments RPG.

## 🎮 Aperçu du Jeu

Just A Dungeon est un RPG d'action 2D où les joueurs explorent des donjons, combattent des monstres, montent de niveau et affrontent des rencontres de boss difficiles. Le jeu propose des graphismes pixel art, des animations fluides et des mécaniques de combat engageantes.

## ✨ Fonctionnalités

### Gameplay Principal
- **Personnage Joueur** : Joueur personnalisable avec système de santé, niveau et XP
- **Système de Combat** : 
  - Attaques de mêlée à courte portée (Clic Droit)
  - Attaques de projectiles à longue portée (Clic Gauche)
  - Temps de recharge et variation de dégâts
- **Mouvement** : Contrôles WASD/Flèches avec animations de sprites fluides
- **Système de Santé** : Régénération de santé, variation de dégâts et mécaniques de mort

### Éléments RPG
- **Système de Niveau** : Gagnez de l'XP en vainquant des monstres pour monter de niveau
- **Stats Progressives** : 
  - Niveaux pairs : +10 Santé Max (jusqu'à 150 max)
  - Niveaux impairs : +2 Dégâts d'Attaque
- **Progression des Compétences** : Les temps de recharge s'améliorent aux niveaux 5, 10, 15 et 20
- **Régénération de Santé** : Système de régénération de santé optionnel

### IA des Monstres
- **Apparition des Monstres** : Générateurs de monstres dynamiques avec limites de population
- **Comportement IA** : 
  - Poursuite des joueurs à portée
  - Attaques avec projectiles
  - Don d'XP à la mort
- **Barres de Santé** : Indicateurs visuels de santé pour les monstres blessés
- **Variation de Dégâts** : Dégâts randomisés avec formules différentes pour joueur vs monstres

### Système de Boss
- **IA de Boss Complexe** : Patterns d'attaque multi-phases
- **Phases d'Attaque** :
  - Phase 1 : Attaques ciblées sur le joueur
  - Phase 2 : Barrage de projectiles dans toutes les directions
  - Phase 3 : Attaques circulaires progressives
- **Barre de Santé du Boss** : Interface dédiée pour les rencontres de boss
- **Conditions de Victoire** : Vaincre le boss pour terminer la démo

### Fonctionnalités UI/UX
- **Barre de Santé** : Visualisation de la santé du joueur
- **Barre d'XP** : Suivi du progrès d'expérience
- **Affichage du Niveau** : Niveau actuel du joueur
- **Indicateurs de Dégâts** : Retour visuel pour les dégâts reçus
- **Système de Pause** : Pause du jeu avec messages popup
- **Écran de Mort** : Écran de fin de partie avec option de recommencer
- **Effets de Fondu** : Transitions fluides et effets visuels

### Fonctionnalités Développeur
- **Mode Admin** : Contrôles de debug pour les tests
  - Ctrl + Pavé Num 1 : Retirer 1 santé
  - Ctrl + Pavé Num 2 : Ajouter 1 santé
  - Ctrl + Pavé Num 3 : Gagner 1 XP
  - Ctrl + Pavé Num 0 : Ressusciter le joueur
- **Système de Triche** : Implémentation du code Konami
- **Journal de Debug** : Logging complet pour le développement

## 🛠️ Détails Techniques

### Version Unity
- **Unity Editor** : 6000.0.29f1
- **Pipeline de Rendu** : Universal Render Pipeline (URP) 17.0.3
- **Système d'Entrée** : Unity Input System 1.11.2
- **Fonctionnalités 2D** : Unity 2D Feature Set 2.0.1

### Composants Clés
- **Système Joueur** : Player.cs, PlayerControls.cs, PlayerAnimationHandler.cs
- **Système de Combat** : Attack.cs, Projectile.cs
- **Système de Monstres** : MonsterStats.cs, MonsterSpawner.cs, MonsterAnimationHandler.cs
- **Système de Boss** : BossScript.cs avec patterns d'attaque complexes
- **Système UI** : Divers gestionnaires UI pour santé, XP et état du jeu
- **Système d'Animation** : Animations personnalisées basées sur sprites

### Structure du Projet
```
Assets/
├── Scripts/           # Scripts de logique de jeu C#
├── Prefabs/          # Prefabs d'objets de jeu
├── Scenes/           # Scènes Unity (DungeonMap, Overworld, SampleScene)
├── Animations/       # Contrôleurs d'animation et clips
├── Images/           # Sprites et textures de jeu
├── Materials/        # Matériaux de shader
├── Shaders/          # Shaders personnalisés (HealthBarShader)
├── TileSet2D/        # Jeux de tuiles 2D pour la conception de niveaux
└── UI/               # Prefabs et composants UI
```

## 🎯 Contrôles du Jeu

### Mouvement
- **WASD** ou **Flèches** : Déplacer le personnage joueur
- **Souris** : Viser les attaques de projectiles

### Combat
- **Clic Gauche** : Attaque de projectile à longue portée
- **Clic Droit** : Attaque de mêlée à courte portée
- **Entrée** : Mettre le jeu en pause

## 🚀 Démarrage

### Prérequis
- Unity 2022.3 LTS ou plus récent
- Visual Studio ou IDE C# préféré

### Installation
1. Cloner le repository
2. Ouvrir le projet dans Unity
3. S'assurer que tous les packages sont importés (vérifier Package Manager)
4. Ouvrir la scène désirée (DungeonMap.unity pour le gameplay principal)
5. Appuyer sur Play pour démarrer le jeu

### Scènes
- **DungeonMap.unity** : Gameplay principal du donjon
- **Overworld.unity** : Exploration du monde extérieur
- **SampleScene.unity** : Scène de test

## 🎨 Assets Artistiques

Le jeu propose :
- **Graphismes Pixel Art** : Sprites et animations personnalisés
- **Niveaux Basés sur Tuiles** : Jeux de tuiles 2D pour la création de donjons
- **Effets de Particules** : Retour visuel pour le combat
- **Éléments UI** : Barres de santé personnalisées, barres d'XP et menus
- **Shaders Personnalisés** : Shader de visualisation de barre de santé

## 🔧 Notes de Développement

### Scripts Clés
- **Player.cs** : Logique principale du joueur, santé, XP, montée de niveau
- **MonsterStats.cs** : IA des monstres, combat et comportement
- **BossScript.cs** : Patterns d'attaque complexes du boss et phases
- **Attack.cs** : Système de combat du joueur avec temps de recharge
- **Projectile.cs** : Physique des projectiles et dégâts

### Considérations de Performance
- Pool d'objets pour les projectiles
- Apparition efficace des monstres avec limites
- Systèmes d'animation optimisés
- Optimisation des mises à jour UI

## 🎮 Modes de Jeu

- **Mode Démo** : Terminer le combat de boss pour finir la démo
- **Mode Admin** : Mode debug avec contrôles spéciaux
- **Mode Pause** : Le jeu peut être mis en pause pour des pauses

## 📝 Améliorations Futures

Domaines potentiels d'expansion :
- Plus de types de monstres et comportements
- Rencontres de boss supplémentaires
- Systèmes d'objets et d'équipement
- Niveaux de donjon multiples
- Fonctionnalité de sauvegarde/chargement
- Effets sonores et musique
- Support multijoueur

## 🤝 Contribution

 - Developpeur : Massil - https://github.com/Massil-br

## 📄 Licence

Ce projet est à des fins éducatives et personnelles.

---

**Note** : Il s'agit d'un dungeon crawler 2D basé sur Unity avec des éléments RPG, proposant des animations de sprites personnalisées, une IA de boss complexe et des mécaniques de combat engageantes. Le jeu démontre divers systèmes Unity incluant la physique 2D, l'animation, l'UI et la gestion d'état du jeu.
