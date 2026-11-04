# Contributing

Outside contributions are welcome. This is the default for every repository under
[its-janghoon](https://github.com/its-janghoon); a repository with its own `CONTRIBUTING.md`
uses that one instead.

## What gets merged quickly

- A bug fix with a reproduction.
- Accessibility fixes: focus order, contrast, labels, reduced-motion paths.
- A crash, a data-loss path, or anything that breaks on one platform only.
- Copy that reads wrong, in English or Korean.
- Dead code and dependencies you can show are unused.

## What needs a discussion first

Open an issue before writing the code.

- A new dependency.
- A change to a file format, a config schema, or anything existing users rely on.
- A rewrite of a subsystem.

## Branches

Base your work on the default branch. Working branches are `<type>/<short-slug>`, with `type`
one of:

```
feat fix chore docs test refactor perf ci build sync hotfix release
```

The list lives in [`.github/workflows/gitflow.yml`](.github/workflows/gitflow.yml), and a pull
request from any other prefix fails the branch-name check. A branch name says what the change is,
not who or what made it.

## Commits

Conventional prefix or a component prefix, imperative mood, lower-case subject:

```
fix: keep the composer focused after a drop
site: publish to GitHub Pages
```

## Pull requests

- Fill in all four sections of the template: What's done, What's not done, What to review,
  Intentions. "nothing" is a fine answer.
- Before asking for a review, review your own pull request: one comment of 100 characters or
  more on what you checked and what you are unsure about.
- At most three open pull requests per author per repository. A fourth is closed automatically.

Both rules are enforced by [`.github/workflows/pr-policy.yml`](.github/workflows/pr-policy.yml).

## Secrets

Never commit a credential, token or `.env` file. If you did, say so in the pull request; it has
to be rotated, not just deleted.
