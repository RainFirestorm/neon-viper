# Changelog

All notable changes to Neon Viper are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2025

### 🎉 Initial Release

**The first public release of Neon Viper.**

#### Added
- 50 hand-crafted sectors each with a unique neon palette and live event
- 1 Player mode — arrow key controls
- 2 Player mode — shared map, WASD + arrow keys, free-for-all body eating
- Bomber plane enemies that drop live explosives with blast radius
- 4 powerups: Phase (invincibility), Nova (size + speed), Blast (shockwave), Ward (shield)
- Combo chain system (x1 → x8 multiplier)
- Color ripple effect on every glyph eaten
- Hall of Vipers global leaderboard (top 10, initials only)
- Sector Codex — full preview of all 50 sectors and events
- Exit Portal spawn at max score (1000 points)
- Melt win sequence with rainbow cascade effect
- Scanline CRT overlay for authentic 80s aesthetic
- Orbitron typography for neon-punk visual identity
- Score progress bar in HUD
- Sector flash banner on every level transition (900ms, non-blocking)
- 3-second spawn invincibility for both players
- Neon grid with perspective vanishing point lines
- Wanderer NPC that roams and builds data node structures
- Sprite orb creatures that bounce around the grid
- Shade enemies that hunt the viper (spawn from sector 2+)
- Volatile crystal golem that charges and explodes (sector 5+)
- Teleport pads (Rift Valley sector event)
- Shadow viper visual effect
- Star particle field effect
- Singularity collapse ring effect
- Prism rainbow particle burst
- Supernova full-screen flash effect
- HUD scramble effect (Deep Static sector)
- Fire trail viper effect (Ember Grid sector)
- Freeze pulse that locks all enemies (Cryo Zone)
- Gem rain mode with high diamond spawn rate (Amber Grid)
- Auto-blast that clears all threats (Pulse Canyon)
- Warp teleport that moves the viper instantly (Quantum Leap)
- Score burst bonus (Solar Nexus)
- Double score mode (Binary Fall / Score Frenzy)
- Triple gem value mode (Neon Cathedral)
- Chain max lock at x8 (Electric Dawn)
- Turbo lock — permanent speed (Scarlet Wire / Hypergrid)
- Auto-nova — permanent size (Nova Core)
- Auto-ward — free shield charges (Chrome Abyss / Iron Mesh)
- Giant volatile (Titan Fall)
- Pack shades — 6 simultaneous hunters (Dark Resonance)
- All threats simultaneous (Oblivion Edge)
- Singularity invincibility window (Singularity sector)
- GitHub Pages deployment
- MIT License
- Full documentation suite

#### Architecture
- Single HTML file — zero dependencies, zero build step
- ES5-compatible JavaScript throughout
- Canvas 2D API for all rendering
- Callback-based async for leaderboard storage
- Retry-loop canvas initialization for reliable startup
- Cross-snake collision with grace period (snake length > 5)
- 3-second spawn invincibility for crash-proof game start

---

## Roadmap

### [1.1.0] — Planned
- [ ] Web Audio API — 80s synth sound effects
- [ ] Mobile touch controls — virtual D-pad
- [ ] High score persistence for GitHub Pages via JSONBin.io
- [ ] Animated GIF in README
- [ ] Social share card on win screen

### [1.2.0] — Planned
- [ ] Additional sector events
- [ ] Boss sector every 10 levels
- [ ] Time attack mode
- [ ] Replay system

### [2.0.0] — Future
- [ ] Mobile app wrapper
- [ ] Tournament mode
- [ ] Custom sector editor
