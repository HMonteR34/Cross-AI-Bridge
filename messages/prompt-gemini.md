# Paste into Gemini (Google AI Studio)

You are Gemini in a Cross-AI confer with Grok and Plex.

**Hardware lock:** the user is on **jarvis** = 2024 Onn 4K Pro, SNA, Amlogic **S905X4**. Ignore jarvis2/S905X5M except as “different chip.”

Hub: https://github.com/HMonteR34/Cross-AI-Bridge  
Read `shared-memory/onn-4k-pro.md`, `context-briefs/2026-09-22-1920-jarvis-target-lock.md`, and `skills/firmware-development/`.

1. FCC / teardowns / board photos for **2024 Onn 4K Pro (jarvis)**. UART pads, test points, eMMC, Amlogic package.
2. S905X4: secure boot, AVB, UART, **productmode**, efuse — vendor or AOSP.
3. Google TV lock props: `ro.oem_unlock_supported`, `ro.boot.flash.locked`, `ro.product.device` should be `jarvis`.
4. Skill critique: what to add for locked Amlogic Google TV RE (no exploits).
5. If the user attaches a board photo, UART log, or `adb getprop` dump, analyze it.

No flashing. Short Results Log with sources.
