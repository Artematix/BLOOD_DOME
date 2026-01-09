# Blood Dome Conventions

## ID Naming Rules

All entities have unique IDs. IDs are **lowercase**, use **underscores**, and have **prefixes**.

### Format: `{type}_{subtype}_{name}`

| Entity Type | Prefix | Example |
|-------------|--------|---------|
| Character | `char_` | `char_barbarian`, `char_shadow_rogue` |
| Weapon | `item_wpn_` | `item_wpn_greataxe`, `item_wpn_flaming_sword` |
| Armor | `item_arm_` | `item_arm_chainmail`, `item_arm_dragon_scale` |
| Consumable | `item_con_` | `item_con_health_potion`, `item_con_bomb` |
| Artifact | `item_art_` | `item_art_crown_of_thorns` |
| Misc Item | `item_msc_` | `item_msc_rope`, `item_msc_lockpick` |
| Universal Ability | `ability_` | `ability_second_wind`, `ability_multiattack` |
| Character Ability | `ability_{char}_` | `ability_barbarian_rage`, `ability_rogue_sneak_attack` |
| Enemy | `enemy_` | `enemy_pit_fiend`, `enemy_goblin_horde` |
| Quest (Universal) | `quest_` | `quest_first_blood`, `quest_treasure_hunter` |
| Quest (Character) | `quest_{char}_` | `quest_barbarian_champion` |
| Event | `event_` | `event_meteor_shower`, `event_shop_sale` |

### Rules
1. Use only lowercase letters, numbers, and underscores
2. No spaces or special characters
3. Keep names concise but descriptive
4. Character-specific content includes character name in ID

---

## File Naming

Files are named by their ID: `{id}.md`

Examples:
- `content/characters/char_barbarian.md`
- `content/items/weapons/item_wpn_greataxe.md`
- `content/abilities/exclusive/ability_barbarian_rage.md`

---

## Asset Paths

Assets follow predictable paths relative to `assets/`:

| Entity | Path Pattern |
|--------|--------------|
| Character Portrait | `characters/{id}/portrait.png` |
| Character Token | `characters/{id}/token.png` |
| Item Image | `items/{id}.png` |
| Enemy Portrait | `enemies/{id}/portrait.png` |
| Enemy Token | `enemies/{id}/token.png` |

### Missing Images

If an image doesn't exist yet, create a placeholder file:
- `characters/{id}/portrait.placeholder`
- `items/{id}.placeholder`

This marks that an image is needed.

---

## Status Values

All content has a `status` field in frontmatter:

| Status | Meaning | Location |
|--------|---------|----------|
| `draft` | Work in progress, incomplete | `drafts/` folder |
| `review` | Ready for feedback/approval | `drafts/` folder |
| `final` | Approved, ready for use | `content/` folder |

---

## Frontmatter Requirements

All entity files MUST have:
```yaml
---
id: {unique_id}
name: "Display Name"
status: draft|review|final
author: "AuthorName"
created: YYYY-MM-DD
modified: YYYY-MM-DD
---
```

---

## Price Convention

Items and abilities that can be bought/sold:
```yaml
shop:
  buy: 100      # Price to purchase (null if not for sale)
  sell: 50      # Price when selling (typically 50% of buy, null if can't sell)
```

---

## Cross-References

Always reference other entities by ID:
```yaml
# Good
starting_equipment:
  - item_wpn_greataxe
  - item_arm_hide

# Bad
starting_equipment:
  - "Greataxe"
  - "Hide Armor"
```

---

## Markdown Body

The YAML frontmatter contains structured data. The markdown body contains:
- Flavor text / description
- Special mechanics explanation
- Any prose that doesn't fit in structured fields
