# Manitowoc Google Traffic Test v2

Standalone TV test for Johnny Vapes Manitowoc.

Features:
- Full-screen 16:9 signage layout
- CURRENT TRAFFIC CONDITIONS banner
- Google Maps JavaScript API
- Google TrafficLayer with autoRefresh enabled
- Custom Johnny Vapes store marker
- Reserved closures/incidents panel
- Traffic legend
- No periodic page/map reload

This is still a TEST build. Do not put the demo API key into production.

GitHub Pages:
Enable Pages from `main` / root, then open the repository's Pages URL in a desktop browser first and then TV Bro.


## 511WI Incidents / Closures

The right-side CLOSURES & INCIDENTS panel now uses the 511WI Events API.

Before deploying, open `index.html` and replace:

`PASTE_YOUR_511WI_API_KEY_HERE`

with your 511WI developer key.

The page requests the 511WI event feed every 5 minutes and filters it to:
- Manitowoc County
- `accidentsAndIncidents`
- `closures`

The Google Maps traffic layer remains separate and unchanged.

Note: because this is a static GitHub Pages site, the 511WI key is necessarily exposed to the browser. If 511WI later provides a safer browser/CORS approach or you want to hide the key behind a server-side proxy, the feed can be moved to that architecture.
