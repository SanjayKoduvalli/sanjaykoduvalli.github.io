# AI Context Guide — Portfolio hub

> Start here for any portfolio work. This repo is the home site, and this file is the map of the whole portfolio. Each project has its own `AI_CONTEXT.md` with its rules, detail and status; read that one before working in the project.

Last updated: 2026-11-11

## 1. What the portfolio is
AI-assisted analyses of public datasets by Sanjay Koduvalli (marketing analytics, IBM; previously Macy's), each a case study with reproducible code, validation at every layer, and a dashboard or code output. One GitHub repo per project, served by GitHub Pages at `https://sanjaykoduvalli.github.io/<repo>/`; this repo is the home page (credentials, project cards, skills × projects matrix, résumé).

## 2. Map
| Part | Local folder (Sanjay's Mac) | GitHub | Status |
|---|---|---|---|
| Home site | `~/projects/sanjaykoduvalli.github.io` | github.com/SanjayKoduvalli/sanjaykoduvalli.github.io | Live; Upworthy card and blog to come |
| Project 1: Olist (SQL, funnel and cohort, dashboard design) | `~/projects/olist_marketing_and_sales_dashboard` | github.com/SanjayKoduvalli/olist_marketing_and_sales_dashboard | Dashboard built; write-up, deck and QA left |
| Project 2: Upworthy (Python, cleaning, A/B testing, regression) | `~/projects/upworthy_headlines` (raw data: `~/Downloads/jd64p-osfstorage-archive`) | github.com/SanjayKoduvalli/upworthy_headlines | Classifying headlines; analysis next |

**Open work across everything: `TODO.md` in this repo.** Update it at the end of every session.

## 3. How work is organized (Sanjay, 2026-11-10)
- Work happens in a Claude Project ("Analytics portfolio"). **One conversation per repo at a time**, so two conversations never edit the same files. Different repos can be worked on in parallel.
- The repos are the memory, not the chats. Each conversation starts by reading this file, `TODO.md`, and the project's `AI_CONTEXT.md`, and ends by updating the project's status section and `TODO.md`.
- Work that crosses projects (e.g. adding a finished project to the home site) goes through a short handoff note in `TODO.md`.
- Push to GitHub at the end of each session; resync the Claude Project's GitHub files after pushing.

## 4. Rules that apply to every project
The full rule set is in each project's `AI_CONTEXT.md` (it began in Olist's, §2). In short: one step at a time with Sanjay's approval; approve every calculation before running it; original sources only and always cited; never modify raw files; log every decision (NOTES and `docs/decision_register.md`); state limitations honestly; reproducible by one command; validate meticulously (tests, independent re-derivation, mutation tests); teach the statistics when asked.

## 5. Home-site files
- `index.html`: the home page (plain HTML, no build step). `assets/site.css`: shared styles, copied into each project repo (keep the copies in sync). `assets/Sanjay_Koduvalli_Resume.pdf`, `assets/olist-dashboard.png`.
- Adding a project: build it in its own repo with a case-study `index.html` at the root using `assets/site.css`, turn on Pages, then add a card and a matrix column here. Give the column header an id (like `matrix-olist`), point the card's "See them in the skills matrix" link at it, and add its `:has(#id:target)` highlight rule in `site.css`. Case studies lead with findings paired with recommended actions (Olist R34). No "Project 1/2" labels (Sanjay, 2026-11-11).
