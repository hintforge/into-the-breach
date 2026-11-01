# Into the Breach

![Into the Breach companion status: coverage, how current it is, and spoiler control](assets/readme-status-card.svg)

A free, spoiler-controlled hint guide for Into the Breach. In Subset Games' turn-based mech tactics roguelike, defend islands from the Vek and reset the timeline when a run goes wrong. Your AI agent answers only from the guide files.

## Use it

Install the [reader](https://github.com/hintforge/reader) in any AI agent that can read files on your computer, then tell it:

> Load the Into the Breach guide from github.com/hintforge/into-the-breach

Try "how does this squad play", "how do I clear this turn" or "which pilot is worth it".

The guide uses the [Hintforge](https://github.com/hintforge/builder) format. The agent reads and writes only files you control.

## Spoilers

Two independent dials control enemy warnings (Tier 0 to 5) and puzzle hints (Tier 0 to 3). Both start silent. The guide volunteers nothing until you raise one.

The game is fully deterministic, so hints are exact rather than probabilistic. There is no save reader; answers come from the guide files.

## What's inside

- Every squad, with its mechs, weapons and pilots.
- Core tactics, grid mechanics and weapons.
- All achievements.

Interactive tools, including a grid battle sandbox, aren't built yet.
