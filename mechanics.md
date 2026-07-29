# Into the Breach -- Mechanics

**status:** research-integrated
**last_reconciled:** 2026-06-02 (P2)

Core game-system rules for Into the Breach. Stable cross-zone knowledge -- this file covers systems that apply across all islands and runs. Per-island specifics live in `sections/`; squad/weapon/pilot/upgrade detail lives in `items/` and `crew/`.

---

## Perfect information system

Vek telegraph their attacks one full turn ahead — the core mechanic. Every enemy's move and attack target is shown at the start of your turn, before you act, so combat is a planning puzzle about preventing damage rather than reacting to surprises. Hold **Alt** to show the attack-order / effects overlay. [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: none_

## Turn structure

Vek emerge → Vek declare attacks (telegraphed) → you move mechs and fire → Vek execute attacks → end of turn. **Undo Move** is unlimited per turn but movement-only — you cannot move after firing, and firing cannot be undone. Undo can be blocked if a later unit's action affected the vacated tile. **Reset Turn** (once per battle by default) rewinds all units to the start of your turn; you cannot reset after the enemy turn resolves. "Battle" = one mission/map section. **Abandon Timeline** ends the entire run — you keep one pilot for the next timeline; no other mid-run abort option exists. [Confirmed: 2 sources (Abandon Timeline: P2)]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: none_

## Power grid

Civilian buildings feed the power grid; the grid total is shared across the whole run. If the grid hits zero, the run ends immediately. Buildings are lost to Vek attacks or friendly fire; grid power is regained from mission rewards, time pods, and vendor purchase (1 Reputation per Grid Power). Grid starts at **5**, maximum is **7**; gains beyond 7 convert to Grid Defense bonus instead (base 15%; 0% on Unfair; max 40% with full Overpower stack). Civilians-per-region scales by difficulty (Easy 500 / Normal 1,000 / Hard 2,000 per region). [Confirmed: 2 sources (P2 for grid max)]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: none_

## Mech damage and repair

Mechs take damage from Vek attacks and terrain (fire, ACID, drowning). A mech reduced to 0 HP is disabled for the rest of that battle but repaired afterward; a pilot is only lost if killed outright (e.g. drowned/knocked into a hazard, or disabled at the final battle). Repair is an action that also heals 1 HP and clears fire/ACID/freeze on the mech. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: none_
> **Cross-system dependency** -- see `dependencies.md` DEP-011: Pilots disabled in Volcanic Hive Phase 1 are permanently dead (replaced by A.I. for Phase 2), unlike regular missions where disabling is temporary.

## Push and displacement mechanics

Most mech attacks push or pull units one tile. Displacement is the core puzzle lever — redirect Vek attacks into each other, into water/ACID/chasms/lava (instant kill for non-flying, non-Massive units), or away from buildings. Non-flying, non-Massive Vek drown in water/ACID/chasm/lava. Freezing stops a unit's action and acts as a shield. ACID doubles weapon damage taken and disables Natural Armor. Webbing prevents movement (broken by pushing the webbed unit or its target). Grounded Leaders are "Massive" (immune to water/ACID). [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_
> **Cross-system dependency** -- see `dependencies.md` DEP-002: ACID status disables Natural Armor passive, removing the mech's 1-damage-negation until ACID is cleared.
> **Cross-system dependency** -- see `dependencies.md` DEP-010: Detritus Disposal's ACID pools make ACID status the primary island hazard; the AE Thick Skin bonus skill grants ACID immunity.

## Pilots and ability system

