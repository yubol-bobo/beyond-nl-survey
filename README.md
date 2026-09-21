# Beyond Natural-Language Interfaces

**Decisions, Scores, and Predictive Distributions**

Yubo Li · Ramayya Krishnan · Rema Padman<br>
Carnegie Mellon University · 21 September 2026

[Project website](https://yubol-bobo.github.io/beyond-nl-survey/) · [Read the survey](pdf/beyond-natural-language-interfaces.pdf) · [BibTeX](citation.bib)

Language models increasingly supply the predictions on which other systems act. This survey connects decisions, scores, numerical estimates, and predictive distributions through the information a downstream decision actually requires.

The project page presents the taxonomy, two representative evidence figures, and a compact interface-selection guide. The full 59-page manuscript contains the detailed comparisons, statistical foundations, references, and appendices.

## Repository

- `index.html` — the English, single-page project website.
- `assets/styles.css` and `assets/site.js` — responsive styling and accessible evidence tabs/citation copying.
- `assets/figures/` — the original taxonomy and two selected analytical figures.
- `pdf/beyond-natural-language-interfaces.pdf` — complete survey, including all appendices. Appendices B and D use portrait tables.
- `citation.bib` and `CITATION.cff` — citation metadata for the survey manuscript.

This repository intentionally contains the public project page, selected figures, and manuscript PDF, rather than the local working archive or downloaded source papers.

## Local preview and publication

No build, package installation, or external service is required. Run a static server in this directory, for example `python -m http.server 8000`, and open `http://localhost:8000`.

GitHub Pages publishes the root of the `main` branch. The `.nojekyll` file preserves the static assets. To update the site, edit the HTML/CSS/JS or replace the PDF at its existing path, then push to `main`.

All site asset URLs are relative, so the same files work under the GitHub Pages project path and a local preview. Fonts use the system font stack. The website has no analytics, tracking, or third-party script dependencies.

## Figure provenance

- `taxonomy.svg`: survey Figure 2, report roles and production mechanisms.
- `report-adequacy.svg`: survey Figure 4, xVal/FP15 number look-up results (source Tables 12–13, survey reference [8]). The two pipelines change encoding, head, and training together.
- `computation-schedules.svg`: survey Figure 6, production schedules and one documented timing configuration (survey references [2, 12–15]). Timings exclude offline teacher sampling and fitting.

Figures are taken from the manuscript assets. The website computation diagram clarifies the repeated-generation lane: setup differs by method (GenRM-CoT fits a verifier), and repeated online sampling does not rule out encoding or cache reuse. Website summaries preserve the distinctions between report roles, uncertainty targets, matched comparisons, and computation schedules. See the PDF for complete captions and source attribution.

## Citation

```bibtex
@unpublished{li2026beyond,
  title = {Beyond Natural-Language Interfaces: Decisions, Scores, and Predictive Distributions},
  author = {Li, Yubo and Krishnan, Ramayya and Padman, Rema},
  year = {2026},
  note = {Survey manuscript},
  url = {https://yubol-bobo.github.io/beyond-nl-survey/}
}
```
