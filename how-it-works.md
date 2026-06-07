# How We Built the World Cup 2026 App 🏆

A short write-up of what the app is, what it does, and how it came together — so you can get the full picture in a couple of minutes.

## 🔗 The live app

**https://arthur-falcon1999.github.io/worldcup-2026/**

That's it — open the link on any phone or computer, no install, no login. Share it with anyone.

## What it is

A single web page showing the **full FIFA World Cup 2026 schedule** (hosted across USA · Canada · Mexico). Every match, every stage, in one scrollable page.

### What it does

- **🕐 All kickoff times in Mountain Time** — times are stored in UTC and converted to your local Mountain Time right in the browser, so there's no timezone math to do.
- **🔍 Search** — type a team name to instantly filter to just their matches.
- **🏷️ Filter chips** — tap to jump to a group (A through L) or a knockout round (Round of 32, Round of 16, Quarter-finals, Semi-finals, Final).
- **⏳ Countdown** — a live countdown to the opening match.
- **📊 FIFA rankings** — each team shows its world ranking in parentheses (e.g. "Argentina (1)").
- **🔗 Team links** — tap any team name to open its official FIFA.com page.
- **🚩 Flags & clean design** — flag emojis, a dark theme, and a layout that works well on a phone.

## How it was built

The whole thing was built conversationally — I described what I wanted, and it was created and refined step by step:

1. **First version** — the core schedule with all fixtures, kickoff times converted to Mountain Time, and links to each team's FIFA page.
2. **Added a README** with the live link so it's easy to share.
3. **Added group filters** — the A–L chips to jump to any group.
4. **Added FIFA world rankings** next to each team name.

Each change was a small request, applied on top of the last — that's why it ended up polished without ever being one big complicated task.

## The tech (the simple version)

- It's **one self-contained `index.html` file**. All the styling, the schedule data, and the interactive bits (search, filters, countdown) live inside that single file — nothing else to load.
- It's hosted **free on GitHub Pages**, which just serves that one file at the link above. No server, no database, no running costs.
- Because everything runs in your browser, the timezone conversion is automatic and the page loads instantly.

## TL;DR

It's a free, shareable, single-page World Cup 2026 schedule with search, filters, a countdown, and team links — all kickoff times in Mountain Time. Built piece by piece in a chat, and it lives at the link up top. 🌎⚽
