## Agent-ready API endpoints, snapshot 15 Nov 2026

- 2,518,343 endpoints passed a keyless data call, tested 10–15 Nov 2026 (IST)
- 65,954 services · 251 country codes · 2,518,343 keyless JSON rows

### Download

- `Agent_Ready_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz`: the full list, 2,518,343 rows, 83.3 MB gzipped (787.8 MB as CSV), SHA-256 `77bfadf95a8a9e3be870b2a8b3179f10effe05eee64ffa9518aab5dc2a1a8e1e`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Agent_Ready_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Agent_Ready_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 84,731 · Wrap one URL pattern per source as a tool (get_observation, get_river_level, get_forecast, get_metar): pass a station id, airport code or coordinates, return the value, its unit and its time, with a timeout.
- 📱 App features: 81,911 · Show what is near a user on a card or a map: bikes and docks at a station, the status of a transit line, open parking spaces or the air-quality reading, refreshed when the card opens.
- 🧠 Grounding and data pipelines: 206,812 · Load indicators and statistics tables on a schedule into your own store, so an agent answers with a figure, its period and the source URL.
- 🧪 Evals and testing: 2,518,343 · Run your agent against a fixed set of URLs from many services and topics; check that each JSON body parses into the fields your tools return, and keep last_tested as the baseline for your own re-tests.

### Changes

- First release
- Left out: 1,747 rows whose URL carried a credential-looking parameter or a login.
- Left out: 52 rows with a private or local address.
- Left out: 134 rows with an email-like address.
- Left out: 43,873 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 12 camera or image URLs (webcam and camera feeds, picture and video files).
- Left out: 1,241 class-exercise copies of the same few ArcGIS Online layers (Miami Beach sea level rise, high-risk areas without shelter, flooded areas, sea level rise and storm surge maps) across many organisations, many with a person's name in the title.
- Left out: 508 layers marked editable in the title (they can hold entries that people added).
- Left out: 63 police traffic-stop layers (they can hold details of people stopped).
- Left out: 7,384 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 118 rows that passed a data call only from a network location in India.
- Left out: 6 rows whose address or title held a token-like string, a private address or a similar string.
- Left out: 29,512 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 2,829 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 102,908 rows of server information from Mastodon, PeerTube, Lemmy, Nostr and other social network servers (instance documents name the server's contact person).
- Left out: 1 row that repeats an address already in the pack.
- Overlap: 130,964 of these URLs are also in 190k-weather-apis-for-agents.
- Overlap: 196,830 of these URLs are also in 270k-transit-apis-for-agents.
- Overlap: 226,036 of these URLs are also in 270k-water-apis-for-agents.
- Overlap: 89,012 of these URLs are also in 130k-finance-economy-apis-for-agents.
- Overlap: 32,824 of these URLs are also in 130k-india-apis-for-agents.
- Overlap: 1,008,314 of these URLs are also in 1.3m-government-open-data-apis.
- Overlap: 206,713 of these URLs are also in 290k-statistics-apis-for-agents.
- Overlap: 68,292 of these URLs are also in 86k-oceans-apis-for-agents.
- Overlap: 14,548 of these URLs are also in 24k-maritime-apis-for-agents.
- Overlap: 117,721 of these URLs are also in 170k-environment-apis-for-agents.
- Overlap: 10,830 of these URLs are also in 20k-air-quality-apis-for-agents.
- Overlap: 247,162 of these URLs are also in 380k-maps-gis-apis-for-agents.
- Overlap: 68,037 of these URLs are also in 96k-health-apis-for-agents.
- Overlap: 206,647 of these URLs are also in 380k-science-apis-for-agents.
- Overlap: 45,322 of these URLs are also in 53k-hazards-apis-for-agents.
- Overlap: 6,146 of these URLs are also in 6.5k-wildfire-apis-for-agents.
- Overlap: 51,239 of these URLs are also in 72k-energy-apis-for-agents.
- Overlap: 23,300 of these URLs are also in 25k-aviation-apis-for-agents.
- Overlap: 14,404 of these URLs are also in 24k-traffic-apis-for-agents.
- Overlap: 10,126 of these URLs are also in 12k-parking-apis-for-agents.
- Overlap: 8,696 of these URLs are also in 10k-earthquake-apis-for-agents.
- Overlap: 3,371 of these URLs are also in 5.2k-volcano-tsunami-apis-for-agents.
- Overlap: 16,136 of these URLs are also in 17k-bike-share-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 10–15 Nov 2026; snapshot 15 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 15 Nov 2026.

Credit: Agent-ready API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 15 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
