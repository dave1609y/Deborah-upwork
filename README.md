# Deborah E. — AI UGC Ads & Avatar Video Studio

A single-page portfolio site for an AI UGC ad / avatar commercial studio, built to be hosted free on GitHub Pages. Emerald & cream editorial design, no build step, no dependencies beyond two Google Fonts.

## Files

- `index.html` — the entire site (structure, styles, and script in one file)
- `robots.txt` — tells search crawlers the site is fully indexable and points to the sitemap
- `sitemap.xml` — the one-page sitemap search engines use to find and re-check the page
- `README.md` — this file

## 1. Put it on GitHub Pages

1. Create a new GitHub repository (public), e.g. `debbie-ai-studio`.
2. Upload all four files to the root of that repository.
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a live URL shortly after, in the form:
   `https://YOUR-USERNAME.github.io/YOUR-REPO/`

If you'd rather the site live at the root of your GitHub username (no repo name in the URL), name the repository exactly `YOUR-USERNAME.github.io` instead — the URL will then just be `https://YOUR-USERNAME.github.io/`.

## 2. Replace the placeholder domain (important)

Three files currently use `https://your-username.github.io/your-repo/` as a placeholder:

- `index.html` — in the `<link rel="canonical">` tag, the Open Graph/Twitter tags, and the JSON-LD structured data block near the top of `<head>`
- `robots.txt` — in the `Sitemap:` line
- `sitemap.xml` — in the `<loc>` tag

Once your Pages URL is live, do a find-and-replace across these three files, swapping the placeholder for your real URL (from step 5 above). This step matters for SEO — search engines and AI answer engines use these exact URLs to confirm the page is genuinely at that address.

## 3. What's built in for search and AI visibility

- **SEO**: descriptive `<title>` and meta description, semantic HTML5 (`header`, `main`, `section`, `article`, `footer`), one `<h1>`, a logical heading order, a canonical URL, Open Graph and Twitter card tags, and a submitted sitemap.
- **AEO/GEO** (answer engine & generative engine optimization): the FAQ section is marked up with `FAQPage` structured data (JSON-LD) so AI-driven search and chat answers can quote it directly and attribute it correctly, plus a `Person` and `ProfessionalService` schema describing who you are and what you offer in language a model can parse without guessing.
- **Accessibility/quality floor**: visible keyboard focus states, `prefers-reduced-motion` support, alt-free decorative graphics marked `aria-hidden`, and a responsive layout down to small phones.

## 4. Easy things to customize

- **Contact details** live in the `#contact` section and the floating WhatsApp button near the end of `index.html` — search for `wa.me` and the email address to update either.
- **Portfolio cards** are in the `#work` section (`grid-portfolio`) — swap in your own titles and one-line descriptions as new projects go live. If you'd like real thumbnail images instead of the styled color blocks, replace the `.work-thumb` `<div>` with an `<img>` tag pointing at an image file you add to the repo.
- **FAQ answers** are duplicated in two places on purpose: once in the visible `<details>` accordion in `#faq`, and once in the JSON-LD `FAQPage` script in `<head>`. Keep both in sync if you edit them, since the structured data is what AI answer engines actually read.
- **Rates**: the site intentionally avoids stating a fixed price in the visible text (rates on Upwork can change), pointing people to message for a quote instead. Edit the pricing FAQ answer if you'd like to state a number directly.

## 5. Testing locally before you deploy

No server or build step is required — `index.html` can be opened directly in a browser to preview it. For a closer approximation of how GitHub Pages serves it, run a simple local server from the folder, e.g. `python3 -m http.server`, then visit `http://localhost:8000`.
