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
- **Single file:** `index.html` contains everything
- **Target:** Browser, touch + mouse

## Rules

### Git
The human does Git. No commits, pushes or branch operations by Claude.

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

- **Menu:** Title, high score, start button
- **Countdown:** 3 → 2 → 1
- **Game:** 3 stacks, PLING button, 3 hearts, score
- **Game over:** Score, high score, back to menu

### Design

- No sounds – play alongside music or podcasts
- CLI aesthetic – dark theme, monospace font
- One button – maximum focus
- Cards show symbols in dice-style layout (1–4 symbols)

## Context

This prototype is part of a larger exploration:
- Try out game ideas
- Learn Vanilla JS/HTML
- Find out what works

No product, no launch pressure. Just: is it fun?

## Open questions

- [ ] How fast should cards appear? Does speed increase over time?
- [ ] How to implement 2-player mode? (split screen?)
- [ ] Persist high score with localStorage?

## Learnings

- Dice-style symbol layout is instantly readable (subitizing)
- Canvas gives full control – worth the extra setup
- Small commits keep things testable and reversible
- State machine ('menu' | 'countdown' | 'playing' | 'feedback' | 'gameover') keeps logic clean
