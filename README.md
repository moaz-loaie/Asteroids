# Asteroids

Arcade-style Asteroids clone built with Pygame. Pilot a ship, avoid collisions, and break apart incoming asteroids as they drift across the screen.

## Features

- Classic top-down movement and rotation
- Projectile shooting with cooldown
- Asteroid spawning and splitting logic
- Simple collision detection and game-over state

## Controls

- W: thrust forward
- S: thrust backward
- A: rotate left
- D: rotate right
- Space: shoot
- Close window: quit

## Requirements

- Python 3.13 or newer
- uv

## Getting Started

1. Install dependencies.

```bash
uv sync
```

2. Run the game.

```bash
uv run python main.py
```

## Logging

The game writes lightweight telemetry to the project root while it runs:

- `game_state.jsonl`: periodic snapshots of sprite positions and velocities
- `game_events.jsonl`: discrete events such as asteroid splits and player hits

State logging runs for approximately 16 seconds per session by default.

## Configuration

Tune gameplay in `constants.py`, including:

- Screen size
- Player speed, turn speed, and shoot cooldown
- Asteroid spawn rate and sizes

## Project Structure

- `main.py`: game loop and entity setup
- `player.py`: player movement and shooting
- `asteroid.py`: asteroid behavior and splitting
- `asteroidfield.py`: asteroid spawning
- `shot.py`: projectile behavior
- `circleshape.py`: base sprite class
- `constants.py`: gameplay constants
- `logger.py`: state and event logging
