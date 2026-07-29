# Into the Breach -- Achievements

**status:** research-integrated
**last_reconciled:** 2026-06-02
**stub_source:** vgtimes.com (mirroring Steam appid 590380)
**stub_fetched:** 2026-06-02

70 achievements (55 base + 15 Advanced Edition). Each grants 1 Coin (spent to unlock squads; the last 5 coins cannot be spent). **Coverage: 70/70 resolved, 0 deferred, 0 unreachable** — there is no paid DLC. Reorganized from the flat stub list into the six `trigger_type` sections below (the `branch` section is omitted — Into the Breach has no mutually-exclusive achievements).

**Conventions:** Squad-specific achievements have **PoNR = squad selection at run start** (you must pick that squad). Run-condition achievements fail mid-run if the condition is broken. The Secret Squad itself has NO achievement (it is the reward for the others).
> **Cross-system dependency** -- see `dependencies.md` PON-001: Squad selection at run start locks out all squad-specific achievements for other squads for that run.

## Genre vocabulary

- `roguelike` — run-bound / cross-run / meta-progression achievements (Into the Breach tracks several totals "across all games").
- `meta` — easter-egg / fourth-wall / crossover (FTL).

---

## Progression

Every player who reaches the milestone earns these on the default path.

| Achievement | Trigger | Missable / PoNR | Vector-binding |
|---|---|---|---|
| Victory | Beat the game (complete the final battle, any run length) | none | `sections/volcanic_hive.md` |
| Emerging Technologies | Unlock a new Mech Squad (spend Coins) | none | `mechanics.md` (squad system), `items/builds.md` |
| Field Promotion | Have a pilot reach maximum level | none | `crew/index.md` |
| Island Secure | Complete the 1st Corporate Island with the Rift Walkers | PoNR: select Rift Walkers | `items/builds.md`, `sections/` |

---

## Mastery

Skill feats or self-imposed restrictions beyond normal play. Each pairs the constraint with a strategy pointer.

