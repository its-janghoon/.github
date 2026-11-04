# Security policy

## Reporting a vulnerability

Use GitHub's private reporting: open the repository's **Security** tab and choose
**Report a vulnerability**. Do not open a public issue.

Include the repository, the version or commit, what you found, and the steps to reproduce it.
Please give a reasonable window for a fix before publishing details.

This is the default policy for every repository under
[its-janghoon](https://github.com/its-janghoon). A repository with its own `SECURITY.md` is
authoritative for itself.

## In scope

- Remote code execution or privilege escalation.
- Loss or theft of funds, keys or signed authority, including a signature accepted where it
  should be refused.
- A path that sends a user's files, credentials or prompts somewhere they did not choose.
- A secret exposed in a repository, a build log or a release asset.
- Dependency vulnerabilities reachable from a shipped artifact.

## Out of scope

- Findings that need an already-compromised machine.
- Missing hardening headers on a static GitHub Pages site.
