# Change History

## MANDATORY: Log ALL Content Changes Here

Every time you create, modify, delete, or move content, add an entry at the TOP of this file (below the `---` line).

**Exception**: Read-only actions (exploring, answering questions) don't need logging.

---

## [2026-01-09 19:45] AI

### Created
- Created Moan-a's Fang weapon per user request
- Trident containing the spirit of a shark demigod
- Priced at 5 gold (affordable early weapon)
- Character-exclusive to Yyroizgt
- Special properties:
  - Shark Spirit: Apply wet status on hit (once per turn, no action required)
  - Predator's Hunger: Gain temp HP equal to CHA mod when killing with weapon
- Versatile weapon (1d6/1d8), throwable (20/60 range)
- Files:
  - drafts/items/item_wpn_moanas_fang.md (created)
  - drafts/items/_index.md (updated)
  - assets/items/item_wpn_moanas_fang.placeholder (created)

**Result**: Yyroizgt now has a signature weapon that synergizes perfectly with his wet-based mechanics and provides sustain through temp HP on kills. The weapon embodies the shark spirit theme from his rest ability.

---

## [2026-01-09 19:30] AI

### Deleted
- Removed Undertow ability per user request
- Updated character file to reflect removal of Tactical path
- Now only 2 Tier 2 options: Crushing Depths (Bloodbending/Aggressive) and Blood Sharks (Summoner)
- Updated build recommendations to show 2 paths instead of 3
- Files:
  - drafts/abilities/ability_yyroizgt_undertow.md (deleted)
  - drafts/abilities/_index.md (removed Undertow entry, updated Crushing Depths description)
  - drafts/characters/char_yyroizgt.md (removed from exclusive_items, ability paths, build recommendations, compliance notes)

**Result**: Character now has simplified tier structure with only Bloodbending and Summoner playstyles at Tier 2. Tactical path (Undertow) removed entirely.

---

## [2026-01-09 19:15] AI

### Modified
- Redesigned Crushing Depths as a bloodbending ability per user request
- Changed flavor from pressure-based crushing to controlling water/blood inside the victim's body
- Updated all flavor text to emphasize bloodbending mechanics:
  - Yyroizgt seizes control of the water in the target's blood, organs, and fluids
  - Victim's body becomes a weapon against them as their blood is puppeted
  - Described as forbidden dark magic - controlling another's blood
  - Enhanced with wet status: external water + internal blood both controlled
- Kept same mechanics (3d8 damage, stun on failed save, +1d8 if wet)
- Files:
  - drafts/abilities/ability_yyroizgt_crushing_depths.md (rewrote flavor text, interaction notes)

**Result**: Crushing Depths now feels like dark bloodbending magic - seizing control of the victim's blood and crushing them from within. Much more visceral and fitting for a brutal water-controlling paladin.

---

## [2026-01-09 19:00] AI

### Modified
- Changed Blood Tide quest objective from "kill 2 wet players" to "damage 2 wet players" per user request
- Updated quest type from "kill" to "damage"
- Revised all quest text to reflect damage requirement instead of kill requirement
- Updated Design Intent and Balance Considerations to note quest is now much easier to complete
- Files:
  - drafts/quests/quest_yyroizgt_levelup.md (updated objectives, description, notes)

**Result**: Quest is now significantly easier - Yyroizgt only needs to damage 2 wet players (not kill them). With Ocean's Domain's 10ft wet aura, he can complete this by simply getting close to 2 enemies and hitting them once each.

---

## [2026-01-09 18:45] AI

### Modified
- Renamed rest ability from "Feeding Frenzy" to "Ritual of Moan-a" per user request
- Updated name in ability file YAML frontmatter
- Updated all references to the ability across related files
- Files:
  - drafts/abilities/ability_yyroizgt_moanas_rest.md (changed name field)
  - drafts/abilities/_index.md (updated ability name and description)
  - drafts/characters/char_yyroizgt.md (updated rest ability reference)
  - drafts/quests/quest_yyroizgt_levelup.md (updated reward description)

