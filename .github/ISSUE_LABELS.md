# Issue label taxonomy

This document describes the proposed issue labels for the discussion-first workflow.

The goal is to keep labels useful for engineering without turning them into a database. Labels should answer three questions:

1. What kind of work is this?
2. Which product area owns the investigation or implementation?
3. What state is the issue in?

Details such as platform, deployment type, IdP provider, affected version, and logs should stay in the discussion or issue form unless we decide they need dedicated tracking.

## General rules

- Use labels for validated issues, not every discussion.
- Prefer one `type:*` label, one primary `area:*` label, and one `status:*` label.
- Label by the most likely root cause or owning area, not only by the visible symptom.
- Avoid adding new labels for one-off cases. If a pattern becomes common, revisit the taxonomy.

## Type labels

- `type: bug` — a reproducible defect or regression.
- `type: feature` — a validated feature request, enhancement, or product idea.
- `type: docs` — documentation work.

## Area labels

- `area: control-plane` — management service, API, accounts, peers, and backend product logic.
- `area: identity` — login, SSO, OIDC/SAML, and identity provider integrations.
- `area: client-agent` — daemon, CLI, local agent behavior, and OS client behavior.
- `area: connectivity` — peer connectivity, NAT traversal, relay, signal, and connection establishment.
- `area: dns-routing` — DNS, routes, exit nodes, and related routing behavior.
- `area: access-control` — policies, posture checks, NetBird SSH access, and permission logic.
- `area: ui` — dashboard, desktop UI, and frontend UX.
- `area: mobile` — iOS and Android apps.
- `area: deployment` — self-hosting, Docker, Kubernetes, reverse proxies, installs, and upgrades.

## Status labels

- `status: needs-triage` — not reviewed or not fully sorted yet.
- `status: needs-info` — blocked on more details from the reporter or community.
- `status: validated` — confirmed enough for a maintainer or contributor to act on.
- `status: blocked` — waiting on a dependency, decision, or external constraint.

## Notes

Kubernetes is currently included under `area: deployment`. If it becomes a separate engineering queue for issue triage, we can split it into `area: kubernetes` later.

Provider-specific labels such as Keycloak, Zitadel, Authentik, Okta, Azure, and Google Workspace are intentionally not part of the core set. They should be captured in the form fields first and only promoted to labels if they become useful for recurring engineering reports.
