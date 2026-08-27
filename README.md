# Manitowoc Google Traffic Test v3

Standalone TV display for Johnny Vapes Manitowoc using Google Maps JavaScript API TrafficLayer.

## Layout
- Current Traffic Conditions header
- Google live traffic map fills the content area
- Johnny Vapes Manitowoc marker
- Closures & Incidents information panel on the RIGHT side
- Compact traffic legend overlaid on the bottom of the map
- Map zoom is set to 14 (one level closer than the previous test)

## Important
The Google Maps JavaScript TrafficLayer provides the live traffic visualization, but does not expose Google's separate incident/closure list to page JavaScript. The right-side panel therefore does not fabricate incident data.

The API key in index.html is the temporary demo/test key previously supplied for this test. Replace it with the production-restricted key before deployment to the stores.

## GitHub Pages
Publish the `main` branch from `/ (root)`, then open:
`https://johnnyvapes.github.io/google-reviews-test/`
