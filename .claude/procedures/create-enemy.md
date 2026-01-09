# Procedure: Create Enemy

## When to Use

When creating a new enemy/monster for Blood Dome encounters.

## Prerequisites

- Read `.claude/CONVENTIONS.md` for ID naming rules
- Read `.claude/templates/enemy.md` for the template
- Know the enemy concept and threat level

## ID Format

`enemy_{name}`

Examples:
- `enemy_goblin`
- `enemy_pit_fiend`
- `enemy_skeleton_horde`

## Threat Levels

| Level | Description | HP Range | Use Case |
|-------|-------------|----------|----------|
| minion | Fodder, dies quick | 1-20 | Swarms, trash mobs |
| standard | Normal enemy | 20-60 | Regular encounters |
| elite | Mini-boss | 60-120 | Challenging fights |
| boss | Major encounter | 120+ | Climactic battles |

## Steps

### 1. Generate the ID

Format: `enemy_{name}`

Use underscores for multi-word names: `enemy_fire_elemental`

### 2. Copy the Template

Copy from `.claude/templates/enemy.md`

### 3. Fill Out the Template

Required fields:
```yaml
id: enemy_yourenemy
name: "Display Name"
status: draft
author: "RequesterName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

type: beast|humanoid|undead|fiend|etc
threat_level: minion|standard|elite|boss

hp: 0
ac: 0
```

Fill in:
- Ability scores
- Actions (attacks, special abilities)
- Rewards (coin range)
- Spawn conditions

### 4. Create Asset Folder

Create: `assets/enemies/{id}/`

Add placeholders:
- `assets/enemies/{id}/portrait.placeholder`
- `assets/enemies/{id}/token.placeholder`

### 5. Save the Enemy File

**Draft (default):**
`drafts/enemies/{id}.md`

**Final (if instructed):**
`content/enemies/{id}.md`

### 6. Update the Index

**For drafts:** `drafts/enemies/_index.md`

**For final:** `content/enemies/_index.md`

Example row:
```markdown
| enemy_goblin | Goblin | humanoid | 1/4 | minion | 5-10 | final |
```

### 7. Log in HISTORY.md

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Created
- New enemy: enemy_goblin
- Threat level: minion
- Files: drafts/enemies/enemy_goblin.md
- Assets: assets/enemies/enemy_goblin/ (placeholders)
```

## Checklist

- [ ] ID follows convention: `enemy_{name}`
- [ ] All required YAML fields filled
- [ ] Threat level assigned
- [ ] Actions have attack bonus and damage
- [ ] Coin rewards set (min/max)
- [ ] Asset folder created with placeholders
- [ ] Index file updated
- [ ] HISTORY.md logged

## Balancing Guidelines

### By Threat Level

**Minion**
- HP: 1-20
- AC: 10-13
- Damage: 1d4 to 1d6
- Coins: 1-10

**Standard**
- HP: 20-60
- AC: 12-15
- Damage: 1d8 to 2d6
- Coins: 10-30

**Elite**
- HP: 60-120
- AC: 15-17
- Damage: 2d8 to 3d8
- Coins: 30-75
- Consider: Multi-attack, special abilities

**Boss**
- HP: 120+
- AC: 17+
- Damage: 3d8+
- Coins: 100+
- Consider: Legendary actions, resistances, phases

## Example

Creating a Goblin:

1. **ID**: `enemy_goblin`
2. **Threat**: minion
3. **File**: `drafts/enemies/enemy_goblin.md`
4. **Stats**: HP 7, AC 13, 1d6+2 damage
5. **Coins**: 2-8
6. **Assets**: `assets/enemies/enemy_goblin/`
7. **Index**: Added to `drafts/enemies/_index.md`
8. **Logged**: HISTORY.md updated
