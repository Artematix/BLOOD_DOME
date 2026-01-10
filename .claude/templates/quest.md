# Quest Template

Copy this template when creating a new quest.

**File location:** `drafts/quests/{id}.md` → `content/quests/{id}.md`

**ID formats:**
- Universal: `quest_{name}`
- Character-specific: `quest_{char}_{name}`

---

```yaml
---
id: quest_CHANGEME
name: "Quest Name"
status: draft
author: "YourName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

# Quest Type
type: character|universal|hidden
# character = specific to one character (includes level-up quests)
# universal = anyone can complete
# hidden = not shown until triggered

# Exclusivity
exclusive_to: null               # null = universal, or char ID

# Level-Up Quest (character quests only)
is_levelup_quest: false          # true if this quest grants level 6 progression

# Display
show_in_journal: true            # Whether players see this quest
show_progress: true              # Show objective progress

# Requirements to Start
requirements:
  level: null
  quests_completed: []           # Quest IDs that must be done first
  # other: ""

# Objectives
objectives:
  - id: obj_1
    description: "What to do"
    type: kill|collect|reach|interact|survive|custom
    target: null                 # enemy ID, item ID, location, etc.
    count: 1                     # How many needed
    # hidden: false              # Hide this objective until triggered

# Rewards
rewards:
  coins: 0
  items: []                      # Item IDs
  abilities: []                  # Ability IDs
  level_up: false                # true if this quest grants level 6 (for level-up quests only)
  # other: ""                    # Custom rewards

# Failure Conditions (optional)
failure:
  conditions: []                 # What causes failure
  consequences: []               # What happens on failure

# Timing
timing:
  available_from: start          # When quest becomes available: start, level_X, after_quest_Y
  time_limit: null               # Rounds/minutes if timed
---

# Quest Name

*Quest giver quote or flavor text*

## Description

What the quest is about, narrative context.

## Objectives

Detailed breakdown of what needs to be done.

## Rewards

What the player gets upon completion.

## Notes

Design notes, balance considerations, story connections.
```

---

## Quest Types

### Character Quests
Personal objectives for specific characters. These define part of a character's identity and progression.

**IMPORTANT:** Each character MUST have exactly one level-up quest with ID format `quest_{char}_levelup`
This quest rewards the character with level 6 progression when completed.

Example: `quest_barbarian_levelup` - Kill 3 players in melee combat to reach level 6

### Universal Quests
Available to all players. Often competitive.

Example: `quest_first_blood` - Be the first to kill another player

### Hidden Quests
Not shown until triggered. Can be secret achievements or event-based.

Example: `quest_survivor` - Survive for 10 rounds without taking damage
