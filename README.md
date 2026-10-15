<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/readme/01_hero_dark.svg">
  <img src="docs/readme/01_hero_light.svg" width="100%" alt="Study Hub: a single file study dashboard for researchers and students, built for cognitive science. Stuck on a topic? Type it once and get a plain language explanation and the top papers on one page, then keep a focus timer, tasks, a reading list and notes next to them. A search box shows the example query predictive coding. Facts: 1 HTML file, no install and no account, 8 top papers per search drawn from 250M+ scholarly works on OpenAlex. Animated focus timer card: a ring counts down a 25 minute focus session, with 25, 50, 5 and 15 minute modes.">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/readme/02_search_dark.svg">
  <img src="docs/readme/02_search_light.svg" width="100%" alt="How a search works. One query fans out to two answers on one page. A quick explanation from Wikipedia. Eight top papers from OpenAlex, with authors, year, journal, a short abstract, citation count and free PDF links when available; example results from the screenshot for predictive coding include The Predictive Coding Account of Psychosis (Sterzer, Adams, Fletcher and others, 2018, Biological Psychiatry, 854 citations, free PDF). Sort by most relevant, most cited, newest, or reviews only. One click buttons: Explain with Claude, Stanford Encyclopedia of Philosophy, lectures, and focus on this. Optional extra tabs: Google Scholar, PubMed, PsyArXiv, Semantic Scholar, OpenNeuro, SEP and YouTube. Press slash anywhere to jump to the search box.">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/readme/03_desk_dark.svg">
  <img src="docs/readme/03_desk_light.svg" width="100%" alt="The study desk around the search. Focus timer: 25 or 50 minute focus and 5 or 15 minute break modes, labelled with your topic; it keeps a 7 day chart, a daily streak and a session log, and shows a notification when time is up. Reading list: save papers from search results, or paste a DOI to see the paper's details and copy an APA 7 citation. Study tasks you can tick off. My shelf: links and files you open often. Scratchpad: notes that save as you type and export to Markdown.">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/readme/04_reference_dark.svg">
  <img src="docs/readme/04_reference_light.svg" width="100%" alt="Quick reference tabs for cognitive science. Choosing a stats test: 2 groups, independent t test or Mann Whitney if non normal; same people in 2 conditions, paired t test or Wilcoxon signed rank; 3 or more groups, one way ANOVA or Kruskal Wallis; trials nested in participants, linear mixed model (lmer) with random effects; binary outcome, logistic mixed model (glmer, binomial); many channels by time points, cluster based permutation tests. EEG frequency bands: delta 0.5 to 4 Hz deep sleep; theta 4 to 8 Hz memory encoding and cognitive control; alpha 8 to 13 Hz relaxed wakefulness and inhibition; beta 13 to 30 Hz active thinking and motor control; gamma 30 to 100 Hz feature binding and perception. ERP components by latency: ERN about 50 to 100 ms after an error, P1 about 100 ms, N1 100 to 200 ms, N170 about 170 ms for faces, MMN 150 to 250 ms auditory deviance, P300 300 to 600 ms context updating, N400 about 400 ms semantic violations, LPP 400 to 1000+ ms emotional salience. lme4 mixed model syntax: random intercept (1 | g), intercept and slope (1 + x | g), crossed effects (1 | a) + (1 | b). Three pass reading: pass 1, 5 minutes, title, abstract, figures, conclusion; pass 2, 30 minutes, intro and methods; pass 3, deep, results in detail and limitations. Also a brain regions tab.">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/readme/05_use_dark.svg">
  <img src="docs/readme/05_use_light.svg" width="100%" alt="Use it in three steps: download index.html or clone the repo; open it in Chrome, Safari, Firefox, Edge or Brave; click the pencil next to the greeting to set your name. Nothing to install and no account; search and DOI lookup need an internet connection. Privacy: there is no server and no tracking. Tasks, notes, reading list and focus history live only in your browser's localStorage. When you search, the query goes straight from your browser to the public Wikipedia and OpenAlex APIs. MIT license.">
</picture>

# Study Hub

A single file study dashboard for researchers and students, built for cognitive science. When you're stuck on a topic, type it once and get a plain language explanation and the top papers on one page, then keep a focus timer, tasks, a reading list and notes next to them.

![Study Hub showing a search for "predictive coding"](docs/screenshot.jpg)

## Features

* **"Stuck on something?" search**
  * A quick explanation from Wikipedia
  * Eight top papers from [OpenAlex](https://openalex.org) (250M+ scholarly works), with authors, year, journal, a short abstract, citation count and free PDF links when available
  * Sort by most relevant, most cited, newest, or reviews only
  * One click "Explain with Claude", Stanford Encyclopedia of Philosophy and lecture searches
  * Optional extra tabs for Google Scholar, PubMed, PsyArXiv, Semantic Scholar, OpenNeuro, SEP and YouTube
* **Focus timer:** 25 or 50 minute focus and 5 or 15 minute break modes, labelled with your topic. It keeps a 7 day chart, a daily streak and a session log, and shows a notification when time is up.
* **Reading list:** save papers from search results, or paste a DOI to see the paper's details and copy an APA 7 citation.
* **Study tasks, a "My shelf" of links and files you open often, and a scratchpad** that saves as you type and exports to Markdown.
* **Quick reference tabs:** choosing a stats test, brain regions, EEG frequency bands, ERP components, `lme4` mixed model syntax and a three pass method for reading a paper.

## Use it

1. Download `index.html`, or clone the repo.
2. Open it in your browser (Chrome, Safari, Firefox, Edge or Brave).
3. Click ✎ next to the greeting to set your name.

There's nothing to install and no account. Search and DOI lookup need an internet connection.

**Tip:** press `/` anywhere on the page to jump to the search box.

## Privacy

There is no server and no tracking. Your tasks, notes, reading list and focus history are stored only in your browser's `localStorage`. When you search, the query goes straight from your browser to the public Wikipedia and OpenAlex APIs.

## Files

* `index.html`: the whole app
* `docs/screenshot.jpg`: the screenshot above
* `docs/readme/`: the panels at the top of this page, their source page and build script
* `LICENSE`: MIT

## Rebuilding the panels

The panels at the top are SVG images generated from one HTML page. Edit `docs/readme/one_sheet.html`, then run:

```bash
node docs/readme/build_readme_svgs.js docs/readme/one_sheet.html docs/readme 960
```

This needs Node with Playwright and curl (fonts are fetched from Google Fonts and embedded). It writes a light and a dark SVG for every panel.

## License

MIT
