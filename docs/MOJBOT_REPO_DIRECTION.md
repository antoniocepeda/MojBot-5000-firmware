# MojBot Firmware Repo Direction

This repo is in the middle of an intentional identity cleanup.

## What changed

- firmware is now separated into `MojBot-5000-firmware`
- runtime service moved to `MojBot-5000-runtime`
- website/product work lives in `MojBot-5000`

## What still needs cleanup

A lot of source structure and supporting docs still reflect the earlier upstream-derived codebase.
That means this repo still contains:

- references to older project names
- documentation for unrelated boards and flows
- legacy naming in scripts/build outputs
- broad upstream scope that exceeds MojBot's actual product needs

## Cleanup priorities

1. keep the robot dog working
2. remove branding confusion
3. reduce repo scope to MojBot-relevant targets
4. rename build/release artifacts to MojBot terms
5. rewrite docs around the MojBot product path

## Rule of thumb

If a file helps ship the MojBot robot dog, keep it.
If it only reflects old upstream breadth, evaluate it for removal later.
