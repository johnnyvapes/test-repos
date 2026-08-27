# Manitowoc Google Traffic Test v3

Standalone Google Maps traffic display for Johnny Vapes Manitowoc.

## Included

- Google Maps JavaScript API
- Google live TrafficLayer
- TrafficLayer auto-refresh
- Johnny Vapes Manitowoc marker
- Large map occupying the full content area
- Compact CLOSURES & INCIDENTS panel on the right
- Traffic legend overlaid on the bottom of the map
- No duplicate footer
- No favicon dependency

## Important

The test page uses the temporary/demo Google Maps API key supplied for testing.

Google's Maps JavaScript TrafficLayer provides the live traffic visualization, but it does not expose a separate list of Google's underlying traffic incidents/closures to webpage JavaScript. Therefore the incident panel does not fabricate incident data.

For production, replace the demo key with a restricted production API key and restrict it to the production GitHub Pages domain.

## GitHub Pages

Set:

- Source: Deploy from a branch
- Branch: main
- Folder: / (root)

Then wait for the GitHub Pages deployment to complete.
