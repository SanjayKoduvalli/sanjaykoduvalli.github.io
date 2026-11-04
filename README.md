# sanjaykoduvalli.github.io

Source for my analytics portfolio home page: https://sanjaykoduvalli.github.io/

The home page lists my credentials, a skills × projects matrix, and the projects. Each project lives in its own repository with its own case-study page and dashboard, served by GitHub Pages at `https://sanjaykoduvalli.github.io/<repo-name>/`.

| Project | Repository |
|---|---|
| Olist: from seller lead to customer revenue | [olist_marketing_and_sales_dashboard](https://github.com/SanjayKoduvalli/olist_marketing_and_sales_dashboard) |

## Files
- `index.html`: the home page (plain HTML, no build step).
- `assets/site.css`: site styles, shared with every project's case-study page (each project repo keeps its own copy).
- `assets/Sanjay_Koduvalli_Resume.pdf`: the résumé behind the download button.
- `assets/olist-dashboard.png`: project thumbnail.

## Adding a project
1. Build the project in its own repo, with a case-study `index.html` at the root using `assets/site.css`, and turn on GitHub Pages for it.
2. Add a column to the skills matrix and a project card in `index.html`.
