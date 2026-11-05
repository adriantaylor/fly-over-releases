# Fly:Over

A **free Pegasus Quantum 15 flexwing simulator for VR**. Train at home, in the cockpit, over real-world scenery.

[![Fly:Over video (YouTube)](https://img.youtube.com/vi/kZpX0uHBisA/maxresdefault.jpg)](https://youtu.be/kZpX0uHBisA)

▶ **[Watch the video on YouTube](https://youtu.be/kZpX0uHBisA)**

- **Flight model** developed to be as close to the Quantum as possible, based on data and experience. Choose the Rotax 582 or 912.
- **A cockpit scanned from a real Quantum**: a yellow 582, LIDAR-scanned, with working gauges and a windscreen as worn as you like (pristine to heavy). The other colours and the 912 use a drawn cockpit.
- **Real-world scenery**: LIDAR and OS Terrain 50 terrain for all of Great Britain, with trees and hedges. Photo scenery streams as you fly: Google 3D, Google or Bing aerial photos on the LIDAR terrain, or a hybrid.
- **Hundreds of airfields**: Over Farm (Gloucestershire) is built in; hundreds of grass strips and airfields, including Shobdon, Plaistows, Sywell, Darley Moor and Kemble, come in free regional scenery packs you download in the sim (Menu → Scenery → Scenery packs): South West, South East and East of England, the Midlands, the North of England, South and North Wales, and Southern and Northern Scotland.
- **Multiplayer**, each on their own PC, over a LAN or the internet. **Fly together**, a trike each and seeing each other's. Or a **lesson**, one trike and two seats: the instructor can set up the exercise, cut the engine and take control at any time.
- **Real weather**: live OverWX forecasts (up to a week ahead) or the nearest METAR set the wind, gusts, cloud, QNH, temperature, thermals and the wind gradient. Or set your own.
- **The real sun**: the sun for any date, time and place, seasons included, with oranges, reds and purples at sunrise and sunset. Volumetric clouds, shaped by the wind at their height.
- **Maps and route planning**: choose airfields and plan routes on a zoomable chart of GB with its airspace, then fly them with a kneeboard map at a true 1:250,000. For the sim only: not for real-world navigation.
- **See yourself in SkyDemon**: Fly:Over sends its position as GDL90 over Wi-Fi, like an ADS-B receiver, so SkyDemon (or ForeFlight) on a tablet follows your flight.

## Download

Get the latest zip from **[Releases](../../releases/latest)**. Then [get your free Cesium ion token](#get-the-photo-scenery-a-free-cesium-ion-token) for the photo scenery.

## Install and run

1. Unzip anywhere. You'll get a **FlyOver** folder.
2. Start SteamVR for a headset (any OpenXR / SteamVR headset), then double-click **FlyOver.exe** in that folder. To fly on a monitor, run it with `-novr`.
3. Windows may say *"Windows protected your PC"* because the program isn't code-signed. Click **More info → Run anyway**.

Don't start it from an ordinary shortcut: on some Windows 11 builds that hangs at start-up. For a shortcut, use the target
`cmd.exe /c start "" "<folder>\FlyOver.exe"` with *Run: Minimised*.

**Keyboard:** arrows = bar, W/S = throttle, Z/X = steer, B = brake, Tab = menu, F1 = controls, M = map. Joysticks, throttles and VR controllers can be bound from the menu.

## Upgrading

The sim tells you when there's a new version at start-up (from 1.2.4 on) and offers to download it. Unzip the new zip where the old one is, over the old **FlyOver** folder: your settings, scenery packs and cache stay.

Coming from 1.2.2 or earlier? Those zips had no **FlyOver** folder, so unzip the new one beside your old files, and if you kept scenery packs in a `Packs` folder there, move it into the new **FlyOver** folder.

**Scenery packs and the photo cache** live beside FlyOver.exe by default (`Packs` and `Cache`). You can move them to another drive in Menu → Scenery.

## Get the photo scenery: a free Cesium ion token

> [!IMPORTANT]
> **For the real aerial-photo scenery you need your own free Cesium ion access token.** It takes about two minutes, and you only do it once.
> Without one, Fly:Over still runs but uses its basic built-in scenery.

1. **Create a free account** at **[ion.cesium.com](https://ion.cesium.com)** (*Sign up*; the free Community plan is all you need).
2. **Open the Access Tokens page.** Once signed in, click **Access Tokens** in the menu bar along the top of the page, or go straight to **[ion.cesium.com/tokens](https://ion.cesium.com/tokens)**.
3. **Copy the Default token.** In the list on the left, click **Default Token**. Its details open on the right: the token is the long string of letters starting **`eyJ`**. Click **Copy** next to it (or select all of it and press Ctrl+C).
4. **Paste it into Fly:Over.** With the token still on this PC's clipboard, start the sim, open the menu (**Tab** on the keyboard; in VR, the left controller's menu button or **B** on the right) and choose **Scenery → Paste Cesium ion token**. The sim reads the token from the clipboard; you'll see *"Cesium ion token saved"* and the menu item changes to **set**.

The token is saved on your PC, so you won't need to paste it again. It's linked to your own account, so don't share it. If you do share it by accident, click **Regenerate** on the same page to cancel it and get a new one.

## SkyDemon / ForeFlight (GDL90)

Fly:Over can send the aircraft's position, height, speed and track the way an ADS-B receiver such as a SkyEcho or Stratux does (GDL90 on UDP port 4000), so your moving map on a phone or tablet follows the sim.

1. Put the tablet on the **same Wi-Fi network** as the PC.
2. In Fly:Over open the menu and turn **Settings → GDL90 out** on. It broadcasts on every network the PC is on; the menu item shows where.
3. In SkyDemon, connect a **GDL90** device (the option for ADS-B receivers such as SkyEcho or Stratux). ForeFlight picks it up on its own and lists it as *Fly:Over*.

If Windows asks whether FlyOver may use the network, allow it on private networks. If nothing arrives (some VPNs and guest networks block broadcasts), copy the tablet's IP address to the clipboard and select **GDL90 address** in the menu to send straight to it. Your registration (Menu → Aircraft → Registration) is used as the call sign.

## Multiplayer

Both PCs need the same version. In **Menu → Multiplayer**, one PC hosts and the other joins, found automatically on the same network or by the host's address. Over the internet, forward UDP port 47800 on the host's router, or use something like Tailscale and join by its address. There are no accounts or servers. Use Discord or a phone for voice.

Choose the **Type**:

- **Fly together**: a trike each. Everyone sees each other's trike and shares the host's weather and time of day, and each keeps their own registration, colour and load.
- **Lesson**: one trike, two seats. The host chooses pilot or instructor. The instructor can take control (T), set up the weather and start position, restart, and cut the engine for a practice forced landing.

## Credits and licence

Fly:Over is free to download and share **non-commercially**. The built-in imagery is licensed CC BY-NC-SA.

- Terrain, trees and building heights: Environment Agency LIDAR Composite 2022, © Environment Agency; Welsh Government LIDAR (DataMapWales); Scottish public-sector LIDAR (Scottish Remote Sensing Portal); where there's no LIDAR, OS Terrain 50: all [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
- Trees in Scotland beyond its LIDAR: Meta / World Resources Institute global canopy height map, CC BY 4.0.
- Buildings, power lines, woods: © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors, ODbL.
- Built-in satellite imagery: Sentinel-2 cloudless 2024 by EOX IT Services GmbH (contains modified Copernicus Sentinel data 2024), [CC BY-NC-SA 4.0](https://s2maps.eu).
- Map: contains OS data © Crown copyright and database right 2026 (OS Open Zoomstack, OS Terrain 50), Open Government Licence. Airspace from the UK AIP via [YAIXM](https://github.com/ahsparrow/airspace) (CC0).
- Distant terrain: Terrarium tiles, AWS Open Data / Mapzen.
- Streamed photo scenery (not redistributed): Google Maps satellite imagery and Google Photorealistic 3D Tiles via Cesium ion, map data © Google; Microsoft Bing Maps via Cesium ion. Cesium for Unity, Apache 2.0.
- Made with Unity.

The full list is in `CREDITS.txt` inside the zip.
