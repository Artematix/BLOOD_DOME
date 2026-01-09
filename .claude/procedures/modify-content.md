# Procedure: Modify Content

## When to Use

When editing existing content (characters, items, abilities, enemies, quests, events).

## Types of Modifications

1. **Minor edits**: Typos, stat adjustments, clarifications
2. **Major changes**: New abilities, restructuring, balance overhauls
3. **Status promotion**: Moving from draft to final

---

## Minor Edits

Small changes that don't affect structure or balance.

### Steps

1. **Read the current file**
2. **Make the edit**
3. **Update `modified` date** in frontmatter
4. **Log in HISTORY.md**

### HISTORY.md Entry

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Modified
- Fixed typo in char_barbarian description
- Files: content/characters/char_barbarian.md
```

---

## Major Changes

Significant alterations that affect gameplay or structure.

### Steps

1. **Read the current file** completely
2. **Understand dependencies**
   - What references this content?
   - What does this content reference?
3. **Make the changes**
4. **Update `modified` date**
5. **Update any dependent content**
   - If changing an item ID: update characters that use it
   - If changing ability effects: check balance
6. **Update index files** if name/stats changed significantly
7. **Log in HISTORY.md** with full details

### HISTORY.md Entry

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Modified
- Rebalanced char_barbarian
  - HP: 45 → 50
  - Added new starting ability: ability_barbarian_danger_sense
- Files: content/characters/char_barbarian.md
- Also updated: content/abilities/exclusive/_index.md
```

---

## Status Promotion (Draft → Final)

Moving content from `drafts/` to `content/`.

### Steps

1. **Read the draft file**
2. **Verify completeness**
   - All required fields filled?
   - All references valid?
   - Balance checked?
3. **Change status**: `status: draft` → `status: final`
4. **Move the file**:
   - From: `drafts/{category}/{id}.md`
   - To: `content/{category}/{id}.md`
5. **Update indexes**:
   - Remove from `drafts/{category}/_index.md`
   - Add to `content/{category}/_index.md`
6. **Update shop catalog** (if purchasable)
7. **Log in HISTORY.md**

### HISTORY.md Entry

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Moved
- Promoted char_barbarian from draft to final
- From: drafts/characters/char_barbarian.md
- To: content/characters/char_barbarian.md
- Updated indexes
```

---

## Checklist for All Modifications

- [ ] Read the file before editing
- [ ] Updated `modified` date
- [ ] Checked for dependent content
- [ ] Updated any affected references
- [ ] Updated index files if needed
- [ ] HISTORY.md logged

---

## Finding Dependencies

### What might reference this content?

| Content Type | Check These |
|--------------|-------------|
| Character | Items (exclusive_to), Abilities (exclusive_to), Quests (exclusive_to) |
| Item | Characters (starting_equipment), Shop catalog |
| Ability | Characters (starting_abilities, progression), Shop catalog |
| Enemy | Events (spawn lists) |
| Quest | Characters (quests array) |
| Event | Other events (chains) |

### How to find references

Search for the ID in all files:
```
Search for: char_barbarian
In: content/, drafts/
```

---

## Example: Rebalancing a Character

Task: Increase Barbarian's HP from 45 to 50

1. **Read**: `content/characters/char_barbarian.md`
2. **Edit**: Change `hp: 45` to `hp: 50`
3. **Update**: `modified: 2025-01-09`
4. **Dependencies**: None affected by HP change
5. **Index**: Update HP in `content/characters/_index.md` if shown
6. **Log**:
   ```markdown
   ## [2025-01-09 15:00] DM

   ### Modified
   - Increased char_barbarian HP: 45 → 50
   - Reason: Survivability too low in playtesting
   - Files: content/characters/char_barbarian.md
   ```
