# MetricForge Website

Static website for MetricForge — analytics templates & workflow automation.

## Site structure

```
/
├── index.html        → Homepage
├── templates.html    → Template store
├── services.html     → Automation services
├── blog.html         → Blog listing
├── about.html        → About page
├── contact.html      → Contact form (Netlify Forms)
├── style.css         → Shared brand stylesheet (colors, nav, footer, cards)
└── posts/
    └── fair-daily-targets.html  → Sample blog post (copy this file for new posts)
```

## Brand system (defined in style.css)

| Token | Value | Use |
|---|---|---|
| Navy | `#1B2A4A` | Primary, headings, buttons |
| Teal | `#00C2A8` | Accent, links, highlights |
| Slate | `#5C6B7A` | Body/secondary text |
| Off-white | `#F7F9FB` | Page background |
| Amber | `#FFB020` | CTA buttons |

Fonts: **Poppins** (headings), **Inter** (body) — loaded from Google Fonts.

## How to deploy (GitHub + Netlify)

1. Create a GitHub repo (e.g. `metricforge-site`) and upload ALL files/folders, keeping the structure above.
2. In Netlify: **Add new site → Import an existing project → GitHub → select the repo**.
   - Build command: leave blank
   - Publish directory: `/`
3. Deploy. Netlify gives you a `*.netlify.app` URL immediately.
4. Custom domain: Site settings → Domain management → Add custom domain, then add the DNS records Netlify shows you at your registrar.

## How to add a new blog post

1. Copy `posts/fair-daily-targets.html` → rename it (e.g. `posts/my-new-post.html`).
2. Edit the title, meta description, post-meta line, and article content.
3. In `blog.html`, add (or update) a post card linking to the new file.
4. Commit/push (or drag-drop to Netlify) — the site updates automatically.

## Forms

The contact form and blog subscribe form use **Netlify Forms** (`data-netlify="true"`).
Submissions appear in the Netlify dashboard under **Forms** — no backend needed.
Works automatically once deployed on Netlify.

## Notes

- All demo content uses fictional sample data only.
- Template prices/copy are placeholders — edit freely in the HTML.
