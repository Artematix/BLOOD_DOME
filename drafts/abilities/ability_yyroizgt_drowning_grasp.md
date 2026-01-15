```yaml
---
id: ability_yyroizgt_drowning_grasp
name: "Drowning Grasp"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_yyroizgt

# Shop Information (null if not purchasable)
shop:
  buy: 200                       # Expensive tier ability
  sell: null

# Requirements
requirements:
  level: 6
  abilities: ["ability_yyroizgt_wave_crash"]

# Action Economy
action_type: action

# Resource Cost
resource:
  type: per_rest
  amount: 2
  recharge: long_rest

# Targeting
target:
  type: single
  range: touch
  area: null

# Mechanical Effect (structured)
effect:
  damage: "3d8 necrotic"
  healing: null
  save: "CON 15"
  duration: "1 minute (concentration)"
  condition: "wet, suffocating"
---

# Drowning Grasp

*"Breathe deep, child. Let Moan-a's embrace fill your lungs..."*

## Effect

**Action** - 2 uses per long rest - Concentration, up to 1 minute

Yyroizgt touches a creature and surrounds their head with suffocating seawater. The target must make a Constitution saving throw (DC 15):

**On a Failed Save:**
- Takes 3d8 necrotic damage immediately
- Begins suffocating (as if drowning)
- Gains "wet" status for the duration
- At the start of each of their turns, they can repeat the save to end the effect

**On a Successful Save:**
- Takes half damage (rounded down)
- Gains "wet" status for 1 minute
- No suffocation effect

**While Suffocating:**
- Target has disadvantage on attack rolls
- Cannot speak or cast spells with verbal components
- Takes 1d6 necrotic damage at the start of each of their turns

## Interaction Notes

**This is Yyroizgt's "Setup" Ability:**
- Guaranteed "wet" status application (even on successful save)
- Creates an urgent threat that forces enemy action/positioning
- Strong control ability that can take a dangerous enemy out of the fight temporarily
- Enables quest completion if Yyroizgt can finish the target while suffocating

**Strategic Uses:**
1. **Quest Enabler**: Applies "wet" then finish with weapon attacks
2. **Caster Shutdown**: Prevents verbal spellcasting
3. **Pressure Tool**: Forces saving throws each turn
4. **Damage Over Time**: Consistent necrotic damage

**Why It's Expensive (200 coins):**
- Strong control effect (suffocation is debilitating)
- Guaranteed "wet" status application
- Good damage (3d8 necrotic = ~13.5 average)
- Multi-turn effect creates sustained pressure
- Requires touch range (risk vs reward)
- Only 2 uses per long rest
- Requires concentration (can be broken)

**Counterplay:**
- Make the CON save each turn to break free
- Break Yyroizgt's concentration (damage him)
- Stay away from Yyroizgt (touch range)
- Allies can help disrupt his concentration

## Balance Considerations

**Compared to similar 200-coin abilities:**
- High impact but limited uses (2/long rest)
- Concentration requirement adds vulnerability
- Touch range requires Yyroizgt to get close (puts him at risk)
- Strong but not auto-win (saves each turn to break free)
```
