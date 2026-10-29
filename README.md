# Phone Alert Atlas

Live site: https://vis772.github.io/phone-alert-atlas/

Interactive map of every wireless emergency alert (WEA) in FEMA's IPAWS archive since Jan 2025,
with state DOT traffic-camera locations and ±5-minute footage windows.

## Files
- `index.html` – the whole app (HTML, CSS, JavaScript). Loads d3 and topojson from cdnjs.
- `alerts.json` – 21,058 alerts (built from FEMA OpenFEMA IpawsArchivedAlerts, pulled Oct 28, 2026).
- `cameras.json` – camera sets: `master` (144 matched master-sheet cameras), `mn`, `wi`, `mo` (state DOT lists).
- `counties-10m.json` – US county/state boundaries (us-atlas 3.0.1).

## Run locally
Browsers block a page opened by double-click from loading its data files, so serve the folder:

    cd phone-alert-atlas
    python3 -m http.server 8000
    # then open http://localhost:8000

## Host it
GitHub Pages: upload all four data files + index.html to a public repo, then
Settings → Pages → Deploy from branch → main / root.
