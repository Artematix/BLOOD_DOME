```yaml
---
id: ability_sharkshooter_harpoon_shot
name: "Harpoon Shot"
status: draft
author: "User"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_sharkshooter

# Tier System (for character-exclusive abilities only)
tier: 2
subtype: control

# Shop Information
shop:
  buy: 10
  sell: null

# Requirements
requirements:
  level: null
  abilities: []

# Action Economy
action_type: action

# Resource Cost
resource:
  type: per_rest
  amount: 3
  recharge: short_rest

# Targeting
target:
  type: single
  range: 60
  area: null

# Mechanical Effect (structured)
effect:
  damage: "weapon + 1d6 piercing"
  healing: null
  save: STR DC 14
  duration: until escaped or until you release
  condition: grappled
---

# Harpoon Shot

*The hunted becomes the hunter. Come here.*

## Effect

As an action, make a ranged weapon attack against a Large or smaller creature within 60 feet. On a hit, the attack deals normal weapon damage plus an additional 2d6 piercing damage, and the target becomes harpooned by a barbed bolt that tears deeper with every struggle.

A harpooned creature is grappled by you (escape DC 14) and connected to you by a supernatural tether of crackling energy. While the creature is harpooned:

- You can use a bonus action on your turn to violently pull the creature up to 20 feet closer to you. The creature takes 1d6 piercing damage from the barbs tearing through flesh.
- If the creature tries to move away from you, it must succeed on a Strength saving throw (DC 14) or its movement is reduced to 0 for that turn and it takes 1d6 piercing damage as the harpoon rips deeper.
- If the creature attempts to escape the grapple and fails, it takes 1d8 piercing damage.
- You can release the harpoon at any time (no action required).
- **Reel and Strike:** When you pull a creature to within 5 feet of you using this ability, you can immediately make one melee weapon attack against it as part of the same bonus action.

The harpoon lasts until the creature escapes the grapple, you release it, the creature is reduced to 0 hit points, or you use this ability again. You can harpoon only one creature at a time.

You can use this ability 3 times, and you regain all expended uses when you finish a short or long rest.

## Interaction Notes

This ability turns the battlefield into a nightmare for enemies - get shot, get hooked, get dragged screaming to their death. Every attempt to escape causes more damage. The Reel and Strike feature allows for brutal follow-up melee attacks. Perfect for isolating priority targets and executing them while their allies watch helplessly.
```
