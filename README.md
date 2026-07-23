# Hotel Feasibility Studio

## What does this project do?

Hotel Feasibility Studio helps you figure out whether building a hotel at a specific location would actually make financial sense.

Click anywhere on the map, and the app pulls two real data sources: that country's GDP per capita from the World Bank (to scale realistic construction costs and room rates to that economy), and OpenStreetMap data on hotels, attractions, and restaurants within 3 km of the pin (to estimate occupancy). From there it calculates total investment, profit per year, payback period, RevPAR, break-even occupancy, and a 15-year cash flow projection — all in real time as you adjust any assumption.

## How do I use it?

Live site: **https://mirad010.github.io/hotel-feasibility/**

1. Click anywhere on the map, or pick one of the city presets, to choose a site
2. The sliders on the right fill in with realistic starting numbers for that location
3. Adjust any slider (rooms, cost, rate, occupancy, fixed costs) — everything recalculates instantly
4. Check the break-even bar and the 15-year chart to see if the site works financially
5. Switch currencies with the dropdown, and save a scenario to compare it against another site

## What I learned building this

- How to combine multiple free public APIs (World Bank, OpenStreetMap's Overpass API, a reverse geocoding service, and a live exchange rate API) into one tool without needing a backend
- How to translate financial concepts from my accounting and finance classes (break-even analysis, payback period, NPV) into working JavaScript formulas
- How to handle unreliable third-party APIs gracefully — the Overpass API is sometimes slow, so the app falls back to multiple mirror servers and degrades gracefully instead of breaking
- How to use localStorage to persist data across sessions without a database

## Status

Deployed and working at the live URL above.