# Fly:Over

A **Pegasus Quantum 15 / Rotax 582 flexwing simulator for VR**. Train at home, in the cockpit, over real-world scenery.

- **Flight model** developed to be as close to the Quantum as possible, based on data and experience.
- **Real-world terrain**: Environment Agency LIDAR terrain, trees and hedges, with optional photoreal scenery streamed as you fly.
- **Instructor in the back seat**: multi-crew over a LAN or the internet, each on their own PC. The instructor can set up the exercise, fail the engine and take control at any time.
- **Your weather**: wind, gusts, turbulence, thermals, cloud cover and base, time of day.
- Airfields: Over Farm (Gloucestershire), Shobdon and Plaistows.

## Download

Get the latest zip from **[Releases](../../releases/latest)**.

## Install and run

1. Unzip anywhere.
2. Start SteamVR for a headset (any OpenXR / SteamVR headset), then double-click **FlyOver.exe**. To fly on a monitor, run it with `-novr`.
3. Windows may say *"Windows protected your PC"* because the program isn't code-signed. Click **More info → Run anyway**.

Don't start it from an ordinary shortcut: on some Windows 11 builds that hangs at start-up. For a shortcut, use the target
`cmd.exe /c start "" "<folder>\FlyOver.exe"` with *Run: Minimised*.

**Keyboard:** arrows = bar, W/S = throttle, Z/X = steer, B = brake, Tab = menu, F1 = controls. Joysticks, throttles and VR controllers can be bound from the menu.

## Photoreal scenery (optional, free)

Without a token the sim uses its built-in scenery. For aerial photos on the LIDAR terrain:

1. Make a free account at [ion.cesium.com](https://ion.cesium.com).
2. Open **Access Tokens** and copy the **Default** token.
3. In the sim choose **Menu → Paste Cesium ion token**.

## Flying with an instructor

Both PCs need the same version. One PC hosts (choose pilot or instructor seat in the menu) and the other joins, found automatically on the same network or by the host's address over the internet (UDP ports 47800–47801). Use Discord or a phone for voice.

## Credits and licence

Fly:Over is free to download and share **non-commercially**. The built-in imagery is licensed CC BY-NC-SA.

- Terrain, trees and building heights: Environment Agency LIDAR Composite 2022, © Environment Agency, [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
- Buildings, power lines, woods: © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors, ODbL.
- Built-in satellite imagery: Sentinel-2 cloudless 2024 by EOX IT Services GmbH (contains modified Copernicus Sentinel data 2024), [CC BY-NC-SA 4.0](https://s2maps.eu).
- Distant terrain: Terrarium tiles, AWS Open Data / Mapzen.
- Streamed photo scenery (not redistributed): Microsoft Bing Maps via Cesium ion; Google Photorealistic 3D Tiles, map data © Google. Cesium for Unity, Apache 2.0.
- Made with Unity.

The full list is in `CREDITS.txt` inside the zip.
