# Same Colors

A puzzle game for iOS where you swipe to slide colored tiles and merge matching ones before your moves run out.

## Gameplay

- Swipe in any direction (up, down, left, right) to slide all tiles on the 4x4 grid
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
- Background music and sound effects (toggleable)
- Fullscreen dark-themed UI with neon accents
- Game state auto-saved on pause/exit and restored on relaunch
- Per-difficulty high score tracking with reset option

## Requirements

- iOS 16.0+
- iPhone and iPad

## Privacy

Same Colors displays ads via Google AdMob and requests App Tracking Transparency consent. See the full [Privacy Policy](privacy_policy.md) for details.
