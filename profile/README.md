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
3. **Verification** keeps it honest: automated notebooks regression-test
   every computational workflow, and eval cases test scientific judgment.

New to these terms? The [glossary](https://github.com/open-science-pillars/marketplace/blob/main/GLOSSARY.md)
defines skill, knowledge bundle, golden notebook, surface, and connector in
plain language.

## Start here

```bash
claude plugin marketplace add open-science-pillars/marketplace
claude plugin install core@open-science-pillars
claude plugin install ocean-science@open-science-pillars
```

Cowork and Claude Science: add the marketplace and install from it, or see
[marketplace/docs/surface-testing-guide.md](https://github.com/open-science-pillars/marketplace/blob/main/docs/surface-testing-guide.md).

## Repositories

- [marketplace](https://github.com/open-science-pillars/marketplace) *(start here)*: catalog, glossary, governance, canonical docs
- [core](https://github.com/open-science-pillars/core) *(installable)*: foundation plugin
- [ocean-science](https://github.com/open-science-pillars/ocean-science) *(installable)*: ECCO, SWOT, the PO.DAAC arc
- [hydrology](https://github.com/open-science-pillars/hydrology) *(in development)*: SWOT rivers/lakes, GRACE-FO, streamflow, soil moisture
- [tutorials](https://github.com/open-science-pillars/tutorials) *(start here)*: timed walkthroughs and a browser demo
- [plugin-template](https://github.com/open-science-pillars/plugin-template) and [knowledge-template](https://github.com/open-science-pillars/knowledge-template) *(scaffolds)*: for contributors building new plugins or bundles
- [nasa-daac-knowledge](https://github.com/open-science-pillars/nasa-daac-knowledge) *(knowledge)*: canonical per-DAAC dataset knowledge bundles
- [build-kit](https://github.com/open-science-pillars/build-kit) *(for maintainers)*: how to continue developing the project

New here? The [tutorials](https://github.com/open-science-pillars/tutorials)
are timed and fresh-install-tested (10, 20, and 30 minute tracks), and
the demo folder has a browser-runnable companion.

Questions: GitHub Discussions on the marketplace repo. Governance: lazy
consensus with domain maintainers, DCO (a one-line commit sign-off) on PRs;
see GOVERNANCE.md.
