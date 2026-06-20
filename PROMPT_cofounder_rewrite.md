# Prompt — reposition site for co-founder / venture-creation roles

Paste everything below into Claude (run from the repo root).

---

You are an expert technical-founder positioning editor and Jekyll developer. This is my personal site (Jekyll). Content lives in `_config.yml` (author bio/role/tagline/skills) and `_data/*.yml` (experience, education, awards, patents, publications, projects); `index.html` renders it. **Read the repo first** before editing.

## Goal
Reposition the copy so I read as a **technical co-founder / Founder-in-Residence candidate** for deep-tech, climate, industrial-decarbonisation, aerospace/space, defence/dual-use, and scientific-ML venture studios and VCs (e.g. Deep Science Ventures, Marble, Entrepreneur First, Creator Fund, Seraphim, Oxford Science Enterprises). Keep my technical credibility fully intact, but make the framing **outcome- and ownership-oriented** — someone who takes first-of-a-kind technology from physics → product → pilot → commercial readiness, not just an engineer "open to collaborations."

## Audience
Studio partners, VCs, and potential co-founders skim for 20 seconds. They want to see: deep, rare technical edge; evidence of taking things to the real world (pilot/plant/patents); product and commercial judgement; and that I could lead the technical side of a venture.

## Tone rules (this is the important part)
- Confident and direct, founder-minded, plain English. Lead with the problem and the result.
- **No bullshit:** no "passionate", "visionary", "synergy", "thought leader", "ninja", "10x", buzzword stacking, or vague superlatives. If a sentence would survive on a serious deep-tech founder's page, keep it; if it sounds like LinkedIn filler, cut it.
- **Truth only.** Do not invent metrics, titles, revenue, team sizes, or outcomes. Only reframe facts already in the repo/CV. Where a number isn't verifiable, describe the capability qualitatively rather than fabricating a figure.
- Active voice, short sentences, concrete nouns. Show judgement, not adjectives.
- Don't imply I've already founded a company, and don't imply I'm leaving or competing with my current employer. Respect that my employer's confidential info, designs, and IP stay private — describe my *transferable* skills and my *own* independent work (e.g. HydrAI), not proprietary specifics.

## What to change (be surgical; preserve all facts and structure)

1. **`_config.yml`**
   - `author.role`: keep my real current title, but add a positioning line that signals founder-track (e.g. a `tagline`/`role` that reads as "builds first-of-a-kind industrial/energy technology from physics to product"). Don't fabricate a co-founder title.
   - `author.tagline`: sharpen into a crisp value line a studio would remember.
   - `author.bio`: rewrite (~3–5 sentences) to lead with the rare combination — deep turbomachinery/thermofluids + scientific ML + taking FOAK tech through pilot validation and patents — and end with what I want next: **co-founding / technical-founder roles in hard industrial, climate, deep-tech, and dual-use ventures.** Keep the ASME award and Oxford PhD.
   - `skills`: keep the technical list; optionally add 2–4 builder-relevant items only if truthful (e.g. "Scale-up & pilot validation", "Technical product definition", "Patents / IP", "FOAK de-risking"). No marketing fluff.

2. **`_data/experience.yml`**
   - Rewrite each `summary` and `highlights` to **lead with the outcome and the decision it enabled**, then the method — without changing any underlying facts. Frame Coolbrook work around: translating PhD research into product architecture, technical product definition, taking hardware to live pilot, reconciling model-vs-plant reality, drafting patents, and producing evidence that supported go/no-go and investment decisions. Frame HydrAI as **my own independently-built scientific-ML IP** (a venture-grade asset), not a hobby.
   - Keep it honest and specific; trim any line that's pure task description with no result.

3. **`index.html` (copy only, not design)**
   - Hero: make the role/tagline render the new positioning.
   - Add **one short new section or sub-block** near the top — e.g. "Founder profile" or "What I build" — 2–3 sentences (driven from a new `_config.yml` field or inline) stating the kind of company I'm positioned to help start and the problems I'm unusually equipped to solve (industrial heat, turbomachinery, separations, scientific-ML for physical systems). Keep it factual.
   - Rewrite the **Contact** section CTA from "open to collaborations" to an invitation to **co-founder / Founder-in-Residence / venture conversations** (still warm, not salesy).
   - Do **not** restyle, change the CSS/layout, or alter `_data` for publications/awards/patents content (only their framing if a summary line exists).

## What NOT to do
- Don't break Liquid/Jekyll (test that `bundle exec jekyll build` still succeeds).
- Don't touch design, colours, fonts, or layout unless I ask.
- Don't remove technical depth, publications, awards, or patents — they're the proof.
- Don't add anything you can't trace to my real record.

## Output
1. Make the edits.
2. Show me a concise **diff/summary of every copy change** (old → new) so I can sanity-check tone and truth.
3. Give me **2 alternative versions of the hero tagline and the bio** to choose from (one more technical, one more founder-forward).
4. Confirm the site still builds.
