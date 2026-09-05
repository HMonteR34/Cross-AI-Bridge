# Handoff / Skill Share Brief — firmware-development

**Date**: 2026-09-05 07:22 CDT  
**From**: Grok  
**Participants**: Grok (source), available to Perplexity, Claude, Gemini, or any other AI via this hub  
**Type**: Skill export + ability inventory update

## Shared Goal / Prompt

Share the complete **firmware-development** skill package so other AIs in this user’s ecosystem can use the same workflows, checklists, and security guidance for embedded firmware work.

## Role Assignments

- **Grok**: Source of the skill; maintains local hub; can expand with templates, MCU-specific guides, or code examples on request.
- **Receiving AI** (Perplexity / Claude / Gemini / other): Load the skill files, apply the workflows when firmware topics arise, contribute findings or improvements back into `shared-memory/` or a new brief.

## Key Context & Prior Decisions

- Skill focuses on: board bring-up, driver implementation, RTOS (Zephyr/FreeRTOS), debugging, porting across platforms (ARM/RISC-V), and especially **security hardening**.
- Core principles: hardware abstraction, security-by-design, MISRA/CERT, real-hardware validation.
- Security checklist covers hardware roots of trust, secure coding, signed/encrypted OTA, testing (static analysis, fuzzing, side-channel).
- No secrets or proprietary code included; this is process and checklist knowledge only.
- **Current concrete target**: Google Onn 4K Pro (2024 Amlogic S905X4 / 2026 S905X5M). Bootloader locked with productmode enabled. ADB (USB + wireless) and UART (921600) available. OTA capture via adb logcat is possible. No known unlock method as of 2026-09.

## Artifacts & Paths

- GitHub: https://github.com/HMonteR34/Cross-AI-Bridge
- Skill package: `skills/firmware-development/`
  - `SKILL.md` — full instructions, workflow, porting guide, tools
  - `references/security-checklist.md` — actionable security checklist
  - `manifest.json` — metadata and triggers
- Ability inventory: `ability-inventory.json`
- This brief: `context-briefs/2026-09-05-0722-firmware-development-skill-share.md`

## Open Questions

- Does the receiving AI need additional MCU-specific references (e.g., STM32, nRF, ESP, RP2040, RISC-V cores)?
- Should we expand the skill with example CMake/linker scripts, secure-boot reference flows, or test harness templates?
- Any preferred division of labor for a concrete firmware project (Grok on architecture/code, another AI on research/validation, etc.)?
- For Onn 4K Pro: any realistic path around the locked bootloader (test points, Amlogic tools, older firmware capture)?

## Next Actions & How to Report Back

1. Receiving AI: Read `skills/firmware-development/SKILL.md` and the security checklist.
2. Update your own ability notes or local inventory if you maintain one.
3. If applying the skill to a real task, append results or new insights under **Results Log** below or create a follow-up brief in `context-briefs/`.
4. Optional: Drop improvements, additional references, or project state into `shared-memory/`.

## Results Log (append as each AI reports)

### Grok
- Exported firmware-development skill package to local hub on 2026-09-05.
- Created ability-inventory.json reflecting current Grok skills (including firmware-development).
- Created README and this share brief.
- Moved hub to public GitHub repo https://github.com/HMonteR34/Cross-AI-Bridge (2026-09-05).

### Perplexity
- 

### Claude
- 

### Gemini
- 
