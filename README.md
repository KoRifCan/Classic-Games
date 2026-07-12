# Classic Games

16 classic HTML5 games built from scratch with vanilla JavaScript. No frameworks, no dependencies, no ads, no trackers. Fully responsive for mobile & desktop with touch, keyboard, and mouse support.

Every game features procedural background music via Web Audio API, sound effects, high score tracking (localStorage), glass-morphism dark UI, and a mute button.

## Games

| # | Game | Category | Description |
|---|------|----------|-------------|
| 1 | [Tetris](https://korifcan.github.io/Classic-Games/games/tetris/) | Puzzle | Stack blocks, clear lines, beat your high score. 7-bag randomizer, ghost piece, hold piece, wall kicks |
| 2 | [Snake](https://korifcan.github.io/Classic-Games/games/snake/) | Arcade | Guide the snake, eat food, grow longer. Progressive speed, bonus items, high scores |
| 3 | [2048](https://korifcan.github.io/Classic-Games/games/2048/) | Puzzle | Merge numbered tiles to reach 2048. Undo support, score animation, win/keep-going |
| 4 | [Flappy Bird](https://korifcan.github.io/Classic-Games/games/flappy/) | Arcade | Tap to flap through pipes. Frame-rate independent physics, increasing speed, score milestones |
| 5 | [Space Shooter](https://korifcan.github.io/Classic-Games/games/space/) | Action | Blast waves of aliens, collect power-ups, defeat screen-filling bosses |
| 6 | [Tic Tac Toe](https://korifcan.github.io/Classic-Games/games/ttt/) | Strategy | X vs O with Minimax AI. Easy & Hard modes with win-line highlighting |
| 7 | [Memory](https://korifcan.github.io/Classic-Games/games/memory/) | Puzzle | Flip cards and match pairs. 4×4 or 6×6 grid with move counter and timer |
| 8 | [Minesweeper](https://korifcan.github.io/Classic-Games/games/mine/) | Puzzle | Find all mines without blowing up. 3 difficulties, flag counter, chord-click |
| 9 | [Pong](https://korifcan.github.io/Classic-Games/games/pong/) | Arcade | Retro paddle vs AI duel. Progressive ball speed, particle effects on scoring |
| 10 | [Breakout](https://korifcan.github.io/Classic-Games/games/breakout/) | Arcade | Break rainbow bricks with paddle and ball. Velocity-based collisions, particle explosions |
| 11 | [Dino Runner](https://korifcan.github.io/Classic-Games/games/dino/) | Arcade | Chrome-style endless runner. Cacti, pterodactyls, day/night cycle, speed progression |
| 12 | [Sudoku](https://korifcan.github.io/Classic-Games/games/sudoku/) | Puzzle | 9×9 grid with 3 difficulties. Notes/pencil mode, timer, mistake tracking, puzzle generator |
| 13 | [Connect 4](https://korifcan.github.io/Classic-Games/games/connect4/) | Strategy | Drop discs, connect four. PvP & PvAI modes with heuristic AI, round tracking |
| 14 | [Typing Test](https://korifcan.github.io/Classic-Games/games/typing/) | Skill | Timed typing challenge. Real-time WPM, accuracy, per-character feedback, high scores |
| 15 | [Simon Says](https://korifcan.github.io/Classic-Games/games/simon/) | Memory | Repeat the growing sequence. Strict & regular modes, speed increases, high score |
| 16 | [15-Puzzle](https://korifcan.github.io/Classic-Games/games/puzzle15/) | Puzzle | Slide tiles into order. 3×3 & 4×4 modes, move counter, timer, best time tracking |

## Features

- **Zero dependencies** — pure HTML, CSS, JavaScript, no frameworks or libraries
- **Procedural audio** — every game has unique Web Audio API background music (no audio files)
- **Sound effects** — distinct SFX for actions, collisions, scoring, and game events
- **Touch support** — all games fully playable on mobile via touch/gesture
- **Keyboard support** — keyboard controls for desktop play
- **Mobile responsive** — canvas and UI scale to any screen size
- **High scores** — persistent score tracking via localStorage
- **Dark theme** — glass-morphism UI with neon accent gradients and animated backgrounds
- **Mute button** — toggle sound in any game
- **Single file** — each game is one self-contained HTML file, easy to host anywhere
- **No ads, no trackers, no analytics** — completely clean

## Controls

| Game | Desktop | Mobile |
|------|---------|--------|
| Tetris | Arrow keys, P=pause, H=hold, Z/X=rotate | Swipe, tap |
| Snake | Arrow keys or WASD | Swipe |
| 2048 | Arrow keys | Swipe |
| Flappy Bird | Space/Click | Tap |
| Space Shooter | Arrow keys + Space | Touch drag |
| Tic Tac Toe | Click | Tap |
| Memory | Click | Tap |
| Minesweeper | Left/Right click, 1-3=level, R=reset | Tap, long-press flag |
| Pong | Arrow Up/Down, mouse move | Touch drag |
| Breakout | Mouse move | Touch drag |
| Dino Runner | Space/Up/W | Tap |
| Sudoku | 1-9 keys, click numbers | Tap cell + tap number |
| Connect 4 | Click column | Tap column |
| Typing Test | Type words | (desktop preferred) |
| Simon Says | G/R/Y/B or 1-4, Enter=start | Tap quadrant |
| 15-Puzzle | Click tile, Arrow keys | Tap tile |

## Play

Visit **[https://korifcan.github.io/Classic-Games/](https://korifcan.github.io/Classic-Games/)**

## Run locally

```bash
git clone https://github.com/KoRifCan/Classic-Games.git
cd Classic-Games
# Open index.html in any browser
```

## Technical details

- **Audio**: Procedural Web Audio API (`OscillatorNode` + `GainNode` + `BiquadFilterNode`)
- **Rendering**: HTML5 Canvas 2D for action games, DOM for puzzle/strategy games
- **Responsive**: CSS `clamp()`, viewport units, media queries
- **Storage**: `localStorage` for high scores, sound preferences, and game state
- **Animation**: `requestAnimationFrame` with delta-time for frame-rate independent physics
- **No polyfills**: Modern browser APIs only (Chrome, Firefox, Safari, Edge)

## Bug fixes & improvements

- Frame-rate independent physics across all games (fixed speed-up on high-refresh monitors)
- Key repeat prevention (`e.repeat` check) to prevent input spam on held keys
- Ball clipping fixes in Pong & Breakout
- AI scoring duplication fix in Connect 4
- Tail interpolation fix in Snake
- WPM calculation fix in Typing Test (was using total time instead of elapsed)
- Background music lifecycle fixes (stop on game over, restart on new game, visibility handling)
- Touch input refinements across all mobile games
