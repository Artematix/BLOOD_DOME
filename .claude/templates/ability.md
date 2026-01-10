# Ability Template

Copy this template when creating a new ability.

**File location:**
- Universal: `drafts/abilities/{id}.md` → `content/abilities/universal/{id}.md`
- Exclusive: `drafts/abilities/{id}.md` → `content/abilities/exclusive/{id}.md`

**ID formats:**
- Universal: `ability_{name}`
- Character-specific: `ability_{char}_{name}`

---

```yaml
---
id: ability_CHANGEME
name: "Ability Name"
status: draft
author: "YourName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

# Exclusivity
exclusive_to: null               # null = universal, or char ID like "char_barbarian"

# Tier System (for character-exclusive abilities only)
# Character abilities have 3 tiers per character
# Universal abilities do not use tiers
tier: null                       # 1 (low), 2 (medium), or 3 (high) - null for universal abilities
subtype: null                    # Playstyle/ability subtype (e.g., "defensive", "burst_damage", "mobility")

# Shop Information (null if not purchasable)
shop:
  buy: null                      # Price based on tier: Tier 1 = 5g, Tier 2 = 10g, Tier 3 = 20g
  sell: null                     # Abilities typically can't be sold

# Requirements
requirements:
  level: null                    # Minimum character level
  abilities: []                  # Required abilities (prerequisites)
  # other: ""                    # Any other requirements

# Action Economy
action_type: action|bonus_action|reaction|passive|special
# special = has unique activation rules explained in description

# Resource Cost
resource:
  type: null                     # per_rest, per_day, charges, etc.
  amount: null                   # How many uses
  recharge: null                 # How it recharges: short_rest, long_rest, etc.

# Targeting
target:
  type: self|single|multiple|area
  range: null                    # In feet, or "touch", "self"
  area: null                     # If area: "15ft cone", "20ft radius", etc.

# Mechanical Effect (structured)
effect:
  damage: null                   # e.g., "2d6 fire"
  healing: null                  # e.g., "1d8+CON"
  save: null                     # e.g., "DEX 15"
  duration: null                 # e.g., "1 minute", "concentration"
  condition: null                # Conditions applied: prone, frightened, etc.
---

# Ability Name

*Flavor text*

## Effect

Full mechanical description of what this ability does.

## Interaction Notes

How this interacts with other abilities or rules (if relevant).
```

---

## Examples

### Universal Ability (anyone can buy)
```yaml
id: ability_second_wind
exclusive_to: null
shop:
  buy: 75
```

### Character-Specific Ability (Tier 1 - Low)
```yaml
id: ability_barbarian_rage
exclusive_to: char_barbarian
tier: 1
subtype: damage
shop:
  buy: 5  # Tier 1 = 5 gold
```

### Character-Specific Ability (Tier 2 - Medium)
```yaml
id: ability_barbarian_brutal_critical
exclusive_to: char_barbarian
tier: 2
subtype: damage
shop:
  buy: 10  # Tier 2 = 10 gold
```

### Character-Specific Ability (Tier 3 - High)
```yaml
id: ability_barbarian_primal_fury
exclusive_to: char_barbarian
tier: 3
subtype: damage
shop:
  buy: 20  # Tier 3 = 20 gold (only ONE tier 3 per character)
```
