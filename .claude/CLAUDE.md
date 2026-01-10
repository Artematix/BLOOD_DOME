# Blood Dome - AI Agent Instructions

**READ THIS ENTIRE FILE BEFORE DOING ANYTHING.**

---

## What is Blood Dome?

Blood Dome is a custom PvPvE "battle to the death" game mode for D&D 5e (2024). Players spawn as premade characters (Level 5), collect coins, upgrade via a shop, complete quests, survive events, and fight until one remains. This repository contains all game content: characters, items, abilities, enemies, quests, events, and rules.

---

## Your Role

You are an AI agent helping to build and maintain Blood Dome content. You can:
- **Create** new content (characters, items, abilities, enemies, quests, events)
- **Modify** existing content
- **Delete** content
- **Add ideas** to `drafts/_ideas.md` (user ideas or generate your own)
- **Modify templates** and the system structure itself
- **Answer questions** about the system (read-only, no logging needed)

---

## CORE RULES (NON-NEGOTIABLE)

These rules apply to ALL content changes. No exceptions.

### 1. ALWAYS Log Changes
Every content modification MUST be logged in `.claude/HISTORY.md`.

Format:
```
## [YYYY-MM-DD HH:MM] AuthorName

### Action (Created/Modified/Deleted/Moved)
- Brief description
- Files: list affected files
```

### 2. ALWAYS Update Index Files
When you create, delete, or significantly modify content, update the relevant `_index.md` file.

### 3. ALWAYS Use Templates
Templates are in `.claude/templates/`. Copy and fill them out - don't invent new formats.

### 4. ALWAYS Use Proper IDs
Read `.claude/CONVENTIONS.md` for ID naming rules. Examples:
- Characters: `char_barbarian`
- Weapons: `item_wpn_greataxe`
- Character abilities: `ability_barbarian_rage`

### 5. Drafts vs Final Content
- **Default**: New content goes to `drafts/` folder with `status: draft`
- **Exception**: If explicitly told to create final content, put it directly in `content/` with `status: final`

### 6. Author Attribution
- Use the name of whoever requested the content
- If you're self-initiating, use "AI" as the author

---

## Quick Reference

| Task | Procedure | Key Files |
|------|-----------|-----------|
| Add an idea | See below | `drafts/_ideas.md` |
| Create a character | [create-character.md](procedures/create-character.md) | `drafts/characters/`, `content/characters/_index.md` |
| Create an item | [create-item.md](procedures/create-item.md) | `drafts/items/`, `content/items/{category}/_index.md` |
| Create an ability | [create-ability.md](procedures/create-ability.md) | `drafts/abilities/`, `content/abilities/{type}/_index.md` |
| Create an enemy | [create-enemy.md](procedures/create-enemy.md) | `drafts/enemies/`, `content/enemies/_index.md` |
| Create a quest | [create-quest.md](procedures/create-quest.md) | `drafts/quests/`, `content/quests/_index.md` |
| Create an event | [create-event.md](procedures/create-event.md) | `drafts/events/`, `content/events/_index.md` |
| Modify content | [modify-content.md](procedures/modify-content.md) | Varies |
| Delete content | [delete-content.md](procedures/delete-content.md) | Varies |
| Change system/templates | [modify-system.md](procedures/modify-system.md) | `.claude/`, affected content |

### Adding Ideas

To add an idea to `drafts/_ideas.md`:

1. Open the file
2. Add entry at the TOP (below the `---` line):
   ```markdown
   ## [Category] Idea Name
   Author: RequesterName (or "AI" if self-generated)
   Date: YYYY-MM-DD

   Description of the idea...
   ```
3. Log in HISTORY.md (ideas count as content changes)

Categories: Character, Item, Ability, Enemy, Quest, Event, Rule, System, Other

---

## File Structure Overview

```
BLOOD_DOME/
├── .claude/                    # YOU ARE HERE - Agent instructions
│   ├── CLAUDE.md               # This file
│   ├── CONVENTIONS.md          # ID naming, formatting rules
│   ├── HISTORY.md              # Change log (YOU MUST UPDATE THIS)
│   ├── PROGRESS.md             # What's being worked on
│   ├── procedures/             # Step-by-step guides
│   └── templates/              # Entity templates
│
├── docs/                       # Rules and guides
│   ├── OVERVIEW.md
│   ├── rules/                  # Game rules
│   └── guides/                 # DM and player guides
│
├── drafts/                     # Work-in-progress content
│   ├── _ideas.md               # Brainstorm dump
│   ├── characters/
│   ├── items/
│   ├── abilities/
│   ├── enemies/
│   ├── quests/
│   └── events/
│
├── content/                    # Final, approved content
│   ├── characters/
│   ├── items/
│   │   ├── weapons/
│   │   ├── armor/
│   │   ├── consumables/
│   │   ├── artifacts/
│   │   └── misc/
│   ├── abilities/
│   │   ├── universal/
│   │   └── exclusive/
│   ├── enemies/
│   ├── quests/
│   ├── events/
│   └── shop/
│       └── catalog.md
│
├── assets/                     # Images, tokens, maps
│   ├── characters/{id}/
│   ├── items/
│   ├── enemies/{id}/
│   └── maps/
│
├── CHANGELOG.md                # Version history
└── README.md
```

