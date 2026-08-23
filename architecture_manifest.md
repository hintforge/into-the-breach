# Into the Breach -- Architecture Manifest

**status:** research-integrated
**last_reconciled:** 2026-06-02 (P2)
**research_run:** P1 + P2

Cross-zone structural primitives for Into the Breach. The persona reads this file for all cross-zone reasoning. Per-island notes live in `sections/` and reference this manifest's zone-ids. Drift between this file and per-island files is a bug; run a consistency pass after each ingestion.

> **P1 taxonomy correction (2026-06-02):** The original scaffold (and the P1 brief) carried a scrambled island map ("Grass = R.S.T., Desert = Pinnacle, Snow = Archive, Mountain Island"). P1 research corrected this against 3 sources / 2 languages. **There is no "Mountain Island."** The four canonical islands are Archive, Inc. (Temperate), R.S.T. Corporation (Desert), Pinnacle Robotics (Ice/Snow), and Detritus Disposal (Industrial/Acid), plus the Volcanic Hive final battle. Run-order ("Island 1/2/3/4") is kept distinct from canonical island identity.

## Hintforge manifest

```
corpus-core-version: 6
game-version: "latest"
game-version-platform: "PC / Steam"
game-version-as-of: 2026-06-02
vector-extensions: crew
```

## Vector extensions

- `crew/` -- named pilots with passive abilities, level state, and run-persistence tracking, indexed by `crew/index.md`

## Zone Graph

**Game-type label:** procedural (turn-based-tactics roguelike with procedurally generated missions)
**Localization-mechanism class:** map-system (hub-spoke island deploy screen)
**Entry node:** archive_inc (Archive, Inc. is always the first available island)
**Hub nodes:** deploy_screen (between-island upgrade, pilot-assignment, and weapon-swap screen)
**Source-language set:** English (dev: Subset Games, USA). Advanced Edition added Arabic, Thai, Swedish, Korean, Traditional Chinese, Turkish, and Latin American Spanish. Strong non-English communities: Korean (NamuWiki), Chinese (Bilibili/Tieba), Russian (CIS Steam).
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

**Notes on procedural structure:** Into the Breach has no fixed linear zone traversal. The player selects a 2-, 3-, or 4-island run from the four corporate islands; after the first save file all four can be tackled in any order. Each island has **8 regions (numbered 0–7)**; the player completes missions in 4 regions before the Vek attack the Corporate HQ (the remaining 3 regions are then overrun). The final mission of each island is the Corporate HQ defense against a Hive Leader (island boss) — **mandatory to secure the island, not optional.** Per-mission tile layouts and objectives are procedurally generated per run and are not modeled here. [Confirmed: 3 sources]

**Nodes:**
- `archive_inc` -- **Archive, Inc.** — Temperate/Museum (forest tiles, water). CEO Dewey Alms. Always the first available island.
- `rst_corporation` -- **R.S.T. Corporation** — Desert (sand → smoke tiles, chasms). CEO Jessica Kern.
- `pinnacle_robotics` -- **Pinnacle Robotics** — Ice/Snow (frozen tiles, hijacked Sentient Weapon robots). CEO Zenith.
- `detritus_disposal` -- **Detritus Disposal** — Industrial/Acid (A.C.I.D. pools, conveyor belts, teleport pads). CEO Vikram Singh.
- `volcanic_hive` -- **Volcanic Hive** — Final Battle ("The Last Stand"), lava environment, two phases (surface then underground Caverns). Unlocks after 2 islands secured.
- `deploy_screen` -- Hub: between-island screen for reactor upgrades, pilot assignment, and weapon swaps.

**Edges:**

| From | To | Type | Direction | Condition | Point of no return | Notes |
|---|---|---|---|---|---|---|
| deploy_screen | archive_inc | hub-spoke | bidirectional | always available; first island by default | none | first save: Archive is the entry island |
| deploy_screen | rst_corporation | hub-spoke | bidirectional | available for selection | none | any order after first save |
| deploy_screen | pinnacle_robotics | hub-spoke | bidirectional | available for selection | none | any order after first save |
| deploy_screen | detritus_disposal | hub-spoke | bidirectional | available for selection | none | any order after first save |
| [any 2 islands secured] | volcanic_hive | story-gate | one-way | 2+ islands secured (run length chosen at the Hive: 2/3/4 islands) | permanent | triggers run end; final battle |

