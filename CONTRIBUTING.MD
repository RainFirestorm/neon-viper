# Contributing to Neon Viper

First off — thank you for taking the time to contribute. Every improvement, bug fix, and idea makes Neon Viper better for everyone.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Architecture Guidelines](#architecture-guidelines)
- [Commit Convention](#commit-convention)
- [Pull Request Process](#pull-request-process)
- [Sector Event Ideas](#sector-event-ideas)

---

## Code of Conduct

Be respectful. Be constructive. No harassment, no discrimination, no toxicity. Issues or PRs that violate this will be closed without discussion.

---

## How Can I Contribute?

### 🐛 Reporting Bugs

Before opening a bug report:
1. Check existing [Issues](https://github.com/RainFirestorm/neon-viper/issues) to avoid duplicates
2. Test in a clean browser session (clear cache)
3. Try both 1P and 2P modes if relevant

Use the **Bug Report** issue template and include:
- Browser and version
- OS and version
- Steps to reproduce
- Expected vs actual behavior
- Screenshot or screen recording if possible

### 💡 Suggesting Features

Open a **Feature Request** issue with:
- Clear description of the idea
- Why it fits the game's aesthetic and design principles
- Rough implementation approach (optional but helpful)

### 🔧 Code Contributions

We welcome:
- Bug fixes
- New sector events
- Performance improvements
- Visual effect enhancements
- Accessibility improvements
- Documentation improvements

---

## Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/neon-viper.git
cd neon-viper

# No install step needed — open directly
open index.html

# Make changes to index.html
# Refresh browser to test
# That's the entire dev workflow
```

**There is no build step, no package manager, no dev server required.**

For live reload during development, you can optionally use:
```bash
# If you have Python installed
python3 -m http.server 8080
# Then open localhost:8080
```

---

## Architecture Guidelines

These are non-negotiable for all contributions:

### ✅ DO

- Keep everything in `index.html` — single file architecture
- Write ES5-compatible JavaScript (no arrow functions in critical paths, no const/let, no async/await in game logic)
- Use `var` for variable declarations in game-critical code
- Use callback patterns instead of Promises for storage operations
- Test in both 1-player and 2-player modes
- Test across Chrome, Firefox, and Safari
- Keep the neon 80s aesthetic consistent

### ❌ DO NOT

- Add npm dependencies or a package.json
- Add a build step or bundler
- Use ES6+ features that may break in sandboxed environments
- Add external JavaScript CDN imports
- Use localStorage or sessionStorage
- Add images or binary assets (keep it code-only)
- Break the single-file constraint

### Adding a New Sector Event

Sector events live in the `fireSectorEvent()` function and the `SECTORS` array. To add a new event:

1. Add an entry to the `SECTORS` array:
```javascript
{n:'YOUR SECTOR NAME', bg:'#hexcolor', acc:'#accentcolor', ev:'EVENT NAME', sub:'short description', fx:'your_fx_key'}
```

2. Add a handler in `fireSectorEvent()`:
```javascript
if(fx==='your_fx_key') {
  // your event logic here
  // use existing helpers: spawnShades(), spawnRipple(), addTxt(), etc.
}
```

3. Test that it fires correctly at the right score threshold
4. Add it to the Sector Codex wiki page

---

## Commit Convention

Use conventional commits for clear history:

```
feat: add new sector event for Acid Zone
fix: prevent P2 instant death on spawn
perf: reduce particle array allocation
docs: update sector codex with events 48-50
style: improve bomber neon glow intensity
refactor: consolidate killSnake logic
```

Format: `type: short description (under 72 chars)`

Types: `feat` `fix` `perf` `docs` `style` `refactor` `test`

---

## Pull Request Process

1. **Fork** the repository
2. **Create a branch** from `main`:
   ```bash
   git checkout -b feat/your-feature-name
   ```
3. **Make your changes** to `index.html`
4. **Test thoroughly** — 1P mode, 2P mode, all affected sectors
5. **Write a clear PR description** including:
   - What changed and why
   - How to test it
   - Screenshots/recordings for visual changes
6. **Open the PR** against `main`

### PR Review Criteria

- Does it maintain the single-file architecture?
- Does it use ES5-compatible syntax?
- Does it fit the visual aesthetic?
- Does it work in 1P and 2P modes?
- Does it introduce any security concerns?
- Is the code readable and commented where needed?

---

## Sector Event Ideas

Looking for inspiration? Here are areas we'd love to see expanded:

- **Audio events** — Web Audio API synth effects on sector transitions
- **Boss encounters** — unique enemy behavior every 10 sectors
- **Environmental hazards** — moving walls, shrinking grid
- **Score modifiers** — negative score zones, score decay
- **Visual themes** — new grid rendering styles per sector group
- **Mobile controls** — touch D-pad overlay

---

## Questions?

Open a [Discussion](https://github.com/RainFirestorm/neon-viper/discussions) for anything that doesn't fit a bug report or feature request.

*Thank you for helping make Neon Viper better. Reach the Apex Throne.* ⚡
