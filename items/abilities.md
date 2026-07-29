# Into the Breach -- Abilities

**status:** research-integrated
**last_reconciled:** 2026-06-02

Pilot passive abilities, mech passive traits, and Advanced Edition skill additions. Per-pilot detail and acquisition live in `crew/`; this file is the ability-mechanic reference.

## Pilot passive abilities (innate)

Each named pilot has one innate passive; full per-pilot detail (acquisition, fates, synergies) is in `crew/<pilot>.md`. Innate skills span XP bonuses (Experienced), survivability (Armored, Starting Shield, Rockman), mobility (Maneuverable, Impulsive, Sidestep, Flying), and unique effects (Preemptive Strike, Double Shot, Fire-and-Forget, Temporal Reset). [Confirmed: 3 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> see crew/index.md for the full pilot roster and per-pilot ability summaries.

## Learnable bonus skills (base game)

Bonus skills are randomized per timeline; a pilot learns one at 25 XP and a second at 75 XP. Base pool: **+2 Mech HP**, **+1 Mech Move**, **+3% Grid DEF**, **+1 Mech Reactor**. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

## Advanced Edition bonus skills (if Advanced Pilot Abilities enabled)

Opener (Boost +2 Move first turn), Finisher (boost on last turn), Popular Hero (sells for 4 rep), Thick Skin (immune to ACID + Fire), Skilled (+1 Move +2 HP), Invulnerable (mech doesn't die when defeated), Adrenaline (+1 Move per kill), Masochist (+2 Move when not full HP), Technician (repair 1 HP at start of enemy turn), Conservative (+1 use for limited weapons). [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: high · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_

**Skill blacklists (rarely documented):** Ariadne and Mafan cannot learn +2 HP / Skilled / Masochist; cyborgs cannot learn Popular Hero / Invulnerable. Mafan (1 HP) has been blacklisted from HP skills since patch 1.0.17. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> **Cross-system dependency** -- see `dependencies.md` DEP-006: Mafan and Ariadne are blacklisted from HP-increasing bonus skills, constraining their build options.
> **Cross-system dependency** -- see `dependencies.md` DEP-007: Popular Hero bonus skill increases pilot sell value from +1 to +4 reputation.

**Late-game edge case:** an Invulnerable pilot whose mech is disabled in the final battle still dies (cannot teleport away). [Single source -- verify · class: wiki]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: low · enemy-tier: 2 · puzzle-tier: 1 · category: mainline · spoiler: late-game_

## Mech passive traits

Some mechs carry built-in passives beyond their weapon: **Natural Armor** (negate 1 damage; disabled by ACID), **Flying** (move over anything, immune to drowning), **Storm Generator** / **Flame Shielding** / **Viscera Nanobots** (heal on kill) / **Vek Hormones** (enemies deal +1 to other enemies) / **Heat Engines** / **Nanofilter Mending**, etc. These are noted inline per mech in `items/weapons.md`. [Confirmed: 2 sources]
_source: deep-research handoff 2026-06-02 · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
> **Cross-system dependency** -- see `dependencies.md` DEP-002: ACID status disables Natural Armor; mechs with Natural Armor lose their 1-damage-negation while afflicted.
> **Cross-system dependency** -- see `dependencies.md` DEP-010: Thick Skin (AE bonus skill) grants ACID immunity, making it a high-value pick for Detritus Disposal's ACID-heavy environment.
