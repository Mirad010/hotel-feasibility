# Final Project Proposal: Hotel Feasibility Studio

## What I'm building

A web app that tells you whether building a hotel at a specific location would actually make financial sense.

## Who it's for / why I chose this

My family owns property in Tashkent and we often talk about building a hotel there, but nobody ever sits down and does the real math. I wanted a tool where you click a location and instantly see whether the numbers work, using real economic data instead of guessing. I'm also connecting concepts from my accounting course (break-even analysis) and finance course (payback period and NPV) to something I would actually use.

## Core features

- Click anywhere on a map to pick a site; the app looks up that country's GDP per capita (World Bank API) and scales realistic construction costs and room rates to that economy
- Checks OpenStreetMap for real hotels, attractions, and restaurants within 3 km of the pin, and uses that to estimate occupancy
- Sliders for every assumption (rooms, cost, rate, occupancy, fixed costs) that recalculate everything live
- Break-even occupancy bar, 15-year cash flow chart, and key metrics (total investment, profit per year, payback period, RevPAR)
- Live currency conversion (USD, UZS, EUR, AED, TRY) and the ability to save and compare multiple sites side by side using localStorage

## What I don't know yet

- Whether the formula I'm using to turn GDP per capita into construction cost and room rate holds up for very rich or very poor countries, or just breaks down at the extremes
- How to make the numbers make sense to someone opening the site for the first time, without me standing there explaining where each one came from
- Whether the free Overpass API (OpenStreetMap data) will stay reliable during the actual demo, since it has been slow or unresponsive at times
- How to make the layout work well on a phone screen, since I've mostly been testing on my laptop