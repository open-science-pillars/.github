# Pull request

## What and why

<!-- One paragraph. Cite the spec section this implements where applicable. -->

## Checklist

- [ ] DCO sign-off on every commit (`git commit -s`)
- [ ] No `commands/` directories anywhere (everything is a skill)
- [ ] Touched SKILL.md files have valid frontmatter; descriptions 200 characters or fewer, keyword-first
- [ ] Workflow skills touched: matching golden notebook in `verification/` runs green headless
- [ ] Knowledge concepts touched: OKF v0.2 frontmatter (`type`; `status` draft/stable/deprecated; `generated`; `sources` with `[^id]` footnote joins), resources resolve, gotchas link their dataset, bundle `log.md` updated
- [ ] Layer check: I ran the five-question decision aid in marketplace docs/knowledge-vs-skills.md; facts live in concepts, behavior lives in skills, and nothing is mirrored between them
- [ ] High-severity gotcha added or edited: matching eval case exists; second reviewer requested
- [ ] No credentials, tokens, or `~/.netrc` contents anywhere in the diff
- [ ] Prose uses no em dashes (commas, colons, parentheses, semicolons instead)

## Reviews

Ordinary PRs need one domain-maintainer review; cross-cutting changes and
high-severity knowledge edits need two (GOVERNANCE.md).
