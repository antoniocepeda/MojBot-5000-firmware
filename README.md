# MojBot 5000 Firmware

Firmware for the MojBot robot dog.

This repo contains the ESP32-side code that runs on the robot, including:

- device boot + Wi-Fi onboarding
- OTA/config fetch flow
- robot config caching/application
- ESP-HI board support for the currently connected dog
- localized assets and local flasher tooling used during development

## Current confirmed hardware target

The currently connected robot on the Mac Mini is configured as:

- **board:** `esp-hi`

This repo has been narrowed around that confirmed target instead of carrying a giant unrelated upstream board matrix.

## Scope

This repo is for **firmware only**.

It is intentionally separate from:

- `MojBot-5000` → website, setup flow, ops panel, product/backend layer
- `MojBot-5000-runtime` → live runtime service, websocket sessions, voice/persona, command handling

## Notes

- This repo is being actively cleaned up from earlier upstream-derived structure.
- The old private backend shim has been moved out to `MojBot-5000-runtime`.
- The current cleanup bias is simple: keep what helps ship the MojBot dog, delete what does not.
