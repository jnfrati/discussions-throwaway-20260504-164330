# [Meta] Moving to a discussion-first approach for bug reports and feature requests

## TL;DR

Starting today, if you want to report a bug or request a feature, please open it as a **GitHub Discussion** rather than an Issue.

From now on, Issues are for validated, maintainer-curated work items: things the team or a contributor can pick up and act on. Maintainers can still open issues directly when they find something internally or while working on the codebase.

For the full workflow, see [How to use Discussions, Issues, and Pull Requests](https://github.com/netbirdio/netbird/blob/main/.github/DISCUSSIONS_GUIDE.md).

## Why we're doing this

We currently have more than 1,400 open issues. Some are confirmed bugs, some are feature requests, some are duplicates, and many are reports that went stale while waiting for reproduction steps or more context.

That makes the Issues tab hard to use. Real problems get buried, newcomers have trouble finding existing reports, and maintainers spend too much time sorting through unvalidated issues instead of fixing the ones we already know are actionable.

This is not about pushing community reports away. It's about creating a cleaner path from report → validation → fix.

We want the Issues tab to answer one question clearly:

> What is the team working on?

Discussions are a better place for reports that still need reproduction, environment details, community confirmation, or prioritization.

## What's changing

- **Bug reports and feature requests** should now start in [GitHub Discussions](https://github.com/netbirdio/netbird/discussions).
- The **DevRel team and maintainers will triage discussions**, ask follow-up questions, check for duplicates, and try to reproduce bugs.
- **Validated reports will be promoted to Issues** once they are confirmed and actionable.
- **Maintainers can still open issues directly** when the work is already understood or found internally.
- Issues opened without enough validation or maintainer context may be closed with a redirect to Discussions.

## Discussion categories

Please choose the category that best fits your post:

- **Issue Triage** — reproducible bugs, regressions, and unexpected behavior.
- **Ideas & Feature Requests** — feature requests, enhancements, integrations, and product ideas.
- **Q&A / Support** — setup, configuration, troubleshooting, self-hosting, and general usage questions.

If you're not sure whether something is a bug, start with **Q&A / Support**. We can always move it into triage if it turns out to be a reproducible product issue.

## What about the existing 1,400+ issues?

We're not doing a mass-close.

Now that new unvalidated reports have a better place to start, we can work through the existing backlog more carefully. Some issues will stay open, some may be moved back to discussions for re-validation, some will be merged into newer reports, and some will be closed if they are no longer actionable.

That cleanup will happen gradually — we'd rather do it carefully and keep useful context than rush through it.

## Multi-repo note

All community discussions should live in this repository (`netbirdio/netbird`), even if the affected component is somewhere else.

When a discussion is validated and promoted to an issue, the issue will be created in the repository where the fix belongs: core, operator, dashboard, or another NetBird repo. You don't need to know which repo owns the fix before reporting something. Sorting that out is part of triage.

## We're not the first to do this

Other projects have moved to a similar model, including [Ghostty](https://github.com/ghostty-org/ghostty/issues/3558) and [Renovate](https://github.com/renovatebot/renovate/discussions/40306). We're following a pattern that has worked for large, active open source projects with busy issue trackers.

## What we're asking from the community

- **Open new bug reports and feature requests as discussions.** Issues opened directly may be closed and redirected.
- **Include enough detail to reproduce the problem.** For bugs, please include your OS, NetBird version, deployment type, reproduction steps, expected behavior, actual behavior, and relevant logs.
- **Search before posting.** If a similar discussion already exists, upvote it and add your use case there.
- **Use reactions and comments to show impact.** Community traction helps us understand which reports affect the most users.
- **Be patient while we transition.** This process is meant to reduce noise, not add bureaucracy.

If you have questions or feedback about the change, drop a comment below — we're listening.