**Result**: Rest ability now has the final name "Ritual of Moan-a" which better emphasizes the sacred nature of the sacrificial act and direct connection to the goddess.

---

## [2026-01-09 18:30] AI

### Modified
- Redesigned Feeding Frenzy to emphasize sacrificial rituals and the trident as a living shark weapon
- Changed flavor from generic feeding to sacred sacrifice:
  - Player drives trident through corpses to offer them to Moan-a
  - Trident prongs are "shark teeth" - weapon is the physical manifestation of the goddess's hunger
  - Seawater erupts from sacrificed corpses and flows into Yyroizgt (healing)
  - Trident "awakens" after feeding - gains predator senses and pulls toward wounded prey
- Updated character description to introduce the sacred trident
- Emphasized the arena as Moan-a's temple and combat as religious ritual
- Files:
  - drafts/abilities/ability_yyroizgt_moanas_rest.md (rewrote flavor text and mechanics description)
  - drafts/characters/char_yyroizgt.md (added trident description to character intro)

**Result**: Rest ability now feels like a dark religious ritual - impaling corpses with a sacred weapon that is also a living shark, feeding the goddess through sacrifice, and being blessed with healing and predator senses. Very fitting for a brutal shark deity.

---

## [2026-01-09 18:15] AI

### Modified
- Completely redesigned rest ability from "Moan-a's Rest" to "Feeding Frenzy" to fit shark goddess theme
- Changed from gentle healing + water manipulation to predatory feeding on corpses
- New mechanics:
  - Heal 1d8 per nearby corpse (max 4d8) + CHA modifier
  - Scales with kills - more corpses = more healing
  - Grants "Blood Scent" for 1 minute: sense wounded prey within 60ft, +10 speed toward them
  - Predator tracking: advantage on Perception, can sense direction/distance of enemies below half HP
- Thematically fits a brutal shark goddess who feeds on the weak
- Perfect for Blood Dome death match where corpses pile up
- Files:
  - drafts/abilities/ability_yyroizgt_moanas_rest.md (renamed to Feeding Frenzy, completely rewritten)
  - drafts/characters/char_yyroizgt.md (updated rest ability reference)
  - drafts/abilities/_index.md (updated ability name and description)
  - drafts/quests/quest_yyroizgt_levelup.md (updated reward description)

**Result**: Rest ability now embodies a shark goddess - feed on the dead to heal, gain predator senses to hunt wounded prey. Very Blood Dome, very brutal, rewards aggressive play.

---

## [2026-01-09 18:00] AI

### Modified
- Renamed "Wave Crash" to "Ocean's Domain" and completely redesigned the ability
- Changed from simple advantage passive to dual-function aura ability:
  - 10-foot radius wet aura that automatically applies wet status to enemies
  - Advantage on all attacks against wet targets (retained from previous version)
- File renamed: ability_yyroizgt_wave_crash.md → ability_yyroizgt_oceans_domain.md
- ID changed: ability_yyroizgt_wave_crash → ability_yyroizgt_oceans_domain
- Updated all references in character file and ability index
- Files:
  - drafts/abilities/ability_yyroizgt_oceans_domain.md (renamed and rewritten)
  - drafts/characters/char_yyroizgt.md (updated references, special mechanics, build notes)
  - drafts/abilities/_index.md (updated ability ID and description)

**Result**: Ocean's Domain now makes Yyroizgt a walking wet zone - anyone who gets within 10 feet is automatically soaked and marked for death. Combined with advantage on wet targets, this makes him devastating in melee combat. The ocean literally follows him wherever he walks.

---

## [2026-01-09 17:45] AI

### Modified
- Enhanced Moan-a's Rest to be a true divine boon from the ocean goddess instead of basic healing
- Added water breathing for 10 minutes (can fight/hide underwater)
- Added ability to summon 5-foot pool of seawater if no water exists (lasts 10 minutes)
- Summoned water can be used for Ocean's Domain, Blood Sharks spawning, and resting
- Enhanced version in water grants advantage on next attack roll in addition to increased healing
- Emphasizes Moan-a's control over water, sea creatures, and her champion's connection to her domain
- Files:
  - drafts/abilities/ability_yyroizgt_moanas_rest.md (completely rewritten with divine boon theme)

