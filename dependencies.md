# Dependencies -- Into the Breach
<!-- hintforge · stitch pass · last run: 2026-06-03 -->
<!-- Every stitch run re-audits ALL existing edges + adds new ones. The per-edge convergence audit (open each cited source, verify the specific value) applies to every row in this file on every run, not just new candidates. A game patch, DLC, or new ingestion phase can change facts that existing edges cite -- only a full re-audit catches that. See `stitch_and_zipper.md` Phase B "Re-run scope: always full." Inconsistencies (cited source contradicts edge text) land in the `## Corpus inconsistencies` section; the edge row stays in place. -->

## Cross-system edges

| Edge ID | System A | System B | Dependency description | Confidence | Source files |
|---------|----------|----------|------------------------|------------|--------------|
| DEP-001 | Pilot progression (crew) | Combat / Vek HP (mechanics) | Defeating a Vek grants 1 XP per HP of damage killed; pilots level at 25 XP (first bonus skill) and 75 XP (second); maximizing XP income requires killing Vek rather than merely neutralizing them | high | `crew/index.md`, `mechanics.md` |
| DEP-002 | Status effects: ACID (mechanics) | Mech passive trait: Natural Armor (items/abilities) | ACID status disables Natural Armor (negation of 1 damage per hit), so an ACID-afflicted mech loses its passive damage reduction until ACID is cleared | high | `mechanics.md`, `items/abilities.md` |
| DEP-003 | Combat mechanic: Reset Turn (mechanics) | Pilot ability: Temporal Reset (crew/isaac_jones) | Fielding Isaac Jones doubles Reset Turn uses from 1 to 2 per battle, allowing an extra tactical rewind in any situation where Reset Turn is the only recovery option | medium | `architecture_manifest.md`, `crew/isaac_jones.md` |
| DEP-004 | Volcanic Hive environment (sections/volcanic_hive) | Perfect Run scoring (architecture_manifest) | Grid pylons destroyed in either Volcanic Hive phase do NOT count against a Perfect Run — the usual grid-loss penalty is suspended for the entire final battle | high | `architecture_manifest.md`, `sections/volcanic_hive.md` |
| DEP-005 | Pilot ability: Zoltan / Mafan (crew) | Reactor upgrade system (items/upgrades) | Mafan's Zoltan ability grants +1 Reactor Core capacity, raising the effective per-mech upgrade ceiling and enabling builds that require more than the base 9-core cap | medium | `crew/mafan.md`, `items/upgrades.md` |
| DEP-006 | Pilot entity: Mafan and Ariadne (crew) | Learnable bonus skills (items/abilities) | Mafan and Ariadne are blacklisted from all HP-increasing bonus skills (+2 HP, Skilled, Masochist), constraining their level-up build options compared to other named pilots | medium | `crew/mafan.md`, `items/abilities.md` |
| DEP-007 | AE bonus skill: Popular Hero (items/abilities) | Corporate vendor pilot sell value (architecture_manifest) | A pilot carrying Popular Hero sells for +4 reputation instead of the default +1, making deliberate pilot selling a significant reputation source when building toward store purchases | high | `items/abilities.md`, `architecture_manifest.md`, `sections/archive_inc.md` |
| DEP-008 | Achievement: Watery Grave (achievements) | Island environment: water tiles (sections/archive_inc) | Watery Grave (drown 3 enemies in one battle, Rift Walkers) is most reliably earned at Archive Inc., which provides native water tiles and water-creation events (Tidal Surge, Destroy the Dam); both files cross-reference each other | medium | `achievements.md`, `sections/archive_inc.md` |
| DEP-009 | Enemy: Psion Tyrant (mechanics) | Final battle structure (sections/volcanic_hive) | The Psion Tyrant appears exclusively in the Volcanic Hive and deals 1 unavoidable damage to ALL player units every turn — unlike standard Psions which only buff other Vek; killing it is the only counter | high | `mechanics.md`, `sections/volcanic_hive.md` |
| DEP-010 | ACID status + Thick Skin passive (mechanics, items/abilities) | Detritus Disposal environment (sections/detritus_disposal) | Detritus Disposal's ACID pools and ACID-mission objectives directly engage ACID status mechanics (doubles weapon damage taken, disables Natural Armor); pilots with the AE Thick Skin bonus skill become ACID-immune, making it a strong pick for this island | high | `mechanics.md`, `sections/detritus_disposal.md`, `items/abilities.md` |
| DEP-011 | Pilot loss conditions (mechanics) | Volcanic Hive Phase 1 (sections/volcanic_hive) | Pilots killed in Volcanic Hive Phase 1 are permanently dead and replaced by A.I. for Phase 2 — unlike regular missions where disabled mechs are repaired and pilots survive after the battle | medium | `mechanics.md`, `sections/volcanic_hive.md` |
| DEP-012 | Pilot ability: Chosen One / Adam (crew) | Combat mechanic: Reset Turn (controls, mechanics) | When a mech piloted by Adam uses Reset Turn, Adam gains Shield + 2 Move on that reset turn — the only pilot ability that triggers on Reset Turn use, making Adam the strongest Reset Turn activator | medium | `crew/adam.md`, `controls.md` |

