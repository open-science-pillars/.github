# Open Science Pillars

AI-assisted open science for earth, planetary, and applied science: skills,
knowledge bundles, verification notebooks, and connectors for Claude Code,
Claude Cowork, and Claude Science. One markdown source, three surfaces.

## The three pillars

1. **Skills** encode workflows and domain expertise (data formats, statistics,
   cartography, quality control, ECCO, SWOT, transport, budgets).
2. **Knowledge bundles** capture what practitioners know about real datasets:
   the traps, the uncertainty structure, the validated recipes, every claim
   carrying evidence and a review status.
3. **Verification** keeps it honest: marimo golden notebooks regression-test
   every computational workflow, and eval cases test scientific judgment.

## Start here

```bash
claude plugin marketplace add open-science-pillars/marketplace
claude plugin install core@open-science-pillars
claude plugin install ocean-science@open-science-pillars
```

Cowork and Claude Science: add the marketplace and install from it, or see
[marketplace/docs/surface-testing-guide.md](https://github.com/open-science-pillars/marketplace/blob/main/docs/surface-testing-guide.md).

## Repositories

- [marketplace](https://github.com/open-science-pillars/marketplace): catalog, governance, canonical docs
- [core](https://github.com/open-science-pillars/core): foundation plugin
- [ocean-science](https://github.com/open-science-pillars/ocean-science): ECCO, SWOT, the PO.DAAC arc
- [tutorials](https://github.com/open-science-pillars/tutorials): Quarto tutorials and demos
- [plugin-template](https://github.com/open-science-pillars/plugin-template) and [knowledge-template](https://github.com/open-science-pillars/knowledge-template): scaffolds for contributors

Questions: GitHub Discussions on the marketplace repo. Governance: lazy
consensus with domain maintainers, DCO sign-off on PRs; see GOVERNANCE.md.