_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: progression_

## Chapter ↔ Zone Mapping

| Chapter / Phase | Zones | Notes |
|---|---|---|
| Run start | deploy_screen | Squad selection, pilot assignment |
| Island 1 | archive_inc (default first) or player choice after first save | missions in 4 of 8 regions + Corporate HQ boss |
| Island 2 | one of the remaining islands | missions + Corporate HQ boss; securing 2 islands unlocks the Volcanic Hive |
| Island 3 (3- or 4-island run) | one of the remaining islands | missions + Corporate HQ boss |
| Island 4 (4-island run) | the remaining island | missions + Corporate HQ boss |
| Final battle | volcanic_hive | two-phase "The Last Stand"; protect the Renfield Bomb |

**Run length & score:** the player chooses a 2-, 3-, or 4-island run at the Volcanic Hive (unlocks after 2 islands secured). A perfect 4-island run scores 10,000 (Easy) / 20,000 (Normal) / 40,000 (Unfair); Hard falls between Normal and Unfair. [Confirmed: 2 sources]

## Optional Content

| Name | Unlock condition | Access window | Parent zone | Recommended chapter | Failure mode |
|---|---|---|---|---|---|
| Time Pods | Appears as an optional pickup on select missions (islands 1–2 always 1 pod; islands 3–4 always 2 pods) | During the mission only | any island | any | missable — destroyed if a Vek kills the pod before pickup |
| Strange Pods (secret-pilot unlock) | 15% chance of replacing a Time Pod on islands 2/3/4; only one may spawn per timeline | During the mission only | islands 2–4 | any | missable; fully random spawn — see `crew/` and `sections/missables.md` |
| Perfect Island bonus | Complete all objectives on an island incl. all pods | Within the island stay | any island | any | failing any objective forfeits the Perfect Island reward |
| Corporate HQ boss mission | Available after the island's regular missions | Before advancing | any island | any island | mandatory (not optional) — must be won to secure the island |

## Support Topology

### Save stations
Into the Breach autosaves after every turn (roguelike design — no in-game save-scumming; only external profile-folder copying circumvents it). No manual save stations. The in-mission **Reset Turn** (once per battle by default) rewinds all units to the start of YOUR turn — it is a turn rewind, not a save.

### Fast-travel network
None within runs. After each island is secured, the player returns automatically to the deploy screen (hub). You cannot return to a prior island once it is cleared.

### Hub access
The deploy screen is accessed automatically between islands. It does not appear mid-island.

### Upgrade access points (P2)

| Question | Answer |
|---|---|
| Deploy screen timing | Appears before every mission (including the HQ defense). Standard "Mission Prep" step for assigning pilots, swapping weapons, and installing reactor cores. |
| Reactor core redistribution window | Cores can be installed / redistributed at any deploy screen and at the post-mission reward screen. Once a mech deploys to a mission carrying a core, that core is locked to that mech for the battle (still reassignable among its own upgrade nodes; not movable to a different mech until the next deploy screen). |
| Corporate Store timing | Fixed: opens once per island, immediately after the HQ/Hive Leader fight. There is no mid-island vendor. |

_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

### Corporate vendor stock (P2)

| Category | Always available | Reputation cost | Notes |
|---|---|---|---|
| Reactor Cores | Yes, every island (1–4) | 3 rep each | Most-valued purchase. |
| Grid Power | Yes, every island (1–4) | 1 rep each | Excess beyond cap of 7 converts to Grid Defense bonus. |
| Weapons | Yes; stock **limited on islands 1–2** | 2 rep each (AE current patch) | Island 1 confirmed at 2 weapons; islands 2–4 count unverified. [Single source — verify · class: community] |
| Pilots | Sell only | +1 rep (+4 with Popular Hero passive) | Pilots enter roster via Time Pods and Perfect Island rewards only — not purchasable. See DEP-007. |

Reputation does NOT carry between islands — unspent rep is lost on island advance. [Confirmed: 2 sources]
_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> **Cross-system dependency** -- see `dependencies.md` SEQ-003: All unspent reputation is permanently lost on island advance; it must be spent at the Corporate Store (Gate 6) before confirming the transition.

### Grid power recovery and cap (P2)

