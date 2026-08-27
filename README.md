# Johnny Vapes Traffic Maps v9 — 511WI Incident Feed Test

This version keeps Google Maps traffic exactly as before, but removes the direct browser-to-511WI API request.

## How the incident feed works

GitHub Actions requests the 511WI Events API every 10 minutes using the repository secret `WI_511_API_KEY`. The returned events are stored in `events.json` on the GitHub Pages site. The three display pages read that same JSON file and locally filter events to an 18-mile radius around their store location(s).

This means:
- The 511WI developer key is NOT placed in the HTML.
- The Chromecast/browser never calls 511WI directly.
- All three displays share one 511WI request every 10 minutes.
- Google TrafficLayer remains independent and continues to provide the live traffic visualization.
- If 511WI has no events near a store, the panel explicitly says there are no active closures/incidents nearby.

## One-time GitHub setup

1. In the repository, open **Settings → Secrets and variables → Actions**.
2. Create a repository secret named exactly:
   `WI_511_API_KEY`
3. Paste the 511WI developer key as the secret value.
4. Make sure Actions are enabled for the repository.
5. Open **Actions → Update 511WI incident feed** and use **Run workflow** for the first test.
6. After the first successful run, `events.json` will be populated and the displays will begin showing nearby readable incidents.

The scheduled workflow runs every 10 minutes. It only commits `events.json` when the actual event data changes, so it does not create a new Git commit every 10 minutes when nothing has changed.

## Pages

- `green-bay.html`
- `manitowoc.html`
- `weston.html`

## Important

Do not put the 511WI developer key directly into any HTML or JavaScript file. The key should remain an Actions repository secret.
