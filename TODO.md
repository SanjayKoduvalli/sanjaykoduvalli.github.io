# Portfolio to-do list

The single to-do list for the whole portfolio: the home site and every project. Each project's `AI_CONTEXT.md` keeps that project's detailed status; this file keeps the open items in one place. Claude updates it at the end of every work session (tick items, add new ones, keep the date current).

Last updated: 2026-11-11 (01:10)

**Status key:** ⬜ not started · 🔄 in progress · ⏸ waiting on Sanjay · ✅ done (moved to "Done" at the bottom)

## Housekeeping (do first)
- ⏸ **Push the feedback changes (2026-11-11).** Home site: `index.html`, `assets/site.css`, `TODO.md`. Olist: `index.html`, `assets/site.css`, `dashboard/index.html`, `AI_CONTEXT.md`, `NOTES.md`, `docs/decision_register.md`.
- ⏸ **Push the latest changes** in all three repos (Upworthy analysis + case study; home-site Upworthy card; shared site.css in each repo). Then turn on GitHub Pages for `upworthy_headlines`.
- ⏸ **Confirm GitHub Pages is on** for `sanjaykoduvalli.github.io` and `olist_marketing_and_sales_dashboard` (Settings › Pages › deploy from `main`, root).
- ⬜ Olist `AI_CONTEXT.md`: a few places still describe the pre-rename repo; tidy when next in that project.

## Home site (`sanjaykoduvalli.github.io`)
- ⏸ **Colin's tooltip note** on "See the projects" was cut off; ask him what he meant. Projects now sit right under the hero, which may already cover it.
- ⬜ Olist card outcome line (Colin): Sanjay chose to change only the case study for now (2026-11-11); revisit if the card should echo the findings → actions.
- ✅ Upworthy card, thumbnail and skills-matrix column added (2026-11-11). Skills list revised: added Data visualization and Text classification rows; rewrote the A/B testing, regression and statistical analysis descriptions to match what was actually shown (no power analysis, logistic not linear regression, no correlation analysis).
- ⬜ **Blog section** (backlog, not started; Sanjay asked to log it, not start it). First post: using AI to build HTML dashboards as an alternative to Tableau. Cover the HTML approach's limitations (including slowing down as data grows), ease of building in Tableau vs. AI + HTML, and how publishing HTML dashboards compares with large-scale platforms (Power BI, Cognos) on very large datasets.

## Project 1: Olist (`olist_marketing_and_sales_dashboard`)
- ⬜ Step 13 leftovers: review together the Active Sellers and Customer Retention deep dives; design Funnel Over Time (deferred).
- ⬜ Companion deck (requirement 8): how the dashboard was built, core insights, assumptions, the cumulative-frequency curves and the day-203 cutoff (A8), why retention uses a 90-day window (A15).
- ⬜ Step 16: final QA.

## Project 2: Upworthy (`upworthy_headlines`)
- ✅ Classifier checked against the 100 hand labels (default model chosen) and run on all 14,465 exploratory headlines; labels imported (`docs/validation/classifier_labels_exploratory.csv.gz`).
- ✅ Sentiment rule kept ("the note it ends on", R16); classifier locked, stage 1 of LOCK.md (R15).
- ✅ Confirmatory headlines labeled (58,613 units, 977 calls) and imported (`docs/validation/classifier_labels_confirmatory.csv.gz`); outcomes still locked.
- ✅ A/A check run: 26% false positives (expected 5%) → overdispersion, φ ≈ 2 (R17).
- ✅ AA6 calibration approved and run: φ = 1.96; held-out false positives 5.5% / 8.6% (R18).
- ✅ Main analysis approved (R19) and run on exploratory; all validation checks pass (`docs/results/main_effects.md`).
- ⏸ **Sanjay:** run the statsmodels check on his Mac (`pip3 install statsmodels`, then `python3 scripts/checks/statsmodels_check.py` in the project folder).
- ✅ Main method: the model's own noise factor φ = 3.83 (R20).
- ✅ Topic analysis approved and run on exploratory (R21): `docs/results/topic_effects.md`.
- ✅ Stage-2 lock approved (R22); confirmatory run once; results of record in `docs/results/confirmatory/` (NOTES §8.4).
- ⬜ Claude: feature tests and an independent check on the imported labels.
- ⬜ Develop the analysis on exploratory: A/A false-positive check first; within-test A/B effects of centering a woman (causal); regression with test fixed effects, topic tags, gender × topic (H2) and gender × sentiment.
- ⬜ Sanjay approves the final analysis definitions → `LOCK.md` stage 2 ("Approved by Sanjay: <date>") → one confirmatory run of the locked analysis.
- 🔍 Case study draft built (R23): `index.html` + `notebooks/walkthrough.ipynb`. **Sanjay:** review the page (open `~/projects/upworthy_headlines/index.html`), then push and turn on GitHub Pages for the repo.

## Done
- ✅ Reviewer feedback (Colin, Sheetal), 2026-11-11. Home: Projects moved above the skills matrix; Olist card lists the matrix skill names and links to its tinted matrix column; placeholder renamed "Coming next". Olist case study: findings paired with four recommended actions near the top (step 14), "Key decisions" → "Analysis decisions", limitations after validation and decisions; R$ what-if declined (Olist R34).
- ✅ Résumé PDF on the home site (2026-11-05).
- ✅ Olist repo restructured, MIT license, case-study page (2026-11-04/05).
- ✅ Upworthy: context, profiling, load and cleaning, 100 blind hand labels, codebook v2 with topic tags (2026-11-04 to 11-10).
