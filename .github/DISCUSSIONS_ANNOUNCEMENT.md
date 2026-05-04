# How to use NetBird Discussions

Welcome to NetBird Discussions. This is the best place for community questions, reproducible bug triage, and product ideas.

This space is community-oriented and does not provide an SLA. For NetBird Cloud support, use the official support channel linked from the issue creation page. Security vulnerabilities must be reported through the repository security policy instead of public discussions.

## Before you post

- Search existing discussions and issues, including closed items.
- Check the relevant NetBird documentation or troubleshooting guide.
- Add your use case, logs, or reproduction details to an existing discussion when one already exists.
- Remove or anonymize secrets, tokens, private keys, internal hostnames, public IPs, and customer/user data from logs, screenshots, and configuration.

## Choose the right category

### Q&A / Support

Use **Q&A / Support** for configuration help, setup questions, self-hosting questions, troubleshooting, and general NetBird usage.

Use this category when:

- You are asking "how do I configure this?"
- You are not sure whether the behavior is a bug.
- The problem is not reproducible yet.
- You need help understanding expected behavior.
- You are troubleshooting a self-hosted, IdP, DNS, routing, firewall, or client setup.

Helpful details to include:

- What you are trying to accomplish
- Deployment type: NetBird Cloud, self-hosted, local development, or unknown
- NetBird versions, if available
- Operating systems and environments involved
- What you already tried
- Relevant anonymized logs, command output, screenshots, or topology details

### Issue Triage

Use **Issue Triage** only for reproducible bugs and regressions.

Post here when:

- You can provide the smallest set of steps that reproduces the bug.
- You can describe the current behavior and expected behavior.
- You reproduced the issue on a current/supported NetBird version, or can explain why you cannot upgrade.
- You can provide relevant environment/topology details.
- You can include logs, status output, debug evidence, or explain why they are not relevant.

Intermittent issues are welcome only when you can include:

- Trigger or suspected trigger
- Frequency
- Timing or timestamps
- Relevant logs/debug evidence

Do **not** use Issue Triage for configuration questions, how-to questions, feature requests, private support, or security vulnerabilities.

DevRel or maintainers may redirect, merge, or close Issue Triage discussions that are duplicates, support/configuration questions, not reproducible, or missing required reproduction details. Validated reports may be promoted to GitHub issues.

Useful commands for client-related reports:

```shell
netbird version
netbird status -dA
netbird debug for 1m -AS -U
```

Uploaded debug bundles are automatically deleted after 30 days.

### Ideas & Feature Requests

Use **Ideas & Feature Requests** for product ideas, enhancements, integrations, and workflow improvements.

A strong request explains:

- The problem or use case
- Who is affected
- Why current behavior or workarounds are not enough
- The proposed workflow, API, UI, or integration
- Any security, privacy, compatibility, or operational considerations

If a similar idea already exists, upvote it and add your use case there instead of opening a duplicate discussion.

## What happens after you post

- Community members, DevRel, or maintainers may ask follow-up questions.
- Duplicate reports may be merged or redirected to an existing discussion/issue.
- Support or configuration questions posted in Issue Triage may be redirected to Q&A / Support.
- Reproducible, actionable bug reports may be promoted to GitHub issues.
- Ideas with strong community traction and clear use cases may influence roadmap or maintainer-curated issues.

Thanks for helping keep NetBird Discussions searchable, useful, and actionable.
