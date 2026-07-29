# Into the Breach -- Limitations & Blocked Sources

Sources I found that look useful but couldn't fully fetch -- paywalls, Cloudflare, age gates, video-only content, etc. URLs preserved so the player (or another contributor) can open them in a real browser.

## How to read this file
- Each entry: topic, URL, block type, what I could glean, best alternative I did get to.
- Each per-topic file (in `crew/`, `items/`, `sections/`) also lists its own blocked sources at the bottom -- the player rarely needs to come hunting here.
- This file is the catch-all for sources that didn't fit a specific topic.

## Block types
- **paywall** -- content gated behind a subscription or article limit
- **cloudflare** -- Cloudflare bot challenge / 403 / 503 from WebFetch
- **video-only** -- YouTube or other video where the answer is shown visually; no readable text equivalent
- **age-gate** -- content blocked behind age verification
- **cookie-wall** -- popup or consent flow that broke the fetch
- **search-snippet-only** -- search engine returned a snippet but the page itself wasn't reachable
- **dead-link** -- URL was in another source but no longer resolves

## Entries

### P1 research gaps & unresolved conflicts (2026-06-02)

These are not blocked *sources* but facts the P1 cascade could not nail down. Recorded here so a future phase / live observation can close them.

- **Default key bindings (Undo Move, Reset Turn, zoom, mech-cycle):** not corroborated in documentation. Only the A/S/D mech-select scheme and Spacebar (End Turn) / Alt (overlay) / Ctrl (info) / tilde (console) are confirmed. The P1 brief's "Tab/Q/E cycle" is unconfirmed. See `controls.md`. — *block type: search-snippet-only*
- **Controller per-button map:** native controller support confirmed, but the exact default button layout could not be confirmed. See `controls.md`.
- **Colorblind mode presets:** colorblind mode confirmed present, but whether it has multiple presets (protan/deutan/tritan) or a single toggle is unconfirmed. Single source. See `settings.md`.
- **UI font sizes:** appears to be a small/big toggle rather than a continuous scale slider. Single source. See `settings.md`.
- **Mid-run difficulty change:** undocumented (likely locked per timeline). See `settings.md`.
- **Renfield Bomb HP (final battle):** Fandom states 4 HP; GameFAQs states 5 HP. Both agree it arms over 5 turns, doesn't explode at 0, and auto-replaces (adding 2 turns). Conflict unresolved. See `sections/volcanic_hive.md`. — *block type: dead-link n/a — source disagreement*
- **Vendor weapon cost:** ~~Resolved in P2 ingestion 2026-06-02.~~ The 2020 v1.2 patch set cost to 1 rep; the 2022 Advanced Edition increased it back to 2 rep. Corpus updated to 2 rep; AE patch notes are authoritative. See `mechanics.md`.
- **Pinnacle shield-generator interaction** (destroying it removes all pilot-granted shields except Mafan's): single source / wiki. See `sections/pinnacle_robotics.md`.
- **Mech base-stat "best" trivia** (Thruster/Drill flying, Judo armored, Pitcher HP): single source / wiki trivia. See `items/weapons.md`.
- **"Distant Friends" hidden flag:** likely hidden on Steam but not positively confirmed from the achievement API. See `achievements.md`.
- **Hazardous Mechs third squad achievement:** P2 research pinned two of the squad's three achievements (Healing, Overkill) but could not confirm the name/precise trigger of the third (described as a "victory-type" achievement). Verify against in-game achievement list. See `achievements.md`. — *block type: search-snippet-only*
- **Per-island weapon stock count (vendor):** island 1 confirmed at 2 weapons; islands 2–4 widely reported as 3/4/4 by community but lacks an authoritative source (AE notes only confirm "limited in first 2 islands"). Treat 3/4/4 as hypothesis pending datamining. See `architecture_manifest.md` Support Topology. — *block type: hypothesis*

## Always-blocked categories

- **Randomized mission layouts:** Into the Breach generates mission layouts procedurally. Specific enemy spawn positions and objectives vary per run. No source documents these definitively; per-session tactical advice must come from live observation.
- **In-game event text (full verbatim):** Subset Games holds copyright on in-game dialogue and event descriptions. Sources paraphrase; verbatim transcripts are not archived publicly.
