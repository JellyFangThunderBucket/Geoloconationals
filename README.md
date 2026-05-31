# Geoloconationals

A self-contained mobile-friendly userscript for reducing location leakage through the browser JavaScript Geolocation API.

## What it protects

`The file` installs a userscript that intercepts:

- `navigator.geolocation.getCurrentPosition`
- `navigator.geolocation.watchPosition`
- `navigator.geolocation.clearWatch`
- `navigator.permissions.query({ name: 'geolocation' })` when the browser allows it

The script can return a real location, a fixed fake location, or a fuzzy/noisy fake location. It also includes mobile-oriented fake `Position` objects with realistic `coords` fields and timestamps.

## What it does not protect

This is only a geolocation API privacy userscript. It does **not** hide or change your IP address, VPN/proxy status, cellular/Wi-Fi network location, timezone, language/locale, browser fingerprint, accounts, cookies, local storage, or server-side location guesses.

## Modes and presets

Menu commands and the built-in panel support:

- Real location mode
- Fixed fake location mode
- Fuzzy/noisy fake location mode
- Pause/resume protection
- Clear cached fake location
- Presets for Pacific Ocean, New York, London, Tokyo, and custom latitude/longitude
- Optional debug logging, disabled by default

## Mobile setup

1. Install a mobile browser/userscript manager combination that supports Tampermonkey/Userscripts-style scripts.
2. Add the contents of `The file` as a new userscript.
3. Keep the script enabled for the sites where you want geolocation API protection.
4. Open the userscript manager menu and choose `Mobile Location Privacy Guard: Open configuration panel`.
5. Pick fixed or fuzzy mode and choose a preset or custom coordinates.
6. If a website still appears to know your area, remember it may be using IP/network/fingerprint signals outside this script's scope.