## PoNR / lockout edges

| Edge ID | Trigger | Locked out | Notes | Source files |
|---------|---------|------------|-------|--------------|
| PON-001 | Selecting any squad at run start other than the one required for a squad-specific achievement | All squad-specific achievements requiring a different squad (e.g., choosing Blitzkrieg locks out Rift Walkers' Watery Grave and Ramming Speed for the entire run) | Squad selection is a one-time commitment per run; applies to all 13 named squads' 3-achievement sets; run must be abandoned to retry with a different squad | `achievements.md`, `items/builds.md` |

## Missable / sequencing dependencies

| Edge ID | Action | Window | Consequence | Source files |
|---------|--------|--------|-------------|--------------|
| SEQ-001 | Recover a Strange Pod (protect the pod until battle end after the Strange Object tile is destroyed) | Islands 2/3/4 only; ~15% chance per pod slot; max one per timeline; never on boss missions | If the Strange Pod is destroyed before pickup, the secret FTL pilot (Kazaaakpleth / Mafan / Ariadne — random) cannot be obtained this timeline; "Distant Friends" achievement missed | `sections/missables.md`, `crew/mafan.md`, `crew/kazaaakpleth.md`, `crew/ariadne.md`, `architecture_manifest.md` |
| SEQ-002 | Complete all mission objectives on an island including all pods | Within the island stay, before advancing | Failing any single mission objective or losing any pod forfeits the Perfect Island reward (pilot / weapon / grid / core choice) for that island with no recovery; also forfeits progress toward Perfect Island achievement and related mastery achievements | `sections/missables.md`, `items/upgrades.md`, `crew/index.md`, `architecture_manifest.md` |
| SEQ-003 | Spend reputation at Corporate Store (Gate 6, post-HQ-boss) before advancing | After the HQ boss fight, before confirming island advance | All unspent reputation is permanently lost on island transition; cannot be recouped | `mechanics.md`, `sections/archive_inc.md`, `architecture_manifest.md` |
| SEQ-004 | Protect Time Pod from Vek during the mission | During the mission only; pod destroyed if any Vek ends its turn on the pod tile | Pod permanently destroyed; 1 guaranteed reactor core lost plus any bonus reward (pilot, grid power, weapon) | `sections/missables.md`, `mechanics.md` |
| SEQ-005 | Attempt to find a Strange Pod on Archive Inc. (island 1) | Any run, any difficulty | Strange Pods never spawn on island 1; only available on islands 2/3/4; players seeking a Strange Pod must leave pod slots accessible on a later island | `sections/archive_inc.md`, `architecture_manifest.md` |

## Stitch run log

| Date | Scope | Edges written | Edges proposed (pending) | Inconsistencies surfaced | Model |
|------|-------|---------------|--------------------------|--------------------------|-------|
| 2026-06-03 | full | 18 | 0 | 1 | sonnet-class |

## Corpus inconsistencies

Stitch's per-edge convergence audit (see [`../../hintforge/stitch_and_zipper.md`](../../hintforge/stitch_and_zipper.md) Phase B) populates this section when a candidate edge's cited sources contradict each other.

| Detected | Files | Conflicting values | Suspected authoritative source | Status |
|----------|-------|--------------------|--------------------------------|--------|
| 2026-06-03 | `items/weapons.md`, `mechanics.md`, `architecture_manifest.md` | `weapons.md` said "vendor cost: 1 Reputation per weapon"; `mechanics.md` and `architecture_manifest.md` say 2 rep (AE patch authoritative; P2 explicitly reconciled this in mechanics.md but weapons.md was not updated) | `mechanics.md` / `architecture_manifest.md` (AE patch notes cited as authoritative) | resolved 2026-06-03: weapons.md updated to 2 rep |
