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

Fill in all stats, abilities, equipment references, etc.

### 4. Create Asset Folder

Create folder: `assets/characters/{id}/`

Add placeholder files for missing images:
- `assets/characters/{id}/portrait.placeholder`
- `assets/characters/{id}/token.placeholder`

### 5. Create Starting Abilities (if new)

If the character has unique abilities that don't exist yet:
1. Create each ability using the [create-ability.md](create-ability.md) procedure
2. Use IDs like `ability_{char}_{ability_name}`
3. Reference these IDs in the character file

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
- [ ] Starting equipment IDs exist (or are being created)
- [ ] Starting abilities IDs exist (or are being created)
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
