# Poly Dip 2 Multiplayer — PolyModLoader port

Version 1.0.0, for PolyTrack / PolyModLoader 0.6.3.

This package was converted from the current installed PD2 app.asar. It contains the same public PD2 runtime and map, adapted through 36 PML global mixins. It does not replace main.bundle.js, alter stock physics, or require the PD2 ASAR.

## Install

Use a clean PolyModLoader 0.6.3 installation, not the existing PD2 app.asar. Do not enable the original PolyDip mod alongside this port.

Add this mod URL in PolyModLoader:

https://cdn.polymodloader.com/gh/zeptjan/PolyDip2/main/dist

The versioned files are hosted in this repository under dist/.

## Included public features

Fixed PD2 map, automatic lobby discovery, host migration and run-continuity hooks, timer and PB/height/fall indicators, stats, spectating, horn, global chat, proximity voice, microphone selection, individual audio controls, run protection, and performance settings. Existing Cloudflare lobby services remain unchanged.

## Owner moderation

The public mod contains no admin key, Discord token, Cloudflare account token, or publisher key. Owner moderation depends on Electron's private polyDipAdminAvailable/polyDipAdminRequest bridge, which ordinary browser PML cannot provide. Consequently the owner admin button stays hidden in ordinary PML. Keep using the owner Electron build for moderation; do not upload its private JSON files with this package.

## Verification

Verified using the real official PML 0.6.3 loader and simulation worker in an isolated test browser: import, all 36 native hooks, initialization, native car attachment, main-menu PolyDip button, F8 settings, native horn and Poly Dip 2 chat/voice controls. Test network access to the public multiplayer service was deliberately blocked/mocked, so live PML-to-PML lobby connection, voice and host-transfer/replay validation require an additional multiplayer test. Existing standalone tests do not substitute for that test.

Source build: pd2-pml/build.cjs. Development references and the test harness are outside dist/ and are not shipped in the distribution ZIP.

Original PolyDip authors: DoraChad + Orangy. PD2 changes and port commissioned by Zeptjan. The included voice-icon license applies to the bundled Discord-style icons.
