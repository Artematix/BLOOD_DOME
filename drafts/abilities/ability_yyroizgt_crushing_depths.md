---
id: ability_yyroizgt_crushing_depths
name: "Crushing Depths"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_yyroizgt

# Tier (for character-exclusive abilities)
tier: 2                          # Tier 2 (Medium)
subtype: "aggressive"            # Aggressive path - burst damage

# Shop Information (null if not purchasable)
shop:
  buy: 10                        # Tier 2 price
  sell: null

# Requirements
requirements:
  level: null
  abilities: ["ability_yyroizgt_tidal_strike"]

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
  damage: "3d8 bludgeoning"
  healing: null
  save: "CON 14"
  duration: "instantaneous"
  condition: "wet, stunned (on failed save)"
---

# Crushing Depths

*"Your blood is seawater. Your body is my ocean. And I am the tide that drowns you from within."*

## Effect

**Action** - 2 uses per long rest

You reach out and seize control of the water within your victim's body - the blood in their veins, the fluid in their eyes, the moisture in their lungs. With a gesture, you **crush** them from the inside out. Their blood becomes a weapon turned against them, their own body the instrument of their destruction. This is bloodbending - the darkest art of Moan-a's priests.

**Save DC 14 Constitution:**

**On a Failed Save:**
- Takes 3d8 bludgeoning damage as their blood crushes them from within
- **Stunned until the end of your next turn** - their body is no longer their own
- Blood and water pour from their eyes, nose, and mouth (wet status, 1 minute)
- They convulse helplessly as you puppet their fluids like marionette strings

**On a Successful Save:**
- Takes half damage (their will resists, but the pain is excruciating)
- Not stunned, but their blood rebels - they stagger, bleeding internally
- Still drenched in their own fluids (wet status, 1 minute)

**If Already Wet:** Those already soaked have more water for you to control. If they're drenched, you seize both the external water AND their blood - take an additional 1d8 bludgeoning damage (before halving) as you squeeze them like a sponge from inside and out.

## Interaction Notes

**This is Yyroizgt's Tier 2 Aggressive Ability - Bloodbending:**

**Why This Fits the Aggressive Path:**
- High burst damage (3d8 = ~13.5 avg, or 4d8 = ~18 avg if wet)
- Offensive debuff (stunned = total loss of bodily control)
- Touch range = intimate, horrifying execution
- Limited uses (2/long rest) = dark forbidden technique
- Synergizes with wet status for enhanced bloodbending

**The Bloodbending Technique:**
This is **bloodbending** - the ability to control the water inside a living body. Every creature is mostly water - blood, lymph, cerebrospinal fluid, tears. Yyroizgt seizes that water and uses it as a weapon against them. Their blood becomes chains. Their tears become knives. Their body drowns itself.

**Blood Dome Execution Sequence:**
1. Mark them wet with Tidal Strike (bonus action) → external water clings to them
2. Close to touch range → Crushing Depths (action) → seize their blood
3. **Bloodbend them from within** → 4d8 damage as you crush internal organs
4. They collapse, stunned, drowning in their own fluids
5. Next turn: Execute the helpless victim → advantage on attacks as they can't resist

**Why Bloodbending is Lethal:**
- **Total Control**: When stunned, their body is yours - you're puppeting their blood
- **Internal Destruction**: 3d8-4d8 damage comes from INSIDE - crushed organs, burst vessels
- **Guaranteed Wet Status**: They bleed profusely, marking them for death
- **Horrifying**: Watch them convulse as their own body betrays them
- **No Escape**: Even on a successful save, their blood rebels and they're injured

**When to Use Bloodbending:**
- **Execution**: Close on wounded prey and crush their heart from inside
- **Disable Threats**: Stun dangerous enemies so allies can finish them
- **Terror Tactic**: Nothing breaks morale like watching someone's blood turn against them
- **Quest Progress**: Guaranteed wet status + massive damage = easy kills

**The Dark Truth:**
This is forbidden magic in most cultures - controlling another's blood is violation of the deepest kind. But Moan-a doesn't care about morality. In the Blood Dome, you use every weapon at your disposal. And when your victim's blood is 60% seawater... well, that makes it your weapon, doesn't it?

**The Blood Dome Reality:**
Touch range means you have to get close. But when you do, you don't just hurt them - you turn their body into a prison. You make their blood your puppet. You drown them from the inside. This is how a priest of the killing seas executes heretics.

## Compliance Notes

**Tier 2 - Aggressive Path**: This ability is properly assigned to Tier 2 (10g) and represents the Aggressive playstyle path, focusing on burst damage and offensive debuffs.
