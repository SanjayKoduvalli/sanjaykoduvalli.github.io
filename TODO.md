# Portfolio to-do list

The single to-do list for the whole portfolio: the home site and every project. Each project's `AI_CONTEXT.md` keeps that project's detailed status; this file keeps the open items in one place. Claude updates it at the end of every work session (tick items, add new ones, keep the date current).

Last updated: 2026-11-10

**Status key:** ⬜ not started · 🔄 in progress · ⏸ waiting on Sanjay · ✅ done (moved to "Done" at the bottom)

## Housekeeping (do first)
- ⏸ **Push the uncommitted changes.** Home site: `assets/site.css` (shared sticky header). Olist: `assets/site.css`, `dashboard/index.html`, `index.html` (the same header on the dashboard and case study).
- ⏸ **Upworthy: first push.** The GitHub repo exists (github.com/SanjayKoduvalli/upworthy_headlines) but the folder isn't a git repository yet: `git init`, add the remote, commit, push. `data/raw/` and `build/` are already excluded by `.gitignore`.
- ⏸ **Confirm GitHub Pages is on** for `sanjaykoduvalli.github.io` and `olist_marketing_and_sales_dashboard` (Settings › Pages › deploy from `main`, root).
- ⬜ Olist `AI_CONTEXT.md`: a few places still describe the pre-rename repo; tidy when next in that project.

## Home site (`sanjaykoduvalli.github.io`)
- ⬜ **Add Upworthy when it's done:** project card with thumbnail; fill its column in the skills matrix (Python automation, A/B testing, regression modeling, statistical analysis, plus data cleaning); add it to the README's project table.
- ⬜ **Blog section** (backlog, not started; Sanjay asked to log it, not start it). First post: using AI to build HTML dashboards as an alternative to Tableau. Cover the HTML approach's limitations (including slowing down as data grows), ease of building in Tableau vs. AI + HTML, and how publishing HTML dashboards compares with large-scale platforms (Power BI, Cognos) on very large datasets.

## Project 1: Olist (`olist_marketing_and_sales_dashboard`)
- ⬜ Step 13 leftovers: review together the Active Sellers and Customer Retention deep dives; design Funnel Over Time (deferred).
- ⬜ Step 14: recommendations for the case-study write-up.
- ⬜ Companion deck (requirement 8): how the dashboard was built, core insights, assumptions, the cumulative-frequency curves and the day-203 cutoff (A8), why retention uses a 90-day window (A15).
- ⬜ Step 16: final QA.

## Project 2: Upworthy (`upworthy_headlines`)
- 🔄 **Classifier step 1 (Sanjay):** in the Headline Classifier artifact (https://claude.ai/artifact/Vw1wA4fVjuhi8yww7d1nta), run the check against the 100 hand labels with both the quick and default model; pick a tier.
- ⬜ Classifier step 2 (Sanjay): run the 14,465 exploratory headlines (242 calls) with the chosen tier.
- ⬜ Claude: export the labels from the artifact's `results` collection, join them to packages via `build/03_features/units.csv.gz`, add feature tests and an independent check, log agreement in NOTES §6.
- ⬜ Develop the analysis on exploratory: A/A false-positive check first; within-test A/B effects of centering a woman (causal); regression with test fixed effects, topic tags, gender × topic (H2) and gender × sentiment.
- ⬜ Sanjay approves the final definitions → `LOCK.md` ("Approved by Sanjay: <date>") → Claude adds the confirmatory data to the classifier page → Sanjay runs it → one confirmatory run of the locked analysis.
- ⬜ Outputs: case-study page with the shared site header, dashboard or charts, and the write-up (state causal vs. descriptive for every result).

## Done
- ✅ Résumé PDF on the home site (2026-11-05).
- ✅ Olist repo restructured, MIT license, case-study page (2026-11-04/05).
- ✅ Upworthy: context, profiling, load and cleaning, 100 blind hand labels, codebook v2 with topic tags (2026-11-04 to 11-10).