| Aspect | Detail |
|---|---|
| Starting grid power | 5 |
| Maximum grid power | 7. Gains beyond 7 convert to Grid Defense bonus. |
| Grid Defense base | 15% (0% on Unfair). Maximum 40% with full Overpower stack. |
| Overpower increment | First 5 overpowers: +2% each. Next 15 overpowers: +1% each. Cap: +25% → 40% total. |
| Recovery sources per island | Grid-power (lightning) bonus objectives; Perfect Island reward (+2, or +4 on Unfair); Corporate Store (1 rep each); Grid Charger weapon (+1 on use). |
| Volcanic Hive pylons | Grid pylons destroyed in either Volcanic Hive phase do NOT count against a Perfect Run — no grid or score penalty. |

_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> **Cross-system dependency** -- see `dependencies.md` DEP-004: Volcanic Hive pylon destruction does NOT count against a Perfect Run — the normal scoring penalty is suspended for the final battle.

### Mission restart and abort (P2)

| Mechanic | Behavior |
|---|---|
| Mid-mission restart | No "abandon mission" or "return to deploy" option exists once a mission begins. |
| Abandon Timeline | Ends the entire run. You keep one pilot for the next timeline. Not reversible. |
| Reset Turn | Rewinds all units to start of your turn (once per battle; Isaac Jones's Temporal Reset grants a second reset per battle). Does NOT restart the mission. See DEP-003 / DEP-012. |
| Undo Move | Unlimited within a turn until any weapon fires. Firing is irreversible. |
| Known bug | Reset Turn occasionally rewinds into a previous mission/timeline — acknowledged by Subset Games, not intended behavior. |

_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

## Locks and Keys

### Summary table

| Lock location | Key required | Key source | Visible before key? | Notes |
|---|---|---|---|---|
| Volcanic Hive (final battle) | 2 islands secured | Completing any 2 of the 4 corporate islands | yes (shown on world map) | run-length choice (2/3/4 islands) made here |
| Secret Squad (Techno mechs) | All 8 named squads unlocked + 25 Coins | 1 Coin per achievement completed | yes (greyed in hangar) | gates Cyborg pilots; see squad table below |
| Cyborg pilots | Secret Squad unlocked | After unlocking the Secret Squad | no | normal pilots can't equip cyborg slots |
| Secret pilots (Kazaaakpleth / Mafan / Ariadne) | Recover a Strange Pod | Strange Object → Strange Pod (random, islands 2–4, 15% chance, 1 per timeline) | partially | fully random; "Distant Friends" achievement; see `crew/` |
| Custom / Random Squad | Own any 2nd squad | Unlock any squad beyond the default Rift Walkers | yes | enables player-assembled or randomized squads |
| All named squads (8 base + 5 AE) | Coins (1 per achievement) | Any achievements | yes (greyed in hangar) | see squad unlock table below |
| Unfair difficulty | None | — | yes | selectable from run start; no prior completion required |

_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

### Squad unlock costs and achievement triggers (P2)

Coins are fungible — any coin works toward any squad. Each achievement grants 1 coin. The last 5 coins in the pool of 70 cannot be spent (per-achievement cap math). Coins accumulate permanently across timelines.

| Squad | Coin cost | Island affiliation | Squad-specific achievements (3 per squad; earn coins toward other squads) |
|---|---|---|---|
| Rift Walkers | 0 (free) | — | Watery Grave (drown 3 enemies in water in 1 battle); Ramming Speed (kill enemy 5+ tiles away with Dash Punch — requires 2-core upgrade); Island Secure (complete 1st Corporate Island) |
| Rusting Hulks | 2 | R.S.T. | Perfect Battle (no mech/building damage in a battle); Overpowered (overpower grid twice); Stormy Weather (12 electric-smoke damage in 1 battle) |
| Zenith Guard | 2 | Pinnacle | Get Over Here (kill by pulling enemy into yourself with Attraction Pulse); Shield Mastery (block damage with shield 4× in 1 battle); Glittering C-Beam (hit 4 enemies with 1 laser) |
| Blitzkrieg | 3 | Detritus | Chain Attack (chain whip through 10 tiles); Hold the Line (block 4 emerging Vek in 1 turn); Lightning War (finish first 2 islands in under 30 min) |
| Steel Judoka | 3 | Archive | Mass Displacement (push 3 enemies with 1 attack); Unwitting Allies (4 enemies die from enemy fire in 1 battle); Unbreakable (mech armor absorbs 5 damage in 1 battle) |
| Flame Behemoths | 3 | R.S.T. | Scorched Earth (end battle with 12 tiles on fire); Quantum Entanglement (teleport unit 4 tiles with Swap Mech, both upgrades); This is Fine (5 enemies on fire simultaneously) |
| Frozen Titans | 3 | Pinnacle | Cryo Expert (fire Cryo-Launcher 4× in 1 battle); Pacifist (kill <3 enemies in 1 battle); Trick Shot (kill 3 enemies with 1 Janus Cannon shot) |
| Hazardous Mechs | 4 | Detritus | Healing (heal 10 mech HP in 1 battle); Overkill (8 damage to a unit in 1 attack); third achievement unconfirmed — verify in-game. [Single source — verify · class: community] |
| Bombermechs (AE) | 4 | — | Hold the Door (block 30 emerging Vek by end of island 2); No Survivors (7 units die in 1 turn); Powered Blast (pierce Walking Bomb with AP Cannon to kill enemy) |
| Arachnophiles (AE) | 4 | — | Spider Breeding (spawn 15 Arachnoids in 1 island); Working Together (Area Shift 4 units at once); Efficient Explosives (kill 3 enemies with 1 Ricochet Rocket) |
| Mist Eaters (AE) | 4 | — | Stay With Me! (heal 12 damage over 1 island); Let's Walk (move enemies 120 spaces with Control Shot in 1 game); On the Backburner (4 damage with Reverse Thrusters) |
| Heat Sinkers (AE) | 4 | — | Boosted (boost 8 mechs in 1 mission); Feed the Flame (light 3 enemies on fire with 1 attack); Maximum Firepower (8 damage with 1 Quick-Fire Rockets activation) |
| Cataclysm (AE) | 4 | — | Unstable Ground (crack 10 tiles in 1 mission); Core of the Earth (drop 10 enemies into pits in 1 island); Miner Inconvenience (destroy 20 mountains in 1 game) |
| Secret Squad | 25 (all 8 named squads must also be owned) | — | Gates Cyborg pilot access; Techno-Beetle / Hornet / Scarab mechs |

_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

### Pilot locks (P2)

| Lock type | Pilots | Key | Notes |
|---|---|---|---|
| Available from run start | Ralph Karlsson (default) | None | Default pilot for first timeline. |
| CorPilots (generic, no special ability) | Island-affiliated generics | None | Fill empty mech slots each timeline. |
| Named pilots (time-pod / Perfect Island pool) | Abe Isamu, Camila Vera, Bethany Jones, Archimedes, Isaac Jones, Chen Rong, Henry Kwan, Gana, Harold Schmidt, Lily Reed, Prospero, Silica, and others | Random time pod content or Perfect Island reward | Once recovered, permanently available in the hangar across timelines. NOT achievement-gated. |
| Secret FTL pilots | Ariadne (+3 HP, immune to Fire), Kazaaakpleth (2-damage melee replaces Repair), Mafan (+1 Reactor Core, reduce mech HP to 1, gain Shield every turn) | Strange Pod via "Distant Friends" event (islands 2/3/4; 15% chance per run; 1 per timeline) | Entity-hidden: yes; spoiler: progression. See `crew/` for full pilot files. |
| Cyborg pilots | Randomly-named Vek-hybrid pilots | Secret Squad unlocked | Cannot equip normal pilots; lose 25 XP when disabled. |

_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: progression_

### Time pod content (P2)

| Aspect | Behavior |
|---|---|
| Guaranteed reward | Every recovered Time Pod always yields 1 Reactor Core. |
| Bonus reward | Plus a chance of a weapon, passive, or pilot; a core-only pod is the minimum. |
| Pod count | Islands 1–2: 1 pod each. Islands 3–4: 2 pods each (count includes any Strange Pod). |
| Strange Pod spawn | 15% chance to replace a Time Pod on islands 2/3/4 only; never island 1; never on Corporate Tower (boss) missions; max 1 per timeline. Found by breaking a faintly glowing tile (a beacon), then moving a mech onto the resulting Strange Pod and protecting it. Rewards a secret FTL pilot and the "Distant Friends" achievement. See SEQ-001 / SEQ-005. |
| Mutually exclusive | A beacon and a regular Time Pod never coexist in the same mission. |

_source: deep-research P2 handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 1 · category: mainline · spoiler: progression_
