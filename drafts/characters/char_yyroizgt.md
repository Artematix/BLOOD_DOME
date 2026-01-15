---
id: char_yyroizgt
name: "Yyroizgt"
status: draft
author: "zebko"
created: 2026-01-09
modified: 2026-01-09

# Core Identity
class: "Paladin"
role: "tank, support"

# Base Stats (Level 5)
hp: 47
ac: 18
speed: 30
proficiency_bonus: 3

# Ability Scores
str: 16
dex: 10
con: 14
int: 8
wis: 12
cha: 16

# Saving Throws (list proficient saves)
saving_throws: ["wisdom", "charisma"]

# Skills (list proficient skills)
skills: ["athletics", "religion", "persuasion"]

# Proficiencies
weapons: ["simple", "martial"]
armor: ["light", "medium", "heavy", "shields"]

# Starting Equipment (item IDs)
starting_equipment: []

# Starting Abilities (ability IDs)
starting_abilities: ["ability_yyroizgt_oceans_domain"]  # Passive wet aura + advantage on wet targets

# Exclusive Items (only this character can buy/use)
exclusive_items: [
  "ability_yyroizgt_tidal_strike",     # Tier 1 - Aggressive (ONLY Tier 1 option now)
  "ability_yyroizgt_crushing_depths",  # Tier 2 - Aggressive (bloodbending)
  "ability_yyroizgt_blood_sharks",     # Tier 2 - Summoner
  "ability_yyroizgt_moanas_deluge"     # Tier 3 - Ultimate (all paths)
]

# Character Quests (quest IDs)
quests: ["quest_yyroizgt_levelup"]

# Progression (Level 6+)
# What they gain when leveling up
progression:
  6:
    hp_bonus: 9
    abilities: ["ability_yyroizgt_moanas_rest"]
  7:
    hp_bonus: 9
    abilities: []
  8:
    hp_bonus: 9
    abilities: []
  9:
    hp_bonus: 9
    abilities: []
  10:
    hp_bonus: 9
    abilities: []

# Assets (relative to assets/ folder)
assets:
  portrait: characters/char_yyroizgt/portrait.png
  token: characters/char_yyroizgt/token.png

# Level-Up Quest
levelup_quest: quest_yyroizgt_levelup

---

# Yyroizgt

*"All blood flows to the sea eventually. Let me hurry your journey to the depths."*

## Description

Yyroizgt is a zealot, a killer wrapped in the guise of a holy warrior. Bronzed skin bears wave-like scars and tattoos - each one a sacrifice made to Moan-a, goddess of the killing tides. His eyes are the cold blue-grey of deep water where drowned sailors rest. The armor he wears is crusted with coral, barnacles, and salt - trophies from those who died screaming in the ocean's embrace.

**His weapon is sacred.** A bronze trident with three wickedly barbed prongs - teeth of a divine shark, blessed by Moan-a herself. The weapon **hungers**. It drinks not blood, but souls, life force, the final breath of the slain. When Yyroizgt drives it through a corpse in ritual sacrifice, seawater wells up from the wounds and the goddess grants her blessing.

From youth, Yyroizgt loved the sea with a fervor that others called madness. That love led him to Moan-a - not the gentle goddess of peaceful waves, but the cruel deity of drowning, shipwrecks, and blood in the water. She demands tribute. She demands sacrifice. And in the Blood Dome, Yyroizgt will give her what she craves.

**In the Arena:** Every puddle of blood becomes sacred water. Every opponent who bleeds becomes marked for drowning. Every corpse is an offering. Yyroizgt doesn't just fight - he performs sacred slaughter. The trident hungers, the goddess feeds, and he is sustained through devotion. The Blood Dome isn't a challenge to him. It's a temple. And he's the high priest of a very bloody faith.

## Special Mechanics

**Ocean's Domain (Passive)**: A 10-foot radius field of water surrounds Yyroizgt at all times. Any enemy that enters or starts their turn in this aura gains the "wet" status for 1 minute. Additionally, Yyroizgt has advantage on all attack rolls against creatures with the "wet" status.

**Tidal Smite**: Yyroizgt's divine smites are infused with seawater. When he uses Divine Smite on a melee attack, the target gains the "wet" status for 1 minute. This "wet" status marks them as touched by Moan-a's domain.

