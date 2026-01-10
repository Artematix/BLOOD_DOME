# Changelog

All notable changes to Blood Dome content will be documented here.

Format: `[YYYY-MM-DD] Category: Brief description (Author)`

---

## [Unreleased]

### Added
- Initial repository structure
- Templates for all entity types
- Convention documentation
- **AI Agent instruction system** (.claude/CLAUDE.md)
- Step-by-step procedures for all content operations (.claude/procedures/)
- **Blood Dome Specific Rules** (2026-01-09)
  - Ability tier system (Low/Medium/High) with fixed pricing
  - Character level-up quest requirements
  - Rest ability requirement for level 6 progression
  - Mandatory item fields (description, buy price, sell price)

### Changed
- HISTORY.md format improved with clearer instructions
- **System Structure Updates** (2026-01-09)
  - Ability template: Added tier and subtype fields, tier-based pricing
  - Character template: Added level-up quest requirement, rest ability field, no starting equipment default
  - Item template: Made description, buy, and sell fields mandatory
  - Quest template: Added level-up quest tracking fields
  - CONVENTIONS.md: Added "Blood Dome Specific Rules" section
  - All procedures updated with new validation requirements

### Removed
- Default starting equipment for characters (now opt-in only)
- Default D&D class abilities from character builds (custom abilities only)

---

## Version History

### v0.1.0 - 2025-01-09
- Initial project setup
- Created folder structure
- Added templates and conventions
