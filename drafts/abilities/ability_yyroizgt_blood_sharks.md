---
id: ability_yyroizgt_blood_sharks
name: "Blood Sharks"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Exclusivity
exclusive_to: char_yyroizgt

# Tier (for character-exclusive abilities)
tier: 2                          # Tier 2 (Medium)
subtype: "summoning"             # Alternative Tier 2 option

# Shop Information (null if not purchasable)
shop:
  buy: 10                        # Tier 2 price
  sell: null

# Requirements
requirements:
  level: null
  abilities: []

# Action Economy
action_type: action

# Resource Cost
resource:
  type: per_rest
  amount: 1
  recharge: long_rest

# Targeting
target:
  type: area
  range: special
  area: "Within water terrain"

# Mechanical Effect (structured)
effect:
  damage: "Special (sharks attack)"
  healing: null
  save: null
  duration: "1 minute (concentration)"
  condition: "summoned creatures"
---

# Blood Sharks

*"The children of Moan-a smell blood in the water. They come to feast!"*

## Effect

**Action** - 1 use per short rest

Yyroizgt raises his weapon skyward and calls upon his goddess. The water answers - whether it's a pool, puddle, or even the blood-soaked flood from Deluge, **spectral shark fins** begin cutting through the surface. Moan-a's children have arrived to feed.

**Requirements:**
- Must have at least one area of water terrain on the battlefield (natural water, or created by Deluge)
- Sharks can only move through water areas

**Summons:**
Yyroizgt summons **2 Blood Sharks** that appear in any water terrain within 60 feet. They last for 1 minute (concentration) or until killed.

**Blood Shark Stats:**
- **AC**: 12
- **HP**: 24
- **Speed**: 30 ft. (swim 60 ft.)
- **Attack**: +4 to hit, reach 5 ft., one target. Hit: 2d6+2 (9 avg) piercing damage
- **Blood Frenzy**: Advantage on attack rolls against any creature that doesn't have all its hit points
- **Home-Ocean Advantage**: Sharks do an extra 1d6 piercing damage if target is wet.

**Tactical Use:**
- Sharks act on Yyroizgt's initiative
- He can command them as a bonus action (where to move, who to attack)
- If he doesn't command them, they attack the nearest bleeding enemy
- Sharks can sense wounded enemies (Blood Frenzy triggers automatically)

## Blood Dome Applications

**Combo with Deluge:**
1. Use Moan-a's Deluge → Create 30-foot water zone
2. Summon Blood Sharks in the flooded arena
3. Sharks patrol the blood-water, attacking anyone who enters
4. Yyroizgt fights with advantage (Ocean's Domain) while his sharks harry enemies

**Zone Control:**
- Natural water features become death traps with sharks patrolling
- Enemies must choose: enter water and face sharks + Yyroizgt's advantage, or stay out and give up positioning
- Wounded enemies are especially vulnerable (Blood Frenzy)

**Hunt Wounded Prey:**
- Sharks prioritize injured enemies (advantage vs wounded)
- After you damage someone, sharks swarm them
- Great for finishing fleeing enemies

**Distraction & Pressure:**
- 2 sharks = 2 extra attacks per round
- Forces enemies to split attention
- Creates openings for Yyroizgt to execute wet targets

## Why This Fits Yyroizgt

**Thematic:** Moan-a is goddess of the killing seas - sharks are her sacred hunters, summoned to feed on blood

**Mechanical Synergy:**
- **Deluge Setup**: Deluge creates water → Summon sharks → Control the flood zone
- **Wet Marking**: Sharks help finish wet targets for quest
- **Water Territory**: Makes water areas even more dangerous
- **Blood in Water**: Very Blood Dome - spectral sharks feeding in gore

**Strategic Depth:**
- Alternative to Crushing Depths (Aggressive) or Undertow (Tactical)
- Pure summoning/minion playstyle option
- Requires water terrain (encourages seeking/creating it)

## Balance Considerations

**Strengths:**
- 2 creatures = 2 attacks per round (~18 damage total)
- Blood Frenzy makes them lethal vs wounded enemies
- Creates zone control in water areas
- Lasts 1 minute with concentration

**Weaknesses:**
- **Requires Water**: Useless if no water terrain available
- **Concentration**: Can be broken by taking damage
- **Limited HP**: 22 HP each - can be killed
- **Water-Bound**: Can't leave water, so limited mobility
- **1/Long Rest**: Only get one use
- **Position Dependent**: Need to be near water to summon

**Counterplay:**
- Avoid water terrain
- Break Yyroizgt's concentration
- Kill the sharks (focus fire, 22 HP each)
- Force Yyroizgt to choose between Deluge OR sharks
- Stay at range, kite the water-bound sharks

## Build Path Options

With Blood Sharks as an alternative Tier 2:

**Aggressive Summoner:**
- Tier 1: Tidal Strike (5g)
- Tier 2: Blood Sharks (10g)
- Tier 3: Moan-a's Deluge (20g)
- Style: Damage + minions + ultimate

**Tactical Summoner:**
- Tier 1: Wave Crash (5g)
- Tier 2: Blood Sharks (10g)
- Tier 3: Moan-a's Deluge (20g)
- Style: Control + minions + ultimate

**Mixed Paths:**
- Can replace Crushing Depths or Undertow with Blood Sharks
- Adds summoning dimension to any build

## Flavor & Lore

In the Blood Dome, when Yyroizgt stands in water (especially water mixed with blood), he can call upon Moan-a to send her sacred predators. These aren't normal sharks - they're spectral manifestations of the goddess's hunger, able to swim through ankle-deep water as if it were the open ocean. They appear as ghostly, translucent sharks with blood-red eyes, leaving trails of dark water as they glide across the arena floor.

When the arena floods with Deluge, the blood mixes with seawater, and the sharks go into a feeding frenzy. They circle wounded enemies, lunging from the shallow water to tear flesh and drag victims down. Their presence turns any water terrain into a hunting ground.

**The goddess provides her champion with hunters as deadly as the tide itself.**

## Compliance Notes

**Alternative Tier 2**: This ability is properly priced at 10g and serves as an alternative to Crushing Depths (Aggressive) or Undertow (Tactical), giving players a third option for their Tier 2 choice - a summoning/minion playstyle.
