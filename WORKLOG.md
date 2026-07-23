# Work Log — Hotel Feasibility Studio

## Week of July 12–19

- Picked the idea: a hotel feasibility calculator, based on my family's property in Tashkent
- Set up the repo, wrote PROPOSAL.md
- Built the first working version: sliders for rooms, cost, room rate, occupancy, fixed costs, all recalculating live
- Added the break-even bar and the 15-year cash flow chart
- Added the map and live currency conversion
- Deployed to GitHub Pages, submitted the live URL

**AI collaboration:** I talked through the idea with Claude first — what a hotel feasibility tool would actually need (break-even, payback, RevPAR) — since I wanted to make sure I was using the right formulas from my accounting and finance classes before building anything. Once I knew what I wanted, I had it help me write the code faster than typing it all myself, but I decided what features to include and checked that the math matched what I learned in class.

## Week of July 20–24

- Noticed the map wasn't actually affecting the results — you could click different cities and the numbers stayed the same, which didn't make sense for a "feasibility" tool
- Talked it through with Claude about how to fix this properly. We went back and forth on a few options — I didn't want to just make up fake numbers per city, so we looked for real data instead. Landed on using GDP per capita by country (real World Bank data) to scale construction cost and room rate, and OpenStreetMap data (real hotels/attractions/restaurants near the pin) to scale occupancy
- First version of the OpenStreetMap part broke during testing — it just didn't respond. Went through it with Claude, figured out the request format was the problem, fixed it so it tries a few backup servers if the first one is slow
- Fixed my PROPOSAL.md and README.md — I originally had the proposal content sitting in the README by mistake, so I split them properly and added the "what I don't know yet" section
- Went through my demo walkthrough a few times to make sure I could actually explain how the map connects to the sliders in my own words — that part confused me at first too, so I made sure I understood it before presenting instead of just reading off a script

**What I'd still improve:** the GDP formula is a simplification. If I kept working on this I'd want to compare it against real hotel investment numbers to see how close it actually gets.