# Into the Breach — Hintforge Companion

![Into the Breach companion status — coverage, how current it is, and spoiler control](assets/readme-status-card.svg)

A spoiler-controlled hint companion for **Into the Breach**, Subset Games' turn-based mech tactics roguelike where you defend islands from the Vek — and reset the timeline when a run goes wrong. Built in the [Hintforge](https://github.com/hintforge/builder) format: a loyal sidekick that answers only from these guide files — never from guesswork — at the spoiler level you set.

## Use it

You need a Hintforge reader running in Claude Code, Codex, or OpenClaw. Point it at this repo:

> Load the Into the Breach guide from github.com/hintforge/into-the-breach

Then just ask — *"how does this squad play," "how do I clear this turn," "which pilot is worth it."* Runtime setup lives in [`hintforge/reader`](https://github.com/hintforge/reader).

## Spoilers

**You** set two independent dials — enemy warnings (Tier 0–5) and puzzle-hint warnings (Tier 0–3) — both **silent by default**; the guide volunteers nothing until you raise one. The game is fully deterministic, so hints are exact rather than probabilistic. There's no save-state reader, so every answer comes from this guide's files.

## What's inside

A structured Markdown corpus — every squad (mechs, weapons, pilots), the core tactics/grid mechanics, weapons, and all achievements. Interactive tools (a grid battle sandbox — the perfect fit for a fully deterministic game) aren't built yet. The companion reads and writes only the files you control.
