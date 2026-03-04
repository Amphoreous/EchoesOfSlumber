# PlatformerGame - Game Development Project Template

A complete 2D platformer game project template designed for Game Development coursework. This template provides a robust foundation for building a feature-rich platformer game across three progressive assignments, integrating SDL3, Box2D physics, Tiled map support, and advanced game systems.

## 🎮 Project Overview

This template is specifically designed to support a three-assignment progression in Game Development:

### Assignment 1: Core Platformer Mechanics
- **Player System**: Physics-based character with Box2D
- **Map System**: TMX map loading with dynamic collider generation
- **Camera System**: Follow-up camera with smooth tracking
- **Performance**: Frame-rate capping and delta-time normalization

### Assignment 2: AI & Save System
- **Enemy AI**: Walking and flying enemies with pathfinding
- **Save/Load**: Game state persistence with checkpoints
- **Combat System**: Enemy destruction mechanics
- **Audio**: Sound effects and feedback

### Assignment 3: Complete Game Experience
- **Collectibles & Items**: Health pickups, coins, power-ups
- **GUI System**: Complete menu system and HUD
- **Multi-level**: Two levels with boss encounter
- **Optimization**: Frustum culling, lazy updates, Tracy profiling

## 🚀 Features

- **SDL3 Integration**: Latest SDL3 with automatic download and setup
- **Box2D Physics**: Integrated 2D physics engine for realistic movement
- **Tiled Support**: TMX map loading with pugixml
- **Image Loading**: SDL3_image with JPEG and PNG support
- **Cross-platform**: Windows (Visual Studio 2022) and Linux support
- **Automatic Dependency Management**: All libraries downloaded and configured automatically
- **Multi-architecture**: x64 and x86 platform support
- **Performance Tools**: Built-in FPS counter, frame capping, and profiling support

## 📁 Project Structure

```
PlatformerGame/
├── src/                      # Source code (.cpp files)
│   ├── PlatformGame.cpp     # Entry point
│   ├── Engine.cpp           # Core engine module
│   ├── Audio.cpp            # Audio system
│   ├── Input.cpp            # Input handling
│   ├── Log.cpp              # Logging utilities
│   ├── PerfTimer.cpp        # Performance timing
│   ├── Render.cpp           # Rendering system
│   ├── Scene.cpp            # Scene management
│   ├── Textures.cpp         # Texture management
│   ├── Timer.cpp            # Timer utilities
│   ├── Vector2D.cpp         # 2D vector math
│   └── Window.cpp           # Window management
│   
│   # Future structure for assignments:
│   ├── entities/            # Player, enemies, items (Entity system)
│   ├── physics/             # Box2D integration
│   ├── map/                 # TMX map loading
│   ├── pathfinding/         # A* pathfinding for enemies
│   └── gui/                 # GUI system (menus, HUD)
│
├── include/                 # Header files (.h files)
│   ├── Engine.h
│   ├── Module.h            # Base module class
│   ├── Audio.h
│   ├── Input.h
│   ├── Log.h
│   ├── PerfTimer.h
│   ├── Render.h
│   ├── Scene.h
│   ├── Textures.h
│   ├── Timer.h
│   ├── Vector2D.h
│   └── Window.h
│
├── assets/                  # Game assets
│   ├── textures/           # Sprites and tilesets (test.png)
│   └── audio/              # Audio files
│       └── music/          # Background music (level-iv-339695.wav)
│
├── build/                   # Build system
│   ├── premake5.exe        # Premake5 build tool (Windows)
│   ├── premake5.lua        # Build configuration script
│   ├── build_files/        # Generated Visual Studio projects
│   │   ├── PlatformerGame.vcxproj
│   │   ├── box2d.vcxproj
│   │   ├── pugixml.vcxproj
│   │   └── obj/            # Intermediate build files
│   └── external/           # External dependencies (auto-downloaded)
│       ├── SDL3/           # SDL3 library (3.2.24+)
│       ├── SDL3_image/     # Image loading library
│       ├── box2d/          # Box2D physics engine (3.1.1+)
│       ├── pugixml/        # XML parser for TMX/config files
│       ├── libjpeg-turbo/  # JPEG support
│       └── libpng/         # PNG support
│
├── bin/                     # Compiled executables and runtime files
│   ├── Debug/              # Debug build output
│   │   ├── PlatformerGame.exe
│   │   ├── PlatformerGame.pdb
│   │   ├── SDL3.dll
│   │   ├── SDL3_image.dll
│   │   ├── jpeg62.dll
│   │   ├── box2d.lib
│   │   └── pugixml.lib
│   └── Release/            # Release build output
│
├── .gitignore
├── build-VisualStudio2022.bat  # Quick build script
├── LICENSE
├── PlatformerGame.sln          # Visual Studio solution
└── README.md
```

