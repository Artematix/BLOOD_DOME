```yaml
---
id: ability_sharkshooter_feeding_frenzy
name: "Feeding Frenzy"
status: draft
author: "User"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_sharkshooter

# Tier System (for character-exclusive abilities only)
tier: 3
subtype: burst_damage

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
  type: multiple
  range: 60
  area: null

# Mechanical Effect (structured)
effect:
  damage: "varies"
  healing: null
  save: null
  duration: instantaneous
  condition: null
---

# Feeding Frenzy

*Blood. Everywhere. The water churns red. Your mother screams from the deep: FEED.*

## Effect

When you use this ability, your predatory instincts consume all reason. Your eyes roll back, your teeth sharpen, and you become pure hunger.

Choose up to three creatures you can see within 60 feet that are bloodied (at half HP or less). You immediately make one ranged weapon attack against each chosen creature. These attacks are made with advantage and score a critical hit on a roll of 18-20. On a hit, you deal an additional 3d10 damage.

**The Frenzy Continues:** After making these attacks, if you reduced at least one creature to 0 hit points, you gain the following benefits for 1 minute:
- Your movement speed increases by 15 feet
- You have advantage on all attack rolls against bloodied creatures
- When you reduce a creature to 0 hit points, you regain hit points equal to your Wisdom modifier + your proficiency bonus

Additionally, after the initial attacks, you can immediately move up to your speed toward any bloodied creature without provoking opportunity attacks. If you end this movement within 5 feet of a bloodied creature, you can make one melee weapon attack against it with advantage. On a hit, you can choose to bite the target, dealing an additional 2d8 piercing damage and gaining temporary hit points equal to half the damage dealt.

The goddess's hunger flows through you - primal, unstoppable, devastating. You are the Endless Maw.

You can use this ability once, and you regain the ability to use it when you finish a long rest.

## Interaction Notes

This is SharkShooter's ultimate predatory ability - a devastating burst that can snowball into a rampage if you secure kills. The critical hit range expansion makes it incredibly lethal, and the ongoing frenzy benefits reward aggressive play. Best used when multiple enemies are bloodied to maximize carnage. This is what happens when a demigod stops pretending to be civilized.

This is the Tier 3 ultimate for SharkShooter's Predatory set.
```
