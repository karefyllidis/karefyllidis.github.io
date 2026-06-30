# CLAUDE.md — karefyllidis.github.io

Jekyll GitHub Pages personal site. Live at https://karefyllidis.github.io.

---

## Stack

- Jekyll + `github-pages` gem (no custom theme gem — layout is fully hand-rolled)
- Content in `_config.yml` (author/bio/skills) and `_data/*.yml` (experience, education, projects, publications, awards, patents, further_education)
- Templates: `_layouts/default.html`, `_includes/` (head, header, footer, project-card, publication)
- Styles: `assets/css/main.scss` (single file — no preprocessor partials)
- Fonts: Inter + Source Serif 4 (Google Fonts)
- No JavaScript framework, no Node tooling

## Build & serve

```bash
bundle exec jekyll build      # build to _site/
bundle exec jekyll serve      # local dev at http://localhost:4000
```

Do not edit files in `_site/` — it is generated. Do not touch `vendor/` or `Gemfile.lock` unless resolving a dependency issue explicitly requested.

---

## File map

| What you want to change | File |
|---|---|
| Name, role, bio, tagline, skills, social links | `_config.yml` → `author:` and `skills:` |
| Work experience | `_data/experience.yml` |
| Education | `_data/education.yml` |
| Courses / professional development | `_data/further_education.yml` |
| Awards | `_data/awards.yml` |
| Patents | `_data/patents.yml` |
| Publications | `_data/publications.yml` |
| Projects | `_data/projects.yml` |
| Nav links | `_includes/header.html` |
| Page sections & layout | `index.html` |
| Visual design | `assets/css/main.scss` |

**Rule:** content belongs in `_config.yml` / `_data/*.yml`. Do not hardcode copy into templates.

---

## Data schemas

### `_data/projects.yml` entry

```yaml
- category: phd | oxford | open_source | independent
  title: "..."
  period: "..."
  description: "..."        # 1–3 sentences, outcome-first
  tags:
    - "..."
  github: "https://..."    # omit if proprietary
  link_url: "https://..."  # optional external link
  link_label: "..."        # label for link_url
  proprietary: true        # omit if not applicable
```

If neither `github` nor `link_url` is present, the card renders "Proprietary — details on reasonable request".

### `_data/experience.yml` entry

```yaml
- role: "..."
  org: "..."
  period: "..."
  url: "https://..."        # omit if none
  summary: "..."            # 2–3 sentences, outcome-first
  highlights:
    - "..."                 # lead with result, then method
```

### `_data/publications.yml` entry

```yaml
- journal_short: "..."
  title: "..."
  award: "..."              # omit if none
  award_url: "https://..."  # omit if none
  authors:
    - name: "..."
      self: true            # marks Nikolas in bold
    - name: "..."
  venue: "..."
  date: "YYYY"
  doi: "..."
  url: "https://..."
  abstract: "..."
  bibtex: |
    @article{...}
```

---

## Ground truth — who Nikolas is

**Do not invent beyond this. Do not fabricate metrics, titles, team sizes, or revenue.**

- **Nikolas Karefyllidis, Ph.D.** — Oxford Engineering Science, DPhil 2019–2023
- **Current role:** Senior Aerodynamics Engineer, Coolbrook Technologies (Aug 2023–present)
- **Visiting Researcher:** University of Oxford, Dept. of Engineering Science (Sep 2024–Sep 2025)
- **Location:** Oxford, UK
- **Email:** karefyllidis@gmail.com | **GitHub:** karefyllidis | **LinkedIn:** karefyllidis
- **Top award:** ASME IGTI John P. Davis Award 2025 (lead author); also ASME Turbomachinery Best Paper 2024 (lead); GPPS Best Paper 2024 (second author)
- **Three-world intersection:** deep turbomachinery / thermofluids physics + scientific ML (PINNs, surrogates, symbolic regression, Bayesian optimisation, Monte Carlo UQ) + FOAK industrial deployment (rig → pilot → plant, live petrochemical pilot, patents)
- **Prior:** Ansys CFX QA (2018–19); AAReST spacecraft propulsion, Surrey Space Centre / Caltech / NASA JPL (2016–17)

