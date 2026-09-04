# Mohamed Selim, personal website

A single-page site. No build step, no framework, no dependencies to install. One HTML file plus the CV.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole website. All CSS and JavaScript are inside it. |
| `Mohamed-Selim-CV.pdf` | The CV the Download CV buttons link to. Do not rename it. |
| `Mohamed-Selim-CV.docx` | The editable CV. Not used by the site; kept here so both versions live together. |
| `robots.txt` | Lets search engines index the site. |
| `sitemap.xml` | One URL, for Google. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. |
| `portrait.png` | **Not included. You need to add this.** See below. |

## Publishing on GitHub Pages

1. Create a new repository on GitHub. If you name it `yourusername.github.io` the site publishes at that address; any other name publishes at `yourusername.github.io/repository-name/`.
2. Upload every file in this folder to the root of the repository, not inside a subfolder. Use **Add file → Upload files** on the repository page and drag them in.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, set Source to **Deploy from a branch**, branch to **main**, folder to **/ (root)**. Save.
5. Wait a minute or two, then open the address GitHub shows at the top of that page.

To update anything later, upload the changed file again and Pages redeploys on its own.

## Adding your photo

The hero shows a placeholder until you add a portrait.

Save it as **`portrait.png`** in the same folder as `index.html`. It should be a cut-out with a transparent background, shoulders up, facing roughly forward. The site drops it into the orange arch automatically. If the file is missing the placeholder shows instead, so nothing breaks either way.

If your photo has a normal background rather than a transparent one, use `remove.bg` or Photoshop first. A rectangular photo will look wrong in the arch.

## Using your own domain

1. Buy the domain, then in **Settings → Pages → Custom domain** enter it and save. GitHub creates a `CNAME` file in the repository.
2. At your domain registrar, add the DNS records GitHub shows on that page.
3. Tick **Enforce HTTPS** once it becomes available, usually within the hour.
4. Then open `index.html` and replace `https://mohamedselim.com/` with your real address in three places: the `canonical` link, the `og:url` tag, and `sitemap.xml`. This only affects search engines and link previews, not whether the site works.

## Editing the text

Everything is in `index.html`. Open it in any text editor and search for the sentence you want to change.

The assistant's answers live near the bottom, after `var K=[`. Each block has an `id`, keywords in `k`, the answer in `a`, and follow-up suggestions in `c`. To change what it says about something, edit the text in `a`. To add a topic, copy an existing block and give it a new `id`.

## Notes

- The site is one file of about 70KB. It loads one web font from Google Fonts and nothing else.
- The assistant runs entirely in the visitor's browser. There is no API key in the file and nothing a visitor types is sent anywhere.
- The page works with JavaScript disabled, and prints cleanly to PDF.
