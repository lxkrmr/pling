# pling! – Design

Game idea, design decisions, and learnings. Living document – updated as the project evolves.

→ See also: [CLAUDE.md](CLAUDE.md) (AI rules) · [README](README.md) (public)

---

## Idea

A reaction game: cards appear automatically, hit the button when you see exactly 5 of a kind.

**Inspiration:** Classic card reaction games – radically simplified. Just the bell.

**Core question:** Does it feel good? Is it fun?

## Core loop

```
Cards appear automatically
        ↓
Count, keep track in your head
        ↓
5 of a kind? → PLING!
        ↓
Correct → Points
Wrong → Penalty (lose a heart)
```

## Design principles

- **No sounds** – play alongside music or podcasts
- **One button** – maximum focus
- **CLI aesthetic** – dark theme, monospace font, GitHub Dark Colorblind palette
- **Colorblind-safe** – blue = correct, orange = wrong (no red/green)

## Scope

| In | Out |
|---|---|
| 2–4 stacks, auto-paced | Sound effects |
| PLING! button | Multiplayer |
| 3 hearts | Leaderboard |
| Score + high score | Achievements |
| DE + EN | Light theme (maybe) |

## Values

- **No dark patterns** – no manipulation, no fake urgency
- **Honest** – what you see is what you get
- **Simple** – as little as possible, as much as needed
- **Joyful** – if it's not fun, why bother?
- **Accessible** – colorblind-safe palette; before release: respect `prefers-reduced-motion`

## Progression

- Start: 2 stacks, 1200ms interval
- Score 3: 3rd stack unlocks
- Score 15: 4th stack unlocks
- Speed increases with score, minimum 500ms

## Screens

- **Menu:** Title, instructions, high score, start button
- **Countdown:** "ready?" → "go!"
- **Game:** 2–4 stacks, PLING button, 3 hearts, score
- **Game over:** Score, high score, back to menu

## Open questions

- [ ] How to implement 2-player mode? (split screen?)
- [ ] Light theme toggle

## Design decisions

*(Document decisions and their rationale here)*

## Ideas & parking lot

*(Things to explore later)*

## Learnings

- Dice-style symbol layout is instantly readable (subitizing)
- Canvas gives full control – worth the extra setup
- Small commits keep things testable and reversible
- State machine (`menu` | `countdown` | `playing` | `feedback` | `gameover`) keeps logic clean
- `setTimeout` chain > `setInterval` for variable tempo
- Data-driven countdown steps (COUNTDOWN_STEPS array) = open/closed principle
- Network-first service worker = always fresh when online, offline as fallback
- Colorblind-safe palette: blue/orange instead of green/red
- Canvas coordinate offset needed when canvas is smaller than viewport (`getBoundingClientRect`)
- Progressive stack unlock makes onboarding natural without a tutorial
