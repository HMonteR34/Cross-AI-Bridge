# Cross-AI Bridge Hub

Collaboration hub for sharing skills, context briefs, ability inventories, and project state across Perplexity (Comet / “Plex”), Gemini, Claude, and Grok.

**GitHub**: https://github.com/HMonteR34/Cross-AI-Bridge  
**Local hub**: `/home/workdir/artifacts/Cross-AI-Bridge/`

## Structure

```
Cross-AI-Bridge/
├── README.md
├── ability-inventory.json
├── skills/firmware-development/
├── context-briefs/
├── shared-memory/
├── connectors-status/
└── messages/
```

## Active project

**Onn 4K Pro firmware analysis** (2024 `jarvis`/SNA S905X4 and 2026 `jarvis2`/JS620K4 S905X5M). Locked bootloader, productmode, ADB + UART, OTA capture. Not the 2026 Streaming Stick (`wayne` / RTD1325), which is a different unlock story.

Latest confer: `context-briefs/2026-09-22-1747-onn-firmware-confer-gemini-plex.md`

## How to use from another AI

1. Clone this repo.
2. Read `ability-inventory.json` and `shared-memory/onn-4k-pro.md`.
3. Load `skills/firmware-development/SKILL.md`.
4. Append findings under **Results Log** in the latest brief, or drop a note in `messages/`.
