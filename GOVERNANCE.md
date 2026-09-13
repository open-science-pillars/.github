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
- Knowledge-concept PRs follow the specification's stewardship and
  review rules: one human review of any role for any concept, and a
  concept becomes `stable` on that one review; two human reviews of any
  role for high-severity gotchas and for any edit that changes severity,
  status, or an Uncertainty section. A provider review is preferred and
  invited for the second, never required: a second maintainer or a
  community reviewer satisfies the rule. The merge-then-sign rule and
  the signature debt are unchanged; they are about edits after a
  signature, not about who signed.
- **Provider confirmation is additive.** The maintainer who holds a
  bundle is its steward. A data provider's confirmation raises a
  concept's trust tier (provider-confirmed, voiced by skills when they
  cite) and is never a precondition for a concept to be stable, a
  capability to be released or promoted, or a composite to exist.

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
  provenance, staleness and high-severity review. The steward teams
  stay in CODEOWNERS: provider bundle stewards are child teams of
  `provider-stewards` (`podaac-stewards`, `esdis-stewards`; a partner's
  team is added when its bundle exists) and own their bundle's paths,
  held by the maintainer who holds the bundle and by anyone who takes
  the top rung of the ladder below. Methods stewards
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

### The ladder of involvement

Provenance is a ladder, and a person at a data center may stand on any
rung of it; nothing above the first is required of anyone.

- **Consulted:** they answer a "confirm this concept" issue (the
  organization's confirm-a-concept template) with confirmed, a
  correction, or not my product. No git or tooling is asked of them:
  the maintainer records the `verified` event on their behalf with
  `role: provider` and the reply's URL as `source`.
- **Reviewer:** they review knowledge pull requests for their products
  on GitHub; their approval is a human review of any role under the
  review rules.
- **Steward:** they join the bundle's steward team in CODEOWNERS (a
  membership change, no file edit) and sign with `tools/sign.py`;
  review authority over the bundle's concepts and authorship credit on
  its releases follow from membership.

The knowledge digest (`tools/digest.py` in nasa-daac-knowledge renders
`knowledge/<bundle>/DIGEST.md`: what the bundle claims about each
product, with status, tier, evidence and a confirm link per claim) is
what a person reads to decide what they could take on.

### Composite review rule

A composite needs a maintainer plus a reviewer from each sphere it
touches, not a steward of its own. A composite change that touches
several spheres needs review representation from each sphere it
touches, in addition to repository merge authority, knowledge steward
review where knowledge changes and runtime review where packaging
changes. While a repository has one active maintainer the solo period
rules above apply.

### Team membership

One person occupies every team today, and each `governance.yaml`
records that as `status: interim` (the maintainer-count word build-kit
validates; it says nothing about stewardship, and the person who holds
a bundle is its steward). Review-enforcing rulesets stay off until a
repository has two maintainers, as the solo period section says; the
team structure exists now so that accepting a maintainer or a steward
is a membership change, never a rearrangement.

### Planned repositories

Creating a planned repository (the honest placeholder for a capability
the organization intends, holding nothing installable) is
administrative. Promoting one out of planned is governed, cross-cutting
work under its own dated entry in the pre-registration
(docs/phase2-preregistration.md in the marketplace repository). It
needs a maintainer, sources on every claim, evals for high-severity
gotchas and a named provider contact who has been invited; it does not
need a signature from anyone at the provider.

## Contribution mechanics

- Contribution policy requires DCO sign-off (`git commit -s`).
  Protected-branch rules remain unverified; do not describe them as enabled
  without live evidence.
- GitHub Discussions on the marketplace repo is the user Q&A channel.
- Security reports follow SECURITY.md, never public issues.
- The Contributor Covenant v2.1 (CODE_OF_CONDUCT.md) applies org-wide.
- Roadmap proposal decisions use `roadmap:accepted`, `roadmap:deferred`, or
  `roadmap:rejected`; only repository maintainers apply the decision.
