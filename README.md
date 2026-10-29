# Wardian community build

An unofficial, locally modified Windows x64 build of Wardian with minimap-based spoken alerts for League of Legends.

## Download and run

1. Open [the latest release](https://github.com/SantiParris8/wardian-offline/releases/latest) and download `Wardian-<version>.zip` from **Assets**.
2. Extract the entire ZIP to a writable folder.
3. Run `Wardian-Offline-Test.exe`. Keep `_internal` next to it. Python is bundled.

## Features

- Enemy jungler sightings, missing warnings, gank timing, dragon and gold reminders.
- Independent Top, Mid and Bot missing-alert switches.
- Visual enemy Teleport warnings: “Watch for Teleport.”
- Enemy lane-roam warnings covering top, mid, ADC and support in other lane corridors.
- Kokoro male or Zira female recordings for all 31 active callouts.
- A summary covering all 13 alert switches.

Existing League display and HUD settings do not need to be changed. Detection depends on visible minimap information and role identification; alerts can be missed or incorrect. The current capture loop requires an enemy carrying Smite in a supported Summoner’s Rift match. Experimental tuning and cross-lane behavior still need broader gameplay validation.

## Updates

Open **Settings → Check for updates**. The first installation uses the full ZIP; subsequent updates download **only changed files**. Missed versions are applied in order. Signed manifests and file hashes are verified before installing; a local backup supports rollback if installation fails. Settings, logs and calibration in `offline-data` are preserved. The app closes and restarts to apply an accepted update.

No GitHub login or token is required in the app. Network access is blocked except League’s local APIs and explicit updater requests to approved GitHub hosts. There are no background update checks or runtime speech synthesis.

## About this build

This repository is a release hub, not a complete reconstruction of Wardian’s original source. This is not an official publisher release. The original executable’s packaged modules remain in the distribution, with local Python adapters adding the community features. Publisher activation, check-ins, telemetry and update services are disabled in this modified build.

The network guards are Python-level controls, not an OS sandbox or a malware-safety guarantee. Keep the whole extracted folder together and install only releases you trust.

See [release notes](https://github.com/SantiParris8/wardian-offline/releases) for each version’s changes.
