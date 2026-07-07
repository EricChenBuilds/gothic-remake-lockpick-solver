# Gothic 1 Remake Lockpick Solver

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with HTML/CSS/JS](https://img.shields.io/badge/Made%20with-HTML%2FCSS%2FJS-1f425f.svg)](https://shields.io/)

A web-based solver for the lockpicking mini-game in **Gothic 1 Remake**. Configure plates, holes, and linkages — get the shortest click sequence in real time.

🌐 **Live:** https://gothicremakelockpickingsolver.com

---

## ✨ Features

- Support for **4–7 metal plates**
- **7 holes** per plate; configurable start pin (target pin defaults to hole 4)
- **Link Grid:** None / Same / Opposite linkage configuration
- Real-time **shortest-move solver**
- Consecutive identical moves are grouped in the output
- **Chest presets:** save and reload lock setups by name
- One-click reset
- Responsive 2:1 layout (collapses on small screens)
- Zero dependencies, no build step

---

## 🚀 Quick Start

This is a fully static site — no install required.

**Option 1 — Open directly:**
```bash
# Just double-click index.html, or:
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

**Option 2 — Local server** (recommended for a cleaner experience):
```bash
python3 -m http.server 8000
# Then visit http://localhost:8000
```

---

## 📖 How to Use

1. Select the number of **PLATES** (4 / 5 / 6 / 7) at the top.
2. Click a hole on **Plate 1** to set the start pin. The target pin defaults to **Hole 4**.
3. Configure the **Link Grid** for each plate on the right side of every plate row:
   - **None** — does not affect the linked plate
   - **Same** — the linked plate moves in the same direction
   - **Opposite** — the linked plate moves in the opposite direction
4. Click **`SOLVE LOCK`**.
5. Read the shortest sequence in the right-hand **SOLUTION** panel.
6. (Optional) Click **`Save chest`** to store the current setup, then reload it later by name.

Click **`HOW IT WORKS`** in the top-right of the page for an in-app visual guide.

---

## 🧠 How the Solver Works

The solver searches the lock's state space for the shortest legal sequence of plate presses, using a BFS-style search with move-merge pruning for non-linked plates.

You don't need to understand the algorithm to use the tool — just set up the lock and hit `SOLVE LOCK`.

---

## 📂 Project Structure

```
├── index.html      # Single-file app (HTML + CSS + JS, all in one)
├── image.jpg       # Reference image used in the in-app tutorial
├── favicon.svg
├── robots.txt
├── sitemap.xml
└── LICENSE         # MIT
```

---

## 🛠 Tech Stack

- Pure **HTML**, **CSS**, and **vanilla JavaScript**
- No frameworks, no build tools, no dependencies
- Hosted on **Cloudflare Pages**

---

## ⚠️ Disclaimer

This is an unofficial fan-made tool. It is **not affiliated with, endorsed by, or sponsored by** the publishers or developers of *Gothic 1 Remake*. All game-related trademarks belong to their respective owners.

---

## 📄 License

[MIT](LICENSE) © Eric (EricChenBuilds)
