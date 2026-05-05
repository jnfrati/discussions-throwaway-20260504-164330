# How to use Discussions, Issues, and Pull Requests

This repository uses a discussion-first workflow for community bug reports and feature requests.

The short version:

```text
Discussion → validation → Issue → Pull Request → release
```

Discussions are where we collect context, reproduce problems, understand impact, and avoid duplicates. Issues are for validated work that is ready for a maintainer or contributor to pick up. Pull requests are where the fix or implementation happens.

## When to open a discussion

Open a discussion when you want to report a problem, request a feature, ask for help, or confirm whether something is expected behavior.

Choose the category that fits best:

- **Issue Triage** — reproducible bugs, regressions, and unexpected behavior.
- **Ideas & Feature Requests** — feature requests, enhancements, integrations, and workflow improvements.
- **Q&A / Support** — setup, configuration, troubleshooting, self-hosted deployments, and general usage questions.

If you are not sure whether something is a bug, start with **Q&A / Support**. We can move it into triage if it turns out to be a product issue.

Do not use public discussions for security vulnerabilities, secrets, private keys, internal hostnames, or sensitive logs. Use the repository security policy for vulnerability reports.

## Before opening a new discussion

Please do three things first:

1. Search existing discussions and issues, including closed ones.
2. Check the relevant NetBird documentation or troubleshooting guide.
3. Remove or anonymize sensitive information from logs, screenshots, and configuration.

If a similar discussion already exists, upvote it and add your use case there instead of opening a duplicate. Extra reproduction details, affected versions, and deployment notes are useful even when the discussion already exists.

## What makes a useful bug report

For **Issue Triage**, the most useful reports include:

- NetBird version and component versions, where applicable.
- Operating system or environment.
- Deployment type: NetBird Cloud, self-hosted, Kubernetes, Docker, or local development.
- Current behavior and expected behavior.
- The smallest set of steps that reproduces the problem.
- Logs, status output, screenshots, or a debug bundle when relevant.
- Whether this worked before, and the last known working version if known.

For client-related reports, these commands are often helpful:

```shell
netbird version
netbird status -dA
netbird debug for 1m -AS -U
```

Uploaded debug bundles are automatically deleted after 30 days.

Intermittent issues are still useful, but they need enough detail to investigate: trigger, frequency, timing, timestamps, and any related logs.

## What makes a useful feature request

For **Ideas & Feature Requests**, try to describe the problem before the solution.

A strong request explains:

- What you are trying to accomplish.
- Who is affected and how often.
- Why the current behavior or workaround is not enough.
- What workflow, API, UI, integration, or behavior you would like to see.
- Any security, privacy, compatibility, or operational concerns.

Community signal matters. Upvotes, comments, real deployment details, and examples from other tools help us understand priority.

## What happens during triage

After a discussion is opened, DevRel, maintainers, or community members may:

- ask for missing details
- link related discussions or issues
- merge or redirect duplicates
- move the discussion to a better category
- try to reproduce the issue
- clarify the expected behavior
- narrow the scope of a feature request
- decide the report isn't actionable yet

Not every discussion becomes an issue. Some are answered in Q&A, some turn out to be configuration problems, some are duplicates, and some need more information before engineering can act on them. That's fine — a well-answered discussion is still a useful outcome.

## When a discussion becomes an issue

A discussion gets promoted to an issue once it's clear enough for someone to pick up and act on.

For a bug, that usually means:

- the behavior is reproducible, or there is enough evidence to investigate confidently;
- the affected component, version, and environment are understood;
- expected and actual behavior are clear;
- logs or debug evidence are available when needed.

For a feature request, that usually means:

- the use case is clear;
- the expected outcome is understood;
- there is enough product or community signal to justify tracking it as work;
- the initial scope is narrow enough to review and implement.

When that happens, a maintainer or DevRel team member opens a validated issue linked back to the source discussion. It should include the summary, evidence, proposed scope, and acceptance criteria so whoever picks it up has everything they need.

The current issue label taxonomy is tracked separately in [Issue label taxonomy](./ISSUE_LABELS.md).

## From issue to pull request

Once an issue exists, it is the work item.

A maintainer or contributor can pick it up, discuss implementation details on the issue, and open a pull request in the repository where the fix belongs. The pull request should link the issue with a closing keyword when appropriate, for example:

```text
Fixes #1234
```

The issue's acceptance criteria should guide review. When the PR is merged, the issue is closed. If the original discussion contains useful community context, maintainers may also post a short update there so people following the discussion know what changed.

## Multi-repo flow

Community discussions live in `netbirdio/netbird`, even when the affected component is maintained in another repository.

During validation, maintainers decide where the implementation belongs. The resulting issue or pull request may be created in `netbirdio/netbird`, `netbirdio/dashboard`, `netbirdio/kubernetes-operator`, `netbirdio/docs`, or another NetBird repository.

You do not need to know the right repository before opening a discussion. Start with the discussion; routing is part of triage.

## Maintainer-created issues

Maintainers can still open issues directly when the work is already validated or discovered internally. Examples include regressions found during development, planned maintenance, release blockers, or follow-up work from an existing PR.

Those issues should still be clear enough for someone else to understand the scope and acceptance criteria.

## Lifecycle examples

### Bug report

```text
Issue Triage discussion
→ maintainer reproduces the bug
→ validated issue is opened
→ contributor opens a PR with a fix
→ PR is merged
→ issue is closed
```

### Feature request

```text
Ideas & Feature Requests discussion
→ community adds use cases and upvotes
→ maintainers narrow the scope
→ validated issue or roadmap item is created
→ implementation happens through one or more PRs
```

### Support question

```text
Q&A / Support discussion
→ community or DevRel helps troubleshoot
→ question is answered, or
→ if it reveals a reproducible product bug, it moves into Issue Triage
```

## The goal

The goal is a cleaner, more useful workflow for everyone:

- community members have a place to ask, confirm, and add context;
- DevRel can validate reports before they become engineering work;
- maintainers get a focused issue queue;
- contributors can find issues that are ready to work on.

Thanks for helping keep NetBird's issue tracker useful and actionable.
