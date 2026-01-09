# Character Template

Copy this template when creating a new character.

**File location:** `drafts/characters/{id}.md` → `content/characters/{id}.md`
**ID format:** `char_{name}`

---

```yaml
---
id: char_CHANGEME
name: "Character Name"
status: draft
author: "YourName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

# Core Identity
class: ""                        # Base D&D class for reference
role: ""                         # tank, damage, support, utility, etc.

# Base Stats (Level 5)
hp: 0
ac: 0
speed: 30
proficiency_bonus: 3             # +3 at level 5

# Ability Scores
str: 10
dex: 10
con: 10
int: 10
wis: 10
cha: 10

# Saving Throws (list proficient saves)
saving_throws: []

# Skills (list proficient skills)
skills: []

# Proficiencies
weapons: []                      # simple, martial, specific weapons
armor: []                        # light, medium, heavy, shields

# Starting Equipment (item IDs)
starting_equipment: []

# Starting Abilities (ability IDs)
starting_abilities: []

# Exclusive Items (only this character can buy/use)
exclusive_items: []

# Character Quests (quest IDs)
quests: []

# Progression (Level 6+)
# What they gain when leveling up
progression:
  6:
    hp_bonus: 0
    abilities: []
    # Optional: choice between abilities
    # choice:
    #   type: ability
    #   options: []
  7:
    hp_bonus: 0
    abilities: []
  8:
    hp_bonus: 0
    abilities: []
  9:
    hp_bonus: 0
    abilities: []
  10:
    hp_bonus: 0
    abilities: []

# Assets (relative to assets/ folder)
assets:
  portrait: characters/char_CHANGEME/portrait.png
  token: characters/char_CHANGEME/token.png
---

# Character Name

*Tagline or quote here*

## Description

Physical description, personality, background flavor.

## Special Mechanics

Any unique rules or mechanics specific to this character.

## Notes

Design notes, balance considerations, etc.
```
