# FieldDraft

A free, open-source CV builder that adapts to your occupation — single HTML file, no backend, no API keys, no accounts, no tracking. Your data never leaves the page.

## What it does

1. **Type your occupation.** FieldDraft matches it against a built-in catalog of 9 fields (Technology, Healthcare, Education, Business/Finance, Creative, Skilled Trades, Customer Service/Hospitality, Legal, Science/Research), each tagged with a catalog code (e.g. `TC-01`, `MD-02`).
2. **Get real search links.** Once matched, the sidebar generates live Google, Bing, and Google Images search links for your *exact* occupation — so you can go look at real CV examples in your field in one click. No scraping, no embedded copyrighted content.
3. **Browse curated hubs.** A short list of reputable general resume-example sites (Indeed, Novorésumé, Resume Genius, Zety) you can browse by field once you're there.
4. **Draft with tailored fields.** The builder's section labels and placeholder hints change based on your matched field — a nurse sees "Clinical Skills" and "Licenses & Certifications," a developer sees "Technical Skills" and "Projects & Certifications," and so on.
5. **Live preview.** Everything you type renders instantly into a clean CV layout styled like an index card.
6. **Export.** Print to PDF using your browser's native print dialog, or download a standalone HTML copy of just the finished CV.

## Why no API / no scraping

A static page can't fetch other sites' content into itself (browsers block cross-origin scraping, and reproducing another site's actual template content would raise copyright concerns anyway). Instead of faking that, FieldDraft gives you **real, live search links** for your occupation and a tailored blank-canvas builder next to them — you look at real examples, then draft your own version informed by them.

## Running it

No installation, no build step, no server required.

- **Locally:** just open `index.html` in any browser.
- **Hosted for free:** drop it into a GitHub Pages repo (same pattern as this project's other portfolio pieces) and it's live.

## Tech

- Vanilla HTML/CSS/JS — one file, zero dependencies
- Google Fonts (Fraunces, IBM Plex Mono, IBM Plex Sans) loaded via CDN link
- No frameworks, no build tools, no package.json

## Adding more occupations

Open `index.html` and find the `CATEGORIES` array in the `<script>` section. Each entry looks like:

```js
{
  id: "tech", code: "TC-01", name: "Technology & Software",
  keywords: ["developer", "engineer", "software", ...],
  labels: {
    summary: "Technical Summary",
    summaryHint: "...",
    exp: "Experience",
    skills: "Technical Skills",
    skillsHint: "...",
    extra: "Projects & Certifications",
    extraHint: "..."
  }
}
```

Add a new object to the array (or extend an existing `keywords` list) to cover more fields.

## License

MIT — do whatever you like with it, including using it commercially.
