# MojBot Firmware Repo Direction

This repo is in the middle of an intentional identity and scope cleanup.

## Current confirmed target

The robot currently connected to the Mac Mini is configured as:

- `CONFIG_BOARD_TYPE_ESP_HI=y`

So the current firmware cleanup is centered on **ESP-HI as the active MojBot hardware target**.

## What changed

- firmware is now separated into `MojBot-5000-firmware`
- runtime service moved to `MojBot-5000-runtime`
- website/product work lives in `MojBot-5000`
- unrelated board directories have been removed from this repo's current working copy so the project reflects the actual robot we have in hand

## Cleanup priorities

1. keep the robot dog working
2. remove branding confusion
3. reduce repo scope to MojBot-relevant targets
4. rename build/release artifacts to MojBot terms
5. rewrite docs around the MojBot product path

## Rule of thumb

If a file helps ship the MojBot robot dog on the confirmed hardware target, keep it.
If it only reflects old upstream breadth, remove or quarantine it.
