# Roni Margolin · Client Onboarding System

Static HTML pages that serve as the kickoff package for new freelance clients.

## Structure

- `/` (root) — master template pages with `{{Variable}}` placeholders
- `/clients/<client-slug>/` — per-client pages with all variables filled in
- `style.css` — shared stylesheet, brand-aligned
- `assets/` — wordmark and favicon
- `TALLY-FORM-SPEC.md` — spec for the Tally questionnaire form (build once, duplicate per client)

## Pages per client

1. `index.html` — Welcome page with project summary, phase timeline, links to next steps
2. `questionnaire.html` — wrapper page that embeds the per-client Tally form
3. `checklist.html` — content checklist with link to client's Drive folder
4. `payment.html` — Wise transfer instructions with deposit and total

## Per-client setup

1. Create a Google Drive folder for the project (set permissions to "specific people, client's email")
2. Duplicate the Tally questionnaire, rename for the client, update the thank-you redirect
3. Create a new folder under `/clients/<slug>/` with copies of the master HTML files
4. Substitute the `{{Variables}}` (ClientName, ProjectName, ServiceType, Timeline, KickoffDate, DepositAmount, TotalAmount, Currency, DriveFolderURL, TallyEmbed)
5. Commit and push, GitHub Pages auto-deploys

## Pages are not indexed

All pages carry `<meta name="robots" content="noindex, nofollow">` so search engines do not list them.

## Hosting

GitHub Pages, custom domain `onboarding.ronimargolin.com`.
