---
id: ability_yyroizgt_tidal_strike
name: "Tidal Strike"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_yyroizgt

# Tier (for character-exclusive abilities)
tier: 1                          # Tier 1 (Low)
subtype: "aggressive"            # Aggressive path - direct damage

# Shop Information (null if not purchasable)
shop:
  buy: 5                         # Tier 1 price
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
  range: melee
  area: null

# Mechanical Effect (structured)
effect:
  damage: "1d8 cold"
  healing: null
  save: null
  duration: "instantaneous"
  condition: "wet (applied on hit)"
---

# Tidal Strike

*"Your blood will freeze in Moan-a's icy embrace! Drown in your own veins!"*

## Effect

**Bonus Action**

You call upon the cruel, freezing depths of the ocean to coat your weapon in brine ice. On your next melee weapon attack this turn, on a hit, seawater floods into the target's wounds, freezing their blood and filling their lungs with saltwater.

**Damage & Effects:**
- Deals an extra 1d8 cold damage as ice crystals form in their bloodstream
- Target gains "wet" status for 1 minute as water seeps from the wound
- If the target is already wet, the ocean claims them further - increase damage to 2d8 cold as their body temperature plummets
- If the weapon is thrown, it leaves a trail of water in its path.

**Flavor:** The target's wound weeps seawater mixed with blood. In the Blood Dome's brutal arena, they're marked for sacrifice to the goddess of the seas.

## Interaction Notes

**This is Yyroizgt's Tier 1 Aggressive Ability:**

**Why This Fits the Aggressive Path:**
- Direct damage bonus (1d8 cold, or 2d8 if target already wet)
- Rewards aggressive melee combat
- Applies "wet" status for quest progress
- Synergizes with repeated attacks on the same target
- Bonus action means it doesn't compete with Attack action

**Blood Dome Combat:**
1. First strike splits them open → seawater floods in, marking them for the goddess
2. Second strike on the bleeding, soaked victim → ice spreads through their body (2d8 cold)
3. Keep striking until they collapse, drowning in their own blood and brine
4. When they fall wet and bleeding, their death counts for your quest

**Strategic Uses:**
- **Mark for Death**: Brand your victims with the ocean's touch
- **Escalating Brutality**: Each strike on a wet target hurts more than the last
- **Blood Sacrifice**: Every wet kill feeds Moan-a's hunger
- **Efficient Slaughter**: 3 charges means multiple victims per rest

**Compared to Wave Crash (Tactical T1):**
- Tidal Strike: Damage-focused, enhances attacks
- Wave Crash: Control-focused, knocks prone

**Balance:**
- 1d8 cold (~4.5 avg) is modest damage boost
- 2d8 cold (~9 avg) when wet is strong but requires setup
- Bonus action efficient
- 3 charges = can use multiple times per fight
- No save (hits automatically if attack lands)

**Aggressive Playstyle:**
In the Blood Dome, Yyroizgt doesn't just fight - he baptizes his enemies in frozen saltwater and watches them bleed out on the arena floor. Each strike is a dedication to Moan-a, each wet victim another step toward her favor. Simple, brutal, relentless.

## Compliance Notes

**Tier 1 - Aggressive Path**: This ability is properly assigned to Tier 1 (5g) and represents the Aggressive playstyle path, focusing on direct damage output.
