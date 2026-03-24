# Same Colors

A puzzle game for Android and iOS where you swipe to slide colored tiles and merge matching ones before your moves run out.

## Gameplay

- Swipe in any direction (up, down, left, right) to slide all tiles on the 4×4 grid
- Adjacent tiles of the **same color** that collide will **merge** into one
- Merging resets your move counter; failing to merge costs a move
- Game over when moves reach zero or the grid is full with no possible merges
- Score is based on how many moves remain when a merge occurs — the more moves left, the higher the reward

## Difficulty

| Level  | Starting Moves | Tiles at Start | Min Empty Cells |
|--------|---------------|----------------|-----------------|
| Easy   | 20            | 2              | 4               |
| Medium | 16            | 2              | 4               |
| Hard   | 12            | 3              | 4               |

High scores are tracked per difficulty level and persist across sessions.

## Features

- Smooth swipe gesture controls
- Animated tile movements, merges, and particle effects
- Synthesized background music and sound effects (toggleable)
- Immersive fullscreen dark-themed UI with neon accents
- Game state auto-saved on pause/exit and restored on relaunch
- Per-difficulty high score tracking with reset option

## Platforms

### Android

- Android 5.0+ (API 21), Target SDK 35
- Java 8

#### Project Structure

```
app/src/main/java/com/albenrisdev/samecolors/
├── MainActivity.java       # Activity lifecycle, preferences, dialogs
├── GameView.java           # Custom View — rendering, gestures, animations
├── GameViewModel.java      # ViewModel for game state management
├── GameLogic.java          # Pure game logic (move, merge, spawn)
├── GameState.java          # State model with JSON serialization
├── Tile.java               # Tile data model
├── Difficulty.java         # Difficulty enum
├── Direction.java          # Direction enum
├── BackgroundRenderer.java # Animated background drawing
├── SplashView.java         # Splash screen
├── SoundManager.java       # Music and SFX lifecycle management
├── SoundSynth.java         # Programmatic audio synthesis
└── ObjectPool.java         # Object pooling for performance
```

#### Build

```bash
./gradlew assembleDebug
```

### iOS

- iOS 16.0+
- iPhone and iPad
- SwiftUI

#### Project Structure

```
SameColors/
├── SameColorsApp.swift              # App entry point
├── ContentView.swift                # Main content view
├── AdManager.swift                  # Google AdMob integration
├── Models/
│   ├── GameLogic.swift              # Pure game logic (move, merge, spawn)
│   ├── GameState.swift              # State model
│   ├── GameConstants.swift          # Game constants
│   └── Tile.swift                   # Tile data model
├── ViewModels/
│   └── GameViewModel.swift          # ViewModel for game state management
├── Views/
│   ├── GameCanvasView.swift         # Canvas-based game rendering
│   ├── SplashView.swift             # Splash screen
│   ├── BackgroundRenderer.swift     # Animated background drawing
│   └── UIColorHex.swift             # Color hex utility
└── Audio/
    ├── SoundManager.swift           # Music and SFX lifecycle management
    └── SoundSynth.swift             # Programmatic audio synthesis
```

#### Build

Open `SameColors.xcodeproj` in Xcode and build.

## Privacy

Same Colors displays ads via Google AdMob. On iOS, the app requests App Tracking Transparency consent before any tracking occurs. See the full [Privacy Policy](privacy_policy.md) for details.
