# ⚡ EV Charger Finder

Easily find EV charging stations and ports near you — fast and simple. Built with **Leaflet.js** and the **OpenChargeMap API**, this lightweight web app lets you search any city/address or use your current location to discover nearby EV charging stations, view connector types, and get directions.

## ✨ Features

- 🔍 **Search by city or address** — geocoded via OpenStreetMap Nominatim
- 📍 **"Use My Location"** — auto-detects your position via browser geolocation
- 🗺️ **Interactive map** — powered by Leaflet with OpenStreetMap tiles
- ⚡ **Live charging station data** — pulled from the OpenChargeMap API
- 🔌 **Connector details** — popup shows connection/plug types per station
- 🧭 **Get Directions** — quick link to OpenStreetMap directions for any station

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (`style.css`) |
| Logic | Vanilla JavaScript |
| Mapping | [Leaflet.js](https://leafletjs.com/) + Leaflet Control Geocoder |
| Map Tiles | OpenStreetMap |
| Geocoding | [Nominatim](https://nominatim.org/) |
| Charging Station Data | [OpenChargeMap API](https://openchargemap.org/) |

## 📁 Project Structure

```
EV-charger-finder/
├── index.html   # Main app page (map, search bar, controls)
├── add.js       # Map init, geolocation, search, and station-fetching logic
├── style.css    # App styling
└── README.md
```

> ⚠️ **Heads up:** `index.html` currently loads `<script defer src="app.js">`, but the script in this repo is named `add.js`. Rename `add.js` to `app.js` (or update the `<script>` tag) or the map/search logic won't load.

## 🚀 Getting Started

No build step needed — it's a static site.

```bash
git clone https://github.com/LOWKEY-VOID/EV-charger-finder.git
cd EV-charger-finder

# fix the script filename first (see note above), then serve it:
npx serve .
# or
python3 -m http.server 8000
```

Open the printed local URL, allow location access when prompted, and nearby charging stations will load automatically.

## 🔑 API Key

The app uses an [OpenChargeMap API key](https://openchargemap.org/site/develop/api) to fetch station data, set via `OCM_API_KEY` in the script.

> ⚠️ **Security note:** a live-looking API key is currently hardcoded directly in the JS file. Since this repo is public, that key is exposed to anyone who views the source. It's best practice to:
> - Revoke/rotate that key on OpenChargeMap
> - Keep your key out of the committed file (use a placeholder + `.env`/config approach, or a build step that injects it)

## 🌍 Coverage

Defaults to Bengaluru, India as the starting map view, but works anywhere OpenChargeMap has data — search any city or use your location worldwide.

## 🤝 Contributing

Personal project — issues and pull requests are welcome, especially around the script filename fix and API key handling above.

## 📜 License

No license specified yet. Add a `LICENSE` file (MIT is a common default) if you want others to freely reuse this project.

---

Built by [LOWKEY-VOID](https://github.com/LOWKEY-VOID)
