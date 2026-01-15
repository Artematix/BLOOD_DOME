```yaml
---
id: ability_yyroizgt_wave_crash
name: "Wave Crash"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_yyroizgt

# Shop Information (null if not purchasable)
shop:
  buy: 75                        # Basic tier ability
  sell: null

# Requirements
requirements:
  level: null
  abilities: []

# Action Economy
action_type: bonus_action

# Resource Cost
resource:
  type: per_rest
  amount: 3
  recharge: short_rest

# Targeting
target:
  type: single
  range: 30
  area: null

# Mechanical Effect (structured)
effect:
  damage: null
  healing: null
  save: "STR 13"
  duration: "instantaneous"
  condition: "prone (on failed save)"
---

# Wave Crash

*"Feel the ocean's pull! None can stand against Moan-a's tide!"*

## Effect

**Bonus Action** - 3 charges per short rest

Yyroizgt summons a crashing wave that strikes a creature he can see within 30 feet. The target must make a Strength saving throw (DC 13) or be knocked prone. If the target is already wet, they have disadvantage on this saving throw.

**Synergy with Wet Status:**
- Wet creatures have disadvantage on the save
- This allows Yyroizgt to knock down wet targets more reliably
- Works well as a setup for advantage on his next melee attack (attacking prone targets)

## Interaction Notes

**Combat Flow:**
1. Hit enemy with Divine Smite → applies "wet" status
2. Use Wave Crash as bonus action → prone with disadvantage on save
3. Attack with advantage (prone target) on next turn

**Why This is Strong:**
- Low cost (bonus action economy)
- 3 charges per short rest = frequent use
- Synergizes with Yyroizgt's core "wet" mechanic
- Enables advantage on attacks even without being in water
- No damage, but control is valuable

**Balance:**
- Requires hitting with smite first for full effect
- DC 13 is moderate (50-60% success rate normally, higher with disadvantage)
- Only works on one target at a time
- Uses bonus action (competes with other bonus action options)
```
