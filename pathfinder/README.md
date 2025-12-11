# 📍 Mini OSM Directions UI

> [!NOTE] A tiny, single-file OpenStreetMap directions interface using Leaflet, Tailwind, and the OSRM demo routing server.
> Includes a rounded modern UI, click-to-set coordinates, zoom/pan, and auto-fitting route display.

## ✨ Features

* One-file implementation (HTML only; Tailwind via CDN)
* OpenStreetMap base layer using Leaflet
* Click the map to autofill coordinates
* First click → Start
* Second click → End
* Alternates automatically
* Rounded UI — inputs, button, and map container
* OSRM routing (public demo server)
* Auto-zoom to route
* Works in any modern browser

## 🚀 Usage

> [!TIP] Just open the index.html file in your browser.
> No build step, no bundlers, no local server required.

## 🗺️ How to Use

1. Click anywhere on the map: *Start field autofills (lon,lat)*
2. Click another point: *End field autofills*
3. Press Route: *The route appears on the map*

You can also manually input coordinates using: `longitude,latitude`

Example: `-122.4194,37.7749`

## 🧱 Technical Overview

### Libraries

* Leaflet for map rendering
* TailwindCSS via CDN
* Ubuntu family of fonts via Google Fonts
* OpenStreetMap tile server
* OSRM (public routing demo server)

## Routing Format

```
https://router.project-osrm.org/route/v1/driving/<start_lon>,<start_lat>;<end_lon>,<end_lat>?overview=full&geometries=geojson
```

The returned GeoJSON line is rendered as a polyline.

## 📦 File Structure

```
project/
└── index.html  # Entire app in one HTML file
```

⚠️ Notes
* The OSRM demo server is not reliable for production, only for experimentation.
* For production routing, consider hosting your own OSRM instance or using OpenRouteService, GraphHopper, or Valhalla.
