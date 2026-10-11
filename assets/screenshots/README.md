# Product screenshot provenance

Captured October 11, 2026 (Africa/Lagos) from the current ValoPeek React UI in
`website/`, commit `58aeeb8532929ec49ce38e944d88681444e53051` on `main`.
No website source was modified for these captures.

The data source is `website/src/data/sample-matches.json`: seven sanitized
own-player research sample matches, including three Ascent matches. This is
partial recorded sample history, not a live player account. The account name
`Sample preview#DEMO` is a capture label. Keep a visible sample-data caption
where these images are used, especially crops that omit the account label.

| File | Pixels | UI state |
| --- | --- | --- |
| `map-stats-desktop.png` | 1440 × 1440 | Ascent, all matches, Zones view, map labels and overall K/D |
| `zone-kd.png` | 1147 × 1073 | Ascent B Site selected: 3 recorded kills, 4 deaths, zone K/D 0.75 |
| `map-filters.png` | 1147 × 1772 | Ascent Zones view, More filters expanded |
| `map-stats-mobile.png` | 347 × 1317 | Actual map panel at 390 × 844 browser viewport; responsive panel crop |

The underlying sample lacks opponent coordinates, round context and timelines.
No duel coordinates or round timeline data were fabricated. Overall scoreboard
totals can differ from recorded event totals; the desktop screenshot includes
the application's own notice explaining this.

Capture used installed Microsoft Edge via Playwright 1.63.0 and Vite only:

```powershell
# From website/:
npm run dev -- --port 5174
# From workspace root:
node valopeek-pages/.qa/capture-product.cjs
```

The temporary capture script is ignored by `.gitignore`. All `/api/` requests
were fulfilled by Playwright routes with the sample fixture. No API server was
started; no account import or live provider request ran. External browser
requests were blocked. Local bundled map/agent/brand assets and fonts were used.
Images were captured after font and image loading; no UI styling was changed.
The script verified 28 map polygons, selected-zone content, no mobile horizontal
overflow, and zero browser page errors. It requested only `/api/status` and
`/api/session`, both mocked. PNG dimensions were verified from their file headers.
