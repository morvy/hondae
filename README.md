# Honda e Dashboard

The website of Honda e Dashboard, an Android app that reads a Honda e's traction battery through a Bluetooth OBD-II adapter: live power, the state of the pack and its 96 cells, and every charge as a curve.

Website: https://morvy.github.io/hondae/

This repository holds only the published website; it is generated and pushed by a deploy script from the app's own repository, so changes made here are overwritten on the next deploy.

Honda e Dashboard is an independent app, not affiliated with Honda Motor Co., Ltd.

## Changelog

### 2.2.1 - 18 November 2026

The TPMS page now learns and watches your tyres while Android Auto shows the dashboard or the phone is in a pocket, not only with the page open on the phone. Once you have entered the pressures, it reads the wheel speeds in the background above 30 km/h; learning takes about ten minutes of steady driving that way, or two with the page open.

### 2.2.0 - 18 November 2026

When the app was off for a whole charge, from before the cable went in until after it came out, it now notices the rise in charge the next time it reads the car and offers to save it: a "Charge not recorded" card on the Charging page and a notification, with the energy estimated from the charge gained and, if you know them, when it started and finished, AC or DC and the charger's peak and energy. Drivetrain, coolant, 12 V and power use tiles now set the size and weight of their row names and figures in place of the row size; larger sizes pack the rows tighter on short tiles, 12V SOC in columns follows them too, and its graph bar no longer touches the names. The tile designer's preview now shows the tile at exactly the size it gets on the dashboard. Altitude shows height above sea level, as maps do; Settings can switch back to the GPS's own ellipsoid height. Reversing into a space no longer logs "Power limited". Battery current adds both halves of the pack. Vehicle information lists four more modules, among them the front camera. Shared raw logs read correctly on phones set to a decimal comma and carry their date, app version and events.

### 2.1.0 - 15 November 2026

New dashboard tiles: COOLANT (the battery loop, with the drive unit's coolant, fan and pump on a larger tile), TEMPERATURES (six temperatures in one strip) and 12V SOC (the 12 V battery sensor's charge, temperature, current and voltage, as rows or columns), plus twelve figures that were only inside widgets, such as regen power, radiator fan, energy used this drive, magnet and gear oil temperature. One list, grouped by topic, adds a tile or changes one from the tile designer; the power bar, kW readout, load, drive graph and next speed are now value tiles with their drawing. Graphs can sit above, below, left or right of the value or replace it, in plain, stepped or colour-scale bars, and the unit can go beside, under, at the bottom or be hidden. Drivetrain, coolant, 12 V and power use tiles take the label, size, colours and limits, with their own row size and weight. Range gets a range curve and a range bar. The 12 V tab shows the car's own battery sensor, Battery health the capacities the BMS has stored, Vehicle information lifetime counts, fault codes every module, and a DC charge the energy from the station and the loss. The app connects at once after parking and notices a sleeping car wake sooner. The Single Pedal tile is removed for now.

### 2.0.3 - 14 November 2026

Settings has a minimum row height for the dashboard, one for portrait and one for landscape. Rows are no longer squeezed below it: a longer layout scrolls, with whole rows filling the screen. At 100 % six tile rows fit in portrait and three in landscape, whatever the column count; lower values fit more rows, higher ones make them taller. On the Tyres page the chip now reads "Brake fluid level OK", because the car reports only the level.

### 2.0.2 - 13 November 2026

Back in the car after a long park, the app connects at once, and a tap on "Adapter out of reach" tries again. Theme has a slider for the width of the tile border, from 0 to 6. Every page now starts at the top of the screen, with its title at the same height on each. On the regen and brakes tile, the size slider changes the figures only; the lamp names keep their size. The app's version is at the bottom of Settings again.

### 2.0.1 - 13 November 2026

Unlocking the car no longer saves a few-second drive before the real one. Vehicle information has two tabs, Car and Modules: the service schedule and the speedometer are tables again, and Read and Export sit at the top. The regen and brakes tile can now be set in the tile designer: text size, weight, which text shows, each lamp's colour and where it lights. The tile designer has Cancel and Done, and Cancel puts the tile back as it was.

### 2.0.0 - 12 November 2026

A new look: bottom navigation and redesigned Battery health (12 V tab, both battery lines), Charging, TPMS, Settings and Drive log, which exports My Honda+ trips. Design each tile's size, label, colours, limits and graphs; share your dashboard. New tiles for power use, regen and brakes, Single Pedal and drivetrain temperature; Cost of speed is gone. Optional My Honda page: Honda's cloud data, trips and paid remote commands. Fault codes, a maintenance minder, steadier readings and reconnects.

