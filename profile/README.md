# Open Science Pillars

Governed, portable scientific capabilities for AI agents, organized by
the five Earth science spheres. Each capability is skills an agent can
run, knowledge signed by the people who steward the data, and
deterministic verification, authored once and delivered to the runtime
you use. A personal open-source project; not a NASA, JPL, or PO.DAAC
product.

## Start here

```bash
claude plugin marketplace add open-science-pillars/marketplace
claude plugin install ocean-science@open-science-pillars
```

One install brings the capability's dependencies (the foundation and the
provider knowledge) with it. Claude Code is the supported runtime today;
Claude Cowork installs from the same marketplace and is tested; the
portable Agent Plugins projection for OpenAI Codex and other clients is
being built. The status per runtime is in the
[runtime distribution note](https://github.com/open-science-pillars/marketplace/blob/main/docs/runtime-distribution.md).
New to a term? The
[glossary](https://github.com/open-science-pillars/marketplace/blob/main/GLOSSARY.md)
defines sphere, capability, skill, knowledge bundle, golden notebook and
runtime in plain language.

## By sphere

A Pillar is a sphere. A domain capability is a discipline inside one;
provider knowledge is signed by its stewards and serves every sphere;
`planned` means visible and not installable.

<!-- osp-sphere-view:start -->
Rendered by build-kit's `osp.py sphere-view --into` from every repository's
`.osp/repository.yaml`; edit the files, not this block.

**Atmosphere**

- no domain capability yet

**Biosphere**

- no domain capability yet

**Cryosphere**

- no domain capability yet

**Geosphere**

- no domain capability yet

**Hydrosphere**

- [hydrology](https://github.com/open-science-pillars/hydrology) *(developing)*: Terrestrial Hydrology; also Cryosphere
- [ocean-science](https://github.com/open-science-pillars/ocean-science) *(available)*: Ocean Physics

**Provider knowledge** (signed by its stewards; cuts across spheres)

- [nasa-daac-knowledge](https://github.com/open-science-pillars/nasa-daac-knowledge) *(available)*: Provider knowledge bundles (PO.DAAC, ESDIS), signed by their stewards; installed as a dependency of the domain capabilities

**Composites** (cross-sphere)

- none yet

**Foundation and tooling** (serve every sphere)

- [.github](https://github.com/open-science-pillars/.github) *(available)*: Organization profile, issue and pull request templates, governance
- [agent-evals](https://github.com/open-science-pillars/agent-evals) *(available)*: The organization's one benchmark repository; each product's cases, fixtures and results under its own directory (ecco/ first), governed by one charter
- [archive-observatory](https://github.com/open-science-pillars/archive-observatory) *(available)*: Data engineers and archive operators: metadata compliance instruments, classified on their own terms rather than by sphere
- [build-kit](https://github.com/open-science-pillars/build-kit) *(available)*: Maintainers: the development harness, the roadmap and the metadata tooling
- [core](https://github.com/open-science-pillars/core) *(available)*: The foundation capability every domain capability depends on
- [evals](https://github.com/open-science-pillars/evals) *(available)*: Eval runner, graders, suite manifests and the scoreboard
- [knowledge-template](https://github.com/open-science-pillars/knowledge-template) *(available)*: Template: a copy renames repository.name before it validates
- [marketplace](https://github.com/open-science-pillars/marketplace) *(available)*: The plugin catalog and the canonical documentation
- [plugin-template](https://github.com/open-science-pillars/plugin-template) *(available)*: Template: a copy renames repository.name (and package.yaml) before it validates
- [tutorials](https://github.com/open-science-pillars/tutorials) *(available)*: Timed walkthroughs and the browser demo
<!-- osp-sphere-view:end -->

## How it fits together

- **KNOW**: concepts, claims about data with evidence, a steward's
  signature and a staleness date, in the provider and domain bundles.
- **ACT**: skills, portable procedures an agent runs; one canonical
  `SKILL.md` per workflow.
- **PROVE**: golden notebooks and attesters, deterministic checks that
  emit receipts, with no language model in the path.
- **REACH**: connectors, the controlled execution surfaces.

The decisions behind the shape are in the marketplace repository's
[decision records](https://github.com/open-science-pillars/marketplace/tree/main/docs/decisions).

New here? The [tutorials](https://github.com/open-science-pillars/tutorials)
are timed and fresh-install-tested (10, 20, and 30 minute tracks), and
the demo folder has a browser-runnable companion.

Questions: GitHub Discussions on the marketplace repo. Governance: lazy
consensus with owning teams, DCO (a one-line commit sign-off) on PRs;
see GOVERNANCE.md.
