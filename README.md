# Aethel Apps

A pair of web apps for the **Aethel** tabletop RPG system.

---

## Apps

**[Aethel Character Sheet](https://essent-aethel.github.io/Aethel-Character-Sheet/aethel-character-sheet.html)**
Full digital character sheet with live calculations, class-aware level tracking, and PDF export.

**[Pasqually's Spell Slinger](https://essent-aethel.github.io/Aethel-Character-Sheet/pasqually-spell-slinger.html)**
Spell builder and library for The Mind and The Spirit classes.

Open either link in your browser. No download or installation required. All game data is embedded — no companion files needed.

---

## Aethel Character Sheet

### Getting Started

1. Enter your **ability scores** first — modifiers, saving throws, and skill totals calculate automatically
2. Fill in your identity fields — name, ancestry, class, archetype, background, alignment, and languages
3. Open the **Level Log** tab and click **+ Add Level** to add your starting level. Your class and archetype determine the features and selection options available at each level. The character level on the main sheet is driven by the log and cannot be edited directly
4. Add your combat actions, bonus actions, reactions, and passives on the **Features** tab
5. Use the **Save** button to export your sheet as a `.json` file, or **Export PDF** for a printable character dossier

---

### Toolbar

The top toolbar contains six tabs and four utility buttons:

- **New Character** — clears all data and resets the sheet for a fresh build (prompts for confirmation)
- **Save** — exports the full character as a `.json` file
- **Load** — imports a previously saved `.json` file
- **Export PDF** — generates a compact, print-optimized character summary via the browser's print dialog (choose "Save as PDF")

---

### Tabs

#### Character Sheet

The main tab. Contains:

**Identity** — character name, player name, ancestry (dropdown), class, archetype, background, alignment, and languages. Level is read-only and driven by the Level Log.

**Ability Scores** — Fortitude, Reflex, Intellect, and Presence. Enter raw scores; modifiers calculate automatically using the game's score-to-modifier table and feed into saving throws, skills, and derived stats.

**Combat Stats** — a single compact band containing:

- *Initiative, Speed, Defense* — manual entry fields
- *Saving Throws* — FORT, REF, INT, and PRES, calculated live from ability modifiers
- *HP* — current and max, manual entry
- *Resource Pool* — current and max. The label updates automatically based on class: Feat Points (FP) for The Body, Arcane Points (AP) for The Mind, Spirit Points (SP) for The Spirit
- *Short Rest* button — tracks once-per-long-rest usage
- *Daily Archetype Ability* — hex toggle to mark as used; resets on long rest

**Skills** — eleven skills from the game system, each showing invested points, ability modifier, and total bonus. Displays points available, points spent, and remaining. Skills exceeding the cap for the current level are flagged. Cap is level + 1.

**Talents** — select talents from the game's five categories (Combat, Magic, Skill, Social, Exploration) via a grouped dropdown. Each talent has two tiers; upgrade or downgrade in place with the ▲/▼ buttons. Talent descriptions display inline.

**Character Summary** — placeholder section that populates as the character is built through the Level Log.

---

#### Features

Contains class and combat ability management:

**Archetype Abilities** — auto-populated reference list of your archetype's passive abilities, active abilities, and level features. Updates when you change your class or archetype on the Character Sheet tab.

**Actions / Bonus Actions / Reactions & Passives** — three manually managed tables for tracking combat abilities. Each entry has fields for name, cost, type, and description. Add entries with the **+ Add** button; delete with the row's ✕ button.

**Spell Forms & Crafted Spells** — import spells built in Pasqually's Spell Slinger. Click **Import JSON** and select a `.json` file exported from the Spell Slinger. Imported spells display as styled cards showing name, spell form, cost, and full description.

---

#### Inventory

A streamlined inventory system:

- **Currency** — Copper (CP), Silver (SP), and Gold (GP) fields
- **Capacity** — Readied Slots (2 + REF mod) and Pack Slots (8 + FORT mod), calculated automatically
- **Four text areas** — Weapons & Combat Gear, Armor & Shields, Magic Items (Attuned), and Consumables & Gear. Free-form entry for maximum flexibility
- **Attunement Slots** — max slots calculated from PRES modifier + 1, with a manual "used" counter

---

#### Level Log

The core character-building interface. Each level entry is class-aware and shows:

- **Status banner** — displays your current class and archetype, or prompts you to set them (with a quick-link button to the Character Sheet tab)
- **Features gained** — pulled from the game data's progression table for your class at that level
- **Archetype features** — displayed at the appropriate levels (typically 4, 7, and 10) with full name and description
- **Selection dropdowns** — choose your level-appropriate maneuvers, battle stances, strand augments, or divine inscriptions depending on your class. Options are level-gated (standard, advanced at L3+, expert at L5+), archetype-filtered, and previously selected choices are grayed out across all levels
- **Starting info** — Level 1 entries show your hit die and resource pool details; Level 2+ entries show HP roll, resource gain, and skill points gained

The **+ Add Level** button is disabled until a class is selected. Entries can be collapsed by clicking the header and deleted with the ✕ button (which also removes all higher-level entries). The level cap is 10.

**Class-specific selection types:**

- **The Body** — Tactical Maneuvers (standard + advanced + archetype-exclusive) and Battle Stances
- **The Mind** — Strand Augments (basic, damage, control, utility, defensive, combination + archetype-exclusive pools for Arcanist/Warden/Animist)
- **The Spirit** — Divine Inscriptions (universal + archetype-specific for Oracle/Templar/Zealot)

**Archetype bonuses:** Arcanists receive extra augment slots per level. Vanguards receive two extra maneuver slots at Level 1.

---

#### Notes & Lore

Five free-form text areas:

- Character Background & Backstory
- Faction Standing & Reputation
- Campaign Notes
- NPC Relationships
- Miscellaneous Notes

---

#### Cheat Sheet

Quick in-session reference covering:

- **Attack Resolution** — roll mechanics, glancing blow/full hit/critical hit thresholds, advantage and disadvantage (2d10 system with 3d10 for adv/disadv)
- **Conditions** — Prone, Staggered, Distracted, Frightened, Restrained, Blinded, Stunned, Paralyzed, Bloodied
- **Actions on Your Turn** — move, action, bonus action, reaction, free action, and the Scaling Threat DC formula
- **Rest & Recovery** — short rest, long rest, death saves, stabilize ally
- **Skill DC Reference** — Easy, Medium, Hard, and Legendary DCs scaled to your current level
- **Spell Forms** — all nine spell forms with base cost, range, and mechanic

---

### Saving & Loading

- The **Save** button exports a `.json` file containing all sheet data: identity, ability scores, combat stats, level log, skill investments, talents, action tables, spells, inventory, notes, and rest state
- **Load** imports a `.json` file — useful for moving between devices or sharing with your GM
- Data also persists automatically in browser `localStorage` between sessions on the same device and browser
- **Export PDF** generates a compact print-optimized dossier covering identity, combat stats, ability scores, skills, talents, level selections, actions, spells, inventory, and notes

> Local storage is per browser, per device. Use Save / Load to move between machines.

---

### Embedded Game Data

The character sheet includes the full Aethel game data (ancestries, backgrounds, skills, classes, archetypes, progression tables, maneuvers, stances, augments, inscriptions, spell forms, and talents) embedded directly in the HTML. No external `aethel-data.json` file is required. If an external file is present alongside the HTML, it takes priority — this allows updating game data without regenerating the sheet.

---

## Pasqually's Spell Slinger

A spell builder and library for **The Mind** and **The Spirit** classes.

---

### Building a Spell

- Select your **class** (Mind or Spirit). The augments update to show only what's relevant to you
- For Spirit, select your **subclass** (Oracle, Templar, or Zealot) to filter subclass-specific augments
- Choose a **Spell Form**. This is the shape and delivery method of your spell
- Add **Strand Augments**. Each one adds to the spell's cost and effect
- The running **Resource Point cost** and **power tier** update live as you build
- Name your spell and save it to your **spell library**

### Spell Library

- Saved spells persist between sessions in your browser
- **Export** your library as a `.json` file to back it up or share it
- **Import** a `.json` file to load spells from another device or player

### Integration with the Character Sheet

The Spell Slinger and Character Sheet are separate apps connected by JSON export/import:

1. Build your spells in the Spell Slinger and export the library as a `.json` file
2. On the Character Sheet's **Features** tab, click **Import JSON** under Spell Forms & Crafted Spells
3. Imported spells display as styled cards with their form, cost, and full description

### Notes

- Higher-tier augments are gated by class level; these are flagged in the interface
- Condition augments include a dropdown to choose the specific condition applied
- The power tier reference table highlights your current spell's tier as you build