**Result**: Rest ability now feels like genuine divine favor from a goddess who commands the seas, granting water manipulation and breathing alongside healing. Creates strategic options for water control and underwater combat.

---

## [2026-01-09 17:30] AI

### Modified
- Converted Wave Crash from active Tier 1 ability to passive starting ability for Yyroizgt
- Wave Crash now grants permanent advantage on all attacks against wet targets (no action required, no resource cost)
- Removed Wave Crash from purchasable abilities (exclusive_items) and added to starting_abilities
- Updated Yyroizgt's tier structure: now has only 1 Tier 1 option (Tidal Strike), 3 Tier 2 options, 1 Tier 3 option
- Updated character special mechanics section to list Wave Crash as core passive feature
- Simplified build paths - all builds start with Wave Crash passive + Tidal Strike, then choose Tier 2 specialization
- Files:
  - drafts/abilities/ability_yyroizgt_wave_crash.md (converted to passive, completely rewritten)
  - drafts/characters/char_yyroizgt.md (updated starting_abilities, exclusive_items, special mechanics, ability paths, build recommendations, compliance notes)
  - drafts/abilities/_index.md (updated to reflect Wave Crash as starting passive)

**Result**: Wave Crash is now a core part of Yyroizgt's identity rather than an optional purchase, emphasizing his role as a hunter of water-marked prey. All builds benefit from the advantage-on-wet mechanic, making wet status application the key to his playstyle.

---

## [2026-01-09 17:15] AI

### Created
- Added Blood Sharks ability - Tier 2 Summoner option for Yyroizgt
- Summons 2 spectral sharks in water terrain to hunt and kill
- Provides third distinct playstyle path alongside Aggressive and Tactical
- Synergizes with Deluge (creates water for sharks) and wet mechanic (sharks hunt wounded)
- Files:
  - drafts/abilities/ability_yyroizgt_blood_sharks.md (created)
  - drafts/characters/char_yyroizgt.md (updated with 3rd path, 6 build options)
  - drafts/abilities/_index.md (updated)

**Result**: Yyroizgt now has 6 total abilities (2 Tier 1, 3 Tier 2, 1 Tier 3) offering greater build variety with Aggressive, Tactical, and Summoner playstyles.

---

## [2026-01-09 17:00] AI

### Modified
- Enhanced all Yyroizgt abilities and character description to fit Blood Dome's brutal "battle to the death" theme
- Rewrote ability descriptions with more visceral, deadly flavor text emphasizing violence and sacrifice
- Updated character description from "earnest ocean lover" to "zealot killer" who serves a cruel goddess
- Modified ability text to emphasize Blood Dome context (arena combat, no escape, death matches)
- Changed tone from tactical/strategic to brutal/lethal throughout
- Files:
  - drafts/abilities/ability_yyroizgt_tidal_strike.md (more brutal flavor)
  - drafts/abilities/ability_yyroizgt_wave_crash.md (execution-focused)
  - drafts/abilities/ability_yyroizgt_crushing_depths.md (emphasized lethality)
  - drafts/abilities/ability_yyroizgt_undertow.md (dragging victims to death)
  - drafts/abilities/ability_yyroizgt_moanas_deluge.md (blood tide massacre)
  - drafts/abilities/ability_yyroizgt_moanas_rest.md (healing between killings)
  - drafts/characters/char_yyroizgt.md (zealot description, Blood Dome strategy)

**Result**: Character now fully embodies Blood Dome's brutal PvPvE death match theme while maintaining mechanical balance.

---

## [2026-01-09 16:30] AI

