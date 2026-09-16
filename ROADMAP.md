# Soaking Wet FO4 — roadmap

## 0.2 — runtime prototype
- [x] Multi-runtime CommonLibF4 AV target
- [x] INI loading
- [x] F4SE task loop
- [x] Player wetness state
- [x] Forced wetness test mode
- [x] Runtime logging
- [ ] Runtime material traversal

## 0.3 — first visual backend
- [ ] Walk player 3D geometry
- [ ] Identify BSLightingShaderProperty / material types
- [ ] Cache original specular/gloss values
- [ ] Apply wetness multiplier without touching DDS files
- [ ] Restore original values at 0 wetness
- [ ] Validate on 1.10.163 / 1.10.984 / 1.11.x

## 0.4 — environment detection
- [ ] Rain detection
- [ ] Water detection
- [ ] Submersion detection
- [ ] Interior/roof handling
- [ ] Heat/sun drying

## 0.5 — full actor support
- [ ] NPC wetness
- [ ] Clothing/armor material classification
- [ ] Hair/skin special handling
- [ ] Drips and optional secondary effects
- [ ] MCM

## Advanced
- [ ] Community Shaders wetness integration
- [ ] Screen-space reflections integration
- [ ] Optional per-material wetness masks


## Dev 0.3 — Droplet system
- Added configurable drip simulation and throttling.
- Added light/heavy drip thresholds.
- Added player/NPC switches.
- Added isolated particle backend boundary so no assets are borrowed from existing mods.
- Next: bind SpawnDrip() to native FO4 NiPSys/particle attachment nodes and create original droplet assets.
