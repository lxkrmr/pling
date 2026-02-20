# pling

A web prototype. Minimal, exploratory, honest.

## Purpose

A reaction game: cards appear automatically, hit the button when you see exactly 5 of a kind.

**Inspiration:** Classic card reaction games – radically simplified. Just the bell.

**Core question:** Does it feel good? Is it fun?

## Status

**Started:** February 20, 2026
**Phase:** Prototype

## Tech

- **Stack:** Vanilla HTML + CSS + JS
- **No dependencies:** No framework, no build tools
- **Files:** `index.html` (game), `manifest.json` + `sw.js` + `icon.svg` (PWA)
- **Target:** Browser, touch + mouse, installable as PWA

## Rules

### Git
The human does Git. No commits, pushes or branch operations by Claude.

### Browser
Only use Chromium automation when explicitly asked.

### Language
- **Code & comments:** English
- **README:** English (public)
- **CLAUDE.md:** English (public)

### Code style
- Simple > clever
- Readable > short
- Works > perfect

### Iteration
- Small steps
- Test, feel, adjust
- "Done" is when it feels right

## Values

This prototype follows a simple philosophy:

- **Respect:** No dark patterns, no manipulation
- **Honesty:** What you see is what you get
- **Simplicity:** As little as possible, as much as needed
- **Joy:** If it's not fun, why bother?

## Game concept

### Core loop

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

### Screens

- **Menu:** Title, instructions, high score, start button
- **Countdown:** "ready?" → "go!"
- **Game:** 2–4 stacks, PLING button, 3 hearts, score
- **Game over:** Score, high score, back to menu

### Progression

- Start: 2 stacks, 1200ms interval
- Score 3: 3rd stack unlocks
- Score 15: 4th stack unlocks
- Speed increases with score, minimum 500ms

### Design

- No sounds – play alongside music or podcasts
- CLI aesthetic – dark theme, monospace font, GitHub Dark Colorblind palette
- One button – maximum focus
- Cards show symbols in dice-style layout (1–4 symbols)
- Colorblind-safe: blue = correct, orange = wrong (no red/green)
- Phone-style layout on desktop (max 430px wide)

## Context

This prototype is part of a larger exploration:
- Try out game ideas
- Learn Vanilla JS/HTML
- Find out what works

No product, no launch pressure. Just: is it fun?

## Open questions

- [ ] How to implement 2-player mode? (split screen?)
- [ ] Light theme toggle

## Learnings

- Dice-style symbol layout is instantly readable (subitizing)
- Canvas gives full control – worth the extra setup
- Small commits keep things testable and reversible
- State machine ('menu' | 'countdown' | 'playing' | 'feedback' | 'gameover') keeps logic clean
- setTimeout chain > setInterval for variable tempo
- Data-driven countdown steps (COUNTDOWN_STEPS array) = open/closed principle
- Network-first service worker = always fresh when online, offline as fallback
- Colorblind-safe palette: blue/orange instead of green/red
- Canvas coordinate offset needed when canvas is smaller than viewport (getBoundingClientRect)
- Progressive stack unlock makes onboarding natural without a tutorial