### 1.9.0 - 7 November 2026

More Bluetooth adapters connect. Picking an adapter now also finds classic Bluetooth adapters that were never paired, such as the OBDLink MX+, MX and LX and vLinker BM, lists adapters above your other Bluetooth devices and pairs them for you. Adapters that refuse the usual connection are tried other ways, and an unknown BLE adapter is tested until it answers. A reading cut off mid-request can no longer show up as the next reading's value.

### 1.8.0 - 5 November 2026

Power tiles, the kW readout and Drive energy can show white numbers instead of colours: set it in the tile editor. Clearer tile names, such as CHARGER TEMP, WEAK CELL, DRAW LIMIT and ENERGY LEFT, and long names shrink to fit. The drive graph counts only driving time and holds the last 10 to 60 minutes, squeezing or cutting older driving. Vehicle information reads every module and exports an anonymised copy. MAINS shows a dash with nothing plugged in. The help now matches the screens.

### 1.7.1 - 4 November 2026

Six new tiles: cabin temperature, motor torque in N·m, the highest cell resistance, HV insulation, mains voltage at the charging inlet and the charging station's current limit.

### 1.7.0 - 4 November 2026

New tiles show the power the battery will give and take back right now, so you can see why regen is weak when it is cold or full. The Battery page has an AH view with each cell's capacity. Logs now record power and regen available, cell and insulation resistance, DC/DC temperature, the charging station's current limit and motor torque in N·m. The app notices more reliably when the car is switched off. Drive energy shows dashes until it has counted. A 100-120 V socket charge shows as AC.

### 1.6.1 - 3 November 2026

Fixed the app freezing when you disconnect or switch the car off, which could leave that drive's logs on the phone instead of in your folder. Logs left behind are now moved within a couple of minutes, and empty log files left by earlier freezes are cleaned up.

### 1.6.0 - 3 November 2026

Range, energy left and kWh to full now use what your battery really holds: the usable window shrinks with battery health, and a percent near empty holds less than one near full, so range reads lower and is right when it matters. The power gauge spends more of its arc on everyday driving, up to 140 kW and 50 kW of regen. An AC charge on a warm battery no longer shows as DC. Logs now record AC mains voltage, battery coolant temperatures and HV bus voltage.

### 1.5.0 - 31 October 2026

Edit a saved charge with what the charger showed: start, end, session time, energy or average. A charge the app sees late gets its missed start estimated. Estimates follow your pack's health, as do kWh to go, parked loss and ABRP on worn packs. A brief adapter dropout no longer splits a drive. Fixed: wrong SoC with the Battery or Tyres page open, Android 9 to 11 stopping with the screen off, false Car asleep, logs stuck on the phone, logs lost after deleting the Drive folder.

### 1.4.1 - 31 October 2026

A charge that drops out no longer splits into several sessions: the app waits for the car to say it is still charging, then asks whether to continue. The question now also comes as a notification with Continue and New session buttons, so you see it with the app closed. Fixed a crash when continuing a charge while the car was drawing power. A slightly smaller app.

### 1.4.0 - 30 October 2026

See what heating costs: the Power bar can show aux power in purple, with new tiles for climate, 12 V load, battery heat and heating cost in km. The new Drive graph shows power, speed and altitude for the whole drive, and Drive energy splits it into drive, aux and regen. The app now says when the car heats the battery, notes a cold pack when charging and reports charge lost while parked. Fewer false cell warnings in the cold, and a smaller app.

### 1.3.0 - 30 October 2026

New: upload your logs to your own Google Drive. Choose a folder in Settings, File storage, and switch it on; each log is copied to a Honda e logs folder, and the app sees only the files it puts there. A new switch deletes logs over 30 days old from the phone; with Drive on only those already in Drive, and nothing is ever deleted from Drive. The app no longer freezes on a folder with hundreds of logs.

### 1.2.4 - 17 October 2026

On a battery worn past its hidden reserve, energy left and the range estimate now count only what the pack can really give, rather than a new car's 28.5 kWh, so they no longer read high. Battery health is now shown in Ah, the unit the car reports; a new pack holds 100 Ah, so the number itself does not change. Raw reply logs now carry the right time of day even with trip readings off.

### 1.2.3 - 14 October 2026

With the drive log on, the tyres and battery pages no longer pause the other readings, so the log keeps charge, distance and temperatures the whole drive; the cells refresh less often instead. Battery health and the cell charge levels now stay live on every page.

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
