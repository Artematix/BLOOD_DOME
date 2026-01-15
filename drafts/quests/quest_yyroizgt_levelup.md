---
id: quest_yyroizgt_levelup
name: "Blood Tide"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Quest Type
type: levelup

# Exclusivity
exclusive_to: char_yyroizgt

# Display
show_in_journal: true
show_progress: true

# Requirements to Start
requirements:
  level: null
  quests_completed: []

# Objectives
objectives:
  - id: obj_1
    description: "Damage 2 player characters with the 'wet' status"
    type: damage
    target: "player_with_wet_status"
    count: 2

# Rewards
rewards:
  level: 6
  coins: 0
  items: []
  abilities: ["ability_yyroizgt_moanas_rest"]

# Failure Conditions (optional)
failure:
  conditions: []
  consequences: []

# Timing
timing:
  available_from: start
  time_limit: null
---

# Blood Tide

*"The waters demand tribute! All who enter Moan-a's domain must pay in blood!"*

## Description

Yyroizgt must prove his devotion to Moan-a, goddess of the seas, by ensuring that those who become touched by her sacred waters pay the ultimate price. Whether submerged in the Blood Dome's water features or drenched by Yyroizgt's divine smites, those who bear the "wet" status are marked for sacrifice to the goddess.

## Objectives

Yyroizgt must damage 2 player characters who have the "wet" status condition. The damage must occur while the target has the status - they cannot be marked wet after being damaged.

**Ways to gain "wet" status:**
- Being submerged in any water terrain feature (pools, streams, flooded areas)
- Being hit by Yyroizgt's water-based abilities (such as water smites)
- Swimming or wading through water
- Being splashed or drenched by water effects

**What counts for the quest:**
- Damaging an enemy player who currently has "wet" status
- The "wet" status can come from environmental sources OR Yyroizgt's abilities
- This gives Yyroizgt more control - he can apply "wet" himself via his smites or Ocean's Domain aura
- Only needs to damage 2 different wet players, not kill them

**What does NOT count:**
- Damaging a player then applying "wet" status afterward
- Damaging a player whose "wet" status expired before the damage landed
- Environmental damage without Yyroizgt's direct involvement

## Rewards

Upon completing this quest, Yyroizgt receives:
- **Level 6 Progression** - Increased hit points and proficiency
- **Ritual of Moan-a** - A unique rest ability that lets you sacrifice corpses to Moan-a to heal and gain predator senses

## Notes

**Design Intent**: This quest gives Yyroizgt agency over his quest completion and makes it much easier to achieve. He only needs to damage (not kill) 2 wet players. With Ocean's Domain providing a 10ft wet aura, he can simply get close to enemies, mark them wet, and hit them once each. This makes the quest achievable early without requiring kills.

**DM Guidelines**:
- Establish "wet" status rules at game start (duration, how it's tracked, what applies it)
- Mark water terrain clearly on the map
- Yyroizgt's water-based smites should apply "wet" status to targets
- Consider a duration (e.g., "wet" lasts 1 minute after leaving water or being hit by water effects)
- Track "wet" status with visible tokens or markers

**Balance Considerations**:
- Very achievable quest - only requires damaging 2 wet players, not killing them
- Ocean's Domain aura makes this trivial: get within 10ft of 2 enemies and hit them once each
- Quest should complete naturally within the first few combat encounters
- No longer requires kills, removing the difficulty of needing to secure final blows on wet targets

## Compliance Notes

**Level-Up Quest**: This quest now properly grants Level 6 progression and includes the required rest ability reward. Complies with Blood Dome conventions.
