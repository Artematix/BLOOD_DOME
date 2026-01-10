```yaml
---
id: quest_sharkshooter_levelup
name: "Blood in the Water"
status: draft
author: "User"
created: 2026-01-09
modified: 2026-01-09

# Quest Type
type: character
# character = specific to one character (includes level-up quests)
# universal = anyone can complete
# hidden = not shown until triggered

# Exclusivity
exclusive_to: char_sharkshooter

# Level-Up Quest (character quests only)
is_levelup_quest: true

# Display
show_in_journal: true
show_progress: true

# Requirements to Start
requirements:
  level: 5
  quests_completed: []

# Objectives
objectives:
  - id: obj_1
    description: "Reduce 3 different enemies to half HP or less with ranged attacks"
    type: custom
    target: null
    count: 3
  - id: obj_2
    description: "Finish at least one of those wounded enemies with a melee attack"
    type: kill
    target: null
    count: 1

# Rewards
rewards:
  coins: 100
  items: []
  abilities: []
  level_up: true
  other: "Your mother's blessing flows through you - gain Level 6 and unlock your rest ability"

# Failure Conditions (optional)
failure:
  conditions: []
  consequences: []

# Timing
timing:
  available_from: start
  time_limit: null
---

# Blood in the Water

*"Show me you are both hunter and killer. Wound them from afar, taste their blood up close. Only then will you be worthy of my full blessing." - Moan-a, the Shark Goddess*

## Description

The SharkShooter's mother watches from the depths, testing her son's mastery of both his human precision and his predatory nature. To earn her full divine blessing and ascend to greater power, he must demonstrate that he is truly the apex predator she created - capable of wounding prey with patient marksmanship before closing in for the savage kill.

This quest embodies the SharkShooter's dual nature: the careful aim of his marksman father and the bloodthirsty frenzy of his shark goddess mother.

## Objectives

1. **Wound from Distance:** Reduce 3 different enemies to half their hit points or less using ranged attacks. Show your father's legendary precision.

2. **Finish in Blood:** Kill at least one of those wounded enemies with a melee attack. Give in to the frenzy. Let your mother's hunger guide your jaws and claws.

## Rewards

- **100 gold coins**
- **Level 6 progression** - Gain +8 HP and unlock your rest ability
- **Moan-a's Blessing** - Your mother acknowledges you as a true child of the deep

## Notes

This quest encourages the SharkShooter's hybrid playstyle - start at range, finish in melee when enemies are weakened. It tests the player's ability to balance calculated shooting with opportunistic savagery, perfectly capturing the character's identity as both marksman and monster.
```
