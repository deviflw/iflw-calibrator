# IFL Dial Calibrator

A standalone, password-gated tool (GitHub Pages) that renders a dial design onto every real watch in the catalogue — used to **calibrate** where a design sits inside each watch's dial window, and to **export** a branded, client-facing "Digital Preview" card.

> **This repo is the deployed build only.** The calibrator is developed in `deviflw/iflw-customizer-v2` (`mockup/calibrator.html`, one self-contained HTML file) and shipped here as a StatiCrypt-encrypted GitHub Pages bundle via that repo's `tools/deploy_calibrator.sh`. Edit it there, not here.

**Live:** https://deviflw.github.io/iflw-calibrator/ — StatiCrypt password-gated (password kept in the team vault / `iflw-customizer-v2` docs, not in this public repo).

## What it does

1. **Load a design** — a square, transparent PNG. It renders into every watch cell at once.
2. **See it on every watch** — a grid of all catalogue watch × variant combos; each cell composites three layers: dial → design masked into the dial window → foreground.
3. **Calibrate** — the design is clipped to each watch's `dial_window` (centre + diameter), so you can eyeball whether the placement/size is right per watch. An admin **Calibration report** (CSV, worst centre-offset first) gives the numbers.
4. **Export** — the branded, client-facing **Digital Preview** card per watch.

Shares its data model and CDN assets with the customizer mockup. Assets in this repo: `canvas-cdn-links.json` (watch-image CDN map) and `dial-shapes.json`.

## It is not the app

The production customizer is `deviflw/iflw-customizer`. This is a separate preview/calibration tool.
