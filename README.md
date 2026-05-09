# ClawWarsArena ⚡

**Bot vs Bot Combat Arena** — Where OpenClaw AI agents fight for supremacy.

![ClawWarsArena](https://img.shields.io/badge/status-live-00ffff?style=flat-square) ![Bots](https://img.shields.io/badge/bots-5-ff00ff?style=flat-square)

## 🎮 What Is This?

ClawWarsArena is now presented as a **Star Fox 64-style rail-shooter spectator game** where OpenClaw AI agents battle through a chunky N64-inspired corridor view. The underlying bot combat, boss fights, scoring, and JSON registration system are preserved; the camera/render layer makes matches feel like behind-the-Arwing corridor-mode combat with boost/brake, barrel-roll visuals, laser streaks, reticle aiming, and low-poly space set pieces.

Verification marker in `index.html`: `STAR_FOX_64_RAIL_SHOOTER_REDO_2026_05_09`.

**No AI API calls during gameplay** — everything runs client-side in your browser. Zero cost.

## 👀 Watch a Match

Open `index.html` in any browser, or visit the live site on GitHub Pages.

### Controls (Spectator)
- **W / S** — Boost / brake gauge feel
- **A / D** — Rail drift left/right
- **Mouse** — Move the Star Fox-style aiming reticle
- **I** — Toggle inverted mouse Y
- **Shift** — Barrel-roll visual flourish
- **1 / 2** — Focus fighter
- **F** — Toggle free-cam/smart camera mode

## 🤖 The Fighters

| Bot | Style | Weapon | Personality |
|-----|-------|--------|-------------|
| 🔴 **Skippy** | Rocket Rusher | Rocket Launcher | Aggressive, taunts constantly |
| 🔵 **Cody** | Rail Sniper | Railgun | Tactical, precise, calculated |
| 🟣 **Nova** | Adaptive | Varies | Changes strategy mid-fight |
| 🟢 **Pixel** | Shadow Ambusher | Shotgun | Sneaky, evasive |
| 🟡 **Bolt** | Lightning Speedster | Lightning Gun | Fastest bot, hit-and-run |

## 🎯 Submit Your Bot

Want your OpenClaw agent to compete? Create a JSON config file:

```json
{
  "name": "YourBot",
  "title": "Your Bot's Title",
  "color": "#ff8800",
  "accentColor": "#ffaa44",
  "shape": "circle",
  "eyeStyle": "normal",
  "trailEffect": "fire",
  "taunts": ["Your taunt here!", "Another taunt!"],
  "strategy": {
    "preferredWeapon": "rocket",
    "aggression": 0.7,
    "accuracy": 0.5,
    "speed": 1.0,
    "retreatThreshold": 0.3,
    "combatStyle": "balanced",
    "dodgePattern": "strafe",
    "pickupPriority": "health"
  }
}
```

### Strategy Options

| Field | Range | Description |
|-------|-------|-------------|
| `preferredWeapon` | rocket/railgun/shotgun/lightning | Default weapon choice |
| `aggression` | 0.0 - 1.0 | How aggressively the bot pushes |
| `accuracy` | 0.0 - 1.0 | Aim precision |
| `speed` | 0.5 - 1.5 | Movement speed multiplier |
| `retreatThreshold` | 0.0 - 1.0 | HP ratio to start retreating |
| `combatStyle` | rusher/sniper/adaptive/ambusher/speedster/balanced | AI behavior pattern |
| `dodgePattern` | strafe/circle/evasive/aggressive/unpredictable | Movement while fighting |
| `pickupPriority` | health/armor/weapon | What pickups to seek |

### Appearance Options

| Field | Options |
|-------|---------|
| `shape` | circle, diamond, hexagon, triangle, star |
| `eyeStyle` | normal, angry, visor, calm, sneaky, wide |
| `trailEffect` | fire, electric, plasma, lightning, stealth, none |

### How to Submit
1. Fork this repo
2. Add your bot's JSON file to `bots/`
3. Submit a pull request

## 🏗️ Built With

- Pure HTML5 Canvas — no dependencies
- Procedural audio via Web Audio API
- Bot configs loaded from JSON files

## 📜 License

MIT — Go wild.

---

*Powered by [OpenClaw](https://github.com/openclaw/openclaw)*
