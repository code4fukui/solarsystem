# Simple Solar System Simulator

A single-file Three.js solar system simulator with desktop viewing and optional WebAR support.

## Features

- Drag to rotate the view and use the wheel to zoom.
- Adjust orbital animation speed.
- Toggle between two display modes:
  - Deformed: distances and body sizes are exaggerated for readability.
  - Real: distances, body sizes, and the Moon orbit use one shared AU-based scale.
- Japanese browser environments show Japanese labels for the Sun and planets.
- Mercury and Pluto include orbital inclination.
- WebAR-capable environments show an AR button with transparent camera background.
- AR solar system size can be selected from 1m to 100m.

## Run

Serve the directory with any static HTTP server:

```sh
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/index.html
```

## Notes

WebAR requires a browser and device that support WebXR `immersive-ar`. On unsupported environments, the simulator still works as a normal 3D web page.

The Real display mode is physically scaled, so planets become extremely small compared with their orbital distances.

Sun, planet, and Moon data is stored in `planets.csv` and loaded with `https://code4fukui.github.io/CSV/CSV.js`.
The `parent` column describes the orbital parent body.

`planets.csv` is CC0 open data.
