# ⚡ NEON VIPER

> *An original 80s neon-punk arcade snake game — built entirely in vanilla HTML5 Canvas. No frameworks. No dependencies. No build tools. Just pure grid chaos.*

![Neon Viper](https://img.shields.io/badge/NEON-VIPER-ff00ff?style=for-the-badge&labelColor=05000f)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla_ES5-ffff00?style=for-the-badge&labelColor=05000f)
![Canvas](https://img.shields.io/badge/HTML5-Canvas-00ffff?style=for-the-badge&labelColor=05000f)
![License](https://img.shields.io/badge/License-MIT-aa00ff?style=for-the-badge&labelColor=05000f)
![Status](https://img.shields.io/badge/Status-Live-00ff88?style=for-the-badge&labelColor=05000f)
![Size](https://img.shields.io/github/size/RainFirestorm/neon-viper/index.html?style=for-the-badge&labelColor=05000f&color=ff6600&label=Game+Size)

---

## 🎮 Play Now

### **[▶ PLAY NEON VIPER → rainfirestorm.github.io/neon-viper](https://rainfirestorm.github.io/neon-viper)**

No install. No account. No dependencies. Click and play instantly in any browser.

---

## 🕹️ What Is Neon Viper?

Neon Viper is a fully original 80s arcade-style snake game set across **50 hand-crafted neon sectors**, each with a unique event that permanently changes the game state. Eat glyphs, dodge bombers, chain combos, and survive long enough to claim the **Apex Throne**.

### ✨ Features

| Feature | Description |
|---|---|
| 🗺️ **50 Sectors** | Each with a unique neon palette, name, and spectacular event |
| ⚔️ **1 & 2 Player** | Share one electrified map — eat each other's bodies in free-for-all |
| ✈️ **Bomber Planes** | Fly across the grid dropping live explosions with real blast radius |
| 💥 **4 Powerups** | Phase, Nova, Blast, Ward — each with distinct visual effects |
| 🌈 **Ripple Effects** | Every glyph eaten erupts in expanding neon color rings |
| 🏆 **Hall of Vipers** | Global top 10 leaderboard with player initials |
| 📋 **Sector Codex** | Preview all 50 sectors and events before you play |
| 📊 **Combo System** | Chain up to x8 multiplier for massive score bursts |
| 🎯 **Max Score: 1000** | Reach it and the Exit Portal appears |

---

## 🎯 How To Play

### Controls

| Action | 1 Player | 2 Players P1 | 2 Players P2 |
|---|---|---|---|
| Move Up | ↑ Arrow | W | ↑ Arrow |
| Move Down | ↓ Arrow | S | ↓ Arrow |
| Move Left | ← Arrow | A | ← Arrow |
| Move Right | → Arrow | D | → Arrow |
| Restart | Space | Space | Space |

### Objective

1. **Eat glyphs** (⊞) to grow your viper and score points
2. **Chain combos** — eat quickly to build x2 → x8 multipliers
3. **Collect powerups** — hexagonal icons scattered across the grid
4. **Dodge bombers** — planes drop live explosives with blast radius
5. **Survive 50 sectors** of escalating chaos and enemy spawns
6. **Reach 1000 points** — the Exit Portal appears at the center of the map
7. **Eat the portal** to win and enter the Hall of Vipers

---

## ⚡ Powerups

| Icon | Name | Effect | Duration |
|---|---|---|---|
| 🌀 | **PHASE** | Full invincibility — pass through everything | 8 seconds |
| 🔥 | **NOVA** | Double viper size + maximum speed | 10 seconds |
| ⚡ | **TURBO** | Speed boost + fire trail effect | 5 seconds |
| 💥 | **BLAST** | Shockwave — instantly clears all enemies & bombs | 12 seconds |
| 🛡 | **WARD** | Absorbs one fatal hit automatically | 1 charge |

---

## 🗺️ Sector Highlights

50 sectors across 10 unique neon grid palettes. Every sector arrival triggers a spectacular event:

| Sector | Name | Event | Effect |
|---|---|---|---|
| 3 | Violet Void | PHANTOM ZONE | Phase invincibility activated |
| 5 | Plasma Rift | GRIDS COLLIDE | Walls explode — 2P maps merge into one |
| 7 | Amber Grid | GEM RAIN | Diamonds flood the field |
| 8 | Cryo Zone | FREEZE PULSE | All enemies frozen solid |
| 14 | Solar Flare | SOLAR PULSE | Full screen whiteout flash |
| 17 | Pulse Canyon | SHOCKWAVE LOOP | Auto-blast clears all threats |
| 20 | Quantum Leap | PHASE JUMP | Viper teleports across the grid |
| 27 | Score Frenzy | SCORE FRENZY | Double points for 8 seconds |
| 33 | Lumen Core | LUMEN BURST | Screen supernova explosion |
| 34 | Rift Valley | RIFT OPENS | Teleport pads appear on map |
| 43 | Prism Vortex | PRISM FRACTURE | Rainbow particle storm |
| 45 | Hypergrid | HYPERSPEED | Maximum velocity locked permanently |
| 49 | Singularity | SINGULARITY BREACH | Expanding reality collapse rings |
| 50 | Apex Throne | THRONE CLAIMED | You are the Neon Viper |

> See the full [Sector Codex](../../wiki/Sector-Codex) for all 50 sectors.

---

## 🛠️ Architecture

### Tech Stack

| Technology | Usage |
|---|---|
| **HTML5 Canvas 2D** | All rendering — grid, vipers, bombers, particle FX |
| **Vanilla JavaScript (ES5)** | Game loop, physics, collision detection, 50 sector events |
| **CSS3** | UI panels, scanline overlay, neon glow effects |
| **Orbitron** (Google Fonts) | Typography — single external request |
| **Zero dependencies** | No npm, no webpack, no frameworks, no build tools |

### File Structure

```
neon-viper/
├── index.html          ← Entire game (single self-contained file)
├── README.md           ← Project documentation
├── CHANGELOG.md        ← Version history
├── CONTRIBUTING.md     ← Contributor guidelines
├── SECURITY.md         ← Security policy
├── LICENSE             ← MIT License
└── .github/
    └── ISSUE_TEMPLATE/
        ├── bug_report.md
        └── feature_request.md
```

### Design Principles

- **Single file** — the entire game ships as `index.html`. No assets, no modules, no dependencies
- **Zero build step** — open the file and it runs. No npm install, no webpack, no compilation
- **ES5 compatible** — written without modern JS syntax for maximum sandbox and browser compatibility
- **Canvas-only rendering** — no DOM manipulation during gameplay, everything drawn via 2D Canvas API
- **Callback-based async** — no async/await, no Promises chaining in game-critical paths

---

## 🔒 Security

Neon Viper is designed with security by default:

- ✅ **No data collection** — zero user PII stored anywhere
- ✅ **No external scripts** — only one Google Fonts CSS import
- ✅ **No eval()** — no dynamic code execution of any kind
- ✅ **No cookies** — no localStorage, no sessionStorage
- ✅ **No backend** — pure static file, no server, no database
- ✅ **Input sanitized** — initials stripped to `[A-Z]` before any storage operation
- ✅ **Offline capable** — download and open locally, no network required

See [SECURITY.md](SECURITY.md) for the full security policy and vulnerability reporting process.

---

## 🚀 Run Locally

```bash
# Clone the repository
git clone https://github.com/RainFirestorm/neon-viper.git

# Navigate into the project
cd neon-viper

# Open in your default browser — that's it
open index.html

# Or on Linux
xdg-open index.html

# Or on Windows
start index.html
```

**No server required. No `npm install`. No build step. No configuration.**

Alternatively, [download the ZIP](https://github.com/RainFirestorm/neon-viper/archive/refs/heads/main.zip) and open `index.html` directly.

---

## 🤝 Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Quick start:

```bash
git clone https://github.com/RainFirestorm/neon-viper.git
cd neon-viper
git checkout -b feature/your-idea
# Edit index.html
# Open index.html in browser to test
git commit -m "feat: your description"
git push origin feature/your-idea
# Open a Pull Request
```

Please keep all contributions within the single-file architecture. No external dependencies, no build tools.

---

## 📋 Changelog

See [CHANGELOG.md](CHANGELOG.md) for full version history and release notes.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for full terms.

Free to use, modify, and distribute. Credit appreciated but not required.

---

## 👤 Author

**RainFirestorm** — [github.com/RainFirestorm](https://github.com/RainFirestorm)

---

<div align="center">

*Reach the Apex Throne. Claim the grid.*

![Footer](https://img.shields.io/badge/NEON-VIPER-ff00ff?style=for-the-badge&labelColor=05000f)
![Made with](https://img.shields.io/badge/Made_with-Canvas_&_Chaos-00ffff?style=for-the-badge&labelColor=05000f)

</div>
