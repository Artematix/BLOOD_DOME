# Procedure: Create Character

## When to Use

When creating a new playable character for Blood Dome.

## Prerequisites

- Read `.claude/CONVENTIONS.md` for ID naming rules
- Read `.claude/templates/character.md` for the template
- Know the character concept (class, role, theme)

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
- **Starting Abilities:** Only custom Blood Dome abilities - NOT default D&D class abilities
- **Level-Up Quest:** Must create a level-up quest with ID `quest_{char}_levelup`
- **Level 6 Progression:** Must define rest_ability in progression.6
- **Do NOT fill out extra data** without checking with the user

Fill in all stats, abilities, equipment references, etc.

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
- [ ] **NO starting equipment** (unless explicitly part of character concept)
- [ ] **NO default D&D abilities** in starting_abilities
- [ ] Level-up quest created (`quest_{char}_levelup`)
- [ ] Rest ability defined in `progression.6.rest_ability`
- [ ] Starting abilities IDs exist (or are being created)
- [ ] **For all abilities:** Asked user for tier and subtype
- [ ] **For all abilities:** Pricing matches tier (1=5g, 2=10g, 3=20g)
- [ ] **Verified:** Only one Tier 3 ability for this character
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
