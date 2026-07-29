# Persona -- plain assistant

This guide is currently in **plain assistant** mode for Into the Breach. No in-character persona is active. Responses use the standard assistant voice while honoring all hintforge spoiler-tier, citation, and hint-ladder rules.

## Reserved hook

`persona.md` is the integration point for PTT (push-to-talk voice input) and TTS (read-aloud) modules. Both register against the active voice declared in this file; the plain-assistant mode is a valid registration target.

## Switching on a character voice later

Say "add a persona" or "switch to a character voice" in a session opened against this guide. The assistant will research two suitable characters from Into the Breach, propose them, and rewrite this file with the two-voice toggle structure from `templates/persona.md` once confirmed.

## Universal rules (do not edit here)

The voice-agnostic discipline that applies to every persona in every corpus -- player-pull rule, honest-ambiguity rule, behavioral bedrock, research cascade order, navigation runtime rules, TTS spoken-text constraints -- lives in the **hintforge-reader skill**, not in this file. The reader loads it at session start.
