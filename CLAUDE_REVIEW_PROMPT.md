# Claude review prompt — paste everything below into Claude

Review my Jekyll GitHub Pages portfolio, then **generate a second prompt** I can paste into Cursor to implement the changes.

---

## Part 1 — Your review task

Review my personal academic/engineering portfolio site. Be direct and specific. Flag anything inaccurate, weak, redundant, or visually off.

**Live site:** https://karefyllidis.github.io  
**Repo:** https://github.com/karefyllidis/karefyllidis.github.io  
**Local path:** `/Users/nikolaskarefyllidis/Desktop/15_GitPage`

### About me (ground truth — do not invent beyond this)

- **Nikolas Karefyllidis, PhD** — Oxford Engineering Science (2019–2024)
- **Current role:** Senior Aerodynamics Engineer, Coolbrook Technologies
- **Location:** Oxford, UK | **Email:** karefyllidis@gmail.com
- **GitHub:** karefyllidis | **LinkedIn:** karefyllidis
- **Key award:** [ASME IGTI John P. Davis Award, 2025](https://www.asme.org/about-asme/honors-awards/unit-awards/john-p-davis-gas-turbine-applications-paper-award) (lead author)
- **Also:** ASME Turbomachinery Best Paper 2024 (lead author); GPPS Best Paper 2024 (second author)
- **Research:** turbomachinery aerodynamics, high-enthalpy gas heating, CFD, scientific ML/surrogates, HPC, turbo-reactors / industrial decarbonisation
- **HydrAI:** proprietary scientific ML — must NOT be presented as open source; separate from Oxford meanline work
- **Public code:** [black-box-optimization](https://github.com/karefyllidis/black-box-optimization) only

### Tech stack

Jekyll + GitHub Pages, custom layout (no theme gem), YAML data in `_data/`, styles in `assets/css/main.scss`, fonts Inter + Source Serif 4.

### Files to review

```
_config.yml
index.html
_data/awards.yml
_data/education.yml
_data/experience.yml
_data/projects.yml
_data/publications.yml
_includes/head.html, header.html, footer.html, publication.html, project-card.html
_layouts/default.html
assets/css/main.scss
Gemfile, .gitignore, README.md
```

### Review dimensions (score 1–5 each)

1. Content accuracy & credibility  
2. Career positioning (turbomachinery / scientific ML / multiphysics audiences)  
3. Information architecture (section order, redundancy, gaps)  
4. Visual design & UX (typography, spacing, mobile, nav)  
5. Jekyll / GitHub Pages correctness  
6. Accessibility & SEO  
7. Privacy & professionalism (employer mentions, proprietary framing)

### Specific questions

- Should Coolbrook stay in the hero role or be softened?  
- Is Experience too long for a portfolio?  
- Are Projects groupings (PhD / Industry / Open Source) right?  
- Top 3 highest-impact changes?  
- What to remove or shorten?

---

## Part 2 — Required output format

Produce **two deliverables** in one response:

### Deliverable A — Review report

```markdown
## Executive summary
(3–5 sentences)

## Scores
| Dimension | Score | One-line note |
|-----------|-------|---------------|

## Critical issues (must fix)
- Issue → file(s) → suggested fix

## Improvements (nice to have)
- Issue → file(s) → suggested fix

## Content edits
- Current: "..." → Proposed: "..."

## Aesthetic notes
(specific CSS/layout suggestions)
```

### Deliverable B — Cursor implementation prompt

After the review, write a **complete, copy-paste-ready prompt** for Cursor (or another coding agent) titled:

**`# Cursor: implement portfolio fixes`**

That prompt must:

1. **Stand alone** — assume the agent has repo access but NOT this review chat; restate the repo path and live URL.
2. **List every change as an ordered task** — numbered, with exact file paths.
3. **Include exact copy** for any `_config.yml`, `_data/*.yml`, or HTML text replacements (before → after).
4. **Include CSS guidance** where visual fixes are needed (selectors + intent, not vague "make it prettier").
5. **State what NOT to change** — e.g. do not add NN-SVG, do not open-source HydrAI, do not edit `vendor/` or `Gemfile.lock`.
6. **End with verification steps:**
   - `bundle exec jekyll build`
   - git commit message suggestion
   - what to check on https://karefyllidis.github.io after push
7. **Prioritise** — label each task `P0` (must), `P1` (should), `P2` (optional).
8. **Keep scope realistic** — one session of work; split into "Phase 1 (ship now)" and "Phase 2 (later)" if needed.

Format Deliverable B as a single fenced code block I can copy in one click.

---

## Part 3 — Constraints for both deliverables

- Do not rewrite the entire site from scratch.
- Do not fabricate publications, employers, or projects.
- Prefer minimal diffs over rewrites.
- Match tone: professional academic/engineering portfolio, not generic "AI portfolio template."
- Reference live site and repo structure by path, not line numbers (lines may drift).

---

Attach or read the repo files, then produce Deliverable A and Deliverable B.
