# Final Project Proposal: Hotel Feasibility Studio

## What I want to build

A web app that helps you decide if building a hotel makes financial sense. You enter the basic numbers (how many rooms, construction cost per square meter, room price per night, expected occupancy) and the app instantly calculates the total investment, monthly revenue and profit, break-even occupancy, and how many years it takes to pay back.

## Why this project

My family owns property in Tashkent and we often discuss building a hotel on it, but nobody ever sits down and does the real math. I want a tool where you can just move sliders and see the answer right away. I am also using concepts from my accounting course (break-even analysis) and finance course (payback period), so this project connects what I study with something I would actually use.

## Main features

- Sliders and inputs for all key numbers, everything recalculates live
- Chart showing revenue vs costs and the payback timeline (Chart.js)
- Map where you can drop a pin on your location (Leaflet + OpenStreetMap)
- Live currency conversion through an exchange rate API, so you can switch between USD and local currency
- City presets (Tashkent, Dubai, Istanbul) that fill in realistic starting numbers
- Save and compare scenarios using localStorage, for example a 40 room hotel in Tashkent vs a smaller one in Dubai

## Tech

HTML, CSS, JavaScript. Chart.js for charts, Leaflet for the map, a free exchange rate API for currency. Deployed on GitHub Pages.