| Achievement | Trigger | Missable / PoNR | Vector-binding |
|---|---|---|---|
| Hard Victory | Beat the game on Hard | prereq: difficulty Hard (locked per timeline) | `settings.md` |
| Perfect Island | No failed objective on one island | fails on any missed objective | `sections/missables.md` |
| The Defenders | Finish an island with no building damage | fails on any building damage | `sections/` |
| Untouchable | Finish an island with no mech damage (repaired damage still counts) | fails if any mech is damaged | `mechanics.md` |
| Best of the Best | 3 pilots at max level simultaneously | none | `crew/index.md` |
| Sustainable Energy | Finish 3 islands without dropping below 4 Grid Power | fails mid-run if grid <4 | `mechanics.md` (power grid) |
| Engineering Dropout | Finish 3 islands without powering a weapon modification | fails on first weapon-mod power | `items/upgrades.md` |
| Chronophobia | Finish 3 islands and destroy every Time Pod discovered | fails if a pod is collected intact | `sections/missables.md` |
| There is No Try | Finish 3 islands without failing an objective | fails on first failed objective | `sections/` |
| Trusted Equipment | Finish 3 islands without equipping any new pilots or weapons | fails on first new equip | `items/`, `crew/` |
| Watery Grave | Drown 3 enemies in one battle (Rift Walkers) | PoNR: Rift Walkers | `sections/archive_inc.md` · see DEP-008 |
| Ramming Speed | Kill an enemy 5+ tiles away with a Dash Punch (Rift Walkers) | PoNR: Rift Walkers; needs Titan Fist Dash (2 cores) | `items/weapons.md` |
| Unbreakable | Mech Armor absorbs 5 damage in one battle (Steel Judoka) | PoNR: Steel Judoka | `items/abilities.md` |
| Unwitting Allies | 4 enemies die from enemy fire in one battle (Steel Judoka) | PoNR: Steel Judoka | `items/builds.md` |
| Mass Displacement | Push 3 enemies with one attack (Steel Judoka) | PoNR: Steel Judoka | `items/weapons.md` |
| Overpowered | Overpower the grid twice when full (Rusting Hulks) | PoNR: Rusting Hulks | `mechanics.md` |
| Stormy Weather | 12 Electric Smoke damage in one battle (Rusting Hulks) | PoNR: Rusting Hulks | `items/weapons.md` |
| Perfect Battle | No mech/building damage in one battle (Rusting Hulks) | PoNR: Rusting Hulks | `items/builds.md` |
| Quantum Entanglement | Teleport a unit 4 tiles (Flame Behemoths) | PoNR: Flame Behemoths | `items/weapons.md` |
| Scorched Earth | End a battle with 12 tiles on fire (Flame Behemoths) | PoNR: Flame Behemoths | `items/weapons.md` |
| This is Fine | 5 enemies on fire simultaneously (Flame Behemoths) | PoNR: Flame Behemoths | `items/builds.md` |
| Get Over Here | Kill an enemy by pulling it into yourself (Zenith Guard) | PoNR: Zenith Guard | `items/weapons.md` |
| Glittering C-Beam | Hit 4 enemies with one laser (Zenith Guard) | PoNR: Zenith Guard | `items/weapons.md` |
| Shield Mastery | Block with a Shield 4× in one battle (Zenith Guard) | PoNR: Zenith Guard | `items/abilities.md` |
| Cryo Expert | Fire the Cryo-Launcher 4× in one battle (Frozen Titans) | PoNR: Frozen Titans | `items/weapons.md` |
| Trick Shot | Kill 3 with one Janus Cannon (Frozen Titans) | PoNR: Frozen Titans | `items/weapons.md` |
| Pacifist | Kill <3 enemies in one battle (Frozen Titans) | PoNR: Frozen Titans | `items/builds.md` |
| Chain Attack | Chain the Electric Whip through 10 tiles (Blitzkrieg) | PoNR: Blitzkrieg | `items/weapons.md` |
| Lightning War | Finish Islands 1+2 under 30 min (Blitzkrieg) | PoNR: Blitzkrieg | `items/builds.md` |
| Hold the Line | Block 4 emerging Vek in one turn (Blitzkrieg) | PoNR: Blitzkrieg | `mechanics.md` |
| Healing | Heal 10 mech HP in one battle (Hazardous Mechs) | PoNR: Hazardous Mechs | `items/builds.md` |
| Immortal | Finish 4 islands with no mech destroyed at end of a battle (Hazardous Mechs) | PoNR: Hazardous Mechs; fails if any mech dies | `items/builds.md` |
| Overkill | 8 damage to a unit with one attack (Hazardous Mechs) | PoNR: Hazardous Mechs | `items/weapons.md` |
| Lucky Start | Beat the game without spending Reputation (Random squad) | PoNR: Random squad | `mechanics.md` (reputation) |
| Mech Specialist | Beat the game with 3 of the same Mech (Custom squad) | PoNR: Custom squad | `items/builds.md` |
| Class Specialist | Beat the game with 3 mechs of the same class (Custom squad) | PoNR: Custom squad | `items/builds.md` |
| Flight Specialist | Beat with 3 flying mechs (Custom squad — must fly by default; Prospero's grant doesn't count) | PoNR: Custom squad | `items/builds.md`, `crew/prospero.md` |
| No Survivors | 7 units (any team) die in one turn (Bombermechs) | PoNR: Bombermechs | `items/builds.md` |
| Powered Blast | Pierce a Walking Bomb with the AP Cannon to kill an enemy (Bombermechs) | PoNR: Bombermechs | `items/weapons.md` |
| Working Together | Area Shift 4 units at once (Arachnophiles) | PoNR: Arachnophiles | `items/weapons.md` |
| Efficient Explosives | Kill 3 with one Ricochet Rocket (Arachnophiles) | PoNR: Arachnophiles | `items/weapons.md` |
| On the Backburner | 4 damage with Reverse Thrusters (Mist Eaters) | PoNR: Mist Eaters | `items/weapons.md` |
| Feed the Flame | Light 3 enemies on fire with one attack (Heat Sinkers) | PoNR: Heat Sinkers | `items/weapons.md` |
| Maximum Firepower | 8 damage with one Quick-Fire Rockets activation (Heat Sinkers) | PoNR: Heat Sinkers | `items/weapons.md` |