## IP and privacy boundaries

| Item | Status | How to handle |
|---|---|---|
| **Coolbrook Technologies work** | Employer — proprietary | Describe transferable capability and public outcomes only. Never expose designs, data, customer names, non-public specifics, or pilot details beyond what is already in `_data/experience.yml`. |
| **hydrAI / NESP** | Nikolas's own independent IP — **not open source** | Describe as proprietary scientific-ML IP. Do not add a GitHub link. Render as "Proprietary — details on reasonable request". |
| **Multi-stage meanline code** | In-house Oxford code | Frame as extended/contributed-to, not sole-authored. Do not publish code. |
| **black-box-optimization** | Superseded by SEBO — already public and linked under `open_source` in `_data/projects.yml` | No action needed; do not re-add as a separate project entry |
| **super-rotor-designer** | Nikolas's own tool | Add if requested; treat as independent/proprietary unless a repo link is explicitly provided. |
| **turbulence-deep-forecasting** | Personal project | Can be shown; confirm GitHub visibility before linking. |

---

## Strategic positioning (read before editing copy)

The site targets two overlapping audiences who skim for ~20 seconds:
1. **Venture studio partners, FiR programme leads, potential co-founders** (DSV, Marble, EF, Antler, Creator Fund, Seraphim, OSE)
2. **Technical hiring teams at deep-tech / scientific-ML companies** (e.g. PhysicsX)

**The narrative to reinforce:** Nikolas sits at the intersection of three worlds that rarely share a person — rigorous physics (turbomachinery, reacting flows, high-temperature thermofluids), modern scientific ML (PINNs, neural operators, symbolic regression, UQ), and FOAK industrial deployment (validating models against live plant data, closing the offline-to-online gap, producing investment-grade evidence packages, filing patents). Most engineers own one of these. A few own two. He demonstrably owns all three.

**The ask to surface:** co-founding / Founder-in-Residence / technical co-founder roles in hard industrial, climate, deep-tech, aerospace, and dual-use ventures. Also open to senior scientific-ML and physical-systems research roles.

---

## Tone rules

- **Outcome first, method second.** Lead every bullet with what was achieved or enabled, then how.
- **Plain English.** No "passionate", "visionary", "synergy", "thought leader", "10x", buzzword stacking.
- **Active voice, short sentences, concrete nouns.**
- **No fabrication.** If a number isn't in the existing record, describe the capability qualitatively.
- **Do not imply Nikolas has already co-founded a company**, or that he is leaving / competing with Coolbrook.
- **Confident, not salesy.** A sentence that would survive on a serious deep-tech founder's page: keep it. LinkedIn filler: cut it.

---

## What NOT to change without explicit instruction

- CSS / layout / typography — the design is intentional; do not restyle
- Publications, awards, patents content — these are the proof, not the pitch
- `Gemfile`, `Gemfile.lock`, `vendor/`
- `_site/` (generated)
- Liquid template logic unless fixing a rendering bug

---

## Adding a new project section

If adding a new `category` value (e.g. `independent`):
1. Add entries in `_data/projects.yml` with the new category value
2. Add a new `{% assign … = site.data.projects | where: "category", "independent" %}` block in `index.html` with a matching `<h3>` title
3. No other files need changing

## Adding a nav item

Edit `_includes/header.html` — add an `<a href="#section-id">Label</a>` matching the section `id` in `index.html`.

---

## Verification

After any change:
```bash
bundle exec jekyll build
```
No errors = good. Then check `_site/index.html` to confirm rendered output is correct before committing.

Suggested commit message format: `content: <what changed>` (e.g. `content: reposition bio and experience for founder-track`)
