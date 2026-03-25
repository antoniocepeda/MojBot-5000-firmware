# MojBot 5000 Firmware

Firmware for the MojBot robot dog.

This repo contains the ESP32-side code that runs on the robot, including:

- device boot + Wi-Fi onboarding
- OTA/config fetch flow
- robot config caching/application
- board support and audio stack
- localized assets and flasher tooling

## Scope

This repo is for **firmware only**.

It is intentionally separate from:

- `MojBot-5000` → website, setup flow, ops panel, product/backend layer
- `MojBot-5000-runtime` → live runtime service, websocket sessions, voice/persona, command handling

## Origin

This repo was split out from our earlier development work that lived in a customized `xiaozhi-esp32` codebase.

The goal now is to make MojBot firmware its own first-class project rather than leaving it as an implementation detail inside an upstream-derived repo.

## Notes

- This repo keeps only the firmware-relevant portions.
- The old private backend shim has been moved out to `MojBot-5000-runtime`.
- The firmware includes MojBot-specific config sync work, kid-name config support, and local flasher assets used during development.
