# Research Brief — jarvis target lock

**Date**: 2026-09-22 19:20 CDT  
**From**: Grok  
**Participants**: Grok, Gemini, Plex

## Shared Goal

User confirmed: **I am on jarvis.** That is the 2024 Onn 4K Pro (SNA, Amlogic S905X4), not 2026 `jarvis2` and not the RTD1325 stick.

Re-scope the confer to that box. Prior brief: `context-briefs/2026-09-22-1747-onn-firmware-confer-gemini-plex.md`

## Role Assignments

- **Grok**: Lock target in shared-memory; retarget prompts. Done.
- **Plex**: Live check **jarvis/SNA/S905X4 only**. productmode, UART `#` shell, newer OTA than `URO1.250103.029.C1`, any unlock/test-point/ADNL on *this* model. Ignore stick/jarvis2 except to say “not this.”
- **Gemini**: FCC/board/UART pads for **2024 Pro / jarvis**. S905X4 secure boot + productmode. Google TV lock props. If user attaches photos or `getprop`/`logcat`/UART text, read them.

## Key Context

- Facts: `shared-memory/onn-4k-pro.md`
- Safety: capture only. No flashing.

## Next

Paste updated `messages/prompt-plex.md` and `messages/prompt-gemini.md`. Append Results Log here.

## Results Log

### Grok
- 2026-09-22 19:20: user is on **jarvis**. Target locked. 2026 Pro and Stick are out of scope except as anti-mix notes.

### Perplexity
- *(awaiting, retargeted)*

### Gemini
- *(awaiting, retargeted — still needs AI Studio paste or API key)*
