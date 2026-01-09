# Procedure: Create Quest

## When to Use

When creating a new quest (universal or character-specific).

## Prerequisites

- Read `.claude/CONVENTIONS.md` for ID naming rules
- Read `.claude/templates/quest.md` for the template
- Know if it's universal or character-specific

## ID Formats

| Type | Format | Example |
|------|--------|---------|
| Universal | `quest_{name}` | `quest_first_blood` |
| Character-specific | `quest_{char}_{name}` | `quest_barbarian_champion` |

Note: `{char}` is the character name without the `char_` prefix.

## Quest Types

- **universal**: Available to all players
- **character**: Specific to one character
- **hidden**: Not shown until triggered

## Steps

### 1. Determine Type and Generate ID

**Universal:**
`quest_{name}`

**Character-specific:**
`quest_{charname}_{questname}`

### 2. Copy the Template

Copy from `.claude/templates/quest.md`

### 3. Fill Out the Template

Required fields:
```yaml
id: quest_yourquest
name: "Quest Name"
status: draft
author: "RequesterName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

type: universal|character|hidden
exclusive_to: null              # or char_id for character quests
```

Fill in:
- Objectives (what needs to be done)
- Rewards (coins, item IDs, ability IDs)
- Requirements (if any)

### 4. Save the Quest File

**Draft (default):**
`drafts/quests/{id}.md`

**Final (if instructed):**
`content/quests/{id}.md`

### 5. Update the Index

**For drafts:** `drafts/quests/_index.md`

**For final:** `content/quests/_index.md`

Example row:
```markdown
| quest_first_blood | First Blood | universal | - | 50 coins | final |
```

### 6. Link from Character (if character-specific)

If this is a character quest:
1. Open the character file
2. Add the quest ID to the `quests` array:
   ```yaml
   quests:
     - quest_barbarian_champion
   ```

### 7. Log in HISTORY.md

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Created
- New quest: quest_barbarian_champion
- Type: Character-specific (char_barbarian)
- Files: drafts/quests/quest_barbarian_champion.md
- Updated: content/characters/char_barbarian.md (added quest reference)
```

## Checklist

- [ ] ID follows convention (universal vs character)
- [ ] `exclusive_to` set correctly
- [ ] Objectives are clear and measurable
- [ ] Rewards use valid IDs (items, abilities exist or being created)
- [ ] Index file updated
- [ ] Character file updated (if character-specific)
- [ ] HISTORY.md logged

## Reward Guidelines

| Quest Difficulty | Coin Reward | Item Tier |
|-----------------|-------------|-----------|
| Easy | 25-50 | Common |
| Medium | 50-100 | Uncommon |
| Hard | 100-200 | Rare |
| Epic | 200+ | Very Rare+ |

## Examples

### Universal Quest

Creating "First Blood":
- **ID**: `quest_first_blood`
- **Objective**: Be the first player to kill another player
- **Reward**: 100 coins
- **File**: `content/quests/quest_first_blood.md`

### Character Quest

Creating Barbarian's "Champion" quest:
- **ID**: `quest_barbarian_champion`
- **Exclusive to**: `char_barbarian`
- **Objective**: Kill 3 players in melee combat
- **Reward**: 150 coins + `ability_barbarian_brutal_critical`
- **File**: `content/quests/quest_barbarian_champion.md`
- **Also**: Updated `char_barbarian.quests` array
