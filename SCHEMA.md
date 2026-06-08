# Wiki Schema

## Domain
Personal project memory and knowledge base — infrastructure, tools, projects, and decisions for the user's self-hosted environment (Odoo, n8n, Hermes, Paperclip, and related systems).

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `odoo-19-docker.md`)
- Every wiki page starts with YAML frontmatter (see below)
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- **Provenance markers:** On pages that synthesize 3+ sources, append `^[raw/articles/source-file.md]` at the end of paragraphs whose claims come from a specific source.

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
# Optional quality signals:
confidence: high | medium | low
contested: true
contradictions: [other-page-slug]
---
```

### raw/ Frontmatter
```yaml
---
source_url: https://example.com/article
ingested: YYYY-MM-DD
sha256: <hex digest>
---
```

## Tag Taxonomy
- Infrastructure: server, docker, network, domain, cloudflare, reverse-proxy
- Tools: n8n, odoo, hermes, vault, postgres, redis
- Projects: paperclip, wiki-llm, automation
- Concepts: orchestration, agent, heartbeat, ticket, org-chart
- Meta: decision, lesson, config, troubleshooting

Rule: every tag on a page must appear in this taxonomy. Add new tags here BEFORE using them.

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions, minor details, or things outside the domain
- **Split a page** when it exceeds ~200 lines
- **Archive a page** when fully superseded — move to `_archive/`, remove from index

## Entity Pages
One page per notable entity. Include: overview, key facts, relationships ([[wikilinks]]), source references.

## Concept Pages
One page per concept. Include: definition, current state, open questions, related concepts ([[wikilinks]]).

## Comparison Pages
Side-by-side analyses with table format, verdict/synthesis, and sources.

## Update Policy
When new information conflicts with existing content:
1. Check dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in lint report
