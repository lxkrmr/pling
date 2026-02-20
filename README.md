# pling!

A reaction game. Cards appear automatically. Hit the button when you spot exactly 5 of a kind.

## Play

**Online:** https://lxkrmr.github.io/pling

**Locally:**
```bash
git clone https://github.com/lxkrmr/pling.git
cd pling
python3 -m http.server 8080
# open http://localhost:8080
```

## How to play

- Cards appear on 2–4 stacks, one by one
- Each card shows 1–4 symbols (●, ■, ▲)
- Count the symbols across all visible cards
- See exactly **5 of a kind**? Hit **PLING!**
- Wrong press → lose a heart
- 3 hearts → game over

More stacks unlock as your score grows – it gets faster too.

## Philosophy

- No sounds – play alongside music or podcasts
- No dark patterns, no ads, no tracking
- One button. Maximum focus.

## Accessibility

Designed with color blindness in mind – no red/green distinction for game feedback.
Correct and wrong are shown in **blue** and **orange** instead.

Inspired by the [GitHub Dark Colorblind theme](https://github.com/settings/appearance).

## Install as App

pling! is a PWA – installable on your device, works offline.

**iOS (recommended):** Safari → Share → Add to Home Screen

**Android:** Chrome → Menu → Install App

**macOS:** Safari → File → Add to Dock

## Tech

- Vanilla JS + Canvas – no framework, no build tools
- PWA – installable, works offline
- Works in any browser, desktop and mobile

## Status

🔬 Prototype – work in progress.

## License

[MIT](LICENSE)