### Modified
- Restructured Yyroizgt character to comply with Blood Dome tier system
- Converted quest_yyroizgt_blood_tide to quest_yyroizgt_levelup (proper level-up quest)
- Created rest ability: ability_yyroizgt_moanas_rest (Level 6 reward)
- Created 2-path tier structure with 5 abilities total:
  - Tier 1 Aggressive: ability_yyroizgt_tidal_strike (5g)
  - Tier 1 Tactical: ability_yyroizgt_wave_crash (5g, updated)
  - Tier 2 Aggressive: ability_yyroizgt_crushing_depths (10g)
  - Tier 2 Tactical: ability_yyroizgt_undertow (10g)
  - Tier 3 Ultimate: ability_yyroizgt_moanas_deluge (20g, rebalanced)
- Deleted ability_yyroizgt_drowning_grasp (replaced by new tier system)
- Updated character file with proper ability references and quest link
- Files:
  - drafts/quests/quest_yyroizgt_blood_tide.md → quest_yyroizgt_levelup.md (renamed and updated)
  - drafts/abilities/ability_yyroizgt_moanas_rest.md (created)
  - drafts/abilities/ability_yyroizgt_tidal_strike.md (created)
  - drafts/abilities/ability_yyroizgt_wave_crash.md (updated to Tier 1 Tactical)
  - drafts/abilities/ability_yyroizgt_crushing_depths.md (created)
  - drafts/abilities/ability_yyroizgt_undertow.md (created)
  - drafts/abilities/ability_yyroizgt_moanas_deluge.md (rebalanced to Tier 3)
  - drafts/abilities/ability_yyroizgt_drowning_grasp.md (deleted)
  - drafts/characters/char_yyroizgt.md (updated with all new abilities and paths)
  - drafts/abilities/_index.md (updated)
  - drafts/quests/_index.md (updated)

**Result**: Character now fully complies with Blood Dome conventions with two distinct playstyle paths (Aggressive and Tactical) that share a common ultimate ability.

---

## [2026-01-09 16:10] AI

### Modified
- Repaired Blood Dome convention violations across Yyroizgt character content
- Fixed YAML formatting (removed triple backticks wrapping frontmatter)
- Added tier and subtype fields to all abilities (marked as null with NEEDS ASSIGNMENT notes)
- Added compliance notes to all files documenting violations and missing content
- Updated character file to note missing level-up quest and rest ability
- Updated quest file to clarify it's NOT a level-up quest
- Files:
  - drafts/characters/char_yyroizgt.md (added levelup_quest field, compliance notes)
  - drafts/abilities/ability_yyroizgt_wave_crash.md (fixed YAML, added tier/subtype, compliance notes)
  - drafts/abilities/ability_yyroizgt_drowning_grasp.md (fixed YAML, added tier/subtype, compliance notes)
  - drafts/abilities/ability_yyroizgt_moanas_deluge.md (fixed YAML, added tier/subtype, compliance notes)
  - drafts/quests/quest_yyroizgt_blood_tide.md (fixed YAML, added compliance notes)
  - .claude/HISTORY.md

**Issues Identified:**
1. Missing level-up quest: `quest_yyroizgt_levelup` (CRITICAL)
2. Missing rest ability for Level 6 progression (CRITICAL)
3. Ability pricing doesn't follow tier system (75g, 200g, 400g instead of 5g, 10g, 20g)
4. Abilities missing tier assignments (Low/Medium/High)
5. Abilities missing subtype classifications

---

## [2026-01-09 16:00] AI

### Created
- Logged missing character creation for Yyroizgt and related content
- Files: .claude/HISTORY.md

**Note**: The following content was created but not logged. Adding entry retroactively:
- Character: char_yyroizgt (Paladin devoted to Moan-a)
- Quest: quest_yyroizgt_blood_tide (Kill 2 wet PCs)
- Abilities: ability_yyroizgt_wave_crash, ability_yyroizgt_drowning_grasp, ability_yyroizgt_moanas_deluge
- Files: drafts/characters/char_yyroizgt.md, drafts/quests/quest_yyroizgt_blood_tide.md, drafts/abilities/ability_yyroizgt_*.md
- Index files updated: drafts/characters/_index.md, drafts/quests/_index.md, drafts/abilities/_index.md

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
