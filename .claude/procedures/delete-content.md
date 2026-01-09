# Procedure: Delete Content

## When to Use

When removing content from Blood Dome (characters, items, abilities, enemies, quests, events).

## IMPORTANT: Check Dependencies First

Before deleting ANYTHING, check what references it. Deleting referenced content breaks the system.

---

## Steps

### 1. Identify the Content

Know exactly what you're deleting:
- Content type
- ID
- File location

### 2. Search for Dependencies

Search the entire repository for the ID.

**What to search:**
- `content/` folder
- `drafts/` folder
- `content/shop/catalog.md`

**Common dependencies:**

| Deleting | Check For References In |
|----------|------------------------|
| Character | Abilities (exclusive_to), Items (exclusive_to), Quests |
| Item | Characters (starting_equipment), Shop catalog |
| Ability | Characters (starting_abilities, progression), Shop catalog |
| Enemy | Events (spawn lists) |
| Quest | Characters (quests array) |
| Event | Other events |

### 3. Handle Dependencies

For each reference found:

**Option A: Remove the reference**
- Delete the ID from arrays
- Update the referencing file's `modified` date

**Option B: Delete the dependent content too**
- If the dependent content is only relevant to what you're deleting
- Follow this procedure for each

**Option C: Abort**
- If dependencies are too complex, reconsider deletion

### 4. Delete the File

Remove the content file:
- `content/{category}/{id}.md` or
- `drafts/{category}/{id}.md`

### 5. Delete Assets (if any)

Remove associated assets:
- `assets/characters/{id}/` (entire folder)
- `assets/items/{id}.png` or `.placeholder`
- `assets/enemies/{id}/` (entire folder)

### 6. Update Index Files

Remove the entry from:
- The category's `_index.md`
- Summary counts if applicable

### 7. Update Shop Catalog

If the deleted content was purchasable:
- Remove from `content/shop/catalog.md`

### 8. Log in HISTORY.md

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Deleted
- Removed item_wpn_broken_sword
- Reason: Never used, cluttering shop
- Files deleted: content/items/weapons/item_wpn_broken_sword.md
- Assets deleted: assets/items/item_wpn_broken_sword.png
- Updated: content/items/weapons/_index.md, content/shop/catalog.md
```

---

## Checklist

- [ ] Searched for all dependencies
- [ ] Handled all references (removed or deleted dependent content)
- [ ] Deleted the content file
- [ ] Deleted associated assets
- [ ] Updated index file(s)
- [ ] Updated shop catalog (if applicable)
- [ ] HISTORY.md logged with reason

---

## Special Cases

### Deleting a Character

Characters have many dependencies. Check:
1. Exclusive abilities (`ability_{char}_*`)
2. Exclusive items (`exclusive_to: char_X`)
3. Character quests (`quest_{char}_*`)

Usually: Delete all exclusive content with the character.

### Deleting During Playtest

If content is being removed due to balance issues:
1. Consider moving to `drafts/` instead of deleting
2. Change `status: final` to `status: draft`
3. Add note about why it was pulled

---

## Example: Deleting an Unused Item

Task: Remove "Broken Sword" item

1. **Identify**: `item_wpn_broken_sword` in `content/items/weapons/`

2. **Search dependencies**:
   - Not in any character's starting_equipment
   - Not in shop catalog
   - No exclusive_to

3. **Delete file**: `content/items/weapons/item_wpn_broken_sword.md`

4. **Delete asset**: `assets/items/item_wpn_broken_sword.placeholder`

5. **Update index**: Remove row from `content/items/weapons/_index.md`

6. **Log**:
   ```markdown
   ## [2025-01-09 16:00] DM

   ### Deleted
   - Removed item_wpn_broken_sword
   - Reason: Placeholder item, never implemented
   - Files: content/items/weapons/item_wpn_broken_sword.md
   - Assets: assets/items/item_wpn_broken_sword.placeholder
   ```
