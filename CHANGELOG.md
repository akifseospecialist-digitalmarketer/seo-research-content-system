# Changelog

## 1.0.0 - 2026-10-26

First release.

- `SKILL.md`: Step 0 input engine with three modes: use supplied inputs, pull from the Claude Project (instructions, knowledge, memory, past chats), attached files and the live website, or ask once for critical fields. Every field is labelled with its source and conflicts are surfaced.
- Field classes: critical (asked if missing), derived (filled and labelled), never invented (USPs, credentials, reviews, prices, guarantees).
- Research phase: autocomplete, PAA, PASF, related searches, AI-style queries, SERP features, and a keyword/query map split into observed and inferred.
- Top-3 competitor analysis: page-level, tone and structure, comparison table and gap list.
- Separate service-page and blog-article playbooks.
- On-page deliverables: metadata, heading hierarchy, internal linking plan with real URLs, schema with verified JSON-LD, AEO/GEO recommendations.
- Quality audit: 10 scored categories with auto-revision below 8/10.
- 16-part report plus a separate content-only file.
- Templates: `project-brief.md` (per client, for Claude Project knowledge) and `content-task.md` (per page).
- Standalone prompt version for any LLM.
