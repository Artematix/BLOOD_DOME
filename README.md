# BLOOD DOME

A custom PvPvE "battle to the death" game mode for D&D 5e (2024 Rules).

---

## What is Blood Dome?

Blood Dome is a one-shot arena experience where players compete in a deadly free-for-all:

1. **Spawn** as a premade character (Level 5)
2. **Fight** enemies (PvE) and other players (PvP)
3. **Earn coins** from kills, quests, and events
4. **Upgrade** at the Shop (weapons, abilities, potions)
5. **Survive** until you're the last one standing

---

## Repository Overview

This repository is the master source for all Blood Dome content.

```
BLOOD_DOME/
├── .claude/              # AI agent instructions & templates
│   ├── CLAUDE.md         # START HERE (for AI agents)
│   ├── CONVENTIONS.md    # ID naming rules
│   ├── HISTORY.md        # Change log
│   ├── procedures/       # Step-by-step guides
│   └── templates/        # Entity templates
│
├── docs/                 # Game documentation
│   ├── OVERVIEW.md       # Blood Dome concept
│   ├── rules/            # Game rules
│   └── guides/           # DM and player guides
│
├── drafts/               # Work-in-progress content
│   └── _ideas.md         # Brainstorm dump
│
├── content/              # Final, approved content
│   ├── characters/       # Playable characters
│   ├── items/            # Weapons, armor, consumables, etc.
│   ├── abilities/        # Universal and exclusive abilities
│   ├── enemies/          # Monsters and NPCs
│   ├── quests/           # Objectives
│   ├── events/           # Map/game events
│   └── shop/             # Shop catalog
│
└── assets/               # Images, tokens, maps
```

---

## How to Add Content

### For Humans

1. **Got an idea?** Tell the AI agent, or add it to `drafts/_ideas.md`
2. **Want to create something?** Tell the AI: *"Create a character called X with Y abilities"*
3. **Need changes?** Tell the AI: *"Update the barbarian's HP to 50"*
4. **Want to brainstorm?** Ask the AI: *"Generate some ideas for new consumable items"*

The AI knows the system and will handle templates, indexes, and logging.

### For AI Agents

1. **Read** `.claude/CLAUDE.md` first (mandatory)
2. **Follow** the procedure in `.claude/procedures/`
3. **Use** the template from `.claude/templates/`
4. **Log** your changes in `.claude/HISTORY.md`

---

## Quick Start: Creating a Character

```
1. Pick an ID:           char_warrior
2. Copy template:        .claude/templates/character.md
3. Fill it out:          Name, stats, abilities, equipment
4. Save to:              drafts/characters/char_warrior.md
5. Create asset folder:  assets/characters/char_warrior/
6. Update index:         drafts/characters/_index.md
7. Log change:           .claude/HISTORY.md
```

See [.claude/procedures/create-character.md](.claude/procedures/create-character.md) for full details.

---

## ID Naming Conventions

Everything has a unique ID. Format: `type_name`

| Type | Prefix | Example |
|------|--------|---------|
| Character | `char_` | `char_barbarian` |
| Weapon | `item_wpn_` | `item_wpn_greataxe` |
| Armor | `item_arm_` | `item_arm_chainmail` |
| Consumable | `item_con_` | `item_con_health_potion` |
| Ability | `ability_` | `ability_rage` |
| Character Ability | `ability_{char}_` | `ability_barbarian_rage` |
| Enemy | `enemy_` | `enemy_goblin` |
| Quest | `quest_` | `quest_first_blood` |
| Event | `event_` | `event_meteor_shower` |

Full rules: [.claude/CONVENTIONS.md](.claude/CONVENTIONS.md)

---

## Content Status

All content has a status in its frontmatter:

| Status | Meaning | Location |
|--------|---------|----------|
| `draft` | Work in progress | `drafts/` |
| `review` | Ready for feedback | `drafts/` |
| `final` | Approved, ready to use | `content/` |

---

## Key Files

| File | Purpose |
|------|---------|
| [docs/OVERVIEW.md](docs/OVERVIEW.md) | Blood Dome concept and gameplay loop |
| [docs/rules/_index.md](docs/rules/_index.md) | All game rules |
| [content/characters/_index.md](content/characters/_index.md) | All playable characters |
| [content/shop/catalog.md](content/shop/catalog.md) | Shop prices and inventory |
| [.claude/CLAUDE.md](.claude/CLAUDE.md) | AI agent master instructions |
| [CHANGELOG.md](CHANGELOG.md) | Version history |

---

## Contributing

### Rules

1. **Use templates** - Don't invent new formats
2. **Follow ID conventions** - See [CONVENTIONS.md](.claude/CONVENTIONS.md)
3. **Log all changes** - Update [HISTORY.md](.claude/HISTORY.md)
4. **Update indexes** - Keep `_index.md` files current

### Workflow

```
Idea → Draft → Review → Final
```

- Start in `drafts/`
- When approved, move to `content/`
- Always log in HISTORY.md

---

## For AI Agents

If you're an AI agent working on this repository:

1. **START HERE**: Read [.claude/CLAUDE.md](.claude/CLAUDE.md)
2. This file contains all instructions, rules, and procedures
3. You MUST log all changes to [.claude/HISTORY.md](.claude/HISTORY.md)
4. You CAN modify the system itself (templates, structure) - see [modify-system.md](.claude/procedures/modify-system.md)

---

## License

Private project. Not for distribution.