---

## Collection

Complete a finite, enumerable set in full.

| Achievement | Trigger | Set | Vector-binding |
|---|---|---|---|
| Adaptable Victory | Beat the game once per each length (2, 3, 4 islands) | {2-island, 3-island, 4-island wins} — 3 runs | `architecture_manifest.md` |
| Squads Victory | Beat the game with 4 different squads | 4 distinct squads | `items/builds.md` |
| Complete Victory | Beat the game with all 10 primary squads | all 10 primary squads | `items/builds.md` |
| Come Together | Unlock 6 additional pilots | 6 distinct pilots | `crew/index.md` |

---

## Threshold

Cumulative counts with no finite-set ceiling. `genre: roguelike` on the cross-run ("across all games") totals.

| Achievement | Trigger | Scope | Vector-binding |
|---|---|---|---|
| Friends in High Places | Spend 50 Reputation | across all games (`genre: roguelike`) | `mechanics.md` (reputation) |
| Immovable Objects | Block 100 Vek | across all games (`genre: roguelike`) | `mechanics.md` |
| Humanity's Savior | Rescue 100,000 civilians | across all games (`genre: roguelike`) | `mechanics.md` (power grid) |
| Perfect Strategy | Collect 10 Perfect Island rewards | across all games (`genre: roguelike`) | `sections/missables.md` |
| I'm getting too old for this... | One pilot fights the final battle 3 times | across all games (use the Last Traveler; `genre: roguelike`) | `crew/index.md` |
| Backup Batteries | Earn/buy 10 Grid Power | on one island | `mechanics.md` |
| Good Samaritan | Earn 9 Reputation from missions | on one island | `mechanics.md` |
| Loot Boxes! | Open 5 Time Pods (Random squad) | in one game; PoNR: Random squad | `sections/missables.md` |
| Change the Odds | Raise Grid Defense to ≥30% (Random squad) | PoNR: Random squad | `mechanics.md` |
| Spider Breeding | Spawn 15 Arachnoids (Arachnophiles) | in one island; PoNR: Arachnophiles | `items/weapons.md` |
| Stay With Me! | Heal 12 damage (Mist Eaters) | over one island; PoNR: Mist Eaters | `items/builds.md` |
| Let's Walk | Move enemies with Control Shot 120 spaces (Mist Eaters) | in one game; PoNR: Mist Eaters | `items/weapons.md` |
| Boosted | Boost 8 mechs (Heat Sinkers) | in one mission; PoNR: Heat Sinkers | `items/abilities.md` |
| Hold the Door | Block 30 emerging Vek by the end of Island 2 (Bombermechs) | PoNR: Bombermechs | `mechanics.md` |
| Unstable Ground | Crack 10 tiles (Cataclysm) | in one mission; PoNR: Cataclysm | `items/weapons.md` |
| Core of the Earth | Drop 10 enemies into pits (Cataclysm) | on one island; PoNR: Cataclysm | `items/weapons.md` |
| Miner Inconvenience | Destroy 20 mountains (Cataclysm) | in one game; PoNR: Cataclysm | `mechanics.md` |

---

## Discovery

Found by deliberate exploration of a non-obvious mechanic; often hidden-flagged.

| Achievement | Trigger | Hidden | Vector-binding |
|---|---|---|---|
| Distant Friends | Encounter a familiar face — unlock a secret FTL pilot the legit way (Strange Pod; cheat-code unlocks do NOT count) | hidden-flag candidate (`genre: meta`) | `sections/missables.md`, `crew/kazaaakpleth.md` / `crew/mafan.md` / `crew/ariadne.md` |

---

## Sources

- https://vgtimes.com/games/into-the-breach/achievements-and-trophies/ (fetched 2026-06-02; mirrors Steam appid 590380)
- https://steamcommunity.com/stats/590380/achievements (canonical Steam URL — hidden-flag data for "Distant Friends" not positively confirmed; flagged as candidate)
