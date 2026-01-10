# Procedure: Create Item

## When to Use

When creating a new item (weapon, armor, consumable, artifact, or misc).

## Prerequisites

- Read `.claude/CONVENTIONS.md` for ID naming rules
- Read `.claude/templates/item.md` for the template
- Know the item category and concept

## ID Formats by Category

| Category | Prefix | Example |
|----------|--------|---------|
| Weapon | `item_wpn_` | `item_wpn_flaming_sword` |
| Armor | `item_arm_` | `item_arm_dragon_scale` |
| Consumable | `item_con_` | `item_con_health_potion` |
| Artifact | `item_art_` | `item_art_crown_of_thorns` |
| Misc | `item_msc_` | `item_msc_grappling_hook` |

## Steps

### 1. Determine Category and Generate ID

Pick the category, then create ID:
`item_{category_prefix}_{name}`

### 2. Copy the Template

Copy from `.claude/templates/item.md`

### 3. Fill Out the Template

Required fields:
```yaml
id: item_wpn_youritem
name: "Display Name"
status: draft
author: "RequesterName"
created: YYYY-MM-DD
modified: YYYY-MM-DD
category: weapon|armor|consumable|artifact|misc
rarity: common|uncommon|rare|very_rare|legendary

shop:
  buy: 100    # REQUIRED: Price to purchase (gold)
  sell: 50    # REQUIRED: Price when selling (gold, typically 50% of buy)
```

**CRITICAL REQUIREMENTS:**
- **ALL items MUST have buy and sell values defined**
- **Description MUST be clear and specific**
- **Do NOT fill out extra data** without checking with the user

Fill in category-specific fields (weapon stats, armor AC, etc.)

### 4. Create Asset Placeholder

Create: `assets/items/{id}.placeholder`

Example: `assets/items/item_wpn_flaming_sword.placeholder`

### 5. Save the Item File

**Draft (default):**
`drafts/items/{id}.md`

**Final (if instructed):**
`content/items/{category}/{id}.md`

Categories map to folders:
- weapon → `content/items/weapons/`
- armor → `content/items/armor/`
- consumable → `content/items/consumables/`
- artifact → `content/items/artifacts/`
- misc → `content/items/misc/`

### 6. Update the Index

**For drafts:** `drafts/items/_index.md`

**For final:** Update BOTH:
1. `content/items/_index.md` (summary counts)
2. `content/items/{category}/_index.md` (item row)

Example row for weapons index:
```markdown
| item_wpn_flaming_sword | Flaming Sword | 1d8+1d6 fire | 200 | 100 | - | final |
```

### 7. Update Shop Catalog (if purchasable)

If `shop.buy` is not null, add to `content/shop/catalog.md` in the appropriate section.

### 8. Log in HISTORY.md

```markdown
## [YYYY-MM-DD HH:MM] AuthorName

### Created
- New weapon: item_wpn_flaming_sword
- Files: drafts/items/item_wpn_flaming_sword.md
- Assets: assets/items/item_wpn_flaming_sword.placeholder
```

## Checklist

- [ ] ID follows convention for category
- [ ] All required YAML fields filled
- [ ] **Shop prices REQUIRED:** buy and sell values defined
- [ ] **Description REQUIRED:** Clear and specific item description written
- [ ] Exclusive character noted if applicable
- [ ] **No extra data filled** without user confirmation
- [ ] Asset placeholder created
- [ ] Index file(s) updated
- [ ] Shop catalog updated (if purchasable)
- [ ] HISTORY.md logged

## Example

Creating a Health Potion:

1. **ID**: `item_con_health_potion`
2. **Category**: consumable
3. **File**: `drafts/items/item_con_health_potion.md`
4. **Shop**: buy: 50, sell: 25
5. **Asset**: `assets/items/item_con_health_potion.placeholder`
6. **Indexes updated**: `drafts/items/_index.md`
7. **Logged**: Entry added to HISTORY.md
