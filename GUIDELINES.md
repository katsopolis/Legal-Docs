# Legal Docs Guidelines

## Purpose and scope

These rules govern the central proprietary legal-document repository and project-specific notices. They complement the root `README.md`, `SERVICES.md` and `SECURITY.md`. Established project behavior and design tokens override generic examples.

## Architecture and ownership

- Keep one authoritative copy for each legal document. Project folders may reference the central text but must not silently diverge from it.
- Keep public interfaces typed, narrow and validated at trust boundaries.
- One module owns each product invariant, transformation and persistence rule; do not maintain silent parallel implementations.
- Generated files and build artifacts are not hand-edited or committed unless the repository explicitly treats them as source.

## Product and visual system

- Documents use plain, professional structure with consistent headings, dates and ownership statements. Decorative branding must not reduce legal readability.
- Reuse current spacing, radius, type, color and motion tokens. Add a token only when it represents a reusable project decision.
- Use the established icon or authored asset system; do not use emoji or platform-dependent glyphs as product icons.
- Text must wrap, truncate or scale by a documented rule and may not obscure essential controls.
- Support reduced motion, visible focus, semantic labeling and sufficient contrast where the platform allows it.

## Layout and interaction

- Markdown must render cleanly on GitHub and in plain-text review. Tables stay narrow enough to read without hiding clauses.
- Every primary interaction works without hover. Disabled states remain legible and explain prerequisites when needed.
- Reserve space for asynchronous content to prevent layout jumps. Use restrained skeletons/progress only while work is pending.
- Empty and error states expose the next valid action. Irreversible actions state their scope and require confirmation.

## State, data and failure handling

- Draft, reviewed, effective and superseded status must be explicit when applicable. Never overwrite historical effective text without a traceable revision.
- Persist the minimum needed data. Version stored formats and define migration, backup or safe-reset behavior.
- Never turn an unknown or failed state into a plausible zero, success message or silent fallback.
- Logs omit secrets, access tokens, private content and unnecessary personal identifiers.

## Security and dependencies

- Follow `SECURITY.md`. Secrets belong in ignored environment files, platform secret storage or deployment-provider settings, never in distributable clients.
- Apply least privilege to filesystem, network, database, extension, plugin and store permissions.
- Keep lockfiles and toolchain declarations current. Update dependencies in reviewed groups and read migration notes before major upgrades.
- Preserve third-party licenses and provenance for code, fonts, art, audio, datasets and models.

## Performance and resilience

- Keep documents text-first and avoid large embedded assets. Link to controlled source material only when the link is expected to remain available.
- Every cache has an owner, key, lifetime and invalidation rule.
- Network operations use timeouts, cancellation and bounded retries. Degraded/offline behavior is explicit.
- Interface motion must not block input; prefer transform/opacity animation unless product behavior needs another technique.

## Verification and release

- Review changed text for ownership, contact address, project name, dates, internal consistency and third-party notices. Legal approval remains a human release gate.
- Review a small, representative and large/edge-case input or viewport for affected behavior.
- A build alone is not runtime proof; test the packaged/exported artifact when platform boundaries change.
- Publishing legal text requires explicit owner approval; documentation builds must not imply legal review occurred automatically.
- Keep future publication checks in release documentation, not in the active defect register until a release decision makes them actionable.

## Documentation maintenance

Update this file when architecture, platform targets, visual tokens, permissions, service boundaries or release commands change. Keep product/setup material in `README.md` and provider/runtime details in `SERVICES.md`.