---

## Documentation Requirements

### HISTORY.md (Required for ALL changes)
Add entry at the TOP of the file, below the `---` line:

```markdown
## [2025-01-09 14:30] YourName

### Created
- New barbarian character
- Files: drafts/characters/char_barbarian.md, drafts/characters/_index.md
```

### CHANGELOG.md (For significant changes)
Update when:
- Adding new content types or categories
- Major system changes
- Version milestones

### Index Files (_index.md)
Every category has an index. Update when adding/removing content.

---

## System Modification Rules

You CAN modify the system itself. When doing so:

### Modifying Templates
1. Update the template in `.claude/templates/`
2. Check if existing content needs updates
3. If yes, update all affected files
4. Document in HISTORY.md AND CHANGELOG.md

### Adding New Categories
1. Create folder structure in both `drafts/` and `content/`
2. Create `_index.md` in each
3. Create template in `.claude/templates/`
4. Add procedure in `.claude/procedures/`
5. Update this file's quick reference table
6. Document in CHANGELOG.md

### Changing Conventions
1. Update `.claude/CONVENTIONS.md`
2. Update all affected content files
3. Document in CHANGELOG.md

---

## Common Mistakes to Avoid

1. **Forgetting HISTORY.md** - Log EVERY change
2. **Wrong ID format** - Check CONVENTIONS.md
3. **Skipping index updates** - Always update `_index.md`
4. **Missing asset placeholders** - Create `.placeholder` files for missing images
5. **Wrong folder** - Drafts go in `drafts/`, final in `content/`
6. **Inventing formats** - Use the templates
7. **Not asking for tier/subtype** - Always ask user for ability tier and subtype
8. **Filling extra data** - Don't fill out extra fields without user confirmation
9. **Missing item requirements** - All items need description, buy price, and sell price
10. **Forgetting level-up quest** - Every character needs a `quest_{char}_levelup`
11. **Wrong tier pricing** - Tier 1=5g, Tier 2=10g, Tier 3=20g
12. **Including D&D defaults** - Don't include default D&D class abilities

---

## When You're Unsure

1. **Check the template** - `.claude/templates/`
2. **Check conventions** - `.claude/CONVENTIONS.md`
3. **Check existing examples** - Look at similar content in `content/`
4. **Ask the user** - When in doubt, ask

---

## Read-Only Mode

If you're just answering questions or exploring (not making changes):
- No need to log anything
- Just read and respond

---

## Getting Started

For your first task:
1. Read the relevant procedure in `.claude/procedures/`
2. Read the template in `.claude/templates/`
3. Check `CONVENTIONS.md` for ID rules and Blood Dome specific rules
4. **For abilities:** Ask user for tier and subtype
5. **For items:** Ensure description, buy, and sell are all filled
6. **For characters:** Create level-up quest and rest ability
7. Create the content
8. Update the index
9. Log in HISTORY.md
10. Done!

## Critical Blood Dome Rules

### Character Rules
- All characters start at **Level 5**
- **NO starting equipment** unless explicitly described
- **NO default D&D abilities** - only custom Blood Dome abilities
- Each character **MUST** have a level-up quest (`quest_{char}_levelup`)
- Level 6 progression **MUST** include a rest ability

### Ability Rules (Character-Exclusive)
- **3 tiers per character**: Low (1), Medium (2), High (3)
- **Pricing**: Tier 1 = 5g, Tier 2 = 10g, Tier 3 = 20g
- **Only ONE Tier 3 ability** per character
- **Always ask user** for tier and subtype before creating
- Universal abilities do NOT use tiers

### Item Rules
- **ALL items MUST have**:
  - Item description (clear and specific)
  - Buy price (in gold)
  - Sell value (in gold, typically 50% of buy)

### Quest Rules
- Each character needs one level-up quest (`quest_{char}_levelup`)
- Level-up quests grant Level 6 progression
