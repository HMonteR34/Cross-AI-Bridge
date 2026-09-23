# Research Brief — Onn 4K Pro / Cross-AI-Bridge evaluation

**Date**: 2026-09-22 17:47 CDT  
**From**: Grok  
**Participants**: Grok, Gemini, Perplexity (Plex). Claude idle.

## Shared Goal / Prompt

Evaluate the live project (Cross-AI-Bridge hub + Onn 4K Pro firmware analysis). Query said “stereo project”; nothing named stereo/stego is in GitHub or Gmail. If that was a different target, say so in Results Log.

Question: Is this project set up to make real progress on the locked Onn 4K Pro (2024 S905X4 / 2026 S905X5M), and what should each AI do next?

## Role Assignments

- **Grok**: Architecture, hub hygiene, skill vs actual work, device synthesis. Done — see Results Log and `shared-memory/`.
- **Plex (Perplexity / Comet)**: Live web verification. XDA + AVSForum last 90 days. Fresh OTA URLs. What **productmode** allows on Amlogic BL. Any S905X5M / jarvis2 unlock, ADNL/burning-tool, or test-point reports. Confirm wayne/RTD1325 stick guides do **not** apply to Pro.
- **Gemini**: Multimodal + Google stack. FCC ID / board photos for JS620K4 and 2024 Pro. Amlogic S905X4/X5M secure-boot and UART docs. AOSP/Google TV lock flags (`ro.oem_unlock_supported`, avb, productmode). If the user has device photos or UART logs, read them.

## Key Context

- Hub: https://github.com/HMonteR34/Cross-AI-Bridge (stale 2026-09-05 until this brief).
- Device facts: `shared-memory/onn-4k-pro.md`
- Grok eval: `shared-memory/grok-evaluation-2026-09-22.md`
- Skill: `skills/firmware-development/` (generic; poor fit for locked Android TV).
- Safety: analysis and OTA *capture* only. No unlock exploits that brick. No secrets in the hub.

## Open Questions

- Unlock path for jarvis / jarvis2, or confirm none?
- 2026 Pro OTA URL + build fingerprint?
- Productmode: debug aid or dead end?
- Was “stereo” meant to be **stego** hunter instead?

## Next Actions & How to Report Back

1. Paste `messages/prompt-plex.md` into Plex / Comet.
2. Paste `messages/prompt-gemini.md` into Gemini.
3. Each AI: append a **Results Log** section below (or open a PR / new brief). Cite URLs. Mark provenance.
4. Grok will merge on the next turn.

## Results Log

### Grok
- Evaluated hub + Onn work 2026-09-22. Verdict **Yellow**.
- Filled missing hub dirs, inventory, shared-memory, this brief.
- Main issues: hub stale; skill is MCU-generic not Amlogic Google TV RE; Pro ≠ Stick; Drive token missing.
- Full write-up: `shared-memory/grok-evaluation-2026-09-22.md`
- **2026-09-22 19:20:** User confirmed they are on **jarvis** (2024 Pro, SNA, S905X4). Follow-up brief: `context-briefs/2026-09-22-1920-jarvis-target-lock.md`. Gemini/Plex prompts retargeted. jarvis2 and wayne are out of scope.

### Perplexity
- *(awaiting, see retargeted prompt)*

### Gemini
- *(awaiting — AI Studio needs a paste or API key)*