Each mech is piloted by one named pilot with a passive ability. Pilots gain **1 XP per Vek HP killed**; first bonus skill at 25 XP, second at +50 (75 total cap). Bonus skills are randomized at timeline start. Artificial (A.I.) pilots gain no XP. The "Last Traveler" carries XP/skills to the next timeline (the run-persistence/time-travel mechanic). Full roster, abilities, and acquisition: see `crew/`. [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> see crew/index.md for the full pilot roster and per-pilot summaries.
> **Cross-system dependency** -- see `dependencies.md` DEP-001: XP gain from Vek kills drives pilot leveling; killing Vek rather than merely neutralizing them maximizes bonus-skill acquisition speed.

## Reactor upgrades

Reactor cores are the primary upgrade currency. You can install up to **9 cores** per mech (effective ceiling 11 once pilot/Mafan reactor bonuses are added). Cores buy universal nodes (+2 HP, +1 Move, +1 Reactor) and weapon-specific upgrade tiers. Cores can be freely redistributed (Undo install). Full detail: `items/upgrades.md`. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

## Time pod system

Time Pods are optional per-mission pickups (islands 1–2 = 1 pod each, islands 3–4 = 2 pods each). Each pod **always yields 1 reactor core** (guaranteed), plus a chance of an additional reward (pilot, grid power, weapon); a pod yielding only the core is the minimum ("core-only"). A pod is **missable** — destroyed if a Vek ends its turn on the pod tile or hits it. A **Strange Pod** has a ~15% chance of replacing a Time Pod on islands 2/3/4 (never island 1; only one per timeline) and unlocks a secret FTL pilot. See `sections/missables.md`. [Confirmed: 2 sources (P2)]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: progression_
> **Cross-system dependency** -- see `dependencies.md` SEQ-004: A Vek ending on the pod tile permanently destroys it; 1 guaranteed reactor core and any bonus reward are lost.
> **Cross-system dependency** -- see `dependencies.md` SEQ-001: Strange Pods only spawn on islands 2/3/4; recovering one is the only way to unlock secret FTL pilots.

## Island structure and run flow

A run is 2–4 islands chosen by the player (length picked at the Volcanic Hive once 2 islands are secured). Each island has 8 regions (numbered 0–7); complete missions in 4 regions, then the Corporate HQ defense (island boss, mandatory). Securing the island returns you to the deploy screen. Canonical islands and the zone graph: see `architecture_manifest.md`. [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

## Weather and environmental events

Each island carries its own environmental/weather events, shown before mission selection. Archive: Air Support, Mines, Tidal Waves (advancing ocean drowns ground units), Destroy the Dam. R.S.T.: Seismic Activity / Cataclysm (tiles → chasm), Lightning Storm, Hornet Attack, Sandstorm (4-turn missions). Pinnacle: Ice Storm, Freeze Mines, Cryo-nanites, Frozen Mechs/Thawing. Detritus: ACID pools, Conveyor Belts, Teleport Pads. Per-island detail: `sections/`. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

## Squad system

The player picks one squad of 3 mechs at run start. 8 named base squads + 5 Advanced Edition squads + Secret Squad, plus Random (Balanced Roll / Chaos Roll) and Custom (player-assembled). Squads are unlocked by spending Coins (1 Coin per achievement). Rift Walkers are free; the Secret Squad costs 25 Coins; Custom/Random unlock once a second squad is owned. Full squad/weapon tables: `items/weapons.md` and `items/builds.md`. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

## Scoring and reputation

Score scales with islands secured and difficulty (perfect 4-island run: 10,000 Easy / 20,000 Normal / 40,000 Unfair). **Reputation** is earned from mission performance and spent at corporate vendors between islands: weapons cost **2 Reputation** (the 2020 v1.2 patch temporarily reduced this to 1, but the 2022 Advanced Edition increased it back to 2 and limits weapon stock on islands 1–2; AE patch notes are authoritative), Reactor Cores cost 3 Reputation, Grid Power costs 1 Reputation. Reputation does **not** carry to the next island — unspent rep is lost on island advance. [Confirmed: 2 sources — AE patch notes, Fandom Corporate Reputation (P2)]
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> **Cross-system dependency** -- see `dependencies.md` SEQ-003: Reputation is permanently lost on island advance; it must be spent at the Corporate Store (Gate 6, post-HQ-boss) before confirming the advance.

## Vek types and behaviors

Vek are the insectoid enemy faction. Each island has 3 common Vek species + 1 Psion type; rare Vek appear deeper in a run; **Alpha Vek** (stronger, higher HP) spawn more often as the run progresses. All attacks are telegraphed one turn ahead.

| Vek | HP/Move (base → alpha) | Attack |
|---|---|---|
| Hornet | 2/5 → 4/5 | Stab 1 tile (1 dmg); Flying |
| Firefly | 3/2 → 5/2 | Goo projectile (1 → 3 dmg); ranged |
| Scorpion | 3/3 → 5/3 | Web adjacent, stab next turn (1 → 3 dmg) |
| Leaper | 1/4 → 3/4 | Web + bite (3 → 5 dmg); leaps over terrain |
| Scarab | 2/3 → 4/3 | Artillery 1 tile (1 → 3 dmg, 5-range) |
| Beetle | 4/2 → 5/2 | Charge forward, push (1 → 3 dmg) |
| Crab | — | Projectile hitting 2 tiles in a row |
| Blobber | 3/2 → 4/2 | Shoots Blob that explodes adjacent next turn (1 → 3) |
| Centipede | 3/2 | Goo, applies ACID to target + adjacent |
| Digger | 3/4 → 5/4 | Hits 3 tiles in a row; burrows when damaged; can't be moved |
| Burrower | 3/4 → 5/4 | Slam 3-tile swath; immune to forced movement |
| Spider | 2/2 → 4/2 | Lays egg → Spiderling next turn |
| Spiderling | 1/3 | 1 dmg melee |
| Mosquito (AE) | 2 / fast | Flying (resembles a squid — a dev naming oversight) |
| Moth (AE) | high HP (5) | Arcing projectile; pushes self back when firing; Flying; hardest common AE Vek |
| Bouncer (AE) | — | Pushed back when attacking; smoke cancels it |
| Gastropod (AE) | — | Leader ignites all adjacent tiles |
| Starfish (AE) | — | Attacks adjacent DIAGONAL tiles (Leader also pushes orthogonal) |
| Tumblebug (AE) | — | Summons an Unstable Boulder that explodes adjacent when damaged; max 2/mission; never on island 1 or mine missions |
| Plasmodia (AE) | — | rare Tier-2 Vek |

_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

**Psions (one per island; buff all OTHER Vek, never themselves):** Soldier (+1 HP to all Vek, +1 XP each), Shell / Hardened Carapace (Armor: −1 weapon dmg), Blood (heal 1/turn), Blast (explode on death for 1 adjacent dmg), Psion Abomination (+1 HP, regen, explode on death — a Leader). AE adds an Arachnid Psion (Vek leave a Spiderling egg on death). The **Psion Tyrant** is Volcanic-Hive-only and deals 1 damage to ALL player units every turn (unavoidable except by killing it). [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression (Psion Tyrant entry: late-game — Volcanic Hive only)_
> **Cross-system dependency** -- see `dependencies.md` DEP-009: The Psion Tyrant (Volcanic Hive only) deals 1 unavoidable damage to ALL player units each turn — unlike standard Psions; eliminating it is the top priority.

**"Hoist by their own petard" interactions** (under-documented by mainstream wikis): Beetles/Gastropods lured into hazards; Blobbers blown up by their own blobs; Diggers damaged on their own rock walls; Beetle Leaders standing in their own fire trail; Tumblebugs pushed into their own boulders; Bouncers/Moths recoiled into obstacles. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

## Advanced Edition mechanics

Advanced Edition is a **free** update (launched July 19, 2022) and is fully in scope — not a paid DLC. It added 5 squads, 15 squad achievements, 7 Vek, 3 Psions, 10 boss battles, 12 mission types, 4 pilots, 10 random pilot abilities, 39 weapons/equipment, 2 music tracks, 7 languages, and Unfair difficulty. All AE content can be individually toggled off in settings (balance changes are NOT reversible). New status mechanics introduced: KO effects, Cracking (tiles fracture into chasms), and Boosted (damage buff). [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
