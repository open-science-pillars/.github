# Governance

Open Science Pillars is governed by lazy consensus: proposals (issues, PRs,
Discussions) proceed unless a maintainer objects within a reasonable review
window. This is the governance the specification sets
(docs/SPECIFICATION.md in open-science-pillars/marketplace).

## Federated repository authority

The organization coordinates a portfolio, but each repository is governed by
the maintainers declared in that repository's `.osp/governance.yaml` and
CODEOWNERS. Organization roadmap work enters a repository as a proposal. The
repository maintainers accept, defer, reject, prioritize, implement, and close
that work. Organization stewards cannot mark repository work accepted or
complete for them.

Cross-repository initiatives complete only when every required repository has
accepted and completed its deliverables. A repository may disable organization
proposal seeding in its governance file; the organization then supplies a
review artifact instead of creating an issue.

### Interim solo period

While a repository has one active maintainer, repository-local work may merge
after its documented verification passes. Governance, roadmap schemas,
organization templates, and other cross-repository changes receive a 72-hour
public review window. Security fixes and urgent breakage may bypass the window
only when the exception and reason are recorded. Review-enforcing rulesets are
not enabled until a repository has at least two maintainers.

## Review rules

- One review from the owning team merges an ordinary PR (a domain maintainer for a capability, the foundation team for a foundation or tooling repository).
- Two reviews for cross-cutting changes (anything touching more than one
  plugin, the marketplace catalog, governance, or org-wide templates).
- Knowledge-concept PRs follow the specification's stewardship rules: one
  steward review for any concept; two reviews, including a provider steward
  on provider bundles, for high-severity gotchas and for any edit that
  changes severity, status, or an Uncertainty section.
- **Interim period:** while a bundle has no provider steward, the
  provider second review is deferred until handoff, and the interim steward's
  single review merges in the meantime. The high-severity gotchas verified
  during this period are re-reviewed by the incoming provider steward when
  they accept the bundle (see the steward playbook), so their review
  authority is real rather than a rubber stamp at handoff.

## Teams (2026-09-12)

Ownership is by team, never by individual: every CODEOWNERS owner and
every team a repository's `.osp/governance.yaml` names is one of the
teams declared in build-kit's `osp/teams.yaml`, written
`@open-science-pillars/<team>`, and build-kit's `osp.py validate`
refuses anything else. Four responsibilities, four kinds of team
(ADR A, docs/decisions in the marketplace repository):

- **Repository and sphere maintainers** own implementation, roadmap,
  repository changes and sphere coordination: `foundation-maintainers`
  for the foundation and tooling repositories, and one team per Earth
  science sphere (`hydrosphere-maintainers`, `cryosphere-maintainers`,
  `geosphere-maintainers`, `atmosphere-maintainers`,
  `biosphere-maintainers`) for the domain capabilities in it. A sphere
  team coordinates proposals across its capabilities; each repository's
  authority stays federated as above.
- **Knowledge stewards** own scientific correctness, evidence,
  provenance, staleness, high-severity review and provider approval.
  Provider stewards are child teams of `provider-stewards`
  (`podaac-stewards`, `esdis-stewards`; a partner's team is added when
  its bundle exists) and own their bundle's paths. Methods stewards
  (`hydrosphere-methods-stewards`) own the recipes and attested
  computations that combine several providers' products, the third
  steward type the model document records (docs/MODEL.md in the
  marketplace repository). Sphere teams do not
  override stewards, and a sphere tag on a concept moves no authority.
- **Runtime maintainers** own packaging, runtime compatibility,
  connector binding, permission mapping and qualification for one
  projection each: `runtime-cowork-maintainers` (the Claude package
  files, `.claude-plugin` and `.mcp.json`), `runtime-agent-plugins-maintainers`
  (the Agent Plugins `plugin.json` and `mcp.json`) and
  `runtime-codex-maintainers` (Codex qualification). A runtime
  maintainer may reject a package that does not resolve its required
  knowledge on their runtime; they may not approve a scientific claim
  as correct, and a runtime projection may not redefine scientific
  semantics. A packaging-only change needs no scientific re-approval
  unless semantics change.
- **Composites maintainers** (`composites-maintainers`) coordinate the
  cross-sphere composites.

Provider staff who accept a bundle join its steward team (the steward
playbook): CODEOWNERS entries on the bundle paths, review authority over
its concepts, and authorship credit on the bundle's releases follow
from membership, with no CODEOWNERS edit.

### Composite review rule

A composite change that touches several spheres needs review
representation from each sphere it touches, in addition to repository
merge authority, knowledge steward review where knowledge changes and
runtime review where packaging changes. During the interim solo period
the exception below applies.

### Interim membership

One person occupies every team until a handoff, and that is recorded in
each `governance.yaml` as `status: interim`. Review-enforcing rulesets
stay off until a repository has two maintainers, as the interim solo
period section says; the team structure exists now so that accepting a
maintainer or a steward is a membership change, never a rearrangement.

### Planned repositories

Creating a planned repository (the honest placeholder for a capability
the organization intends, holding nothing installable) is
administrative. Promoting one out of planned is governed, cross-cutting
work under its own dated entry in the pre-registration
(docs/phase2-preregistration.md in the marketplace repository).

## Contribution mechanics

- Contribution policy requires DCO sign-off (`git commit -s`).
  Protected-branch rules remain unverified; do not describe them as enabled
  without live evidence.
- GitHub Discussions on the marketplace repo is the user Q&A channel.
- Security reports follow SECURITY.md, never public issues.
- The Contributor Covenant v2.1 (CODE_OF_CONDUCT.md) applies org-wide.
- Roadmap proposal decisions use `roadmap:accepted`, `roadmap:deferred`, or
  `roadmap:rejected`; only repository maintainers apply the decision.