## 📋 Prerequisites

### Windows
- **Visual Studio 2022** (Community, Professional, or Enterprise)
- **Windows SDK** (latest)
- **7-Zip** (recommended, for automatic dependency extraction)
- **Internet connection** (for automatic dependency download)

### Linux
- **GCC** with C17/C++17 support
- **Development libraries**: X11, OpenGL, ALSA
- **CMake 3.10+** (for Box2D compilation)
- **Internet connection** (for automatic dependency download)

## 🎯 Assignment Requirements

This template is designed to help you complete the following assignments:

### 📝 Assignment 1: Core Platformer (Alpha Release)
**Key Features to Implement:**
- ✅ Player movement and jumping with Box2D physics
- ✅ Entity system (base Entity class + EntityManager)
- ✅ Player states: Jump(), Move(), Die()
- ✅ Animations: walk, jump, die
- ✅ WASD movement + SPACE for jump
- ✅ Follow-up camera
- ✅ Death and respawn system
- ✅ Extra movement (dash, double jump, etc.)
- ✅ Tiled TMX map loading (orthographic)
- ✅ Dynamic collider creation from map (platforms, damage, pits)
- ✅ Parameter loading from XML config
- ✅ 60 FPS cap with delta-time normalization

**Debug Keys:**
- `H` - Show/hide help menu
- `F9` - Visualize colliders/logic
- `F10` - God mode
- `F11` - Toggle FPS cap (30/60)

### 📝 Assignment 2: AI & Persistence
**Additional Features:**
- ✅ Walking enemies with pathfinding
- ✅ Flying enemies with pathfinding
- ✅ Real-time path visualization (debug mode)
- ✅ Save/Load system (F5/F6)
- ✅ Checkpoint autosave
- ✅ Enemy destruction mechanics
- ✅ Audio feedback (jump, kill, save, etc.)
- ✅ Enemy perception range and idle state

**Additional Debug Keys:**
- `F1` - Start from first level
- `F5` - Save game state
- `F6` - Load game state

### 📝 Assignment 3: Complete Game (Gold Release)
**Additional Features:**
- ✅ Health/lives recovery items
- ✅ Collectibles (coins, stars, points)
- ✅ Skill pickups (weapons, temporary abilities)
- ✅ Map checkpoints with teleportation
- ✅ Second level with boss fight
- ✅ Complete GUI system:
  - Intro screen
  - Title screen with menu
  - Gameplay HUD (health, coins, timer)
  - Pause menu
  - Die screen
  - End/level completed screen
- ✅ Optimization techniques:
  - Frustum culling
  - Lazy updates
  - Pathfinding restrictions
- ✅ Tracy profiling integration
- ✅ Background music and audio FX

**Additional Debug Keys:**
- `F1/F2` - Start from level 1/2
- `F8` - View GUI bounds
- `ESC` - Pause menu

## 🚀 Quick Start

