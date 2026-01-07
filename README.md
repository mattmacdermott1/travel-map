# Travel Map

> **Note:** This project was entirely built by Claude (Anthropic's AI assistant) through conversational prompts.

An interactive world map to track countries and regions you've visited, with year-based color coding.

![Demo](https://img.shields.io/badge/demo-GitHub%20Pages-blue)

## Features

- **Interactive world map** with country outlines
- **US states and Canadian provinces** as separate selectable regions
- **Year-based heatmap coloring** (dark red for oldest visits → yellow for newest)
- **Autocomplete search** with keyboard navigation (arrow keys + enter)
- **Persistent storage** - data saves automatically to browser storage
- **Optional file sync** - set a CSV file for auto-saving (works on localhost/HTTPS)
- **CSV export/import** for backup and portability

## Usage

### Quick Start

1. Open `index.html` in your browser
2. Start typing a country, US state, or Canadian province
3. Use arrow keys to navigate suggestions, Enter to select
4. Enter the year you visited
5. Press Enter or click "Add Visit"

### Auto-Save to File

For persistent file-based storage:

1. Serve the file locally:
   ```bash
   python3 -m http.server 8000
   ```
2. Open `http://localhost:8000`
3. Click "Set Save File" and choose where to save your data
4. Data will auto-save to that file on every change

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `↑` / `↓` | Navigate suggestions |
| `Enter` (in country field) | Select highlighted suggestion |
| `Enter` (in year field) | Add the visit |
| `Escape` | Close suggestions dropdown |

## Technical Details

- Pure HTML/CSS/JavaScript - no build step required
- Uses [Leaflet.js](https://leafletjs.com/) for map rendering
- GeoJSON data from open sources
- File System Access API for optional file persistence
- Data stored in localStorage as fallback

## Data Sources

- World countries: [datasets/geo-countries](https://github.com/datasets/geo-countries)
- US states: [PublicaMundi/MappingAPI](https://github.com/PublicaMundi/MappingAPI)
- Canadian provinces: [codeforamerica/click_that_hood](https://github.com/codeforamerica/click_that_hood)

## License

MIT License - see [LICENSE](LICENSE) file.
