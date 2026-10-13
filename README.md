# mkt-main

Throwaway marketplace fixture for testing marketplace browse, install and refresh. Manifest: `.claude-plugin/marketplace.json`.

| Entry | Purpose |
|---|---|
| `skills-only` | 2 skills, one with a very long description (truncation and expand) |
| `mcp-open` | DeepWiki MCP, no auth fields ("No connection needed") |
| `mcp-auth` | Stripe MCP with a `${STRIPE_SECRET_KEY}` header ("Requires a connection") |
| `mixed-unsupported` | skill + Context7 MCP + hooks, agents, rules, commands (banner, skipped parts) |
| `bare` | no description, author, license or README |
| `rich` | README, LICENSE, author, repository, homepage, version, keywords |
| `to-vanish` | removed from the source in a later commit |
| `evolving` | gets v2 and v3 in later commits |
| `not-installable` | npm source ("Not available") |
| `broken-structure` | folder with no `plugin.json` (install fails) |
| `too-big` | 522 files, over the 500-file limit (install fails) |
| `filler-01` … `filler-25` | padding for infinite scroll and search, one topic each |
| `same-name-twice` | two catalog entries with the same name (parser should drop one) |

Every skill body contains a unique `refId: MKT-…` value to confirm which version is loaded.
