# The Gaslight Parlour

A Victorian gentleman's-club arcade of single-file HTML games. No frameworks, no dependencies, no build step — just open a file (or visit the live link) and play.

Built as part of a personal project to make a whole arcade of standalone browser games, each one a "room down the hall" off a shared parlour hub.

---

## Play it live

**[dryleaftrace.github.io/gaslight-parlour](https://dryleaftrace.github.io/gaslight-parlour)**

Or download any `.html` file and open it directly in a browser — every room works completely offline.

---

## The Rooms

### 🏛 The Gaslight Parlour — the hub
The landing page. A wood-and-brass frame with a card for each room, plus a permanently "locked" placeholder card reserved for whatever gets built next.

### ⚫ The Draughts Room — checkers
American draughts (checkers), crimson vs. ebony pieces on a wood/brass board.
- Mandatory capture and multi-jump chains enforced
- King promotion on the back row (kings move any diagonal direction, non-flying)
- AI opponent using alpha-beta pruning, with a "House Rules" difficulty selector from Novice to Master

### 🎱 The Green Baize — 8-ball pool
A physics-driven pool table.
- Cue ball control with English (spin)
- Difficulty-tuned AI opponent, Novice to Master
- Custom collision and friction simulation, no physics library

### ♞ Ink & Ivory — chess
A full chess implementation with an alpha-beta search AI.
- Castling, en passant, and pawn promotion all implemented
- Adjustable AI difficulty
- Wood-grain board styling to match the parlour aesthetic

### 🂡 The Patience Room — Klondike solitaire
Single-player Klondike, played solo against the deck.
- Standard tableau/foundation/stock rules, with Draw One or Draw Three
- Click-to-select movement, double-click auto-send to foundation, full undo history
- Auto-Finish button once the board can safely resolve itself

### ♣ The Sharper's Table — five-card draw poker
Five-card draw against three AI opponents, fixed-limit betting.
- Full hand evaluator (High Card through Straight Flush) and draw-phase discard logic
- Fixed-limit betting rounds with a raise cap, house ante, and a pot that actually pays out
- Three recurring house regulars, each with their own aggressiveness and bluff frequency

### ♦ The River Room — Texas hold'em
Texas hold'em against the same three regulars, blinds instead of antes.
- Four streets (preflop/flop/turn/river) with dealer button and blind rotation
- Best-of-seven hand evaluation (2 hole + 5 community cards) with split-pot handling for ties
- Same fixed-limit betting engine as The Sharper's Table, adapted for community cards

---

## Technical Notes

- **Single-file apps** — each room is one self-contained HTML file (~1,000–1,500 lines of HTML, CSS, and vanilla JS). No bundler, no npm, no framework.
- **Zero dependencies** — no React, no jQuery, no physics, chess, or poker libraries. Every AI, hand evaluator, and animation is built from scratch.
- **Shared aesthetic** — Didot/Palatino type, wood-grain and brass-bright accents across all seven files, so the arcade reads as one coherent place rather than a pile of unrelated demos.
- **Shared card system** — the three card-table rooms (Patience, Sharper's Table, River Room) reuse the same `.pcard` rendering pattern and deck/shuffle helpers, styled consistently but built independently per file.
- **Relative linking** — the hub links to each room via percent-encoded relative hrefs (`The%20Draughts%20Room.html`, `Ink%26Ivory.html`, `The%20Sharper's%20Table.html`) so the whole arcade works identically from a local folder or from GitHub Pages.

---

## Usage

Clone or download the repo and open `The Gaslight Parlour.html` in any browser. No server required.

Or visit the live version: **[dryleaftrace.github.io/gaslight-parlour](https://dryleaftrace.github.io/gaslight-parlour)**

---

## Stack

| Layer | Choice | Why |
|---|---|---|
| Structure | HTML5 | Single-file portability |
| Styling | CSS custom properties + keyframe animations | No preprocessor needed |
| Logic | Vanilla JavaScript (ES6+) | No build step, runs anywhere |
| Game AI | Custom alpha-beta search (checkers, chess); heuristic betting AI (poker rooms) | No engine dependency |
| Physics | Custom `requestAnimationFrame` simulation (pool) | No physics library |
| Hosting | GitHub Pages, served from `/docs` | Free, static, instant |

---

## Related

- [Ink & Ivory](https://github.com/dryleaftrace/Ink-and-Ivory) — chess, also playable standalone or live
- [Cybersecurity Portfolio](https://github.com/dryleaftrace) — incident reports, network analysis, security assessments

---

If you enjoyed a night at the parlour: https://www.buymeacoffee.com/dryleaftrace
