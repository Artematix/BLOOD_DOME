# Enemy Template

Copy this template when creating a new enemy.

**File location:** `drafts/enemies/{id}.md` → `content/enemies/{id}.md`
**ID format:** `enemy_{name}`

---

```yaml
---
id: enemy_CHANGEME
name: "Enemy Name"
status: draft
author: "YourName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

# Classification
type: ""                         # beast, humanoid, undead, fiend, etc.
size: medium                     # tiny, small, medium, large, huge, gargantuan
alignment: ""                    # chaotic evil, neutral, etc.

# Difficulty
challenge_rating: 1              # CR for reference
threat_level: minion|standard|elite|boss
# minion = fodder, dies quick
# standard = normal enemy
# elite = mini-boss tier
# boss = major encounter

# Base Stats
hp: 0
ac: 0
speed: 30

# Ability Scores
str: 10
dex: 10
con: 10
int: 10
wis: 10
cha: 10

# Defenses
saving_throws: []                # e.g., [dex +5, wis +3]
damage_resistances: []
damage_immunities: []
condition_immunities: []

# Senses
senses:
  passive_perception: 10
  darkvision: null               # Range in feet
  # other senses as needed

# Abilities (ability IDs or inline)
abilities: []

# Actions
actions:
  - name: "Attack Name"
    type: melee|ranged|special
    attack_bonus: 0
    damage: ""                   # e.g., "1d8+3 slashing"
    range: 5                     # Reach or range
    description: ""

# Bonus Actions (if any)
bonus_actions: []

# Reactions (if any)
reactions: []

# Legendary Actions (for bosses)
legendary_actions: null
# legendary_actions:
#   points: 3
#   actions:
#     - name: ""
#       cost: 1
#       description: ""

# Rewards
rewards:
  coins:
    min: 0
    max: 0
  # items: []                    # Item IDs if any guaranteed drops

# Spawn Conditions
spawn:
  locations: []                  # Where this enemy appears
  frequency: common|uncommon|rare
  group_size:
    min: 1
    max: 1

# Assets
assets:
  portrait: enemies/enemy_CHANGEME/portrait.png
  token: enemies/enemy_CHANGEME/token.png
---

# Enemy Name

*Flavor description*

## Description

Physical appearance and behavior.

## Tactics

How this enemy fights (for DM reference).

## Encounter Notes

Suggested encounter setups, synergies with other enemies.
```

---

## Threat Levels

| Level | Description | HP Range | Damage Output |
|-------|-------------|----------|---------------|
| Minion | Fodder, dies in 1-2 hits | 1-20 | Low |
| Standard | Normal enemy | 20-60 | Moderate |
| Elite | Mini-boss, needs focus | 60-120 | High |
| Boss | Major encounter | 120+ | Very High |
