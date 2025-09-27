# Just A Dungeon

A 2D dungeon crawler game built with Unity, featuring combat mechanics, monster AI, boss battles, and RPG elements.

## 🎮 Game Overview

Just A Dungeon is a 2D action RPG where players explore dungeons, fight monsters, level up, and face challenging boss encounters. The game features pixel art graphics, smooth animations, and engaging combat mechanics.

## ✨ Features

### Core Gameplay
- **Player Character**: Customizable player with health, level, and XP systems
- **Combat System**: 
  - Close-range melee attacks (Right Mouse Button)
  - Long-range projectile attacks (Left Mouse Button)
  - Attack cooldowns and damage variation
- **Movement**: WASD/Arrow key controls with smooth sprite animations
- **Health System**: Health regeneration, damage variation, and death mechanics

### RPG Elements
- **Leveling System**: Gain XP from defeating monsters to level up
- **Progressive Stats**: 
  - Even levels: +10 Max Health (up to cap of 150)
  - Odd levels: +2 Attack Damage
- **Skill Progression**: Attack cooldowns improve at levels 5, 10, 15, and 20
- **Health Regeneration**: Optional health regen system

### Monster AI
- **Monster Spawning**: Dynamic monster spawners with population limits
- **AI Behavior**: 
  - Chase players within range
  - Attack with projectiles
  - Drop XP upon death
- **Health Bars**: Visual health indicators for damaged monsters
- **Damage Variation**: Randomized damage with different formulas for player vs monsters

### Boss System
- **Complex Boss AI**: Multi-phase attack patterns
- **Attack Phases**:
  - Phase 1: Targeted attacks at player
  - Phase 2: All-direction projectile barrage
  - Phase 3: Progressive circle attacks
- **Boss Health Bar**: Dedicated UI for boss encounters
- **Victory Conditions**: Defeat boss to complete demo

### UI/UX Features
- **Health Bar**: Player health visualization
- **XP Bar**: Experience progress tracking
- **Level Display**: Current player level
- **Damage Indicators**: Visual feedback for damage taken
- **Pause System**: Game pause with popup messages
- **Death Screen**: Game over screen with retry option
- **Fade Effects**: Smooth transitions and visual effects

### Developer Features
- **Admin Mode**: Debug controls for testing
  - Ctrl + Numpad 1: Remove health
  - Ctrl + Numpad 2: Add health
  - Ctrl + Numpad 3: Gain XP
  - Ctrl + Numpad 0: Revive player
- **Cheat System**: Konami code implementation
- **Debug Logging**: Comprehensive logging for development

## 🛠️ Technical Details

### Unity Version
- **Unity Editor**: 6000.0.29f1
- **Render Pipeline**: Universal Render Pipeline (URP) 17.0.3
- **Input System**: Unity Input System 1.11.2
- **2D Features**: Unity 2D Feature Set 2.0.1

### Key Components
- **Player System**: Player.cs, PlayerControls.cs, PlayerAnimationHandler.cs
- **Combat System**: Attack.cs, Projectile.cs
- **Monster System**: MonsterStats.cs, MonsterSpawner.cs, MonsterAnimationHandler.cs
- **Boss System**: BossScript.cs with complex attack patterns
- **UI System**: Various UI handlers for health, XP, and game state
- **Animation System**: Custom sprite-based animations

### Project Structure
```
Assets/
├── Scripts/           # C# game logic scripts
├── Prefabs/          # Game object prefabs
├── Scenes/           # Unity scenes (DungeonMap, Overworld, SampleScene)
├── Animations/       # Animation controllers and clips
├── Images/           # Game sprites and textures
├── Materials/        # Shader materials
├── Shaders/          # Custom shaders (HealthBarShader)
├── TileSet2D/        # 2D tile sets for level design
└── UI/               # UI prefabs and components
```

## 🎯 Game Controls

### Movement
- **WASD** or **Arrow Keys**: Move player character
- **Mouse**: Aim projectile attacks

### Combat
- **Left Mouse Button**: Long-range projectile attack
- **Right Mouse Button**: Close-range melee attack
- **Enter**: Pause game

### Debug (Admin Mode)
- **Ctrl + Numpad 1**: Remove 1 health
- **Ctrl + Numpad 2**: Add 1 health  
- **Ctrl + Numpad 3**: Gain 1 XP
- **Ctrl + Numpad 0**: Revive player

## 🚀 Getting Started

### Prerequisites
- Unity 2022.3 LTS or later
- Visual Studio or preferred C# IDE

### Installation
1. Clone the repository
2. Open the project in Unity
3. Ensure all packages are imported (check Package Manager)
4. Open the desired scene (DungeonMap.unity for main gameplay)
5. Press Play to start the game

### Scenes
- **DungeonMap.unity**: Main dungeon gameplay
- **Overworld.unity**: Overworld exploration
- **SampleScene.unity**: Testing scene

## 🎨 Art Assets

The game features:
- **Pixel Art Graphics**: Custom sprites and animations
- **Tile-based Levels**: 2D tile sets for dungeon creation
- **Particle Effects**: Visual feedback for combat
- **UI Elements**: Custom health bars, XP bars, and menus
- **Custom Shaders**: Health bar visualization shader

## 🔧 Development Notes

### Key Scripts
- **Player.cs**: Core player logic, health, XP, leveling
- **MonsterStats.cs**: Monster AI, combat, and behavior
- **BossScript.cs**: Complex boss attack patterns and phases
- **Attack.cs**: Player combat system with cooldowns
- **Projectile.cs**: Projectile physics and damage

### Performance Considerations
- Object pooling for projectiles
- Efficient monster spawning with limits
- Optimized animation systems
- UI update optimization

## 🎮 Game Modes

- **Demo Mode**: Complete the boss fight to finish the demo
- **Admin Mode**: Debug mode with special controls
- **Pause Mode**: Game can be paused for breaks

## 📝 Future Enhancements

Potential areas for expansion:
- More monster types and behaviors
- Additional boss encounters
- Item and equipment systems
- Multiple dungeon levels
- Save/load functionality
- Sound effects and music
- Multiplayer support

## 🤝 Contributing

This appears to be a personal project. For contributions or questions, please contact the project maintainer.

## 📄 License

This project is for educational and personal use.

---

**Note**: This is a Unity-based 2D dungeon crawler with RPG elements, featuring custom sprite animations, complex boss AI, and engaging combat mechanics. The game demonstrates various Unity systems including 2D physics, animation, UI, and game state management.
