# Ogilvy Writer Project

An **experimental** workflow for drafting advertising copy in the style of David Ogilvy, built to run inside [Claude Code](https://claude.com/claude-code).

It is a set of markdown instructions — one agent, three skills, and some reference context. No code, no build step, nothing to install.

Results vary with the product details you supply and the sample ads you load into `context/`.

## The flow

| # | Stage | Type | Produces |
|---|-------|------|----------|
| 1 | `customer-research` | agent | `<product-slug>-research.md` |
| 2 | `create-brief` | skill | `brief.md` |
| 3 | `write-copy` | skill | `copy-vN.md` |
| 4 | `critique-copy` | skill | `copy-vN(finished).md` |

Research scrapes the subreddits where buyers gather for verbatims, objections and vocabulary. Brief turns that into eight questions on audience, promise and objections. Copy writes twenty headlines, picks one, drafts the body. Critique checks the draft against the rules and the brief, then strips the usual AI tells. Each stage reads the one before it; output lands in `temporary-files/outputs/`. Stages can also be called alone — the critique is useful against copy the flow didn't write.

## Getting started

1. Put what you know about the product into `temporary-files/product-context/`.
2. Fill `context/sample-ads.md` with ads matching the style you want. It ships empty and the copy is noticeably worse without it.
3. Open the project in Claude Code and ask for an ad.

Stage 1 needs the [Apify](https://apify.com) MCP connector for Reddit scraping. Without it the rest still runs on product context alone, minus the voice-of-customer material that makes it worthwhile.

## Layout

```
context/                     writing rules and sample ads (loaded for every draft)
.claude/agents/              customer-research
.claude/skills/              create-brief, write-copy, critique-copy
temporary-files/
  product-context/           what you know about the product — you fill this
  outputs/                   everything the flow produces
CLAUDE.md                    rules Claude reads at the start of a session
```

`temporary-files/` collects client details, scraped quotes and unpublished drafts. Keep it out of version control — git history is permanent, and a later deletion does not remove a file from the repository.

## Disclaimer

Not affiliated with or endorsed by Ogilvy, WPP, or the estate of David Ogilvy. "Ogilvy" is their trademark; the name here describes the style being imitated.

`context/writing-rules.md` quotes *Confessions of an Advertising Man*, *Ogilvy on Advertising* and *The Unpublished Ogilvy* for study and commentary; those quotes remain the property of their rights holders. `context/sample-ads.md` ships empty — what you put in it is your own call, and published advertising is generally still under copyright.
