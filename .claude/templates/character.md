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

# ==============================================================================
# D&D 5e (2024) BASE - Standard character information
# ==============================================================================
# This section contains all the "vanilla" D&D stuff a Level 5 character has.
# These are NOT purchasable - they're what the character IS.

dnd:
  # Race & Racial Traits
  race: ""                       # e.g., "Human", "Half-Orc", "Tiefling"
  racial_traits:                 # Traits granted by race
    # - name: "Darkvision"
    #   description: "You can see in dim light within 60 feet as if bright light."
    # - name: "Relentless Endurance"
    #   description: "When reduced to 0 HP, drop to 1 HP instead (1/long rest)."

  # Class & Subclass
  class: ""                      # e.g., "Barbarian", "Wizard", "Rogue"
  subclass: ""                   # e.g., "Path of the Berserker", "School of Evocation"

  # Class Features (Level 1-5)
  # List all class/subclass features this character has at Level 5
  class_features:
    # - name: "Rage"
    #   description: "Bonus action to rage. Advantage on STR checks/saves, +2 rage damage, resistance to bludgeoning/piercing/slashing."
    #   uses: "3/long rest"
    # - name: "Reckless Attack"
    #   description: "When you make your first attack on your turn, you can decide to attack recklessly, giving you advantage on melee weapon attack rolls using Strength during this turn, but attack rolls against you have advantage until your next turn."
    # - name: "Extra Attack"
    #   description: "You can attack twice when you take the Attack action."

  # Feats (if any)
  feats:
    # - name: "Great Weapon Master"
    #   description: "-5 to hit for +10 damage; bonus action attack on crit/kill."

  # Spellcasting (delete this section if non-caster)
  spellcasting:
    ability: ""                  # "int", "wis", or "cha"
    spell_save_dc: 0             # 8 + proficiency + ability mod
    spell_attack_bonus: 0        # proficiency + ability mod
    slots:                       # Spell slots at Level 5
      1: 0
      2: 0
      3: 0
    cantrips: []                 # List of cantrip names
    known_spells: []             # For known casters (Bard, Ranger, Sorcerer, Warlock)
    prepared_spells: []          # For prepared casters (Cleric, Druid, Paladin, Wizard)
    spellbook: []                # For Wizards only - all spells in book

  # Background (optional, for flavor)
  background: ""                 # e.g., "Soldier", "Criminal", "Sage"

# ==============================================================================
# CORE STATS - Derived from D&D base
# ==============================================================================

role: ""                         # tank, damage, support, utility, hybrid, etc.

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
tools: []                        # thieves' tools, herbalism kit, etc.
languages: []                    # Common, Dwarvish, etc.

# ==============================================================================
# BLOOD DOME CUSTOM - Our additions on top of D&D
# ==============================================================================
# This section contains Blood Dome-specific content that can be purchased,
# unlocked, or is exclusive to this character.

blood_dome:
  # Starting Equipment (item IDs)
  # NOTE: Characters have NO starting gear unless explicitly described in character concept
  starting_equipment: []

  # Starting Abilities (ability IDs)
  # These are CUSTOM Blood Dome abilities the character starts with (if any)
  # Do NOT put D&D class features here - those go in dnd.class_features
  starting_abilities: []

  # Purchasable Abilities (ability IDs)
  # Abilities this character can buy from the shop (tiered: 5g/10g/20g)
  # Only ONE tier 3 ability allowed per character
  purchasable_abilities:
    tier_1: []                   # 5 gold each
    tier_2: []                   # 10 gold each
    tier_3: []                   # 20 gold (ONE max)

  # Exclusive Items (item IDs)
  # Items only this character can buy/use
  exclusive_items: []

# ==============================================================================
# QUESTS & PROGRESSION
# ==============================================================================

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
    new_class_features: []       # New D&D class features gained at level 6
    new_blood_dome_abilities: [] # New Blood Dome abilities unlocked at level 6
    rest_ability: null           # REQUIRED: Rest ability gained at level 6 (ability ID)
    # Optional: choice between abilities
    # choice:
    #   type: ability
    #   options: []
  # Note: Levels 7-10 not yet implemented
  # 7:
  #   hp_bonus: 0
  #   new_class_features: []
  #   new_blood_dome_abilities: []

# ==============================================================================
# ASSETS
# ==============================================================================

assets:
  portrait: characters/char_CHANGEME/portrait.png
  token: characters/char_CHANGEME/token.png
---

# Character Name

*Tagline or quote here*

## Description

Physical description, personality, background flavor.

## Playstyle

How this character plays in Blood Dome. What strategies work well.

## D&D Features Summary

Quick reference for key D&D features (detailed in YAML above):
- **Race:**
- **Class/Subclass:**
- **Key Features:**

## Blood Dome Abilities

Overview of custom Blood Dome abilities available to this character.

### Tier 1 (5g)
-

### Tier 2 (10g)
-

### Tier 3 (20g)
-

## Notes

Design notes, balance considerations, etc.
```
