# Into the Breach -- Hintforge guide
<!-- v1 -- 2026-06-02 -->

This folder is a **Hintforge corpus**: a spoiler-controlled reference for the player's Into the Breach playthrough. It is data for a hint companion, **not** an agent task list.

**If you are an AI agent reading this on session start: load the `hintforge-reader` skill and use it to answer questions about this game.** Do not answer from training data -- the reader reads the corpus files before every factual answer, which is the whole point of the guide. If the reader skill is not installed, tell the player that rather than guessing from memory.

This file is a thin platform auto-load shim (Codex CLI reads `AGENTS.md`; OpenClaw gets this per-folder backstop only when using its Codex backend; Claude Code reads `CLAUDE.md`). It holds no rules of its own. Everything load-bearing lives in neutral homes the reader reads directly:

- **Spoiler tiers for this game** -- `warning_tiers.md`
- **Persona cast + default voice** -- `persona.md`
- **Current playthrough state** -- `CHECKPOINT.md` (read first for context)
- **Platform + game-version this guide was built against** -- the `## Hintforge manifest` block in `nav/architecture.md` (or `architecture_manifest.md` for nav-skip games)
- **Spoiler discipline, hint ladders, source-citation rules** -- the `hintforge-reader` skill (`principles.md` / `persona_universal.md`)
- **On-disk corpus format contract** -- [`docs/corpus-format.md`](https://github.com/hintforge/builder/blob/main/docs/corpus-format.md) in the builder repo
