# marketplace

Claude Code marketplace for the mods and plugins hosted at [github.com/isabel-nh](https://github.com/isabel-nh).

## Install

```
/plugin marketplace add isabel-nh/marketplace
/plugin install sentinel@isabel-nh
/plugin install env-rejector@isabel-nh
```

## Plugins

| Plugin | Repository | Purpose |
|---|---|---|
| `sentinel` | [claude-sentinel](https://github.com/isabel-nh/claude-sentinel) | Inserts a manual-review sentinel line into every file Claude writes, guards it from removal, and gates commits until a person deletes it. |
| `env-rejector` | [claude-env-rejector](https://github.com/isabel-nh/claude-env-rejector) | Denies Read, Bash and Grep access to `.env` files and strips `.env` hits from Grep results. |

## Adding a plugin

Append an entry to `.claude-plugin/marketplace.json` with a `url` source pointing at the plugin repository's HTTPS clone URL (`https://github.com/isabel-nh/<repo>.git`), then run `claude plugin validate .`. Do not use a `github` source: plugin installs clone it over SSH, which fails on machines without a GitHub SSH key.
