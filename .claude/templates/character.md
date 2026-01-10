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
# NOTE: Characters have NO starting gear unless explicitly described in character concept
starting_equipment: []

# Starting Abilities (ability IDs)
# NOTE: Do NOT include default D&D class abilities - only custom Blood Dome abilities
starting_abilities: []

# Exclusive Items (only this character can buy/use)
exclusive_items: []

# Character Quests (quest IDs)
# Each character MUST have exactly one level-up quest (quest_{char}_levelup)
# This quest rewards level 6 progression when completed
quests: []

# Progression (Level 6+)
# Characters start at Level 5 and can progress to Level 6 via their character quest
# Level 7+ is not currently implemented
progression:
  6:
    # Gained upon completing character-specific level-up quest
    hp_bonus: 0
    abilities: []
    rest_ability: null           # REQUIRED: Ability gained on rest at level 6 (ability ID)
    # Optional: choice between abilities
    # choice:
    #   type: ability
    #   options: []
  # Note: Levels 7-10 not yet implemented
  # 7:
  #   hp_bonus: 0
  #   abilities: []

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
