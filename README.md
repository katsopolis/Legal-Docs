# Legal Docs

<div align="center">
  <p><strong>Canonical legal documentation for the Lorewound portfolio.</strong></p>
  <p>Created by Gazi Enes Sedef · Published by Lorewound</p>
</div>

## Overview

Legal Docs is the central repository for privacy notices, terms, disclosures and shared legal material used by Lorewound projects. It gives the portfolio one maintained reference point while allowing a project to keep a specific notice in its own folder when its data, platform or store behavior differs.

This repository records text and presentation. It does not turn an unreviewed draft into approved legal advice, and automated checks cannot replace owner/legal review.

## Repository model

| Area | Responsibility |
| --- | --- |
| Root pages and assets | Shared index, presentation and portfolio-level notices |
| `false-clue/` | False Clue-specific legal material |
| `fifence/` | FiFence-specific legal material |
| Git history | Reviewable changes, effective text and provenance |

Use one authoritative copy for each notice. If a project-specific document diverges from a general policy, state the project name, scope and effective date. Do not maintain two silently different copies of the same policy.

## Editing and review

1. Identify the project, platform and actual data/service behavior covered.
2. Update the smallest authoritative document.
3. Check product names, publisher, contact address, dates and cross-links.
4. Review the rendered page and raw Markdown/HTML.
5. Obtain explicit human approval before treating a revision as effective or publishing it.

Documents use concise headings, readable line lengths and ordinary language. Legal meaning has priority over decorative branding. Tables should remain readable on narrow screens, and links need useful labels.

## Local use

The repository is primarily static HTML, CSS, JavaScript and text. Open `index.html` in a modern browser or use a simple local static server when browser security rules require it. No application database or hosted API is required.

Runtime/build/service boundaries are recorded in [SERVICES.md](SERVICES.md). Maintenance and formatting rules are in [GUIDELINES.md](GUIDELINES.md). Private vulnerability or accidental-disclosure reports follow [SECURITY.md](SECURITY.md).

## Security and privacy

Do not place secrets, account credentials, access codes, private addresses or unnecessary personal data in legal pages or repository history. Public contact text uses [support@lorewound.com](mailto:support@lorewound.com). Verify external links and ensure a legal page does not promise a feature, deletion path or retention period that the product does not actually implement.

## Publication checklist

- Correct project and publisher names.
- Correct contact address and effective/update dates.
- Accurate description of data collection, storage, deletion and third parties.
- Consistent language between store listing, application and legal page.
- Working project/legal links on desktop and mobile.
- Explicit approval for the final text.

## Ownership and publishing

| Role | Details |
| --- | --- |
| Creator and producer | Gazi Enes Sedef |
| Publisher | Lorewound |
| Contact | [support@lorewound.com](mailto:support@lorewound.com) |
| Repository owner | [katsopolis](https://github.com/katsopolis) |

## License

The repository's original material is proprietary and all rights are reserved. No use, copying, modification, distribution, hosting or commercial exploitation is permitted without prior written permission. See [LICENSE](LICENSE). Third-party notices and quoted legal sources retain their own rights.
