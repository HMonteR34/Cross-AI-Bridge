# Shared memory — Onn 4K Pro firmware

**Updated**: 2026-10-01 01:22 CDT (Grok)  
**Target (user-confirmed)**: **Onn 4K Pro — `jarvis`** (2024 SNA / S905X4 unless About later contradicts)  
**Status**: Yellow — locked bootloader; analysis/capture only. Live About dump in.

## Live unit (2026-10-01, About screen, no ADB)

User read **Settings → System → About** with the remote (no phone, no computer):

| Field | What they read | Notes |
|---|---|---|
| Model | **Pro** | Confirms 4K Pro, not stick / Plus / 2023 4K-only |
| Android TV OS build prefix | **`URO4.`** | Not the older `URO1.` C1 line |
| Last section | **`15051976`** | Incremental / build id |

**Reconstructed build (public match, middle not typed):** `URO4.260304.011.B1/15051976`  
Security patch **2026-03-01**; that pairing is documented on other Onn SKUs (2023 4K `YOC`, 2K stick `XNA`). **Not previously catalogued for jarvis.** Treat as this unit’s current About fingerprint until a full `getprop` exists.

Codename `jarvis` is from the user’s earlier confirmation, not from this About read.

## Target device

| Field | Value |
|---|---|
| Product | Onn 4K Pro |
| Codename | **jarvis** (user, 2026-09-22) |
| Board / SKU | SNA (2024 Pro) |
| SoC | Amlogic S905X4 (2024 Pro) |
| This unit’s About | `URO4.` … `/15051976` |
| Bootloader | **Locked.** productmode enabled (2024 Pro public reports). |
| ADB | USB + wireless after 7× tap — needs a computer (user has none right now) |
| UART | Labeled pads, **921600**. Needs a USB-UART adapter. |

Do **not** mix:

| Other | Why ignore for this unit |
|---|---|
| 2026 Pro `jarvis2` / S905X5M | Different SoC. About also says “Pro”; jarvis call is the distinguisher until getprop. |
| Stick `wayne` / RTD1325 | Not a Pro box. |

## Known OTAs

**This unit now (inferred):** `URO4.260304.011.B1/15051976` — zip not yet captured for jarvis.

**Older public jarvis OTA:**
- `URO1.250103.029.C1.13655754` (`onn/jarvis/SNA:14/...`)
- https://android.googleapis.com/packages/ota-api/package/e4201a50e3be05e66663c28325ef76ca2d7fc7ef.zip
- SHA-256 `BDDDB1F5012625CBA0907874A95BF2ABEF8D9A28BC9F62830BC39185B4A643DF`

XDA: [2024 Pro development](https://xdaforums.com/t/2024-onn-4k-pro-development-thread.4670272/) · [SNA firmware](https://xdaforums.com/t/onn-tv-4k-pro-2024-sna-google-tv-onn-tv-stick-2k-xna-firmware.4747015/)

## Decisions

- Capture/analysis only. No flashing.
- No computer/phone → no ADB/UART until hardware exists. About-screen reads are valid captures.
- firmware-development skill stays generic.

## Open (this unit)

- Full About string / `ro.build.fingerprint` to confirm middle `260304.011.B1`.
- Public OTA zip for jarvis URO4, if any.
- productmode, UART `#` shell — parked until a PC exists.
