# Soaking Wet FO4 — OG 1.10.163

Target runtime: **Fallout 4 1.10.163.0 (Old-Gen)**.

This repository is the build-ready source prototype for the wetness system. It does **not** contain a fake DLL: the current environment cannot compile/verify a Windows F4SE plugin against the Fallout 4 1.10.163 runtime.

## Intended runtime dependencies

- Fallout 4 **1.10.163.0**
- F4SE **0.6.23**
- Address Library for F4SE Plugins matching 1.10.163
- Windows build environment with MSVC/clang-cl and CommonLibF4

## Current implementation

- Per-actor wetness state from 0.0 to 1.0.
- Configurable rain/water/submersion accumulation.
- Configurable drying, including heat and sunlight multipliers.
- Player/NPC switches.
- Runtime-only material backend boundary: no `_D`, `_N`, or `_S` files are modified.
- Droplet/drip state manager is present as a separate backend.
- INI configuration under `Data/F4SE/Plugins/SoakingWetFO4.ini`.
- Debug forced-wetness mode for validating the state system.

## Important limitation

The visual part that actually changes `BSLightingShaderMaterial`/renderer material parameters is intentionally not claimed as complete here. Likewise, the droplet manager currently records drip events but does not yet spawn a native FO4 particle system. This package is therefore **source/build infrastructure, not a finished visual wetness mod**.

That distinction is intentional so you don't waste time installing a DLL that only pretends to work.

## Build dependency

Use an OG-compatible CommonLibF4 checkout in `extern/CommonLibF4` and build with a Windows C++23 toolchain. The current CommonLibF4 ecosystem documents OG 1.10.163 support and F4SE 0.6.23 as the OG runtime dependency.
