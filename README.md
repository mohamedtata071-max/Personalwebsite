# Mohamed Selim, personal website

A single-page site. No build step, no framework, no dependencies to install. One HTML file plus the CV.

## Files

| File | What it is |
|---|---|
| `index.html` | Home: intro, about, career story |
| `experience.html` | Expertise, work experience, education |
| `projects.html` | The tools you have built |
| `opportunities.html` | Current industrial opportunities and an enquiry form |
| `contact.html` | WhatsApp, email, phone, LinkedIn, message form |
| `Mohamed-Selim-CV.pdf` | The CV the Download CV links point to. Do not rename it. |
| `Mohamed-Selim-CV.docx` | The editable CV |
| `logo.png`, `favicon.png` | Your signature mark, used in the header and as the browser icon |
| `robots.txt`, `sitemap.xml` | For search engines |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Publishing on GitHub Pages

1. Create a new repository on GitHub. If you name it `yourusername.github.io` the site publishes at that address; any other name publishes at `yourusername.github.io/repository-name/`.
2. Upload every file in this folder to the root of the repository, not inside a subfolder. Use **Add file → Upload files** on the repository page and drag them in.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, set Source to **Deploy from a branch**, branch to **main**, folder to **/ (root)**. Save.
5. Wait a minute or two, then open the address GitHub shows at the top of that page.

To update anything later, upload the changed file again and Pages redeploys on its own.

## Using your own domain

1. Buy the domain, then in **Settings → Pages → Custom domain** enter it and save. GitHub creates a `CNAME` file in the repository.
2. At your domain registrar, add the DNS records GitHub shows on that page.
3. Tick **Enforce HTTPS** once it becomes available, usually within the hour.
4. Then open `index.html` and replace `https://mohamedselim.com/` with your real address in three places: the `canonical` link, the `og:url` tag, and `sitemap.xml`. This only affects search engines and link previews, not whether the site works.

## The opportunities page

The eight parks are real, taken from your own Elsewedy work and cross-checked against elsewedydevelopment.com: October, East, SOKHNA360, Sokhna, Asher, New Sadat, Borg El Arab, and Industria West marked sold out.

No prices, plot sizes or payment terms are published, deliberately. Those change, they vary by client, and they are the company's to quote, not a personal site's. The page says you quote them per enquiry.

If a park sells out or a new one opens, edit the `<article class="opp">` blocks in `opportunities.html` and the matching `<option>` in the enquiry form.

## How the forms work

There is no server behind this site, so the two forms build an email from what the visitor types and open it in their mail app addressed to you. Nothing is stored anywhere and there is no third-party service involved.

If you would rather receive submissions without the visitor's mail app opening, sign up at **formspree.io** (free tier), then in `contact.html` and `opportunities.html` change `<form class="form rv" data-mail ...>` to `<form class="form rv" action="https://formspree.io/f/YOURID" method="POST">` and remove the `data-mail` attribute.

## Editing the text

Everything is in `index.html`. Open it in any text editor and search for the sentence you want to change.

The assistant's answers live near the bottom, after `var K=[`. Each block has an `id`, keywords in `k`, the answer in `a`, and follow-up suggestions in `c`. To change what it says about something, edit the text in `a`. To add a topic, copy an existing block and give it a new `id`.

## Notes

- The site is one file of about 70KB. It loads one web font from Google Fonts and nothing else.
- The assistant runs entirely in the visitor's browser. There is no API key in the file and nothing a visitor types is sent anywhere.
- The page works with JavaScript disabled, and prints cleanly to PDF.