**Tidal Wrath**: Once per long rest, Yyroizgt can channel Moan-a's fury to deal an extra 2d8 radiant damage on his next melee attack. If this attack hits a creature with the "wet" status, the damage becomes 3d8 instead.

## Blood Dome Strategy

**The Wet Status - Mark of the Drowned:**
- **Applied by**: Water terrain, Yyroizgt's Divine Smites, his abilities
- **Duration**: 1 minute (unless otherwise specified)
- **Effect**: Marks victims for Moan-a - they count for quest kills, take extra damage from some abilities, have disadvantage on saves vs water effects
- **Visual**: Tracked with tokens - soaking wet, dripping blood and brine

**How Yyroizgt Wins:**
1. **Mark Victims**: Use smites and abilities to soak enemies in seawater
2. **Control the Fight**: Knock them prone, drag them around, crush them
3. **Execute the Wet**: Kill soaked targets to complete Blood Tide quest
4. **Level Up**: Complete quest → gain Moan-a's Rest → sustain through later fights
5. **Dominate**: Use Deluge to flood the arena and slaughter everyone in your domain

**Playstyle Options:**
- **Aggressive**: Maximum damage, execute wet targets quickly
- **Tactical**: Control positioning, set up perfect kills
- **Hybrid**: Mix both approaches as the fight demands

**Win Condition:**
Yyroizgt doesn't need to kill everyone - just kill 2 wet enemies for the quest. But in the Blood Dome, once you start the slaughter, why stop? The goddess hungers for more.

## Ability Paths

Yyroizgt begins with **Ocean's Domain** as a passive ability (10ft wet aura + advantage on wet targets), then can purchase abilities across 3 tiers:

### Starting Passive (Free)
- **[Ocean's Domain](../abilities/ability_yyroizgt_oceans_domain.md)** - 10ft wet aura + advantage on wet targets

### Tier 1 - Your Foundation (5g)
- **[Tidal Strike](../abilities/ability_yyroizgt_tidal_strike.md)** (Aggressive) - Only Tier 1 option: bonus action cold damage + wet marking

### Tier 2 - Choose Your Playstyle (10g)
- **[Crushing Depths](../abilities/ability_yyroizgt_crushing_depths.md)** (Aggressive) - Bloodbending burst damage + stun
- **[Blood Sharks](../abilities/ability_yyroizgt_blood_sharks.md)** (Summoner) - Summon Moan-a's hunting beasts

### Tier 3 - The Ultimate (20g)
- **[Moan-a's Deluge](../abilities/ability_yyroizgt_moanas_deluge.md)** (Ultimate) - Blood tide tsunami (works with all paths)

### Rest Ability (Level 6 Reward)
- **[Ritual of Moan-a](../abilities/ability_yyroizgt_moanas_rest.md)** - Sacrifice corpses to goddess, gain predator senses

## Build Recommendations

**Note**: All builds start with Ocean's Domain passive (free 10ft wet aura + advantage on wet targets).

**Bloodbender**: Tidal Strike → Crushing Depths → Moan-a's Deluge (35g)
- Bloodbending execution, stun locks, internal destruction
- Best for: Players who want to puppet enemies and crush them from within

**Shark Master**: Tidal Strike → Blood Sharks → Moan-a's Deluge (35g)
- Damage + minions + ultimate, turn water into death zones
- Best for: Players who want spectral sharks patrolling bloody waters

**All Builds**: Since Ocean's Domain is now a passive starter ability, all builds have the same foundation:
- Ocean's Domain passive (free) - 10ft wet aura + advantage
- Tidal Strike (5g) - only Tier 1 option
- Choice of 2 Tier 2 abilities (10g): Bloodbending or Summoner
- Moan-a's Deluge ultimate (20g)
- Total: 35g for full build

**Strategic Note**: With a 10ft wet aura and advantage on wet targets as baseline, every build automatically applies wet to melee enemies and attacks with advantage. Yyroizgt is a walking death zone.

## Compliance Notes

**Fully Compliant**: This character now meets all Blood Dome conventions:
- Level-up quest properly configured ([quest_yyroizgt_levelup](../quests/quest_yyroizgt_levelup.md))
- Rest ability included in Level 6 progression
- 4 purchasable abilities across proper tier structure (1 Tier 1, 2 Tier 2, 1 Tier 3)
- 1 starting passive ability (Ocean's Domain)
- Standard pricing (5g, 10g, 20g)
- Two distinct Tier 2 options (Aggressive/Bloodbending and Summoner)
