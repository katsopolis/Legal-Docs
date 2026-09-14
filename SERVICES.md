# Legal Docs Services

## Scope

Legal Docs is a documentation repository. Git and rendered Markdown are its only required operational services. This file records runtime, local, build-time and delivery services so an offline dependency is not mistaken for “no services.”

## Service map

| Service | Boundary | Status | Responsibility |
| --- | --- | --- | --- |
| Git repository | Versioned storage | Required | Tracks authoritative legal text, history and project-specific documents. |
| Markdown renderer | Presentation | Required for review | Displays documents on GitHub or another controlled viewer. |
| Email contact | External communication | Optional | support@lorewound.com is the public contact where stated in approved documents. |
| Hosted API/database/CDN | External | Not used | No application runtime is defined. |

## Data and credential boundaries

Legal documents must not contain access codes, credentials, private keys or unnecessary personal data.

- Keep secrets in ignored local environment files, operating-system/platform secret storage or the selected deployment service.
- Never print tokens, private paths or user content in routine logs.
- Validate data when it crosses a process, browser, plugin, native, filesystem or network boundary.
- Third-party services require a named owner, least-privilege access and a documented removal/fallback path.

## Offline and failure behavior

All authoritative text remains readable from a local clone. External links or email availability do not affect document integrity.

Every service call or local subsystem operation must expose a bounded failure state. Use timeouts/cancellation for network work, caps for untrusted files or queues, and retries only where the operation is idempotent.

## Operations and release checks

Review ownership, effective dates, project names, contact details and third-party notices before publishing a revision.

Before publication, verify only the services used by that target. Future store, hosting, domain or signing checks are release gates, not active risks while no release is planned.

## Change policy

Update this document when a service, provider, permission, credential class, storage location, port, data owner or failure behavior changes. Also update `SECURITY.md` for security implications and `GUIDELINES.md` for architecture or UX rules.