### Windows (Visual Studio 2022)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/TheUnrealZaka/PlatformerGame.git
   cd PlatformerGame
   ```

2. **Generate Visual Studio solution:**
   ```bash
   .\build-VisualStudio2022.bat
   ```
   
   This will automatically:
   - Download SDL3, SDL3_image, Box2D, pugixml, libjpeg-turbo, and libpng
   - Extract all dependencies
   - Generate Visual Studio 2022 solution
   - Open the solution in Visual Studio

3. **Build and run:**
   - Select `Debug` or `Release` configuration
   - Choose `x64` platform (recommended)
   - Press F5 to build and run

### Linux (GCC/Make)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/TheUnrealZaka/PlatformerGame.git
   cd PlatformerGame/build
   ```

2. **Generate Makefiles:**
   ```bash
   ./premake5 gmake2
   ```

3. **Build:**
   ```bash
   cd ..
   make config=debug_x64
   # or for release:
   make config=release_x64
   ```

4. **Run:**
   ```bash
   ./bin/Debug/PlatformerGame
   ```

## 📦 Dependencies (Auto-managed)

The build system automatically downloads and configures:

| Library | Version | Purpose |
|---------|---------|---------|
| **SDL3** | 3.2.24+ | Core framework, rendering, input, audio |
| **SDL3_image** | 3.2.4+ | Image loading (PNG, JPEG, etc.) |
| **Box2D** | 3.1.1+ | 2D physics engine |
| **pugixml** | 1.15+ | XML parsing for TMX maps and config |
| **libjpeg-turbo** | 3.1.2+ | JPEG image support |
| **libpng** | 1.2.37+ | PNG image support |

All dependencies are downloaded to `build/external/` and automatically linked.    

## SDL Backend Configuration

Choose your preferred graphics backend:

```bash
# OpenGL (default/recommended)
premake5 vs2022 --sdl_backend=opengl

# Vulkan
premake5 vs2022 --sdl_backend=vulkan

# Direct3D 11 (Windows only)
premake5 vs2022 --sdl_backend=d3d11

# Direct3D 12 (Windows only)
premake5 vs2022 --sdl_backend=d3d12

# Auto-detect best backend
premake5 vs2022 --sdl_backend=auto
```

## Platform and Architecture Options

### Platforms
- **x64**: 64-bit (default)
- **x86**: 32-bit

### Build Configurations
- **Debug**: Development build with symbols and assertions
- **Release**: Optimized production build

### Platform-specific Setup

#### Windows
The build system automatically:
- Links SDL3.lib
- Copies SDL3.dll to output directory
- Sets up Windows-specific libraries (winmm, gdi32, opengl32)
- Configures Unicode character set

## 🎨 Development Workflow

### Adding Source Files
1. Add `.c`/`.cpp` files to [`src/`](src/) directory
2. Add `.h`/`.hpp` files to [`include/`](include/) directory
3. Re-run premake to regenerate project files (or let VS auto-detect)
4. Rebuild project

### Recommended Project Organization

```
src/
├── main.c                  # Entry point
├── Engine.cpp              # Core engine module
├── modules/
│   ├── Render.cpp          # Rendering system
│   ├── Input.cpp           # Input handling
│   ├── Audio.cpp           # Audio system
│   ├── Textures.cpp        # Texture management
│   ├── Window.cpp          # Window management
│   └── Scene.cpp           # Scene management
├── entities/
│   ├── Entity.cpp          # Base entity class
│   ├── EntityManager.cpp   # Entity management
│   ├── Player.cpp          # Player entity
│   ├── Enemy.cpp           # Enemy base class
│   ├── WalkingEnemy.cpp    # Walking enemy
│   ├── FlyingEnemy.cpp     # Flying enemy
│   └── Item.cpp            # Collectible items
├── physics/
│   ├── PhysicsWorld.cpp    # Box2D wrapper
│   └── Collider.cpp        # Collider management
├── map/
│   ├── Map.cpp             # TMX map loading
│   └── TileSet.cpp         # Tileset management
├── pathfinding/
│   └── Pathfinding.cpp     # A* implementation
└── gui/
    ├── GuiManager.cpp      # GUI system
    ├── GuiButton.cpp       # Button control
    ├── GuiSlider.cpp       # Slider control
    └── GuiCheckBox.cpp     # Checkbox control

include/
├── Engine.h
├── Module.h               # Base module class
├── modules/
├── entities/
├── physics/
├── map/
├── pathfinding/
└── gui/
```

