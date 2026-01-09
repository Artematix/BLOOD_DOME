# Procedure: Create Ability

## When to Use

When creating a new ability (universal or character-exclusive).

## Prerequisites

- Read `.claude/CONVENTIONS.md` for ID naming rules
- Read `.claude/templates/ability.md` for the template
- Know if it's universal or character-exclusive

## ID Formats

| Type | Format | Example |
|------|--------|---------|
| Universal | `ability_{name}` | `ability_second_wind` |
| Character-exclusive | `ability_{char}_{name}` | `ability_barbarian_rage` |

Note: `{char}` is the character name without the `char_` prefix.

## Steps

### 1. Determine Type and Generate ID

**Universal** (anyone can get):
`ability_{name}`

**Exclusive** (one character only):
`ability_{charname}_{abilityname}`

### 2. Copy the Template

Copy from `.claude/templates/ability.md`

### 3. Fill Out the Template

Required fields:
```yaml
id: ability_yourability
name: "Display Name"
status: draft
author: "RequesterName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

exclusive_to: null                # or char_id like "char_barbarian"

shop:
  buy: 100                        # null if not purchasable
  sell: null                      # abilities usually can't be sold
```

Fill in action type, resource costs, targeting, effects, etc.

### 4. Save the Ability File

**Draft (default):**
`drafts/abilities/{id}.md`

**Final (if instructed):**
- Universal: `content/abilities/universal/{id}.md`
- Exclusive: `content/abilities/exclusive/{id}.md`

### 5. Update the Index

**For drafts:** `drafts/abilities/_index.md`

**For final:**
- Universal: `content/abilities/universal/_index.md`
- Exclusive: `content/abilities/exclusive/_index.md`

Also update `content/abilities/_index.md` summary counts.

Example row:
```markdown
| ability_barbarian_rage | Rage | char_barbarian | null | Yes | final |
```

### 6. Update Shop Catalog (if purchasable)

If `shop.buy` is not null, add to `content/shop/catalog.md`:
- Universal → "Universal Abilities" section
- Exclusive → "Character Abilities" section

### 7. Link from Character (if exclusive)

If this is a character-exclusive ability:
- Add to character's `starting_abilities` if they start with it
- Or note in character's `progression` if gained on level up

### 8. Log in HISTORY.md

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Created
- New ability: ability_barbarian_rage
- Type: Character-exclusive (char_barbarian)
- Files: drafts/abilities/ability_barbarian_rage.md
```

## Checklist

- [ ] ID follows convention (universal vs exclusive)
- [ ] `exclusive_to` set correctly (null or char_id)
- [ ] All required YAML fields filled
- [ ] Action economy specified (action, bonus action, reaction, passive)
- [ ] Shop price set if purchasable
- [ ] Index file(s) updated
- [ ] Shop catalog updated (if purchasable)
- [ ] Character file updated (if exclusive and starting/progression)
- [ ] HISTORY.md logged

## Examples

### Universal Ability

Creating Second Wind:
- **ID**: `ability_second_wind`
- **File**: `content/abilities/universal/ability_second_wind.md`
- **Shop**: buy: 75
- **Exclusive to**: null (anyone can buy)

### Character-Exclusive Ability

Creating Barbarian's Rage:
- **ID**: `ability_barbarian_rage`
- **File**: `content/abilities/exclusive/ability_barbarian_rage.md`
- **Shop**: null (comes with character)
- **Exclusive to**: `char_barbarian`
- **Also**: Added to `char_barbarian.starting_abilities`
