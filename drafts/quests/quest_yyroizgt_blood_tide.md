```yaml
---
id: quest_yyroizgt_blood_tide
name: "Blood Tide"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Quest Type
type: character

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
    description: "Shed the blood of 2 player characters with the 'wet' status"
    type: kill
    target: "player_with_wet_status"
    count: 2

# Rewards
rewards:
  coins: 150
  items: []
  abilities: []

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

Yyroizgt must kill 2 player characters who have the "wet" status condition. The kill must occur while the target has the status - they cannot be marked wet after death.

**Ways to gain "wet" status:**
- Being submerged in any water terrain feature (pools, streams, flooded areas)
- Being hit by Yyroizgt's water-based abilities (such as water smites)
- Swimming or wading through water
- Being splashed or drenched by water effects

**What counts for the quest:**
- Killing an enemy player who currently has "wet" status
- The "wet" status can come from environmental sources OR Yyroizgt's abilities
- This gives Yyroizgt more control - he can apply "wet" himself via his smites

**What does NOT count:**
- Killing a player then applying "wet" status to their corpse
- Killing a player whose "wet" status expired before death
- Environmental water kills without Yyroizgt's direct involvement in the kill

## Rewards

Upon completing this quest, Yyroizgt receives:
- **150 coins** - Sacred offerings to his goddess
- **Moan-a's Blessing** - Future ability unlock (placeholder for potential exclusive ability)

## Notes

**Design Intent**: This quest gives Yyroizgt agency over his quest completion. Unlike a pure environmental quest, he can actively apply "wet" status through his abilities, making the quest more interactive. It still encourages controlling water features but doesn't make him dependent solely on enemy positioning.

**DM Guidelines**:
- Establish "wet" status rules at game start (duration, how it's tracked, what applies it)
- Mark water terrain clearly on the map
- Yyroizgt's water-based smites should apply "wet" status to targets
- Consider a duration (e.g., "wet" lasts 1 minute after leaving water or being hit by water effects)
- Track "wet" status with visible tokens or markers

**Balance Considerations**:
- Yyroizgt can create opportunities through his own abilities, not just wait for enemies to enter water
- Other players can dry off over time, creating tension around timing
- Water areas still provide strategic value for quest completion
- 2 kills is achievable without requiring perfect enemy cooperation
```
