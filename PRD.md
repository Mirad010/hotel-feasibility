# PRD: Hotel Feasibility Studio

## Problem

Someone considering building a hotel usually relies on gut feeling or a generic spreadsheet template that doesn't account for where the hotel would actually be. There's no quick way to see whether a specific site, in a specific country, at a specific level of local competition, would realistically pay for itself.

## Target user

Someone evaluating a real or hypothetical hotel investment — in my case, my family, thinking about a property in Tashkent. More broadly, anyone comparing hotel sites across different countries and wants a fast financial gut-check before commissioning a real feasibility study.

## Core user flow

1. User opens the site and sees a default location (Tashkent) already loaded with example numbers
2. User clicks anywhere on the map, or picks a city preset
3. The app looks up that location's country, pulls GDP per capita (World Bank), and nearby hotels/attractions/restaurants (OpenStreetMap), and uses both to fill in realistic starting values for construction cost, room rate, fixed costs, and occupancy
4. User adjusts any slider (rooms, cost, rate, occupancy, fixed costs, discount rate) and watches all outputs recalculate instantly
5. User reads the verdict: is this site above or below break-even, what's the payback period, what's the 15-year NPV
6. User optionally saves the scenario with a name, then repeats steps 2-5 for a second location, and compares both in a table

## Features (in build order)

1. **Sliders + live math** — rooms, area, construction cost, furniture, room rate, occupancy, variable cost, fixed costs, discount rate. Outputs: total investment, profit/year, payback period, RevPAR, break-even occupancy, NPV
2. **Chart** — 15-year cumulative cash flow line chart (Chart.js)
3. **Map** — Leaflet + OpenStreetMap, clickable, drops a pin
4. **Location-driven defaults** — reverse geocoding to identify country, World Bank GDP per capita to scale cost/rate assumptions, Overpass API to count nearby hotels/attractions/restaurants and scale occupancy
5. **Currency conversion** — live exchange rates, switch between USD/UZS/EUR/AED/TRY
6. **Scenario comparison** — save current inputs + results under a name in localStorage, view saved scenarios in a table, remove any of them

## Out of scope (for this version)

- Real construction cost or hotel pricing data by exact address (no free API provides this — GDP-based scaling is a deliberate simplification, documented in PROPOSAL.md)
- User accounts or syncing scenarios across devices (localStorage is per-browser only)
- Any backend or database — everything runs client-side, deployable as a static site

## Open questions

- Does the GDP-to-cost scaling formula produce sane numbers at the extremes (very low or very high GDP countries)?
- Should occupancy weight attractions and restaurants differently, or is the current formula (attractions + 0.15 × food spots, minus hotel competition) good enough for a v1?
- Is 3 km the right search radius for the "what's nearby" check, or should it change based on whether the site is urban vs rural?