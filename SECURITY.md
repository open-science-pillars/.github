# Security Policy

Skills and knowledge bundles are an instruction supply chain into every
user's agent (SPECIFICATION.md v0.5.1 §5.8). Treat prompt-injection
content in a skill, agent, or knowledge concept as a security issue, not
a content quality issue.

## Reporting

Report vulnerabilities privately via GitHub security advisories on the
affected repository (Security tab, "Report a vulnerability"). Do not open
public issues for security reports. Expect an acknowledgment within one
week.

## Scope

- Instruction-like or imperative content smuggled into knowledge concepts
  (concepts state facts about data; they never instruct the agent).
- Credentials or tokens appearing anywhere in any repo (they never should;
  Earthdata Login lives in ~/.netrc or connector configuration only).
- Malicious code in verification notebooks, fixtures scripts, or CI.

## Controls

Steward review of knowledge and skill PRs is a security control. The
knowledge-linter's imperative-phrasing scan flags instruction-like concept
content for human review. Golden-notebook CI runs on pull_request with no
repository secrets exposed, with action versions pinned by SHA before launch.
