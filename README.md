# Honda e Dashboard

The website of Honda e Dashboard, an Android app that reads a Honda e's traction battery through a Bluetooth OBD-II adapter: live power, the state of the pack and its 96 cells, and every charge as a curve.

Website: https://morvy.github.io/hondae/

This repository holds only the published website; it is generated and pushed by a deploy script from the app's own repository, so changes made here are overwritten on the next deploy.

Honda e Dashboard is an independent app, not affiliated with Honda Motor Co., Ltd.

## Changelog

### 1.2.2 - 8 October 2026

Next speed now shows only what changing speed is worth, worked out on your own consumption. Near empty it no longer promises tens of kilometres for slowing down a little.

### 1.2.1 - 7 October 2026

Tyre estimates now show in 0.05 bar steps, the steps a gauge is set in, with a wider ± that holds the real pressure about 19 times in 20. A tyre whose change is inside its ± shows the pressure you set and reads unchanged, so small wobbles between drives no longer look like one tyre losing air.

### 1.2.0 - 6 October 2026

While charging, see the time and energy left to 80 %, then to 100 %, and plot power against charge level. Tap a saved charge to see its curve; deleting one asks first. The battery page shows health over time from your saved charges. The drive log lists newest first, grouped by month with totals. The default dashboard fits the screen without scrolling. A failed connection now says why, with a fix where there is one, and disconnecting asks first. The car from above has a finer dashboard speaker.

### 1.1.0 - 6 October 2026

The tyres page is rebuilt. Each tyre sits beside its wheel on your car seen from above, in its paint colour. Learning starts at 30 km/h, shows its progress and what it is waiting for, and is kept between drives, so short trips add up; entering the pressures again lets you keep learning or start over. The first estimate comes sooner. A trend under the car shows each tyre drive by drive, so a slow leak stands out. The page stays upright.

### 1.0.2 - 2 October 2026

On supported Android Auto screens, tap a dashboard tile to show it fullscreen and tap again to return to the grid. The Android Auto dashboard stays fixed without scrolling, and the unit button remains available.

### 1.0.1 - 1 October 2026

Shows when the OBD adapter is out of reach instead of an error. Explains background location before asking for it. The connection notification no longer stays after closing the app.

### 1.0.0 - 30 September 2026

Initial app release
