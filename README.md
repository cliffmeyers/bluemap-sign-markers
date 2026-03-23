# BlueMap Sign Markers

A [BlueMap](https://bluemap.bluecolored.de/) addon that creates group-based POI markers from in-game signs. Place a sign with a `[group]` tag on the first line (e.g., `[home]`, `[station]`, `[rip]`) and the remaining lines become a labeled marker on your BlueMap.

Each unique group gets its own toggleable marker set in the BlueMap sidebar.

## Usage

1. Place the JAR in your server's `plugins/BlueMap/packs/` directory
2. Restart the server
3. Place signs in-game with a group tag on the first line:
   ```
   [home]
   Cliff's Base
   Main Island
   ```
4. The marker appears in BlueMap under a "Home" marker set

### Group tag format

- First line must be `[groupname]` where the name contains only letters, numbers, and hyphens
- Case-insensitive: `[Home]`, `[HOME]`, and `[home]` all map to the same group
- Lines 2-4 become the marker label and detail text

## Configuration

Settings are in `plugins/bluemap-sign-markers/settings.conf`:

```hocon
toggleable: true       # Whether marker sets can be toggled in the UI
default-hidden: false  # Whether marker sets are hidden by default
max-distance: 0        # Max camera distance to show markers (0 = always visible)
                       # Note: must be 0 for markers to appear in flat-view mode
```

## Acknowledgments

This project is a fork of [BlueMapSignExtractor](https://github.com/TechnicJelle/BlueMapSignExtractor) by [TechnicJelle](https://github.com/TechnicJelle). Thank you for the excellent foundation — the world-watching, region scanning, and sign text parsing architecture made this project possible.
