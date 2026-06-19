# How We Built the World Cup 2026 App 🏆

A short write-up of what the app is, what it does, and how it came together — so you can get the full picture in a couple of minutes.

## 🔗 The live app

**https://arthur-falcon1999.github.io/worldcup-2026/**

That's it — open the link on any phone or computer, no install, no login. Share it with anyone.

## What it is

A single web page showing the **full FIFA World Cup 2026 schedule** (hosted across USA · Canada · Mexico). Every match, every stage, in one scrollable page — and, once the tournament kicks off, a live picture of who's winning, who's through, and what the USA needs to do next.

### What it does

- **🕐 All kickoff times in Mountain Time** — times are stored in UTC and converted to your local Mountain Time right in the browser, so there's no timezone math to do.
- **🔍 Search** — type a team name to instantly filter to just their matches.
- **🏷️ Filter chips** — tap to jump to a group (A through L) or a knockout round (Round of 32, Round of 16, Quarter-finals, Semi-finals, Final).
- **📅 Today first** — the day's matches sit right at the top; earlier days tuck behind a toggle so you're not scrolling past finished games.
- **⏳ Countdown** — a live countdown to the opening match.
- **📊 FIFA rankings** — each team shows its world ranking in parentheses (e.g. "Argentina (1)").
- **🔗 Team & game links** — tap a team name for its official FIFA.com page, or tap a match to open its ESPN live game page.
- **🚩 Flags & clean design** — flag emojis, a dark theme, and a layout that works well on a phone.
- **🔄 Always fresh** — when a new version is deployed, a small banner offers to reload so you're never stuck on a stale page.

## The four tabs — the live tournament tracker

Once the group stage starts, the app is more than a schedule. Four tabs across the top let you switch between the fixtures and a live, self-updating read on the tournament. All the live data comes straight from ESPN's public soccer feed — the same numbers the scoreboards show — so nothing has to be typed in by hand.

### 📅 Schedule

The home view: every fixture in order. As games go live, the cards show the **current score and a LIVE marker**; once a match finishes, the **final result** sticks so you can scroll back and see how each day went. Past-day scores are backfilled, so a result that happened while you were away still shows up.

### 📊 Group standings

A live league table for **every group, A through L** — played, won, drawn, lost, goal difference, points — sorted exactly the way FIFA sorts them and refreshed straight from ESPN. It's the at-a-glance answer to "who's top of the group right now?"

### 🇺🇸 USA scenarios

The "what does the USA actually need?" tab. It shows the **live Group D table** and then translates the standings into **plain-English qualification paths** — "win and you're through," "a draw still does it unless X happens," and so on. The clever part: it works through *every possible combination* of the other Group D results and the eight-best-third-place math, then writes out the shortest honest version of each outcome — including who a top-2 finish would line the USA up against in the Round of 32.

### 🥉 3rd-place race

The World Cup 2026 format sends the **top two from every group plus the eight best third-placed teams** to the Round of 32 — so finishing third doesn't necessarily mean you're out. This tab pulls the third-placed team from all twelve groups, ranks them by the FIFA tiebreakers (points, then goal difference, then goals scored), and draws the **cut-off line between 8th and 9th**. Teams above the line are provisionally through; the order shifts live as groups finish and results come in.

## How it was built

The whole thing was built conversationally — I described what I wanted, and it was created and refined step by step:

1. **First version** — the core schedule with all fixtures, kickoff times converted to Mountain Time, and links to each team's FIFA page.
2. **Added a README** with the live link so it's easy to share.
3. **Added group filters** — the A–L chips to jump to any group.
4. **Added FIFA world rankings** next to each team name.
5. **Added live ESPN scores** — match cards started showing live and final results, and link out to the ESPN game page.
6. **Added the Group standings tab** — a live table for every group.
7. **Put today's games on top** and tucked earlier days behind a toggle.
8. **Added the USA scenarios tab** — the live Group D table plus every qualification path in plain English.
9. **Added the 3rd-place race tracker** and wired it into the USA scenarios.

Each change was a small request, applied on top of the last — that's why it ended up polished without ever being one big complicated task.

## The tech (the simple version)

- It's **one self-contained `index.html` file**. All the styling, the schedule data, and the interactive bits (search, filters, countdown, the live tabs) live inside that single file — nothing else to load.
- The live scores, standings, and 3rd-place math all read from **ESPN's public soccer API** right in your browser. There's no backend of our own — the page just asks ESPN for the latest numbers and renders them.
- It's hosted **free on GitHub Pages**, which just serves that one file at the link above. No server, no database, no running costs.
- Because everything runs in your browser, the timezone conversion is automatic and the page loads instantly.

## TL;DR

It's a free, shareable, single-page World Cup 2026 app: the full schedule with search, filters, a countdown, and team links — all in Mountain Time — plus four live tabs once play begins (schedule scores, group standings, USA qualification scenarios, and the best-third-place race), all updating straight from ESPN. Built piece by piece in a chat, and it lives at the link up top. 🌎⚽
