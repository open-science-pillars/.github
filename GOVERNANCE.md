# Governance

Open Science Pillars is governed by lazy consensus: proposals (issues, PRs,
Discussions) proceed unless a maintainer objects within a reasonable review
window. Authored in Session 1 per SPECIFICATION.md v0.5.1 §1.2.

## Review rules

- One domain-maintainer review merges an ordinary PR.
- Two reviews for cross-cutting changes (anything touching more than one
  plugin, the marketplace catalog, governance, or org-wide templates).
- Knowledge-concept PRs follow the stewardship rules of SPEC §5.4: one
  steward review for any concept; two reviews, including a provider steward
  on provider bundles, for high-severity gotchas and for any edit that
  changes severity, status, or an Uncertainty section.

## Provider maintainers

Knowledge bundles may be maintained by data-provider staff (for example,
PO.DAAC personnel for the podaac bundle) as domain maintainers for their
bundle: CODEOWNERS entries on the bundle paths, review authority over its
concepts, and authorship credit on the bundle's Zenodo releases.

## Contribution mechanics

- PRs require DCO sign-off (`git commit -s`).
- GitHub Discussions on the marketplace repo is the user Q&A channel.
- Security reports follow SECURITY.md, never public issues.
- The Contributor Covenant v2.1 (CODE_OF_CONDUCT.md) applies org-wide.
