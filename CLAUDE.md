# Better Body Reviews — working rules

Static site for betterbodyreviews.com, hosted on Netlify from this repo. Owner: Jordan (ClickTitans LLC). Every agent working here follows these rules.

## What the site is
An independent health and wellness publisher about looking and feeling great through science. Two content types:
- **Article**: a guide or explainer (e.g. what causes ED, how online treatment works).
- **Listicle**: a ranked brand roundup (e.g. best online ED treatments).

## Voice (non-negotiable)
- Plain English at about a 5th grade reading level. Short sentences. One idea per sentence.
- Down to earth, like a smart friend. No fluff, no hype, no filler intros.
- No big scientific words. If a medical term is unavoidable, explain it in the same sentence.
- Big focus on optimization and life satisfaction: looking and feeling great through science.
- Positive and confident, never fear-based or shaming. Treat stigmatized topics as normal.

## Accuracy and compliance (non-negotiable)
- Every factual or medical claim must trace to a source listed at the bottom of the page. Prefer NIH/NIDDK, MedlinePlus, Mayo Clinic, Cleveland Clinic, FDA drug labels (DailyMed), CDC, and peer-reviewed studies.
- Always include real risks and side effects when discussing a treatment. Simplify the wording, never the facts.
- No dosing instructions. No promises of results. No "cure" language.
- Never invent star ratings, scores, customer reviews, testimonials, quotes, experts, or statistics.
- Brand facts (price, products, process, doctor visit, delivery) come only from the brand's own website, with the date checked.
- Rankings follow the criteria on /how-we-review/: price and value, clinician care, options, convenience, transparency.
- **No links to brands for now.** Brand names appear as plain text. Never add affiliate or tracking links.
- Every page keeps the "Talk to a doctor first" callout and the Sources list. Listicles keep the disclosure note.

## Using Health Geek (healthgeekreviews.com) for inspiration
- Topics and titles only, plus a short format note: article type, who it's for, rough length, and which brands/products it features (market intel only).
- Never copy, summarize, or mirror its text, headings, section order, or rankings. The writer never sees Health Geek content.
- Research every topic independently from primary sources.

## Pipeline
1. **Researcher** → research brief (sources, facts, brand facts with dates).
2. **Writer** → draft in our voice using a template in `_templates/`.
3. **Checker** → verifies every claim against sources, safety info, compliance rules above.
4. **Jordan approves.** Nothing goes live without his approval.
5. **Publisher** → adds the page, updates home "Latest guides", the category page, and `sitemap.xml`, then commits and pushes.

## File layout
- Pages live at `/<category-slug>/<article-slug>/index.html`. Category slugs: sexual-health, weight-loss, hair, testosterone, skin, energy-sleep.
- Build new pages from `_templates/article.html` or `_templates/listicle.html`; replace every `{{PLACEHOLDER}}` and remove template comments.
- Home page cards go between `<!-- LATEST:START -->` and `<!-- LATEST:END -->` (newest first, max 6). Category cards go between `<!-- LIST:START -->` and `<!-- LIST:END -->`. Use the `.cards` / `.card` markup; remove the `.empty` placeholder once a real card exists.
- All styling lives in `assets/style.css`. Don't add inline styles or new fonts.
- Don't edit the trust pages (about, how-we-review, disclosures, privacy, terms) without Jordan's request.