### Entity System Architecture

All game entities (Player, Enemies, Items) should inherit from a base `Entity` class:

```cpp
class Entity {
public:
    virtual bool Start() = 0;
    virtual bool Update(float dt) = 0;
    virtual bool Draw() = 0;
    virtual bool CleanUp() = 0;
    
protected:
    Vector2D position;
    b2Body* physicsBody;
    // ... other common properties
};
```

The `EntityManager` handles all entity lifecycle:
```cpp
class EntityManager : public Module {
public:
    Entity* CreateEntity(EntityType type);
    void DestroyEntity(Entity* entity);
    
    bool Start() override;
    bool Update(float dt) override;
    bool Draw() override;
    bool CleanUp() override;
    
private:
    std::list<Entity*> entities;
};
```

## 🎮 Key Technologies & Features

### SDL3 Integration
Complete access to SDL3 capabilities:
- **Graphics**: 2D rendering with GPU backend support
- **Input**: Keyboard, mouse, gamepad support
- **Audio**: Music playback and sound effects
- **Window**: Multiple windows, fullscreen support
- **File I/O**: Cross-platform file operations
- **Threading**: Multithreading support

### Box2D Physics
Realistic 2D physics simulation:
- Rigid body dynamics
- Collision detection and response
- Joint and constraint systems
- Continuous collision detection (CCD)
- Efficient broad-phase collision

### Tiled Map Support
TMX map integration with pugixml:
- Orthographic map rendering
- Multiple layer support
- Dynamic collider generation from object layers
- Tileset management
- Custom properties support

### Performance Features
- **Frame Rate Control**: Stable 60 FPS cap
- **Delta Time**: Movement normalization
- **VSync Toggle**: Runtime vsync control
- **FPS Display**: Real-time performance monitoring
- **Tracy Integration**: Advanced profiling (Assignment 3)

## 📖 Example: Basic Game Loop

```cpp
#include "Engine.h"
#include "SDL3/SDL.h"
#include "box2d/box2d.h"

int main(int argc, char* argv[]) {
    Engine* engine = new Engine();
    
    if (!engine->Init()) {
        SDL_Log("Failed to initialize engine!");
        return -1;
    }
    
    // Main game loop
    while (engine->IsRunning()) {
        engine->ProcessInput();
        engine->Update();
        engine->Render();
    }
    
    engine->CleanUp();
    delete engine;
    
    return 0;
}
```

### Example: Player Entity with Box2D

```cpp
class Player : public Entity {
private:
    b2Body* body;
    float moveSpeed = 5.0f;
    float jumpForce = 10.0f;
    
public:
    bool Start() override {
        // Create Box2D body
        b2BodyDef bodyDef;
        bodyDef.type = b2_dynamicBody;
        bodyDef.position.Set(position.x, position.y);
        body = physicsWorld->CreateBody(&bodyDef);
        
        // Create collider
        b2PolygonShape shape;
        shape.SetAsBox(0.5f, 1.0f);
        
        b2FixtureDef fixtureDef;
        fixtureDef.shape = &shape;
        fixtureDef.density = 1.0f;
        fixtureDef.friction = 0.3f;
        body->CreateFixture(&fixtureDef);
        
        return true;
    }
    
    bool Update(float dt) override {
        // Handle input
        if (Input::IsKeyPressed(SDL_SCANCODE_A)) {
            Move(-moveSpeed * dt);
        }
        if (Input::IsKeyPressed(SDL_SCANCODE_D)) {
            Move(moveSpeed * dt);
        }
        if (Input::IsKeyJustPressed(SDL_SCANCODE_SPACE)) {
            Jump();
        }
        
        // Update position from physics
        b2Vec2 pos = body->GetPosition();
        position.x = pos.x;
        position.y = pos.y;
        
        return true;
    }
    
    void Move(float velocityX) {
        b2Vec2 vel = body->GetLinearVelocity();
        body->SetLinearVelocity(b2Vec2(velocityX, vel.y));
    }
    
    void Jump() {
        if (IsGrounded()) {
            body->ApplyLinearImpulse(b2Vec2(0, jumpForce), 
                                    body->GetWorldCenter(), true);
        }
    }
};
```

