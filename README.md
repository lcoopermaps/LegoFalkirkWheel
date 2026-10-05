# Moominvalley Explorer

A single-file, procedural Three.js fan prototype for wandering a playful interpretation of Moominvalley.

## Play

The app is static and needs no build step. From a clone of this repository:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

The page loads Three.js from jsDelivr, so the first run needs an internet connection.

## Controls

- **W A S D** — walk
- **Shift** — run
- **Mouse** — look
- **Space** — hop
- **E** — talk, inspect, use doors and stairs
- **M** — valley map
- **J** — field journal

Touch controls appear on coarse-pointer/mobile devices.

## Included in the first playable release

The exterior world contains the tall round Moominhouse, its garden and well, the stream and wooden bridge, Snufkin's tent and campfire, woods, a beach and jetty, a distant Fillyjonk house, the Lonely Mountains and a cave route.

The house is explorable room by room through a separate interior pocket-world: salon, dining room, kitchen, cellar, second-floor landing, parents' bedroom, adult guest room, children's bunk room, third-floor landing, Moominpappa's study, upper guest room, reading room and Moomintroll's roof room.

Residents wander on their own routes and can be spoken to. The current cast is Moomintroll, Moominmamma, Moominpappa, Little My, Sniff, Snorkmaiden, Snufkin and Hemulen.

Sniff has special behavior: he sometimes reverses direction while running, steals nearby shiny trinkets, and later drops them. The Groke follows a long route through the wild parts of the valley and leaves temporary frozen ground behind her. A nearby-Groke screen effect and moving water/fire can be disabled with reduced-motion mode.

The map and field journal record landmarks as they are discovered.

## Visual / copyright approach

This repository deliberately contains **no copied illustrations, audio, book passages, TV/game models, textures or commercial assets**. Everything visible in the prototype is made from simple runtime geometry and short original/paraphrased interaction text.

This is an unofficial fan prototype. Moomin characters, names, places and underlying stories are the property of their respective rights holders. The code does not grant rights to the Moomin IP.

## Reference approach

The house structure and furniture arrangement were guided by public descriptions and an official 2026 Moominhouse activity PDF showing the tall round house and its multi-level cutaway. Public summaries also describe the salon fireplace, table, clock and sofa; dining room table/stove/cabinet; kitchen counter/stove/sink/churn/shelves; guest rooms; Moominpappa's study; Moomintroll's roof room; the bridge/river, Snufkin's camp, Lonely Mountains/cave route, and the Groke's freezing presence.

See [REFERENCE_NOTES.md](REFERENCE_NOTES.md) for the exact research notes used in this build.

## Technical notes

- No framework or bundler; the complete app is in `index.html`.
- Three.js `0.180.0` is imported via an import map.
- The exterior valley and house interiors are kept far apart in world space; doors/stairs teleport between zones. This keeps the prototype lightweight while still making every implemented room traversable.
- NPC movement is waypoint-based and intentionally simple.
- The prototype does not yet implement physical wall/terrain collision, inventory persistence, voice acting, quests, saving, or exact topographic reconstruction.

## Repository state

First playable build commit: `1b0e684c37fbf59d0fe68d65c1020936edf5cd1f`.
