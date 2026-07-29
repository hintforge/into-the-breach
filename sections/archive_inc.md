# Archive, Inc. -- Temperate

**status:** research-integrated
**last_reconciled:** 2026-06-02 (P2)
**zone-id:** archive_inc

Temperate / Museum island. CEO Dewey Alms. **Always the first available island.** See `architecture_manifest.md` for the zone graph.

## Environment

Forest tiles (can be set on fire), water tiles. [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: none_

## Weather / environmental events

Air Support (airstrike), Mines, Tidal Waves (advancing ocean drowns ground units; flying immune), Destroy the Dam (converts a line of tiles to water). [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

## Mission objectives

Defend the Artillery Support, Defend the 2 Tanks, Defend the Satellite Launches, Destroy the Dam. AE adds: Defend the Armored Train, Use 3 Repair Platforms. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

## Island boss

Corporate HQ defense against a Hive Leader (Hornet/Scorpion/Firefly/Spider Leader, etc.) on the final mission — mandatory to secure the island. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

## Achievement note

**Watery Grave** (drown 3 enemies in one battle, Rift Walkers) is easiest here using Tidal Surge or Destroy-the-Dam maps. See `achievements.md`. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: none · ach: watery_grave_
> **Cross-system dependency** -- see `dependencies.md` DEP-008: Archive Inc.'s water tiles and water-creation events are the most reliable environment for earning the Watery Grave achievement.

## Gate list (P2)

All four corporate islands share the same six-gate skeleton. Archive-specific parameters noted below.

**Gate 1 — Region / Mission Selection.**
- Entry condition: island selected from world map (forced first on a new save; freely selectable afterward).
- Decisions: choose one mission in any unlocked region (adjacency-driven). Each mission shows bonus objectives (1–3), reward type (rep / grid / core), and threat level. Reversible until deploy.
- Outgoing edges: completing a mission unlocks adjacent regions; after 4 regions completed the HQ defense triggers.
- Optional branches: 2- and 3-objective missions; AE objective types (Defend the Armored Train, Use 3 Repair Platforms); standard Archive objectives (Defend Artillery Support, Defend Tanks, Defend Satellite Launches, Destroy the Dam). Time Pod (1 per island).
- Common confusions: players sometimes expect free exploration of all 8 regions — only 4 are ever attempted; the remaining 3 are lost to seismic collapse before the HQ fight.
- Soft-lock warnings: none. Losing a mission costs grid power but does not end the run; mechs are repaired post-battle.
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

**Gate 2 — Pre-Mission Deploy Screen.**
- Entry condition: appears before every mission on this island (including the HQ defense).
- Decisions: assign pilots to mechs, swap weapons / passives, install / redistribute reactor cores, choose mech deploy positions. All reversible until the mission begins; once a mech carrying a core deploys, that core is locked to that mech for the battle (still reassignable among its own upgrade nodes).
- Missable content: none expires here.
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

**Gate 3 — Post-Mission Reward Screen.**
- Rewards (reputation / grid / core) are auto-granted per completed bonus objective. Cores can be installed immediately. Reputation cannot be spent until the Store (Gate 6).
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

**Gate 4 — Time Pod Pickup (in-mission, optional).**
- Archive carries 1 Time Pod per island (as an island-1/2 slot). **No Strange Pod on Archive** — secret pilots never appear on island 1. [Confirmed: 2 sources]
> **Cross-system dependency** -- see `dependencies.md` SEQ-005: Strange Pods never spawn on Archive Inc. (island 1); players seeking a Strange Pod must use islands 2/3/4.
- Decisions: move a mech onto the pod tile, protect it until battle ends, or ignore it. Pod always yields 1 reactor core plus a possible bonus (weapon / pilot / grid).
- Missable: a Vek ending on the pod tile destroys it permanently.
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: progression_

**Gate 5 — Island Boss / Corporate HQ Defense (mandatory).**
- Entry condition: triggered automatically after 4 regions attempted.
- Decisions: none — the HQ defense cannot be skipped. Objective: Destroy the Hive Leader (2 rep) + Protect the Corporate Tower (1 rep). Archive bosses: standard Hive Leaders (Scorpion / Hornet / Firefly / Beetle / Spider / Large Goo / Psion Abomination depending on run).
- Common strategy error: treating the boss as optional — the island cannot be secured without completing it.
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_

**Gate 6 — Corporate Store + Perfect Island Reward.**
- Perfect Island bonus (if all objectives on all missions were completed): choose one of — a weapon, a pilot, or +2 Grid Power (+4 on Unfair). Chosen before reputation is spent.
- Store: Reactor Cores (3 rep each), Grid Power (1 rep each), Weapons (2 rep each, limited to 2 weapons on island 1). Unused pilots can be sold for +1 rep (+4 if they have the Popular Hero passive). Reputation does NOT carry to the next island.
> **Cross-system dependency** -- see `dependencies.md` SEQ-003: All unspent reputation is permanently lost when advancing; this window (post-HQ-boss, pre-advance) is the only spending opportunity.
> **Cross-system dependency** -- see `dependencies.md` DEP-007: Pilots with the Popular Hero bonus skill sell for +4 rep instead of +1.
- Outgoing edge: advance to next island (or the Volcanic Hive once 2 islands are secured).
- Common strategy error: failing to spend reputation before advancing — it resets on island transition.
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

## Pilots found here

Archive-affiliated pilots (Harold Schmidt, Gana, Lily Reed) can appear via this island's Time Pods / Perfect Island reward. See `crew/index.md`.
