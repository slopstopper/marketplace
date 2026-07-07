# slopstopper marketplace

One add, three instruments:

```
/plugin marketplace add slopstopper/marketplace
/plugin install plumb-line@slopstopper
/plugin install tokenomics@slopstopper
/plugin install recursive-spine@slopstopper
```

Each plugin also works alone and hosts its own single-plugin marketplace
in its repo; this one aggregates so you don't have to remember three add
commands. What the org is against, and why, lives on the
[org profile](https://github.com/slopstopper).

| plugin | owns | status |
|---|---|---|
| [plumb-line](https://github.com/slopstopper/plumb-line) | whether claims are honest | public, v0.6.x |
| [tokenomics](https://github.com/slopstopper/tokenomics) | which model does the work | public, v0.3.x |
| [recursive-spine](https://github.com/slopstopper/recursive-spine) | where tracked state lives | **private for now** — installs will 404 for non-members until its public flip ([recursive-spine#10](https://github.com/slopstopper/recursive-spine/issues/10)). Listed anyway; hiding it would overstate the other two. |

Shared vocabulary across the seams: [docs/shared-vocabulary.md](docs/shared-vocabulary.md).

Versions in the table are honest approximations; the repos are
authoritative. If the table drifts, that's a bug — file it.
