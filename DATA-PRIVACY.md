# Inactive Studios LLC — Data & Privacy Register

Internal release-control document. Update this register whenever a website, game, SDK, service, or storefront integration changes data handling. Public privacy notices and store disclosures must match the shipped build.

## Studio principles
- Collect only data required for a defined product, security, diagnostic, support, or business purpose.
- Do not sell player personal information.
- Do not create player profiles or retain advertising identifiers unless a documented feature requires them.
- Prefer local game saves unless a cloud feature has a defined requirement.
- Do not place secrets, player data, crash dumps, support messages, or advertising identifiers in the public Git repository.
- Review third-party SDK data practices before integration and again before each store release.

## Current public website
| Component | Purpose | Data intentionally collected by Inactive Studios | Storage | Action |
|---|---|---|---|---|
| GitHub Pages site | Public studio/game information | None through forms/accounts | No studio website database | Re-review if analytics, forms, cookies, or tracking are added |
| Email links | Support/privacy/general contact | Information voluntarily emailed by sender | Business email provider | Retain only as needed for support/business/legal purposes |

## Product register
| Product | Player account DB | Cloud saves | Diagnostics | Advertising | Analytics | IAP | Status |
|---|---|---|---|---|---|---|---|
| Contact Imminent | None | None | Not yet declared | Not yet declared | Not yet declared | Not yet declared | Development |
| Dead Grid | None | None | Not yet declared | Not yet declared | Not yet declared | Not yet declared | Development |

## SDK/service intake checklist
For every proposed SDK/service, record: provider; SDK/version; purpose; data types; whether linked to identity; whether used for tracking/advertising; storage location/provider; retention/deletion controls; encryption/security; child-directed implications; Apple privacy-label impact; Google Play Data Safety impact; consent requirements; privacy-policy changes; owner; approval date.

## Release gate
Before every public store release: inventory SDKs; compare shipped permissions/entitlements with this register; verify product privacy page; verify Apple privacy answers; verify Google Data Safety answers; verify support URL/email; test privacy/support links; confirm no secrets or user data are committed to Git.
