# Digital Jetplus — Full Website (v1)

A complete multi-page static website for Digital Jetplus, the Kampala-based digital marketing agency. Theme matched to your Figma template: near-black surfaces, vibrant green primary accent with periwinkle and peach details, Poppins + Figtree + JetBrains Mono type system. All pricing is in Ugandan Shillings (UGX), positioned as the most affordable professional tier for Ugandan businesses and individuals.

## Run it

No build step. It is plain HTML/CSS/JS.

- **Locally:** double-click `index.html` (or any page). Everything works from the file system.
- **Hosting:** upload the entire folder to any static host (cPanel, Netlify, Vercel, GitHub Pages). Point the domain at it. Done.

## Pages (28)

| Group | Files |
|---|---|
| Core | `index.html`, `about.html`, `services.html`, `portfolio.html`, `blog.html`, `pricing.html`, `contact.html`, `start-project.html`, `404.html` |
| Services | `seo.html`, `web-development.html`, `social-media.html`, `video-production.html`, `content-writing.html`, `ppc.html`, `mobile-apps.html`, `business-consulting.html` |
| Case studies | `case-artem.html`, `case-mayhem.html`, `case-basile.html`, `case-foodhub.html`, `case-learnhub.html`, `case-techstart.html` |
| Blog articles | `blog-social-media-trends-2026.html`, `blog-scale-startup.html`, `blog-conversion-optimization.html`, `blog-data-driven-marketing.html`, `blog-gtm-strategy.html`, `blog-ai-marketing.html` |

Shared assets: `assets/css/styles.css` (design system), `assets/js/main.js` (nav, reveals, counters, portfolio filter, forms), `assets/img/` (15 custom photos generated for this build).

## How to edit

- **Brand color:** open `assets/css/styles.css`, change `--accent` (and `--accent-strong`, `--accent-soft`, `--accent-ink`) at the top. Every page updates instantly.
- **Your real photos:** drop your files into the site root and the site will prefer them automatically:
  - `DIGITALJETPLUS LOGO.png` — logo in nav + footer
  - `FORE FRONT FINAL.png` — homepage hero (falls back to `assets/img/hero-team.jpg` if missing)
  - `CONTROL DESK.png` — "Why choose us" image (falls back to `assets/img/control-desk.jpg`)
  - All other imagery lives in `assets/img/` — replace any `.jpg` keeping the same filename.
- **Contact details:** phone and WhatsApp number are set in `assets/js/main.js` (`WHATSAPP_NUMBER`, `CONTACT_EMAIL`). They are also written in each page's footer and contact page — search-and-replace `256702634715` / `omulebrianfredrick@gmail.com` across files if they ever change.
- **Text content:** all copy is plain HTML in each page. Service prices live in the service pages and `pricing.html`; booking form options live in `start-project.html`.
- **Blog:** each article is one self-contained HTML file; add a new one by copying an existing `blog-*.html` and adding a card in `blog.html`.

## How the forms work

- **Start a project** (`start-project.html`): the form opens WhatsApp with the details pre-filled (`wa.me` link). No backend needed.
- **Contact** (`contact.html`): the form opens the visitor's email app with the message composed (`mailto:`). No backend needed.
- Optional upgrade: wire both forms to Formspree/Netlify Forms if you prefer inbox delivery over WhatsApp.

## Quality notes

- Responsive across desktop, tablet, and mobile (breakpoints at 1080/920/600px).
- Semantic HTML, skip-link, focus states, `aria-current` nav marking, alt text on all images.
- `prefers-reduced-motion` respected (animations collapse to static).
- Portfolio filter, animated counters, mobile menu, and FAQ accordions are dependency-free vanilla JS.
- `404.html` included — configure it as the error page on your host if possible.

## Known intentional placeholders

- Client metrics and testimonials come from your original homepage copy. Replace or verify them before going live.
- The blog article dates are set to 2026 to look current; adjust if you prefer the original dates.
