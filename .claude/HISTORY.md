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

## [2026-01-09 16:00] AI

### Modified (System)
- Restructured character template to separate D&D 5e base info from Blood Dome custom content
- Added `dnd:` section for standard D&D character info (race, racial_traits, class, subclass, class_features, feats, spellcasting, background)
- Added `blood_dome:` section for custom content (starting_equipment, starting_abilities, purchasable_abilities with tiers, exclusive_items)
- Added `purchasable_abilities` structure with explicit tier_1/tier_2/tier_3 organization
- Updated progression structure with `new_class_features` and `new_blood_dome_abilities`
- Added tools and languages to proficiencies
- Updated markdown body template with D&D Features Summary and Blood Dome Abilities sections
- Files:
  - .claude/templates/character.md (major restructure)
  - .claude/CONVENTIONS.md (added "Character Structure" documentation)
  - .claude/procedures/create-character.md (added D&D/Blood Dome workflow, updated checklist)
- Reason: Clear separation between vanilla D&D mechanics and custom Blood Dome content

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
