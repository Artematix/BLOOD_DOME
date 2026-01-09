# Procedure: Modify System

## When to Use

When changing the Blood Dome system itself:
- Templates
- Conventions
- Folder structure
- Procedures
- New content categories

---

## Types of System Changes

1. **Template modification**: Changing entity templates
2. **Convention changes**: ID formats, naming rules
3. **Structure changes**: New folders, categories
4. **Procedure updates**: New or modified procedures
5. **Documentation**: Rules, guides

---

## 1. Modifying Templates

Templates are in `.claude/templates/`.

### Steps

1. **Read the current template**
2. **Make your changes**
3. **Check existing content**
   - Does existing content need to be updated?
   - List all affected files
4. **Update existing content** (if required)
   - Add new fields with sensible defaults
   - Don't break existing content
5. **Update CLAUDE.md** if the change affects workflows
6. **Log in HISTORY.md**
7. **Log in CHANGELOG.md** (template changes are significant)

### HISTORY.md Entry

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Modified (System)
- Updated character template
- Added new field: `playstyle_tags` (array)
- Propagated to existing characters: char_barbarian, char_rogue
- Files: .claude/templates/character.md
- Also updated: content/characters/char_barbarian.md, content/characters/char_rogue.md
```

### CHANGELOG.md Entry

```markdown
## [Unreleased]

### Changed
- Character template now includes `playstyle_tags` field
```

---

## 2. Changing Conventions

Conventions are in `.claude/CONVENTIONS.md`.

### Steps

1. **Read current conventions**
2. **Make your changes**
3. **Identify all affected content**
   - This is often EVERYTHING of a type
4. **Update all affected content**
   - Rename files if ID format changed
   - Update references everywhere
5. **Update CLAUDE.md** if needed
6. **Log in HISTORY.md**
7. **Log in CHANGELOG.md**

### Warning

Convention changes are HIGH IMPACT. Consider:
- Is this absolutely necessary?
- Can it be done incrementally?
- Have you found ALL affected files?

---

## 3. Adding New Content Categories

When adding a completely new type of content.

### Steps

1. **Plan the structure**
   - What fields does it need?
   - How does it relate to existing content?
   - ID format?

2. **Create folders**
   - `drafts/{newcategory}/`
   - `content/{newcategory}/`
   - `assets/{newcategory}/` (if needed)

3. **Create index files**
   - `drafts/{newcategory}/_index.md`
   - `content/{newcategory}/_index.md`

4. **Create template**
   - `.claude/templates/{newcategory}.md`

5. **Create procedure**
   - `.claude/procedures/create-{newcategory}.md`

6. **Update CLAUDE.md**
   - Add to "What You Can Do"
   - Add to Quick Reference table
   - Add to file structure diagram

7. **Update CONVENTIONS.md**
   - Add ID format for new category

8. **Log in HISTORY.md and CHANGELOG.md**

### Example Entry

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Created (System)
- Added new content category: NPCs
- Created: drafts/npcs/, content/npcs/
- Created: .claude/templates/npc.md
- Created: .claude/procedures/create-npc.md
- Updated: .claude/CLAUDE.md, .claude/CONVENTIONS.md
```

---

## 4. Updating Procedures

When procedures need changes.

### Steps

1. **Read the current procedure**
2. **Make your changes**
3. **Verify accuracy**
   - Do the steps actually work?
   - Are file paths correct?
4. **Update CLAUDE.md** if the procedure name changed
5. **Log in HISTORY.md**

---

## 5. Updating Documentation

For rules, guides, and other docs.

### Steps

1. **Make your changes**
2. **Update `docs/rules/_index.md`** if adding new rules
3. **Log in HISTORY.md**

---

## Checklist for System Changes

- [ ] Understood full impact of change
- [ ] Identified all affected files
- [ ] Made the system change
- [ ] Propagated to existing content (if needed)
- [ ] Updated CLAUDE.md (if workflows changed)
- [ ] Updated CONVENTIONS.md (if IDs/formats changed)
- [ ] HISTORY.md logged
- [ ] CHANGELOG.md logged (for significant changes)

---

## Propagation Guidelines

When updating templates, decide:

### Add with Default
For new optional fields:
```yaml
new_field: null  # Added in system update YYYY-MM-DD
```

### Require Update
For new required fields:
- List all files needing updates
- Update each one
- Log all files in HISTORY.md

### Breaking Change
If the change breaks existing content:
1. Document the migration path
2. Update ALL affected files before merging
3. Test thoroughly

---

## Example: Adding "Tags" to All Items

1. **Template change**: Add `tags: []` to `.claude/templates/item.md`

2. **Convention update**: Document tag format in CONVENTIONS.md

3. **Propagation**: Add `tags: []` to all existing items:
   - `content/items/weapons/*.md`
   - `content/items/armor/*.md`
   - etc.

4. **HISTORY.md**:
   ```markdown
   ## [2025-01-09 17:00] DM

   ### Modified (System)
   - Added `tags` field to item template
   - Propagated to 15 existing items
   - Files: .claude/templates/item.md, .claude/CONVENTIONS.md
   - Also: content/items/*/*.md (15 files)
   ```

5. **CHANGELOG.md**:
   ```markdown
   ### Changed
   - Items now support `tags` array for categorization
   ```
