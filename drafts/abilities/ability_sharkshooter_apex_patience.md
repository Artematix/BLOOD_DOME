```yaml
---
id: ability_sharkshooter_apex_patience
name: "Apex Predator's Patience"
status: draft
author: "User"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_sharkshooter

# Tier System (for character-exclusive abilities only)
tier: null
subtype: rest_ability

# Shop Information
shop:
  buy: null
  sell: null

# Requirements
requirements:
  level: 6
  abilities: []

# Action Economy
action_type: special

# Resource Cost
resource:
  type: rest_action
  amount: null
  recharge: null

# Targeting
target:
  type: self
  range: self
  area: 1 biome

# Mechanical Effect (structured)
effect:
  damage: null
  healing: null
  save: null
  duration: 10 minutes
  condition: null
---

# Apex Predator's Patience

*The shark knows when prey enters its territory. Always.*

## Effect

This is a rest ability gained at Level 6. When you use your action to rest (forgoing all movement and actions to gain short rest benefits), you enter a terrifying state of predatory awareness while you recover.

While resting in this way, you gain all normal rest benefits (spend hit dice, recover abilities) AND the following additional benefits:

**Territorial Awareness (Passive during rest):**
- You sense the presence of any creature that enters your biome (the current zone/area you're in) while you rest
- You know the approximate number of creatures and their general direction
- You automatically detect any bloodied creatures (at half HP or less) within the same biome, sensing their exact location even through walls and cover
- If a creature approaches within 120 feet of you, you become aware of their exact position

**Ambush Predator (If disturbed):**
If a hostile creature comes within 60 feet of you while you are resting, you can immediately end your rest (no action required) and gain the following benefits for 10 minutes:
- You have advantage on your first attack roll against each creature you detected during your rest
- Your walking speed increases by 20 feet
- Your weapon attacks deal an additional 2d6 damage on the first hit against creatures you detected during your rest
- You regain hit points equal to twice your Wisdom modifier

**Patient Hunter (If undisturbed):**
If you complete your rest without being approached within 60 feet, you gain the following benefits for 10 minutes after your rest ends:
- Your first attack against any creature you detected during your rest deals an additional 4d10 damage
- You have advantage on all attack rolls for the first round of combat against creatures you detected during your rest
- Your movement speed increases by 15 feet
- You gain temporary hit points equal to your Wisdom modifier + your proficiency bonus

The apex predator controls its territory. You know when prey enters your domain, and you're ready for them - whether they come for you or not.

## Interaction Notes

This rest ability gives SharkShooter tactical intelligence across an entire biome while recovering. It's perfect for recovering in contested territory - you'll know if enemies are nearby before they know you're there. The biome-scale awareness makes it practical for the Blood Dome's large battlefields, and the extended duration (10 minutes) on buffs means you can act on the intelligence you've gathered.

This ability is automatically granted upon reaching Level 6 through the character's level-up quest.
```
