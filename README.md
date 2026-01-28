# Pong — Mini Game Design Document

Created by Dark with the help of Codex.

## Overview
- Classic 2-player Pong with modern powerups.
- First to the selected goal wins (3 or 5).

## Win Conditions
- Players choose a goal limit (3 or 5) on the menu screen.
- The first player to reach the selected score wins.
- After a win, the game returns to the mode selector.

## Controls
- Player 1 movement: `W` (up), `S` (down)
- Player 2 movement: `ArrowUp` (up), `ArrowDown` (down)
- Player 1 powerup activation: `Space`
- Player 2 powerup activation: `Numpad0`

## Powerups
Powerups spawn every 7 seconds (if none is on the field). Only one powerup can exist at a time. A player collects a powerup by hitting the powerup with the ball; the pickup is assigned to the last player who hit the ball. Each player can hold only one powerup at a time and must activate it with their activation key.

### 1) Freeze Enemy (Sky Blue)
- **Collect:** Ball hits the sky-blue powerup; it is stored by the last player who hit the ball.
- **Activate:** Press the player’s activation key.
- **Effect:** The player can fire up to 3 freeze shots.
- **Freeze shots:** Travel in a straight line from the center of the player’s paddle.
- **On hit:** If a freeze shot hits the opponent’s paddle, that paddle is frozen for 2 seconds and cannot move.
- **Duration:** The powerup expires after 6 seconds or after firing 3 shots (whichever comes first).

### 2) Firefall (Fire Red)
- **Collect:** Ball hits the fire-red powerup; it is stored by the last player who hit the ball.
- **Activate:** Press the player’s activation key.
- **Effect:** The next time the player hits the ball, the ball turns red and travels at 2× speed.
- **Duration:** Single use; consumed on the next successful paddle hit.

## Tools Used
- HTML5
- CSS3
- JavaScript (ES6)
- Canvas 2D API
- Web Audio API
