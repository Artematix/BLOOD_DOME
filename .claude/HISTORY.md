# Change History

## MANDATORY: Log ALL Content Changes Here

Every time you create, modify, delete, or move content, add an entry at the TOP of this file (below the `---` line).

**Exception**: Read-only actions (exploring, answering questions) don't need logging.

---

## Format

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### ActionType
- Brief description of what changed
- Files: list of affected files
- Reason: why (optional but helpful)
```

**Action Types:**
- `Created` - New content added
- `Modified` - Existing content changed
- `Deleted` - Content removed
- `Moved` - Content relocated (e.g., draft → final)
- `Modified (System)` - Templates, procedures, structure changed

---

## [2026-01-09 17:25] User

### Modified
- Clarified SharkShooter backstory in character file
- Marcus "Deadshot" Thorne is the FATHER (not SharkShooter himself)
- SharkShooter is the demigod offspring of Marcus and Moan-a
- Inherited marksmanship from father, predatory nature from mother
- Expanded description to clarify family relationships
- Files:
  - drafts/characters/char_sharkshooter.md (expanded description section)

---

## [2026-01-09 17:20] User

### Modified
- Updated Apex Predator's Patience rest ability Patient Hunter path
- Removed initiative/surprise mechanics (not used in Blood Dome)
- Replaced with combat-focused benefits for completing undisturbed rest
- Patient Hunter now grants: 4d10 bonus damage on first attack vs detected creatures, advantage on all attacks first round, +15ft speed, temp HP (WIS+Prof)
- Files:
  - drafts/abilities/ability_sharkshooter_apex_patience.md

---

## [2026-01-09 17:15] User

### Modified
- Balanced SharkShooter abilities between passive and activated
- Updated rest ability for biome-scale awareness (more practical for Blood Dome)
- Ability breakdown: 2 Passive (Tier 1s), 4 Activated (Tier 2s and 3s), 1 Rest ability
- Changes:
  - ability_sharkshooter_scent_of_blood: Confirmed as Passive (always active)
  - ability_sharkshooter_circling_predator: Confirmed as Activated (Bonus Action, 3/short rest)
  - ability_sharkshooter_feeding_frenzy: Confirmed as Activated (Action, 1/long rest)
  - ability_sharkshooter_deadshots_legacy: Confirmed as Passive (always active)
  - ability_sharkshooter_harpoon_shot: Confirmed as Activated (Action, 3/short rest)
  - ability_sharkshooter_abyssal_volley: Confirmed as Activated (Action, 1/long rest)
  - ability_sharkshooter_apex_patience: MAJOR UPDATE - Now provides biome-wide awareness during rest (sense creatures entering biome, detect bloodied in biome, 120ft precise detection), extended buff duration to 10 minutes, increased bonus damage to 4d10 for Patient Hunter path
- Files:
  - drafts/abilities/ability_sharkshooter_apex_patience.md (biome-scale rework)
  - drafts/abilities/_index.md (added Type column showing Passive/Action/Bonus Action/Rest)

---

## [2026-01-09 17:00] User

### Modified
- Made all SharkShooter abilities significantly more brutal for Blood Dome theme
- Replaced rest ability with tactical advantage ability
- Changes:
  - ability_sharkshooter_scent_of_blood: Added bonus damage vs bloodied (1d6) and heavily wounded (1d8) enemies
  - ability_sharkshooter_circling_predator: Increased speed to 20ft, advantage on attacks, 2d6 damage, added kill-chain mechanic
  - ability_sharkshooter_feeding_frenzy: Expanded crit range (18-20), increased damage to 3d10, added 1-minute frenzy state with HP recovery and bite attack
  - ability_sharkshooter_deadshots_legacy: Added total cover penetration, execution shot mechanic (instant kill vs <25% HP on failed save), increased sharpshooter bonus to +12
  - ability_sharkshooter_harpoon_shot: Increased damage to 2d6, added damage on pull (1d6), movement (1d6), and escape attempts (1d8), added Reel and Strike melee follow-up
  - ability_sharkshooter_abyssal_volley: Increased radius to 40ft, range to 150ft, damage to 8d8+2d8 cold, added 1-minute drowning zone with ongoing effects
  - ability_sharkshooter_goddess_blessing → ability_sharkshooter_apex_patience: Completely replaced healing rest with tactical ambush ability (see invisible, detect bloodied, ranged opportunity attacks, ambush trigger, or patient killer buff)
- Files:
  - drafts/abilities/ability_sharkshooter_scent_of_blood.md
  - drafts/abilities/ability_sharkshooter_circling_predator.md
  - drafts/abilities/ability_sharkshooter_feeding_frenzy.md
  - drafts/abilities/ability_sharkshooter_deadshots_legacy.md
  - drafts/abilities/ability_sharkshooter_harpoon_shot.md
  - drafts/abilities/ability_sharkshooter_abyssal_volley.md
  - drafts/abilities/ability_sharkshooter_apex_patience.md (renamed from goddess_blessing)
  - drafts/characters/char_sharkshooter.md (updated rest_ability reference)
  - drafts/abilities/_index.md (updated ability name)

---

## [2026-01-09 16:30] User

### Created
- New character: The SharkShooter (char_sharkshooter)
- Half-shark demigod ranger, son of Moan-a the Shark Goddess
- Level-up quest: Blood in the Water (quest_sharkshooter_levelup)
- 7 character-exclusive abilities:
  - Predatory Set: Scent of Blood (T1), Circling Predator (T2), Feeding Frenzy (T3)
  - Tactical Set: Deadshot's Legacy (T1), Harpoon Shot (T2), Abyssal Volley (T3)
  - Rest Ability: Goddess's Blessing (Level 6)
- Files:
  - drafts/characters/char_sharkshooter.md
  - drafts/quests/quest_sharkshooter_levelup.md
  - drafts/abilities/ability_sharkshooter_scent_of_blood.md
  - drafts/abilities/ability_sharkshooter_circling_predator.md
  - drafts/abilities/ability_sharkshooter_feeding_frenzy.md
  - drafts/abilities/ability_sharkshooter_deadshots_legacy.md
  - drafts/abilities/ability_sharkshooter_harpoon_shot.md
  - drafts/abilities/ability_sharkshooter_abyssal_volley.md
  - drafts/abilities/ability_sharkshooter_goddess_blessing.md
  - drafts/characters/_index.md (updated)
  - drafts/abilities/_index.md (updated)
  - drafts/quests/_index.md (updated)
  - assets/characters/char_sharkshooter/ (placeholders created)
- Notes: Character has TWO Tier 3 abilities (one per set). Player/DM may choose only one for balance per Blood Dome conventions.

---

## [2026-01-09 15:00] User

### Modified
- Completed resting rules documentation (no short/long rests, rest action, spell slot recovery, long rest feature recovery)
- Completed economy rules documentation (gold earning, marketplace, Amith shrines, Amith boons)
- Added item pricing guidelines and enemy gold drop rules
- Updated rules index to reflect completed rules
- Files:
  - docs/rules/resting.md (fully documented)
  - docs/rules/economy.md (fully documented with Amith boons)
  - docs/rules/_index.md (updated status)
  - .claude/CONVENTIONS.md (added pricing guidelines, enemy rules, resting rules)

---

## [2026-01-09 14:45] User

### Modified (System)
- Updated system structure with new Blood Dome game rules
- Added ability tier system (Low/Medium/High) with pricing (5g/10g/20g)
- Added character level-up quest requirements
- Added rest ability requirement for level 6
- Added mandatory item fields (description, buy, sell)
- Removed starting equipment as default (now opt-in only)
- Specified no default D&D abilities in character builds
- Files:
  - .claude/templates/ability.md (tier system, pricing)
  - .claude/templates/character.md (level-up quest, rest ability, no starting gear)
  - .claude/templates/item.md (required description, buy, sell)
  - .claude/templates/quest.md (level-up quest fields)
  - .claude/CONVENTIONS.md (Blood Dome Specific Rules section)
  - .claude/procedures/create-ability.md (tier/subtype workflow)
  - .claude/procedures/create-character.md (level-up quest, rest ability)
  - .claude/procedures/create-item.md (required fields)
  - .claude/CLAUDE.md (Critical Blood Dome Rules section)

---

## [2025-01-09 13:00] AI

### Modified
- README.md: Changed "For Humans" section to explain how to use AI agents
- CLAUDE.md: Added "Add ideas" to agent capabilities and quick reference
- drafts/_ideas.md: Added categories list and AI author option
- Files: README.md, .claude/CLAUDE.md, drafts/_ideas.md

---

## [2025-01-09 12:30] AI

### Modified
- Expanded README.md with comprehensive overview
- Added: how-to guide, ID conventions table, quick start, key files reference
- Files: README.md

---

## [2025-01-09 12:00] AI

### Created (System)
- AI Agent instruction system
- Files:
  - .claude/CLAUDE.md (master instructions)
  - .claude/procedures/create-character.md
  - .claude/procedures/create-item.md
  - .claude/procedures/create-ability.md
  - .claude/procedures/create-enemy.md
  - .claude/procedures/create-quest.md
  - .claude/procedures/create-event.md
  - .claude/procedures/modify-content.md
  - .claude/procedures/delete-content.md
  - .claude/procedures/modify-system.md
  - .claude/HISTORY.md (updated format)

---

## [2025-01-09 00:00] System

### Created
- Initial repository structure
- All template files
- Convention documentation
- Index files for all categories
- docs/OVERVIEW.md
- docs/rules/ stub files
- docs/guides/ stub files

---

<!--
████████████████████████████████████████████████████████████
██  ADD NEW ENTRIES ABOVE THIS LINE                       ██
██  Newest entries go at the TOP, just below the --- line ██
████████████████████████████████████████████████████████████
-->
