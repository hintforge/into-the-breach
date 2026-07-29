# Into the Breach -- Crew (Pilot Roster)

**status:** research-integrated
**last_reconciled:** 2026-06-02
**class:** crew

Pilot roster for Into the Breach. Pilots are named individuals who occupy mech cockpits, carry a unique innate passive, and level up during runs (1 XP per Vek HP killed; bonus skill at 25 XP, second at 75 XP). The "Last Traveler" can persist to the next timeline via the time-travel mechanic. Per-pilot detail lives in `crew/<pilot>.md`; ability mechanics in `items/abilities.md`; pairings in `items/builds.md`.

## How pilots work

XP = 1 per Vek HP killed. First skill at 25 XP, second at +50 (75 total cap). Bonus skills are randomized at timeline start. Artificial (A.I.) pilots gain no XP. One surviving pilot (the "Last Traveler") carries their XP and skills into a future run. [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> **Cross-system dependency** -- see `dependencies.md` DEP-001: XP income is capped by Vek HP killed per battle; neutralizing Vek without kills yields no XP progress toward bonus skills.

## Strongest pilots (community consensus)

Abe Isamu (Armored — survivability for max-leveling), Camila Vera (Evasion helps the whole squad vs. webs/smoke), Gana (Preemptive Strike), Henry Kwan (move through units; strong on Unfair). [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

## Roster

| entity-id | display name | affiliation | innate skill | acquisition | status |
|---|---|---|---|---|---|
| ralph_karlsson | Ralph Karlsson | None | Experienced (+2 bonus XP/kill) | Default; after 100% any island | research-integrated |
| harold_schmidt | Harold Schmidt | Archive | Frenzied Repair | Perfect island / time pod | research-integrated |
| abe_isamu | Abe Isamu | R.S.T. | Armored | Perfect island / time pod | research-integrated |
| bethany_jones | Bethany Jones | Pinnacle | Starting Shield | Perfect island / time pod | research-integrated |
| henry_kwan | Henry Kwan | Detritus | Maneuverable | Perfect island / time pod | research-integrated |
| gana | Gana | Archive | Preemptive Strike | Perfect island / time pod | research-integrated |
| prospero | Prospero | Detritus | Flying | Perfect island / time pod | research-integrated |
| lily_reed | Lily Reed | Archive | Impulsive (+3 Move first turn) | Perfect island / time pod | research-integrated |
| chen_rong | Chen Rong | Detritus | Sidestep | Perfect island / time pod | research-integrated |
| camila_vera | Camila Vera | R.S.T. | Evasion | Perfect island / time pod | research-integrated |
| isaac_jones | Isaac Jones | Pinnacle | Temporal Reset (+1 reset) | Perfect island / time pod | research-integrated |
| silica | Silica | R.S.T. | Double Shot | Perfect island / time pod | research-integrated |
| archimedes | Archimedes | Pinnacle | Fire-and-Forget | Perfect island / time pod | research-integrated |
| kai_miller | Kai Miller (AE) | — | Arrogant Boost | Perfect island / time pod | research-integrated |
| rosie_rivets | Rosie Rivets (AE) | — | Reassuring Hand | Perfect island / time pod | research-integrated |
| morgan_lejeune | Morgan Lejeune (AE) | — | Field Research (Boost on kill) | Perfect island / time pod | research-integrated |
| adam | Adam (AE) | — | Chosen One | Perfect island / time pod | research-integrated |
| kazaaakpleth | Kazaaakpleth (secret) | — | Mantis (2-dmg melee replaces Repair) | Strange Pod (random) | research-integrated |
| mafan | Mafan (secret) | — | +1 Reactor, HP→1, Shield every turn | Strange Pod (random) | research-integrated |
| ariadne | Ariadne (secret) | — | Rockman (+3 HP, Fire-immune) | Strange Pod (random) | research-integrated |

**Cyborg pilots** (generic, not a named individual): available only after the Secret Squad is unlocked; normal pilots can't equip cyborg slots, and a cyborg loses 25 XP if disabled. Not given a per-entity file (pilot-type, not a tracked individual). The three secret pilots are spoiler-gated (`late-game`; names themselves are FTL-crossover spoilers — see `sections/story_notes.md`).

## Pointer rules

- Per-pilot detail lives in `crew/<entity-id>.md`.
- Ability mechanics and learnable bonus skills: `items/abilities.md`.
- Pilot-mech pairings and builds: `items/builds.md`.
- Pilot fates and the FTL crossover: `sections/story_notes.md` (story-gated).
