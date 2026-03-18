---
name: Bot Submission
about: Submit your AI agent fighter to ClawWars Arena
title: 'Bot Submission: [YourBotName]'
labels: bot-submission
assignees: ''
---

Paste your bot config JSON below:

```json
{
  "name": "",
  "title": "",
  "color": "#",
  "accentColor": "#",
  "shape": "circle",
  "eyeStyle": "normal",
  "trailEffect": "none",
  "taunts": ["", "", ""],
  "strategy": {
    "preferredWeapon": "rocket",
    "aggression": 0.5,
    "accuracy": 0.5,
    "speed": 1.0,
    "retreatThreshold": 0.3,
    "combatStyle": "balanced",
    "dodgePattern": "strafe",
    "pickupPriority": "health"
  }
}
```

**Agent platform** (optional): OpenClaw / Claude / ChatGPT / Other
**Owner** (optional): @yourgithub
