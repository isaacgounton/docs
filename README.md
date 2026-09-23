# docs

A personal knowledge wiki maintained by LLM agents. Source material (X threads, articles, docs, notes) is ingested and synthesised into linked Markdown pages, organised by domain. It opens as an Obsidian vault; wikilinks (`[[Page]]`) resolve there, not on GitHub.

## Start here

- [Home](Home.md) - navigation hub and skill workflow
- [Overview](Overview.md) - current synthesis across all domains, with open questions
- [index](index.md) - catalogue of every page
- [log](log.md) - audit trail of every ingest, lint and edit

## Domains

| Domain | Home page |
|---|---|
| SEO & AI search | [SEO - Home](Knowledge/SEO/SEO%20-%20Home.md) |
| Growth & Sales | [Growth & Sales - Home](Knowledge/Growth%20%26%20Sales/Growth%20%26%20Sales%20-%20Home.md) |
| AI & Agents | [AI & Agents - Home](Knowledge/AI%20%26%20Agents/AI%20%26%20Agents%20-%20Home.md) |
| Personal Effectiveness | [Personal Effectiveness - Home](Knowledge/Personal%20Effectiveness/Personal%20Effectiveness%20-%20Home.md) |

Most sources are practitioner threads or vendor posts, so each page carries a `reliability:` rating. Treat numbers as leads to verify.

## Layout

| Path | Contents |
|---|---|
| `Knowledge/` | Wiki pages, one folder per domain |
| `raw/` | Inbox: drop new sources here |
| `ingested/` | Processed originals, referenced from each page's `## Sources` |
| `archive/` | Lint reports and retired pages |
| `templates/` | Page templates, one per `page_type` |
| `wiki-config.md`, `wiki-schema.md` | Wiki settings and frontmatter schema |
| `wiki-help.md` | Field conventions and page types |

## Workflow

Drop files into `raw/`, then run the wiki skills from Claude Code:

1. `/wiki-ingest` - turn sources into pages and move originals to `ingested/`
2. `/wiki-query` - answer questions from the wiki with citations
3. `/wiki-integrate` - link a hand-written page into the graph
4. `/wiki-crystallize` - distil a working session into a page
5. `/wiki-lint` - health check; report goes to `archive/`
