# Governance

Open Science Pillars is governed by lazy consensus: proposals (issues, PRs,
Discussions) proceed unless a maintainer objects within a reasonable review
window. Per SPEC §1.2.

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

- One domain-maintainer review merges an ordinary PR.
- Two reviews for cross-cutting changes (anything touching more than one
  plugin, the marketplace catalog, governance, or org-wide templates).
- Knowledge-concept PRs follow the stewardship rules of SPEC §5.4: one
  steward review for any concept; two reviews, including a provider steward
  on provider bundles, for high-severity gotchas and for any edit that
  changes severity, status, or an Uncertainty section.
- **Interim (pro tem) period:** while a bundle has no provider steward, the
  provider second review is deferred until handoff, and the interim steward's
  single review merges in the meantime. The high-severity gotchas verified
  during this period are re-reviewed by the incoming provider steward when
  they accept the bundle (see the steward playbook), so their review
  authority is real rather than a rubber stamp at handoff.

## Provider maintainers

Knowledge bundles may be maintained by data-provider staff (for example,
PO.DAAC personnel for the podaac bundle) as domain maintainers for their
bundle: CODEOWNERS entries on the bundle paths, review authority over its
concepts, and authorship credit on the bundle's Zenodo releases.

## Contribution mechanics

- Contribution policy requires DCO sign-off (`git commit -s`). Automated DCO
  enforcement and protected-branch rules are not currently verified; do not
  describe either as enabled until a live audit records evidence.
- GitHub Discussions on the marketplace repo is the user Q&A channel.
- Security reports follow SECURITY.md, never public issues.
- The Contributor Covenant v2.1 (CODE_OF_CONDUCT.md) applies org-wide.
- Roadmap proposal decisions use `roadmap:accepted`, `roadmap:deferred`, or
  `roadmap:rejected`; only repository maintainers apply the decision.
