# Procedure: Create Character

## When to Use

When creating a new playable character for Blood Dome.

## Prerequisites

- Read `.claude/CONVENTIONS.md` for ID naming rules and character structure
- Read `.claude/templates/character.md` for the template
- Know the character concept (race, class, subclass, role, theme)

## Steps

### 1. Generate the ID

Format: `char_{name}`

Examples:
- `char_barbarian`
- `char_shadow_rogue`
- `char_battle_mage`

### 2. Copy the Template

Copy the template from `.claude/templates/character.md`

### 3. Fill Out the Template

Required fields:
```yaml
id: char_yourcharacter
name: "Display Name"
status: draft           # or 'final' if instructed
author: "RequesterName"
created: YYYY-MM-DD
modified: YYYY-MM-DD
```

**IMPORTANT RULES:**
- **Starting Level:** All characters start at Level 5
- **Starting Equipment:** NO starting gear unless explicitly described in character concept
- **Level-Up Quest:** Must create a level-up quest with ID `quest_{char}_levelup`
- **Level 6 Progression:** Must define rest_ability in progression.6
- **Do NOT fill out extra data** without checking with the user

### 3a. Fill Out the D&D Section (`dnd:`)

This section contains standard D&D 5e (2024) character information:

```yaml
dnd:
  race: "Half-Orc"
  racial_traits:
    - name: "Darkvision"
      description: "See in dim light within 60 feet as bright light."
    - name: "Relentless Endurance"
      description: "Drop to 1 HP instead of 0 once per long rest."
  class: "Barbarian"
  subclass: "Path of the Berserker"
  class_features:
    - name: "Rage"
      description: "..."
      uses: "3/long rest"
    - name: "Reckless Attack"
      description: "..."
    - name: "Extra Attack"
      description: "..."
  feats: []
  spellcasting: null  # Delete or leave null for non-casters
  background: "Gladiator"
```

**Include ALL class features the character has at Level 5.** Reference the D&D 5e (2024) rules for the class.

### 3b. Fill Out the Blood Dome Section (`blood_dome:`)

This section contains custom Blood Dome content:

```yaml
blood_dome:
  starting_equipment: []        # Usually empty
  starting_abilities: []        # Custom abilities they start with (if any)
  purchasable_abilities:
    tier_1: []                  # 5g abilities
    tier_2: []                  # 10g abilities
    tier_3: []                  # 20g ability (ONE max)
  exclusive_items: []           # Items only they can buy
```

**Key distinction:**
- `dnd.class_features` = What they get from D&D (Rage, Sneak Attack, etc.)
- `blood_dome.purchasable_abilities` = Custom abilities they can BUY in Blood Dome

### 4. Create Asset Folder

Create folder: `assets/characters/{id}/`

Add placeholder files for missing images:
- `assets/characters/{id}/portrait.placeholder`
- `assets/characters/{id}/token.placeholder`

### 5. Create Character-Specific Content

#### A. Create Level-Up Quest (REQUIRED)
1. Create quest using the [create-quest.md](create-quest.md) procedure
2. Use ID: `quest_{char}_levelup`
3. Set `is_levelup_quest: true` and `rewards.level_up: true`
4. Reference this quest ID in the character's `quests` field

#### B. Create Starting Abilities (if applicable)
If the character has unique abilities that don't exist yet:
1. Create each ability using the [create-ability.md](create-ability.md) procedure
2. **IMPORTANT:** Ask user for tier (1/2/3) and subtype for each ability
3. Use IDs like `ability_{char}_{ability_name}`
4. Apply tier pricing: Tier 1=5g, Tier 2=10g, Tier 3=20g
5. Reference these IDs in the character file

#### C. Create Rest Ability (REQUIRED for Level 6)
1. Create the rest ability that character gains at level 6
2. Reference its ID in `progression.6.rest_ability`

### 6. Save the Character File

**Draft (default):**
`drafts/characters/{id}.md`

**Final (if instructed):**
`content/characters/{id}.md`

### 7. Update the Index

Add entry to the appropriate index:

**For drafts:** `drafts/characters/_index.md`
```markdown
| char_yourchar | Your Character | Role | draft | AuthorName | Notes |
```

**For final:** `content/characters/_index.md`
```markdown
| char_yourchar | Your Character | Role | final | AuthorName |
```

### 8. Log in HISTORY.md

Add at the TOP of `.claude/HISTORY.md`:

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Created
- New character: char_yourcharacter
- Files: drafts/characters/char_yourcharacter.md
- Assets: assets/characters/char_yourcharacter/ (placeholders)
- Also created abilities: ability_yourchar_ability1, ability_yourchar_ability2
```

## Checklist

- [ ] ID follows convention: `char_{name}`
- [ ] All required YAML fields filled
- [ ] Stats are balanced for Level 5

**D&D Section (`dnd:`):**
- [ ] Race and racial traits filled out
- [ ] Class and subclass specified
- [ ] ALL class features at Level 5 documented in `dnd.class_features`
- [ ] Feats listed (if any)
- [ ] Spellcasting filled out (if caster) or removed (if not)

**Blood Dome Section (`blood_dome:`):**
- [ ] `starting_equipment` is empty (unless explicitly part of character concept)
- [ ] `starting_abilities` contains only custom Blood Dome abilities (NOT D&D features)
- [ ] `purchasable_abilities` organized by tier (tier_1, tier_2, tier_3)
- [ ] **Only ONE tier 3 ability** for this character
- [ ] **For all abilities:** Asked user for tier and subtype
- [ ] **For all abilities:** Pricing matches tier (1=5g, 2=10g, 3=20g)

**Quests & Progression:**
- [ ] Level-up quest created (`quest_{char}_levelup`)
- [ ] Rest ability defined in `progression.6.rest_ability`

**Final Steps:**
- [ ] Asset folder created with placeholders
- [ ] Index file updated
- [ ] HISTORY.md logged

## Example

Creating a Barbarian character:

1. **ID**: `char_barbarian`
2. **File**: `drafts/characters/char_barbarian.md`
3. **Abilities created**:
   - `ability_barbarian_rage`
   - `ability_barbarian_reckless_attack`
4. **Assets**: `assets/characters/char_barbarian/`
5. **Index updated**: Added row to `drafts/characters/_index.md`
6. **Logged**: Entry added to HISTORY.md
