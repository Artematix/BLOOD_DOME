# Character Template

Copy this template when creating a new character.

**File location:** `drafts/characters/{id}.md` → `content/characters/{id}.md`
**ID format:** `char_{name}`

---

```yaml
---
id: char_sharkshooter
name: "The SharkShooter"
status: draft
author: "User"
created: 2026-01-09
modified: 2026-01-09

# Core Identity
class: "Ranger"
role: "damage"

# Base Stats (Level 5)
hp: 45
ac: 15
speed: 30
proficiency_bonus: 3

# Ability Scores
str: 14
dex: 18
con: 14
int: 10
wis: 16
cha: 8

# Saving Throws (list proficient saves)
saving_throws: [str, dex]

# Skills (list proficient skills)
skills: [athletics, perception, stealth, survival, investigation]

# Proficiencies
weapons: [simple, martial]
armor: [light, medium, shields]

# Starting Equipment (item IDs)
# NOTE: Characters have NO starting gear unless explicitly described in character concept
starting_equipment: []

# Starting Abilities (ability IDs)
# NOTE: Do NOT include default D&D class abilities - only custom Blood Dome abilities
starting_abilities: []

# Exclusive Items (only this character can buy/use)
exclusive_items: []

# Character Quests (quest IDs)
# Each character MUST have exactly one level-up quest (quest_{char}_levelup)
# This quest rewards level 6 progression when completed
quests: [quest_sharkshooter_levelup]

# Progression (Level 6+)
# Characters start at Level 5 and can progress to Level 6 via their character quest
# Level 7+ is not currently implemented
progression:
  6:
    # Gained upon completing character-specific level-up quest
    hp_bonus: 8
    abilities: []
    rest_ability: ability_sharkshooter_apex_patience
    # Optional: choice between abilities
    # choice:
    #   type: ability
    #   options: []
  # Note: Levels 7-10 not yet implemented
  # 7:
  #   hp_bonus: 0
  #   abilities: []

# Assets (relative to assets/ folder)
assets:
  portrait: characters/char_sharkshooter/portrait.png
  token: characters/char_sharkshooter/token.png
---

# The SharkShooter

*"The ocean gave me teeth. My father gave me aim. You gave me a target."*

## Description

The SharkShooter is a terrifying fusion of man and monster - a half-shark, half-human demigod born from the unholy union between his father, legendary marksman Captain Marcus "Deadshot" Thorne, and his mother, Moan-a, the Shark Goddess of the Obsidian Sea.

Born from their savage coupling in the crushing depths, SharkShooter inherited his father's supernatural marksmanship and his mother's predatory nature. Standing at an imposing height with shark-gray skin, razor-sharp teeth, and cold, predatory eyes that track movement with supernatural precision, he embodies the perfect synthesis of calculated human strategy and primal aquatic savagery.

His ranger training (learned instinctively from his father's blood) combines with his divine heritage to create an apex predator who hunts with crossbow and instinct in equal measure. Fins protrude from his forearms, his hands end in webbed claws, and a dorsal fin rises from his back. His human intelligence - inherited from Marcus - provides the cold tactical precision his mother lacks, while her ancient predatory wisdom guides his every move.

SharkShooter excels at ranged combat, picking off targets with supernatural accuracy before closing in for the kill when the scent of blood drives him to frenzy. He is patient, calculating, and utterly ruthless - a circling shark waiting for the perfect moment to strike.

Mortal society rejected him. Too much monster. The ocean rejected him. Too much man. The Blood Dome welcomed him with open arms. Here, his dual nature is celebrated, not feared. Here, blood flows freely, and SharkShooter thrives.

His mother watches from the deep. She approves of every kill.

## Special Mechanics

**Divine Heritage:** As the son of a goddess, SharkShooter has resistance to cold damage and can breathe underwater indefinitely. His predatory senses grant him advantage on Wisdom (Perception) checks that rely on smell, and he can detect blood in water from up to 1 mile away.

**Blood Frenzy:** When SharkShooter reduces a creature to half its hit points or less with a ranged attack, he gains advantage on his next melee attack against that creature as his predatory instincts surge.

**Horizon Walker Abilities:** As a Horizon Walker ranger, SharkShooter can use Detect Portal, Planar Warrior, and Ethereal Step as per standard D&D 5e (2024) rules for this subclass at level 5.

## Notes

Design focuses on creating a character who excels at range but has incentives to close into melee when enemies are wounded. The shark/marksman hybrid creates interesting tactical choices between maintaining distance and giving in to predatory bloodlust. His divine heritage as a demigod gives him unique flavor without breaking game balance.

The two sets of abilities represent different combat philosophies:
- **Set 1 (Predatory):** Focused on hunting, tracking, and executing wounded prey
- **Set 2 (Tactical):** Focused on precision shooting, battlefield control, and ranged superiority
```
