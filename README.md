# MetricForge Website

Static website for MetricForge — free analytics templates & workflow write-ups, for now.

## Site structure

```
/
├── index.html        → Homepage
├── templates.html    → Free template library
├── services.html     → Automation services (free while starting out)
├── blog.html         → Blog listing
├── about.html        → About page
├── contact.html      → Contact form (Netlify Forms)
├── style.css          → Shared brand stylesheet (colors, nav, footer, cards)
├── templates/
│   └── daily-capacity-calculator.html   → Live, working calculator tool
└── posts/
    ├── fair-daily-targets.html          → Full post
    ├── star-schema-basics.html          → Full post
    └── email-automation.html            → Full post
```

## Current model: everything free

Every template and service is marked **Free** right now. The plan is to keep early
templates free permanently, and introduce paid tiers only for more advanced additions
(team dashboards, multi-user tracking, deeper customization) as the library grows.
Update the `price` text on `templates.html` / `services.html` when that changes.

## Daily posting workflow

Since you're publishing daily, here's the fastest path each time:

1. Copy an existing post as your starting point:
   `posts/fair-daily-targets.html` (case study), `posts/star-schema-basics.html` (technical/Power BI),
   or `posts/email-automation.html` (technical/automation) — pick whichever tone fits.
2. Rename the file to match the topic, e.g. `posts/dax-measures-101.html`.
3. Edit these parts only (everything else stays the same):
   - `<title>` and `<meta name="description">`
   - The post-meta line (category + read time)
   - `<h1>` and the lede paragraph
   - The article body content
4. Add a card in `blog.html`'s post grid pointing to the new file, and update
   the featured post block if it's your best post of the week.
5. Commit and push (or drag-drop the changed files into Netlify) — live in seconds.

Keeping every post on the same template means you're never rebuilding design —
just writing.

## How to deploy (GitHub + Netlify)

1. Create a GitHub repo (e.g. metricforge-site) and upload ALL files/folders, keeping the structure above.
2. In Netlify: Add new site → Import an existing project → GitHub → select the repo.
   - Build command: leave blank
   - Publish directory: /
3. Deploy. Netlify gives you a *.netlify.app URL immediately.
4. Custom domain: Site settings → Domain management → Add custom domain, then add the DNS records Netlify shows you at your registrar.

## Forms

The contact form and blog subscribe form use Netlify Forms (data-netlify="true").
Submissions appear in the Netlify dashboard under Forms — no backend needed.
Works automatically once deployed on Netlify.

## Notes

- All content uses fictional/demo sample data — nothing tied to a real employer.
- The Daily Capacity Calculator is a fully working tool, not a mockup — open it directly in a browser.