### Example: TMX Map Loading with pugixml

```cpp
#include "pugixml.hpp"

bool Map::LoadTMX(const char* filename) {
    pugi::xml_document doc;
    pugi::xml_parse_result result = doc.load_file(filename);
    
    if (!result) {
        SDL_Log("Failed to load map: %s", filename);
        return false;
    }
    
    pugi::xml_node mapNode = doc.child("map");
    width = mapNode.attribute("width").as_int();
    height = mapNode.attribute("height").as_int();
    tileWidth = mapNode.attribute("tilewidth").as_int();
    tileHeight = mapNode.attribute("tileheight").as_int();
    
    // Load tile layers
    for (pugi::xml_node layer : mapNode.children("layer")) {
        LoadTileLayer(layer);
    }
    
    // Load object layers (for colliders)
    for (pugi::xml_node objectGroup : mapNode.children("objectgroup")) {
        LoadObjectLayer(objectGroup);
    }
    
    return true;
}
```

## 🐛 Troubleshooting

### Dependency Download Issues
- **Network problems**: Check internet connection and firewall settings
- **GitHub API rate limiting**: Wait a few minutes or use VPN
- **Manual download**: Download missing libraries from their GitHub releases:
  - [SDL3](https://github.com/libsdl-org/SDL/releases)
  - [SDL3_image](https://github.com/libsdl-org/SDL_image/releases)
  - [Box2D](https://github.com/erincatto/box2d/releases)
  - [pugixml](https://github.com/zeux/pugixml/releases)
  - [libjpeg-turbo](https://github.com/libjpeg-turbo/libjpeg-turbo/releases)
- **Extract manually**: Place in `build/external/[library-name]/`

### Build Issues

#### Windows
- **Missing Visual Studio**: Ensure VS 2022 with C++ development tools
- **SDK not found**: Install latest Windows SDK
- **Premake fails**: Try running as Administrator
- **Box2D compilation errors**: Ensure C11 standard is supported

#### Linux
- **Missing libraries**: Install development packages:
  ```bash
  sudo apt-get install libx11-dev libgl1-mesa-dev libasound2-dev
  ```
- **CMake too old**: Update CMake to 3.10 or newer
- **Permission denied**: Make premake5 executable: `chmod +x premake5`

### Runtime Issues
- **Missing DLLs (Windows)**: 
  - DLLs should auto-copy to `bin/Debug/` or `bin/Release/`
  - Manual fix: Copy from `build/external/[library]/lib/x64/` to output folder
  - Required DLLs: `SDL3.dll`, `SDL3_image.dll`, `jpeg62.dll`

- **Crash on startup**:
  - Ensure `config.xml` exists in the executable directory
  - Check asset paths in config file
  - Verify TMX map files are in correct location

- **Physics not working**:
  - Check Box2D initialization
  - Verify collider creation from map
  - Enable debug visualization (F9)

- **Map not loading**:
  - Verify TMX file path in config
  - Check tileset paths are relative
  - Ensure pugixml can parse the XML

### Performance Issues
- **Low FPS**: 
  - Toggle VSync (F11)
  - Check Tracy profiler for bottlenecks
  - Implement frustum culling
  - Optimize pathfinding search radius

- **Physics stuttering**:
  - Verify delta-time integration
  - Check fixed timestep for physics
  - Reduce Box2D iterations if needed

## 🎯 Assignment Submission Guidelines

### Release Structure
```
TeamName-Platformer-[Alpha|Gold].zip
├── Assets/                  # All game assets
│   ├── textures/
│   ├── maps/
│   ├── audio/
│   └── LICENSE.txt         # Asset licenses
├── Game.exe                # Release build executable
├── config.xml              # Game configuration
├── SDL3.dll                # Required DLLs only
├── SDL3_image.dll
├── jpeg62.dll
├── LICENSE                 # Game license
└── README.md               # Game info and controls
```

### GitHub Release Requirements
1. **Tag naming**: `v1.0-alpha`, `v2.0-beta`, `v3.0-gold`
2. **Release title**: Clear assignment identifier
3. **Release description must include**:
   - Game description
   - How to play
   - Debug keys list
   - Implemented features
   - Known issues (if any)
   - Controls reference

### Required Documents
1. **GitHub URL** (in a .txt file on campus)
2. **Team organization document** (one page)
   - Member contributions
   - Work distribution
   - Tools used (Trello, HacknPlan, etc.)
3. **GitHub commits** showing individual contributions

### Grading Criteria
- **70%** Features implementation and completeness
- **15%** Code quality and organization
- **10%** Teamwork and contribution balance
- **5%** Submission compliance

## 🔑 Debug Controls Reference

| Key | Function | Available From |
|-----|----------|---------------|
| `H` | Show/Hide help menu | Assignment 1 |
| `F1` | Start from level 1 | Assignment 2 |
| `F2` | Start from level 2 | Assignment 3 |
| `F5` | Save game state | Assignment 2 |
| `F6` | Load game state | Assignment 2 |
| `F8` | View GUI bounds | Assignment 3 |
| `F9` | Visualize colliders/paths | Assignment 1 |
| `F10` | God mode (fly/invincible) | Assignment 1 |
| `F11` | Toggle FPS cap | Assignment 1 |
| `ESC` | Pause menu | Assignment 3 |

## 📚 Learning Resources

### Official Documentation
- **SDL3 Documentation**: [SDL3 Wiki](https://wiki.libsdl.org/SDL3)
- **Box2D Manual**: [Box2D Documentation](https://box2d.org/documentation/)
- **Tiled Documentation**: [Tiled Map Editor](https://doc.mapeditor.org/)
- **Premake5**: [Premake5 Documentation](https://premake.github.io/docs/)

### Tutorials & Guides
- **Platformer Design**: [The Guide to Implementing 2D Platformers](http://higherorderfun.com/blog/2012/05/20/the-guide-to-implementing-2d-platformers/)
- **A* for Platformers**: [Adapting A* to Platformers](https://howtorts.github.io/2013/12/23/platformer-ai.html)
- **Box2D Tutorials**: [iforce2d's Box2D Tutorials](https://www.iforce2d.net/b2dtut/)
- **Game Architecture**: [Game Programming Patterns](https://gameprogrammingpatterns.com/)

### Asset Resources
- **Open Game Art**: [OpenGameArt.org](https://opengameart.org/)
- **Kenney Assets**: [kenney.nl](https://kenney.nl/assets)
- **itch.io**: [Game Assets on itch.io](https://itch.io/game-assets)
- **GameDev Market**: [gamedevmarket.net](https://www.gamedevmarket.net/)

### Community & Support
- **SDL Discord**: [SDL Community Discord](https://discord.com/invite/BwpFGBWsv8)
- **Box2D Forum**: [Box2D Discussions](https://github.com/erincatto/box2d/discussions)
- **Game Dev Reddit**: [r/gamedev](https://www.reddit.com/r/gamedev/)
- **TIGSource**: [TIGSource Forums](https://forums.tigsource.com/)