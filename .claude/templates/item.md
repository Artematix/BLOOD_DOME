# Item Template

Copy this template when creating a new item.

**File location:** `drafts/items/{id}.md` → `content/items/{category}/{id}.md`

**ID formats:**
- Weapons: `item_wpn_{name}`
- Armor: `item_arm_{name}`
- Consumables: `item_con_{name}`
- Artifacts: `item_art_{name}`
- Misc: `item_msc_{name}`

---

```yaml
---
id: item_TYPE_CHANGEME
name: "Item Name"
status: draft
author: "YourName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

# Item Classification
category: weapon|armor|consumable|artifact|misc
rarity: common|uncommon|rare|very_rare|legendary

# Requirements (who can use this)
requirements:
  # characters: []              # List of char IDs if exclusive (omit if anyone can use)
  # level: 5                    # Minimum level if needed
  # proficiency: martial        # Required proficiency if any

# Shop Information
# REQUIRED: All items MUST have buy and sell values defined
shop:
  buy: 100                       # REQUIRED: Price to purchase (gold)
  sell: 50                       # REQUIRED: Price when selling (gold, typically 50% of buy)

# For WEAPONS
weapon:
  type: ""                       # longsword, greataxe, longbow, etc.
  damage: ""                     # e.g., "1d8 slashing"
  properties: []                 # versatile, two-handed, finesse, reach, etc.
  range: null                    # For ranged: "80/320"
  bonus_attack: 0                # Magic bonus to attack
  bonus_damage: 0                # Magic bonus to damage

# For ARMOR
armor:
  type: ""                       # light, medium, heavy, shield
  base_ac: 0                     # Base AC provided
  dex_mod: true|false|max2       # How dex applies (true=full, false=none, max2=capped)
  stealth_disadvantage: false
  strength_requirement: null     # e.g., 15

# For CONSUMABLES
consumable:
  uses: 1                        # Number of uses before expended
  effect: ""                     # Brief mechanical effect

# Special Properties
properties: []                   # Mechanical effects, special abilities

# Attunement
attunement: false                # Requires attunement?

# Assets
assets:
  image: items/item_TYPE_CHANGEME.png
---

# Item Name

*Flavor text or lore*

## Description

REQUIRED: Physical and mechanical description of the item. Must be clear and specific.

## Effect

Detailed mechanical effect description.

## Lore

Optional backstory or origin.
```

---

## Category Reference

### Weapons
Damage-dealing equipment. Go in `content/items/weapons/`

### Armor
Protective equipment including shields. Go in `content/items/armor/`

### Consumables
Single or limited use items (potions, bombs, scrolls). Go in `content/items/consumables/`

### Artifacts
Powerful unique items, often quest rewards. Go in `content/items/artifacts/`

### Misc
Everything else (tools, utility items). Go in `content/items/misc/`
