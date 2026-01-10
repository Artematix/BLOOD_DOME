```yaml
---
id: ability_sharkshooter_circling_predator
name: "Circling Predator"
status: draft
author: "User"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_sharkshooter

# Tier System (for character-exclusive abilities only)
tier: 2
subtype: mobility

# Shop Information
shop:
  buy: 10
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
  type: self
  range: self
  area: null

# Mechanical Effect (structured)
effect:
  damage: null
  healing: null
  save: null
  duration: 1 round
  condition: null
---

# Circling Predator

*They smell their own blood. They know death is coming. They just don't know when you'll strike.*

## Effect

As a bonus action, you enter a hunting stance until the end of your next turn. While in this stance:

- Your movement doesn't provoke opportunity attacks
- Your walking speed increases by 20 feet
- You can move through enemy spaces as if they were difficult terrain (creatures get opportunity attacks if you end your turn in their space)
- When you move at least 15 feet straight toward a creature that is bloodied (at half HP or less) before making a ranged weapon attack against it, you gain advantage on the attack roll and deal an extra 2d6 damage on a hit

**Killing Momentum:** If your attack during this stance reduces a creature to 0 hit points, you can immediately move up to 10 feet without provoking opportunity attacks and make one additional ranged weapon attack against another bloodied creature within range.

This ability reflects the relentless, circling hunt of a great white shark - building momentum, striking with devastating force, then moving to the next victim.

You can use this ability 3 times, and you regain all expended uses when you finish a short or long rest.

## Interaction Notes

Best used after wounding enemies with opening shots. Encourages aggressive repositioning and execution chains. The movement bonus and opportunity attack immunity allows SharkShooter to weave through the battlefield, picking off wounded enemies one by one like a shark in a feeding ground.
```
