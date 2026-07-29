# Volcanic Hive -- Final Battle ("The Last Stand")

**status:** research-integrated
**last_reconciled:** 2026-06-02 (P2)
**zone-id:** volcanic_hive

> **Spoiler: late-game.** This is the run's final battle. Gated above the player's current enemy tier (0). The persona delivers this on request post-encounter or when the player reaches it. See `architecture_manifest.md`.

Lava-environment final battle, unlocks after 2 islands secured. Two phases: surface, then underground/Caverns.

## Structure

Two phases. The squad deploys in a fixed 2×2 formation (D5–E6). Phase 2 counts as a separate mission for restoring limited-use weapons and disabled mechs; pilots killed in Phase 1 stay dead and are replaced with A.I. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_

## Primary objective -- the Renfield Bomb

Protect the Renfield Bomb until it arms (5 turns). **Source conflict on bomb HP:** Fandom states 4 HP; GameFAQs states 5 HP. Both agree it arms over 5 turns, does NOT explode at 0, and that destroying it deploys a replacement mid-turn while adding 2 turns to the timer. Bombs are effectively unlimited — the only penalty is the extending timer. Win nuance: the bomb only needs to survive the final turn; a 1-HP bomb blocking a spawn still wins. [Contradicted across sources — see notes / Single source for the win-nuance]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: low · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game · conflicts: Fandom 4 HP vs GameFAQs 5 HP_

## The Psion Tyrant

The Hive's Psion is the **Psion Tyrant** — deals 1 damage to ALL player units every turn, unavoidable except by killing it. [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_
> **Cross-system dependency** -- see `dependencies.md` DEP-009: Unlike standard Psions (which only buff Vek), the Psion Tyrant actively damages all player units each turn; it is the top elimination priority.

## Hazards

Surface: Lava Flow, Volcanic Projectiles (never target Power Pylons). Underground Caverns alternate Falling Rocks (convert lava→ground, allow Vek spawns) and Tentacles (convert tiles→lava; the aimed variant targets the exact 3 tiles your mechs occupy). Repeating pattern: Falling Rocks Random → Tentacles Aimed → Falling Rocks Area → Tentacle Area. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_

## Difficulty scaling

On Hard, 1 Vek Leader is present; on Unfair 3/4-island runs, TWO bosses per phase. The Hive does NOT scale to your cores/upgrades — only difficulty and run length matter. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_

## Gate list (P2)

The Volcanic Hive does not follow the corporate-island six-gate template. It has its own structure:

**Entry condition:** unlocks after 2 islands secured. Run-length choice (2 / 3 / 4 islands) is made here; the game calculates score and transitions to the final battle immediately.
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_

**Phase 1 (Surface):** protect the Renfield Bomb for 5 turns. Lava flows and Volcanic Projectiles active (never target Power Pylons). Grid pylons destroyed in this phase **do not count against a Perfect Run** — no grid power or score penalty for losing them here. [Confirmed: 2 sources]
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_
> **Cross-system dependency** -- see `dependencies.md` DEP-004: Grid pylons destroyed in either Volcanic Hive phase do NOT count against a Perfect Run — the normal scoring penalty is suspended for the final battle.

**Phase 2 (Underground Caverns):** treated as a separate mission — limited-use weapons reset, disabled mechs repaired; pilots killed in Phase 1 stay dead and are replaced with A.I. Protect the Renfield Bomb for 5 turns again. Falling Rocks and Tentacle alternation sequence active. [Confirmed: 2 sources]
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_
> **Cross-system dependency** -- see `dependencies.md` DEP-011: Pilots killed in Phase 1 are permanently dead for Phase 2 — the normal "mech repaired, pilot survives" post-battle rule does not apply here.

**No Corporate Store.** There is no vendor or deploy screen between the two phases; no reputation spending here. No between-phase upgrade window.
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_
