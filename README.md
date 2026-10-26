# SEO Research & Content Creation System

A research-first Claude skill that turns a keyword or topic into a **publish-ready service page or blog article**, backed by SERP research, top-3 competitor analysis, content-gap analysis, on-page SEO deliverables, schema, AEO/GEO recommendations and a scored quality audit.

It works three ways:

1. **You give the inputs** → it uses them as the source of truth.
2. **You give almost nothing** → it pulls project details from your Claude Project (knowledge files, instructions, memory, past chats), attached files and the live website, and labels where every value came from.
3. **Something critical is still missing** → it asks you once, in one short question, then carries on.

> Research first. Analyse second. Plan third. Write fourth. Audit fifth. No fabricated metrics, testimonials, prices or rankings — ever.

---

## What you get

| # | Section |
|---|---|
| 0 | Resolved Inputs table (value + source for every field) |
| 1 | Executive Summary |
| 2 | Research Methodology & limitations |
| 3 | Keyword & Query Research — autocomplete, PAA, PASF, related, AI-style queries (Observed vs Inferred) |
| 4 | Top-3 Competitor Analysis |
| 5 | Competitor Comparison Table |
| 6 | Content Gap Analysis |
| 7 | Recommended Content Outline |
| 8 | **Final Publish-Ready Content** |
| 9 | SEO Metadata (title, alt title, meta description, slug, H1, OG) |
| 10 | Internal Linking Plan (real URLs only) |
| 11 | Schema Recommendations + JSON-LD |
| 12 | AEO / GEO Recommendations |
| 13 | Quality Audit (10 scores, auto-revise below 8/10) |
| 14 | Implementation Checklist |
| 15 | Missing Proof / Inputs to Add |

Plus a separate copy-paste file containing only the content.

---

## How inputs are resolved

The skill checks these sources in order and stops asking as soon as it has what it needs:

```
Your message  →  Attached files  →  Claude Project (instructions, knowledge, memory, past chats)
      →  Your general memory  →  Live website  →  SERP research  →  Ask you (critical fields only)
```

**Critical fields** (asked only if they can't be found anywhere): website URL or brand, topic / primary keyword, content type (inferred from intent when obvious), target country (inferred from the domain when obvious).

**Derivable fields** (filled automatically and labelled): industry, audience, services, tone, location, CTA, intent, secondary keywords, word count, internal URLs, competitors, existing page.

**Never invented** (used only if you supply them or they're on the site): USPs, credentials, licences, awards, years in business, testimonials, ratings, case-study results, prices, guarantees, schema addresses/authors.

If sources disagree, the conflict is shown in the Resolved Inputs table instead of being silently resolved.

---

## Installation

### Claude (web / desktop / mobile)
1. Download [`seo-research-content-system.skill`](seo-research-content-system.skill) from this repo (it's a zip of the skill folder), or zip the `seo-research-content-system/` folder yourself (the zip must contain the folder with `SKILL.md` inside it).
2. Upload it in Claude's skills settings and switch it on.
3. Optional but recommended: add a filled copy of [`templates/project-brief.md`](templates/project-brief.md) to each client's **Claude Project knowledge**. The skill will pick it up automatically, so you only ever need to type the keyword.

### Claude Code
```bash
# personal (all projects)
git clone https://github.com/akifseospecialist-digitalmarketer/seo-research-content-system.git
cp -r seo-research-content-system/seo-research-content-system ~/.claude/skills/

# or per project
cp -r seo-research-content-system/seo-research-content-system .claude/skills/
```

### Any other LLM / no skills support
Paste [`prompt/universal-seo-content-prompt.md`](prompt/universal-seo-content-prompt.md) into the chat and fill the bracketed fields (or leave them blank — it will ask).

---

## Usage

**Minimal (inside a client's Claude Project):**
```
Write a service page for "epoxy garage flooring Brisbane"
```

**With a URL:**
```
Blog article for example.com.au on "how long does epoxy flooring last"
```

**Rewrite an existing page:**
```
Rewrite https://example.com/services/roof-repairs/ — primary keyword "roof repairs Melbourne"
```

**Full control:** fill [`templates/content-task.md`](templates/content-task.md) and paste it.

**Batch:**
```
Service pages for: "commercial epoxy flooring", "garage floor coating", "polished concrete" — example.com.au
```
The skill resolves the brand once, writes each page, and flags keyword overlap between them.

More in [`examples/usage-examples.md`](examples/usage-examples.md).

---

## Works better with (optional)

- **Web search + web fetch** — required for real SERP and competitor research.
- **A browser tool** — for SERP features or pages that don't render via fetch.
- **SEO data connectors** (SE Ranking, Ubersuggest, DataForSEO, Semrush, Ahrefs, Google Search Console) — for verified volume, difficulty and current rankings. Without one, metrics are marked *Not verified* instead of guessed.

---

## Repo structure

```
seo-research-content-system/
├── README.md
├── LICENSE
├── seo-research-content-system.skill   ← ready-to-upload skill package
├── seo-research-content-system/      ← the skill (upload / copy this folder)
│   └── SKILL.md
├── templates/
│   ├── project-brief.md              ← save once per client in Claude Project knowledge
│   └── content-task.md               ← per-page task brief
├── prompt/
│   └── universal-seo-content-prompt.md   ← standalone prompt version
└── examples/
    └── usage-examples.md
```

---

## Principles

- Never guarantees rankings, traffic or indexing.
- Separates **observed** data from **inferred** opportunities.
- Learns from competitors' structure without copying their wording.
- Picks word count by intent, not by the longest competitor.
- No doorway pages or near-duplicate location pages.
- Every claim about the business must come from you, your Project data or the live site.

## License

MIT — see [LICENSE](LICENSE).

## 👋 About

Created by **Akif Qureshi | SEO Specialist & Digital Marketer**
🌐 [algoblueprints.com](https://algoblueprints.com)

More skills: [AI Queries Finder](https://github.com/akifseospecialist-digitalmarketer/ai-queries-finder) · [Website Clicks Improver](https://github.com/akifseospecialist-digitalmarketer/website-clicks-improver) · [SEO · AEO · GEO Audit & Working Sheet](https://github.com/akifseospecialist-digitalmarketer/seo-aeo-geo-audit-and-working-sheet) · [GSC Opportunity Finder](https://github.com/akifseospecialist-digitalmarketer/claude-ai-gsc-opportunity-finder) · [AI Prompt Research](https://github.com/akifseospecialist-digitalmarketer/claude-ai-prompt-research-skill) · [SEO Master](https://github.com/akifseospecialist-digitalmarketer/seo-master-skill)
