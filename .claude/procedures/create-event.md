# Procedure: Create Event

## When to Use

When creating a new map/game event for Blood Dome.

## Prerequisites

- Read `.claude/CONVENTIONS.md` for ID naming rules
- Read `.claude/templates/event.md` for the template
- Know the event type and trigger

## ID Format

`event_{name}`

Examples:
- `event_meteor_shower`
- `event_shop_sale`
- `event_horde_attack`

## Event Types

| Type | Description | Examples |
|------|-------------|----------|
| environmental | Weather, terrain | Acid rain, earthquake |
| shop | Shop changes | Flash sale, new stock |
| spawn | Enemy waves | Horde attack, boss spawn |
| hazard | Dangerous effects | Poison gas, fire zone |
| bonus | Beneficial effects | Healing zone, coin drop |
| story | Narrative moments | Announcements, phase changes |

## Trigger Types

| Trigger | When It Fires |
|---------|---------------|
| timed | Specific round number |
| random | Percentage chance per round |
| threshold | When condition is met |
| manual | DM triggers it |

## Steps

### 1. Generate the ID

Format: `event_{name}`

### 2. Copy the Template

Copy from `.claude/templates/event.md`

### 3. Fill Out the Template

Required fields:
```yaml
id: event_yourevent
name: "Event Name"
status: draft
author: "RequesterName"
created: YYYY-MM-DD
modified: YYYY-MM-DD

type: environmental|shop|spawn|hazard|bonus|story

trigger:
  type: timed|random|threshold|manual
  # Plus trigger-specific fields
```

Fill in:
- Trigger conditions
- Duration
- Effects
- Affected area
- Announcement text

### 4. Save the Event File

**Draft (default):**
`drafts/events/{id}.md`

**Final (if instructed):**
`content/events/{id}.md`

### 5. Update the Index

**For drafts:** `drafts/events/_index.md`

**For final:** `content/events/_index.md`

Example row:
```markdown
| event_meteor_shower | Meteor Shower | hazard | timed (round 5) | 2 rounds | final |
```

### 6. Log in HISTORY.md

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Created
- New event: event_meteor_shower
- Type: hazard
- Trigger: timed (round 5)
- Files: drafts/events/event_meteor_shower.md
```

## Checklist

- [ ] ID follows convention: `event_{name}`
- [ ] Event type specified
- [ ] Trigger fully defined
- [ ] Duration specified
- [ ] Effects are clear and mechanical
- [ ] Affected area defined
- [ ] Announcement text provided
- [ ] Index file updated
- [ ] HISTORY.md logged

## Event Design Guidelines

### Pacing
- Early game (rounds 1-3): Light events, resource spawns
- Mid game (rounds 4-7): Increasing pressure, hazards
- Late game (rounds 8+): High stakes, forcing confrontation

### Balance
- Hazards should be avoidable with skill/resources
- Bonuses shouldn't swing the game too hard
- Spawn events should scale with remaining players

## Examples

### Timed Hazard Event

Creating "Meteor Shower":
- **ID**: `event_meteor_shower`
- **Type**: hazard
- **Trigger**: timed, round 5
- **Duration**: 2 rounds
- **Effect**: Random 10ft radius impacts, 3d6 fire damage, DEX 15 half
- **Area**: Global (random zones)

### Random Bonus Event

Creating "Coin Drop":
- **ID**: `event_coin_drop`
- **Type**: bonus
- **Trigger**: random, 15% per round, earliest round 3
- **Duration**: instant
- **Effect**: 50 coins spawn at random location
- **Area**: Single random zone
