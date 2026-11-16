# 🌍 TerraPulse — 3D Globe News Explorer

**TerraPulse** is an interactive, Google Maps-style 3D Earth news explorer built with **MapLibre GL JS**, **Sentinel-2 satellite imagery**, and **OpenStreetMap vector layers**. Explore global headlines anchored to real-world coordinates, fly smoothly to any city on the planet, and automatically load local dispatches when you zoom in.

---

## ✨ What It Is

TerraPulse turns global journalism into a spatial, interactive 3D experience:
- **Realistic 3D Spherical Globe:** Rotatable Earth with an atmospheric blue horizon glow, deep-space starfield backdrop, and optional gentle planetary auto-spin.
- **Satellite + Multi-Zoom Vector Hybrid Map:** Combines EOX Sentinel-2 cloudless satellite imagery with OpenFreeMap vector labels, country/state borders, waterways, roads, and buildings that progressively reveal detail as you zoom in.
- **Geo-Anchored News Dots & City Hubs:** Color-coded story pins and 18 clickable major city markers placed at exact latitude/longitude coordinates.
- **Automatic Local-News Radar (`zoom ≥ 5.2`):** Zooming into any region automatically identifies the city/country at the center of the screen and loads live local news dispatches alongside nearby stories.

---

## 🧭 How to Use It

1. **Navigate the Globe**
   - **Drag** to rotate/pan anywhere on Earth.
   - **Scroll or pinch** to zoom smoothly from world scale down to street level.
   - **Right-click + drag** (or `Ctrl + drag`) to tilt/pitch the camera in 3D.
   - Use the **top-right controls** for zoom buttons, compass reset, and **"Near Me"** GPS geolocation.
2. **Explore News Pins & City Hubs**
   - Hover over any colored dot for a quick headline preview.
   - **Click any news dot or city marker** to smoothly rotate the globe toward that location and open the **Regional News Detail Panel** (showing coordinates, headline, summary, key takeaways, source, and nearby regional stories).
3. **Auto-Load Local News**
   - Zoom in past **level `5.2`** (shown in the bottom telemetry bar) over any city or region.
   - The **Local Radar** automatically reverse-geocodes the center of your map and fetches live regional dispatches.
4. **Search & Filter**
   - Use the **Search bar** to jump to any city, country, topic, or headline worldwide.
   - Click the **Topic Filter Pills** (`World`, `Tech & AI`, `Climate`, `Economy`, `Science & Space`, `Culture`, `Health`) to filter both the globe dots and story feeds in real time.
5. **Save Stories & Switch Basemaps**
   - Click the **Bookmark** icon on any story card or detail view to save it to your **Saved** tab (stored locally in your browser).
   - Toggle between **Satellite** (hybrid satellite + vector labels) and **Vector** (clean atlas map) in the top-right header.

---

## 🚀 How to Run Locally or Host Live

### Option 1: GitHub Pages (Live Website)
1. Ensure the HTML file is named `index.html` in the root folder.
2. Go to **Settings → Pages** in this repository.
3. Under **Branch**, select `main` (`/ (root)`) and click **Save**.
4. Open your live site at `https://royk2002.github.io/3d-globe-news-explorer/`.

### Option 2: Run Locally
Because the app uses ES modules and browser geolocation, serve it over a local HTTP server:

```bash
# Clone the repository
git clone https://github.com/RoyK2002/3d-globe-news-explorer.git
cd 3d-globe-news-explorer

# Start a local server (Python)
python -m http.server 8080
