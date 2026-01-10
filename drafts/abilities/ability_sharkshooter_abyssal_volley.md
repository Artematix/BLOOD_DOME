```yaml
---
id: ability_sharkshooter_abyssal_volley
name: "Abyssal Volley"
status: draft
author: "User"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_sharkshooter

# Tier System (for character-exclusive abilities only)
tier: 3
subtype: area_damage

# Shop Information
shop:
  buy: 20
  sell: null

# Requirements
requirements:
  level: null
  abilities: []

# Action Economy
action_type: action

# Resource Cost
resource:
  type: per_day
  amount: 1
  recharge: long_rest

# Targeting
target:
  type: area
  range: 120
  area: "30-foot radius sphere"

# Mechanical Effect (structured)
effect:
  damage: "6d8 piercing + aquatic pressure"
  healing: null
  save: DEX DC 15
  duration: instantaneous
  condition: prone (on failed save)
---

# Abyssal Volley

*The ocean screams. The pressure of ten thousand fathoms erupts. Everything in the killing zone simply... breaks.*

## Effect

You channel the crushing depths of the Obsidian Sea where your mother dwells - where pressure alone can pulverize steel and the darkness devours all light. Choose a point you can see within 150 feet. You fire a shot infused with abyssal power that detonates on impact.

The attack creates a 40-foot-radius sphere of devastating force - a swirling vortex of crushing pressure, freezing deep-sea water, and razor-sharp projectiles that spin like a school of metallic piranha.

**Immediate Devastation:**
Each creature in that area must make a Dexterity saving throw (DC 15):
- **On a failed save:** The creature takes 8d8 piercing damage and 2d8 cold damage, is knocked prone by the supernatural pressure, and has its speed reduced to 0 until the end of its next turn as phantom currents drag at its limbs.
- **On a successful save:** The creature takes half damage and isn't knocked prone, but still has its movement speed reduced by 15 feet until the end of its next turn.

**Lingering Drowning Zone:** The area becomes difficult terrain filled with phantom water for 1 minute. Any creature that starts its turn in this area must succeed on a Constitution saving throw (DC 13) or take 2d6 cold damage and become unable to speak or breathe air until the start of its next turn (as if drowning). The zone smells of blood, brine, and ancient death.

**Execute the Broken:** Any creature reduced to 0 hit points by this ability is violently crushed - their body showing signs of deep-sea pressure trauma (imploded organs, compound fractures, ruptured eyes).

You can use this ability once, and you regain the ability to use it when you finish a long rest.

## Interaction Notes

This is SharkShooter's ultimate tactical devastation - a zone-control nightmare that can wipe out entire groups and deny areas for a full minute. The drowning effect adds psychological horror as enemies choke on phantom water. The larger radius and lingering zone make it superior for battlefield control compared to Feeding Frenzy's direct damage focus. Use this when you want to say "nothing survives in this space."

This is the Tier 3 ultimate for SharkShooter's Tactical set.
```
