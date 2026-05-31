# Geoloconationals

A small userscript repository containing a hardened copy of the Location Guard userscript.

## What the script does

`The file` overrides the browser Geolocation API from a userscript context so sites receive either:

- a fixed configured location,
- a privacy-preserving noisy location, or
- the real location when the script is paused or configured to use `real` mode.

## Notes

- The userscript still defaults to fixed-location spoofing.
- The configuration surface is exposed as `$locationGuard` on the Location Guard options host.
- The script includes compatibility fallbacks for modern `GM.*` APIs and legacy `GM_*` APIs.
