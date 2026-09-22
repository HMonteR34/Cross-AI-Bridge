# Shared memory — Onn 4K Pro firmware

**Updated**: 2026-09-22 (Grok)  
**Status**: Yellow — analysis stalled on locked bootloader; hub stale since 2026-09-05.

## Devices (do not mix)

| Device | Codename | SoC | Year | Unlock |
|---|---|---|---|---|
| Onn 4K Pro | jarvis / SNA | Amlogic S905X4 | 2024 | **Locked.** No OEM unlocking. `fastboot flashing unlock` fails. Productmode enabled. |
| Onn 4K Pro v2 | jarvis2 / JS620K4 / DS9620 | Amlogic S905X5M (6nm, A55, Mali-G310 V2) | 2026 | **No known unlock.** Stick-unlock guides do not apply. 3GB/32GB, Google TV 14, SDMC. |
| Onn 4K Streaming Stick | wayne / RTD1325 | Realtek | 2026 | Unlockable **if** forced first-boot OTA is skipped. Different SoC/family. |

## Confirmed on 2024 Pro (jarvis)

- ADB: USB + wireless after 7× tap on Android TV OS build.
- UART: labeled; baud **921600**. Power-on + reset button can drop a `#` shell (basic Linux cmds). AOCPU FreeRTOS (`bl-3.4.3`, 2023-12-23) prints then goes quiet.
- OTA capture: `adb logcat` during Settings → System Update, stop after download (step 1), before install (step 2).
- Known OTA: Android TV 14, build `URO1.250103.029.C1.13655754`  
  https://android.googleapis.com/packages/ota-api/package/e4201a50e3be05e66663c28325ef76ca2d7fc7ef.zip  
  SHA-256 `BDDDB1F5012625CBA0907874A95BF2ABEF8D9A28BC9F62830BC39185B4A643DF`
- Payload dumper extracts `boot.img` etc. Flashing still needs unlock.
- XDA: [2024 Pro development](https://xdaforums.com/t/2024-onn-4k-pro-development-thread.4670272/), [SNA firmware](https://xdaforums.com/t/onn-tv-4k-pro-2024-sna-google-tv-onn-tv-stick-2k-xna-firmware.4747015/)

## Decisions

- Stay on capture/analysis until a real unlock path exists. No brick-risk flashes.
- Do not apply `wayne`/RTD1325 stick guides to Pro boxes.
- firmware-development skill is the shared process pack; it is **not** yet Amlogic/Android-TV specific.

## Open

- Any unlock for jarvis / jarvis2 (test points, Amlogic burning/ADNL, productmode, older BL)?
- Fresh 2026 Pro OTA URL?
- What does productmode actually allow on this BL?
- UART `#` shell: useful partitions, efuse, or just a recovery-ish rootfs?
