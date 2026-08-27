# Google Traffic Test — Fixed

This is a standalone Google Maps JavaScript API test for the Johnny Vapes TV traffic display.

The previous version defined `initMap()` but never actually invoked it. That caused the page to remain black.

This version uses Google's standard `callback=initMap` loading method.

## Test URL

https://johnnyvapes.github.io/google-reviews-test/

## Important

The API key currently embedded in this test file is a temporary/demo key. After testing, rotate/restrict the key in Google Cloud.

The page intentionally uses the Google Maps JavaScript API rather than the normal Google Maps website. This should avoid the "Open the Google Maps app?" prompt and the normal Maps web UI/search panel.

It displays:
- Manitowoc centered on Johnny Vapes
- Google live traffic layer
- No normal Maps controls
- Full-screen map
