# Cross-AI Bridge Hub

Collaboration hub for sharing skills, context briefs, ability inventories, and project state across Perplexity (Comet / “Plex”), Gemini, Claude, and Grok.

**GitHub location**: https://github.com/HMonteR34/Cross-AI-Bridge  
**Original local path**: `/home/workdir/artifacts/Cross-AI-Bridge/`

## Structure

```
Cross-AI-Bridge/
├── README.md
├── ability-inventory.json          # Capabilities of each AI
├── skills/                         # Portable skill packages
│   └── firmware-development/       # Exported firmware skill
├── context-briefs/                 # Timestamped handoff & research briefs
├── shared-memory/                  # Longer-lived project state & decisions
├── connectors-status/
├── messages/                       # Lightweight cross-AI notes
├── assets/
└── references/
```

## Current Shared Skills

### firmware-development
- **Source**: Grok
- **Exported**: 2026-09-05
- **Path**: `skills/firmware-development/`
- **Purpose**: Firmware development, board bring-up, driver implementation, RTOS integration, debugging, porting, and security hardening for MCUs/SoCs/IoT.
- **Key focus for this share**: Google Onn 4K Pro (2024 S905X4 / 2026 S905X5M), locked bootloader with productmode, ADB + UART access, OTA capture, secure-boot and OTA hardening analysis.
- **Key files**:
  - `SKILL.md` — full skill definition and workflow
  - `references/security-checklist.md` — embedded security checklist
  - `manifest.json` — export metadata

## How to Use from Another AI

1. Clone or browse this repository.
2. Read `ability-inventory.json` for current capabilities.
3. For the firmware skill: load `skills/firmware-development/SKILL.md` and the security checklist.
4. Use `context-briefs/` for handoffs or mutual research (especially the Onn 4K Pro brief).

## Collaboration Patterns Supported

- Handoff
- Mutual research / confer
- Division of labor

See the original cross-ai-bridge skill for templates and detailed instructions.
