Manitowoc Traffic Map

This package contains the full Manitowoc HTML page with the current 511WI incident-feed logic, Google TrafficLayer, Johnny Vapes logo marker, zoom 14, 10-minute incident refresh, and the incident panel moved to the LEFT side.

Files:
- manitowoc.html — upload/replace the Manitowoc page
- johnny-logo.png — marker image used by the HTML

The page expects events.json to be present beside manitowoc.html. Your GitHub Actions workflow generates/updates that file every 10 minutes, so do not replace the repository's live events.json with an empty copy from this package.
