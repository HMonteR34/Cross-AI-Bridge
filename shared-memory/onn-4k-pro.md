# Shared memory — Onn 4K Pro firmware

**Updated**: 2026-09-22 19:20 CDT (Grok)  
**Target (user-confirmed)**: **2024 Onn 4K Pro — `jarvis` / SNA / Amlogic S905X4**  
**Status**: Yellow — locked bootloader; analysis/capture only.

## Target device

| Field | Value |
|---|---|
| Product | Onn 4K Pro (2024) |
| Codename | **jarvis** |
| Board / SKU | SNA |
| SoC | Amlogic S905X4 |
| OS | Google TV (Android TV 14 lineage on known OTA) |
| Bootloader | **Locked.** No OEM unlocking. `fastboot flashing unlock` / `fastboot oem unlock` fail. **productmode enabled.** |
| ADB | USB + wireless after 7× tap on Android TV OS build |
| UART | Labeled pads, **921600**. Normal boot: AOCPU FreeRTOS then quiet. Power-on **+ reset** can drop a `#` shell (basic Linux). |

Do **not** treat these as the same box:

| Other | Why ignore for this unit |
|---|---|
| 2026 Pro `jarvis2` / JS620K4 / S905X5M | Different SoC, different BL. Research only as contrast. |
| 2026 Stick `wayne` / RTD1325 | Realtek. Stick unlock-before-OTA does **not** apply. |

## Known jarvis OTA

- Build: `URO1.250103.029.C1.13655754` (`onn/jarvis/SNA:14/...`)
- https://android.googleapis.com/packages/ota-api/package/e4201a50e3be05e66663c28325ef76ca2d7fc7ef.zip
- SHA-256 `BDDDB1F5012625CBA0907874A95BF2ABEF8D9A28BC9F62830BC39185B4A643DF`
- Capture: `adb logcat` during System Update, stop after download (step 1), before install (step 2). Payload-dumper can extract `boot.img`; flashing still needs unlock.

XDA: [2024 Pro development](https://xdaforums.com/t/2024-onn-4k-pro-development-thread.4670272/) · [SNA firmware](https://xdaforums.com/t/onn-tv-4k-pro-2024-sna-google-tv-onn-tv-stick-2k-xna-firmware.4747015/)

## Decisions

- User is on **jarvis**. Gemini/Plex briefs retargeted 2026-09-22 19:20.
- Capture/analysis only. No brick-risk flashes.
- firmware-development skill stays generic until an Amlogic/Google-TV pack exists.

## Open (jarvis only)

- What productmode actually allows on this BL.
- UART `#` shell: partitions / proc / useful or dead.
- Newer jarvis OTA than URO1.250103.029.C1?
- Test points / ADNL / burning tool: any *jarvis* report, not stick/jarvis2.
