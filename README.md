# Orbital

A minimal, polished orbital survival game for browser and mobile.

You control a small glowing planet locked in continuous orbit around a central sun.  
Your only control is changing the **radius** of your orbit by dragging anywhere on the screen.  
Dodge hollow geometric threats, collect power-ups, survive escalating bosses, and chase high scores across three difficulty modes.

---

## Features

- Unique one-control gameplay (drag anywhere to change orbit radius)
- Three difficulty modes: **Easy**, **Medium**, **Hard**
- Hollow glowing geometric threats with distinct sizes, speeds, and behaviors
- Power-ups: Shield, Score Multiplier (×2), Rapid Fire, Homing Missiles
- Boss encounters with soft difficulty resets after each boss
- Clean minimal aesthetic with glowing shapes and particles
- Fully mobile-friendly (one-finger control)
- Local high-score saving
- Smooth 60 FPS experience

---

## How to Play

### Controls
- **Mouse or Touch**: Press and **drag anywhere** on the screen
  - Drag farther from the sun → orbit radius increases
  - Drag closer to the sun → orbit radius decreases
- Simply clicking or holding without moving does **not** change the radius
- The entire screen is valid input (no joystick or restricted zone)

### Objective
Survive as long as possible.  
Avoid colliding with threats.  
Collect power-ups.  
Defeat bosses to trigger temporary difficulty drops and score bonuses.

---

## Difficulty Modes

| Mode     | Description                                      |
|----------|--------------------------------------------------|
| **Easy**    | More forgiving spawn rates and speeds           |
| **Medium**  | Balanced challenge                              |
| **Hard**    | Aggressive spawns, faster threats, higher intensity |

Select difficulty from the main menu.  
The selected mode is remembered.

---

## Threats

All threats are **hollow shapes with glowing borders**:

| Shape       | Description                          |
|-------------|--------------------------------------|
| Triangle    | Smallest, basic speed                |
| Square      | Larger and faster than Triangle      |
| Rectangle   | Speedster (fastest regular threat)   |
| Pentagon+   | Progressively larger                 |
| Irregular   | Homing behavior + size/speed variation |

Threats become more frequent and dangerous over time and with higher difficulty.

---

## Power-Ups

Power-ups appear as glowing **circles**:

| Power            | Color    | Effect                                              |
|------------------|----------|-----------------------------------------------------|
| Shield           | Cyan     | Blocks one hit. Long duration. Re-picking resets the timer |
| Score Multiplier | Gold     | ×2 score for a duration                             |
| Rapid Fire       | Orange   | Automatically shoots bullets at nearby threats      |
| Homing Missile   | Magenta  | Fires a rapid burst of strong homing missiles       |

**Active Power Display**  
Compact UI showing the power name + a rounded decreasing progress bar (no heavy borders or number timers).

---

## Boss System

- Difficulty ramps up over time
- A boss appears after a phase
- After defeating a boss → difficulty soft-resets (higher baseline than before)
- Difficulty ramps up again → next boss → another soft reset at an even higher baseline
- Pattern continues

This creates clear “chapters” instead of endless pure chaos.

---

## Scoring

- Points for time survived
- Bonus for close dodges
- Large bonus for defeating bosses
- Score Multiplier power multiplies points while active

Best score is saved in `localStorage`.

---

## How to Run

### Option 1 – Play directly
Open `Orbital.html` (or `index.html`) in any modern browser.

### Option 2 – Live Link
Open - 
```https://orbital-world.netlify.app/```
In the browser and start playing

## Technical Details

- Single-file HTML5 Canvas game
- Vanilla JavaScript (no frameworks)
- Fully responsive and mobile-optimized
- `localStorage` for best score and selected difficulty
- Touch + mouse support
- Prevents page scrolling/zooming during play
- Pauses when the browser tab is hidden

---

## Project Structure

```text
orbital/
├── Orbital.html      # Complete game (single file)
└── README.md
```

---

## Future Improvements

- **Per-difficulty high scores**  
  Currently there is only one global best score.  
  Planned: separate best scores for Easy, Medium, and Hard  
  *(Alternative: keep one score but multiply points earned based on difficulty)*

- **Power-up Shop / Progression**  
  Spend coins earned from runs to permanently upgrade powers  
  (longer Shield duration, stronger missiles, higher multiplier, extra starting lives, etc.)

- Daily Challenge mode with a fixed seed and leaderboard

- More power-ups (Time Slow, Orbit Boost, temporary invincibility, etc.)

- Planet skins / cosmetic unlocks

- Combo system visual feedback and higher score multipliers for long undamaged streaks

- Sound options + music toggle

- Gamepad / keyboard support for desktop

- Particle density and performance settings

- Global online leaderboard

- Boss variety (different attack patterns and unique bosses)

---

## License
MIT License – feel free to use, modify, and share.
