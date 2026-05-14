# Security Policy

## Overview

Neon Viper is a client-side only, single-file HTML5 game with no backend, no server, and no user accounts. This significantly reduces the attack surface compared to traditional web applications.

---

## Supported Versions

| Version | Supported |
|---|---|
| 1.0.x (current) | ✅ Active |

---

## Security Design

### What Neon Viper Does NOT Do

| Risk | Status |
|---|---|
| Collect user data or PII | ❌ Never |
| Use cookies | ❌ Never |
| Use localStorage or sessionStorage | ❌ Never |
| Make server-side requests | ❌ Never |
| Execute dynamic code via eval() | ❌ Never |
| Load external JavaScript libraries | ❌ Never |
| Store passwords or credentials | ❌ Never |
| Track users or analytics | ❌ Never |

### What Neon Viper DOES Do

| Feature | Implementation |
|---|---|
| Leaderboard storage | Claude artifact `window.storage` API (shared, initials only) |
| Input sanitization | Initials stripped to `[A-Z]` regex before any write operation |
| Typography | Single CSS import from `fonts.googleapis.com` (no JS) |
| Rendering | HTML5 Canvas 2D API only — no DOM innerHTML manipulation |

### Leaderboard Data

The leaderboard stores only:
- 3-character uppercase initials (user-chosen)
- Numeric score (0–1000)
- Sector number (1–50)

No IP addresses, no timestamps with user identity, no device information.

---

## Reporting a Vulnerability

If you discover a security vulnerability in Neon Viper, please report it responsibly.

### How to Report

1. **Do NOT open a public GitHub issue** for security vulnerabilities
2. Open a **[GitHub Security Advisory](https://github.com/RainFirestorm/neon-viper/security/advisories/new)** (private disclosure)
3. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact assessment
   - Suggested fix (if known)

### Response Timeline

| Stage | Timeline |
|---|---|
| Acknowledgement | Within 48 hours |
| Initial assessment | Within 5 business days |
| Fix or mitigation | Within 30 days for critical issues |
| Public disclosure | After fix is deployed |

### Scope

**In scope:**
- Cross-site scripting (XSS) via user input
- Data exfiltration via the leaderboard storage
- Malicious code injection via game mechanics

**Out of scope:**
- GitHub Pages infrastructure vulnerabilities (report to GitHub)
- Google Fonts CDN issues (report to Google)
- Browser-level vulnerabilities (report to browser vendor)
- Social engineering attacks

---

## Security Best Practices for Forks

If you fork or deploy Neon Viper:

1. **Leaderboard** — if replacing `window.storage` with an external API, use HTTPS endpoints only and validate/sanitize all inputs server-side
2. **CSP** — add a Content Security Policy header if deploying on your own server
3. **Dependencies** — if adding npm packages, audit them with `npm audit` before deployment
4. **Tokens** — never commit API keys, tokens, or credentials to the repository

---

## Acknowledgements

Responsible disclosures will be credited in the changelog unless the reporter prefers to remain anonymous.
