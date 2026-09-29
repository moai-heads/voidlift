# VOIDLIFT

A tiny, self-contained browser FPS built around an old-school raycaster—with a jetpack, free vertical movement, a low-gravity station, hostile drones, pickups, and an escape-skiff extraction.

**Play:** https://moai-heads.github.io/voidlift/ (after Pages finishes its first deploy)

## Controls

- **WASD** move · **Mouse** aim · **Click / F / Ctrl** fire
- **Space** jetpack · **C** descend · **Shift** sprint · **E** board the skiff
- **Arrow keys** turn / look; touch buttons are available on small screens.

Neutralize all six drones, then reach the gold skiff marker and press **E**. Fuel and repair cells are scattered around the station. Jet over low barriers and bulkheads, then release thrust to land on their tops; the perimeter contains the play area.

## Tiny-by-design

The playable build is one HTML file. It has no libraries, images, fonts, audio files, external requests, asset pipeline, or runtime dependencies. A compact character grid stores the map; the elevation-aware raycaster draws wall faces, panelled floor and exposed wall tops; you can jet onto the 0.72-unit barriers and 2.5-unit bulkheads and land there. The sky, sprites, radar, and weapon are procedural. The raycaster and game logic are plain JavaScript.

The source is deliberately readable rather than minified. Current playable payload: **28,341 bytes raw / 10,295 bytes gzip-9**. To recheck the footprint:

```sh
wc -c index.html
 gzip -9 -c index.html | wc -c
```

Only the HTML is downloaded by the game page; `README.md` is documentation, not a runtime asset. GitHub Pages publishes the site directly from the repository branch; `.nojekyll` keeps the plain HTML build simple.

## Run locally

Open `index.html` directly, or use any static web server. Pointer lock works best over `http://localhost`.

## Inspiration

A small original homage to the fast, spare, early-3D FPS lineage. [Quod by daivuk](https://daivuk.itch.io/quod) is a useful reference for the 64-KB, everything-in-the-executable constraint; VOIDLIFT explores a different browser-native version of that idea. No game assets or code are copied.
