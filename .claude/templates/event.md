# Event Template

Copy this template when creating a new map/game event.

**File location:** `drafts/events/{id}.md` → `content/events/{id}.md`
**ID format:** `event_{name}`

---

```yaml
---
id: event_CHANGEME
name: "Event Name"
status: draft
author: "YourName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

# Event Classification
type: environmental|shop|spawn|hazard|bonus|story
# environmental = weather, terrain changes
# shop = shop-related events (sales, new stock)
# spawn = enemy spawn events
# hazard = dangerous effects
# bonus = beneficial events
# story = narrative beats

# Trigger
trigger:
  type: timed|random|threshold|manual
  # timed = happens at specific round
  # random = chance each round
  # threshold = when condition met (HP, kills, etc.)
  # manual = DM triggered

  # For timed:
  round: null                    # Which round(s)

  # For random:
  chance: null                   # Percentage per round
  earliest: null                 # Don't trigger before this round

  # For threshold:
  condition: ""                  # What triggers it

# Duration
duration:
  type: instant|rounds|until_condition
  value: null                    # Number of rounds, or condition to end

# Effects
effects:
  - type: damage|healing|spawn|terrain|shop|condition|custom
    description: ""
    # Depending on type:
    # damage: "2d6 fire to all players"
    # spawn: [enemy_id, enemy_id]
    # terrain: "Area becomes difficult terrain"
    # condition: "All players frightened for 1 round"

# Affected Area
area:
  type: global|zone|random_zone|targeted
  zones: []                      # If zone-specific

# Announcement
announcement:
  pre_warning: null              # Warning message before event
  warning_rounds: 0              # How many rounds before
  active_message: ""             # Message when event activates
---

# Event Name

*Dramatic description or flavor text*

## Description

What happens during this event, narratively.

## Mechanical Effects

Precise mechanical effects on gameplay.

## DM Notes

How to run this event, timing considerations.
```

---

## Event Types

| Type | Description | Example |
|------|-------------|---------|
| Environmental | Weather, terrain | Acid rain, earthquakes |
| Shop | Shop changes | Flash sale, new legendary item |
| Spawn | Enemy waves | Horde attack, boss spawn |
| Hazard | Dangerous areas | Poison gas, collapsing floor |
| Bonus | Positive effects | Healing zones, coin drops |
| Story | Narrative | NPC announcements, phase changes |

## Trigger Types

| Trigger | When It Fires |
|---------|---------------|
| Timed | Specific round number |
| Random | Percentage chance per round |
| Threshold | When condition met |
| Manual | DM discretion |
