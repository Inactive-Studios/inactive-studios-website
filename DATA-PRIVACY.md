# Inactive Studios LLC — Data & Privacy Register

Internal release-control document. Update this register whenever a website, game, SDK, service, permission, or storefront integration changes data handling. Public privacy notices and store disclosures must match the shipped build.

## Studio principles
- Collect only data required for a defined product, security, diagnostic, support, advertising, transaction, or business purpose.
- Do not sell player personal or sensitive information.
- Minimize collection and use of device identifiers.
- Prefer local game saves unless a cloud feature has a defined requirement.
- Do not request sensitive device permissions unless required for an implemented feature.
- Do not place secrets, player data, crash dumps, support messages, advertising identifiers, or other user data in the public Git repository.
- Review third-party SDK data practices before integration, after material SDK/configuration changes, and before each store release.
- Keep shipped application behavior, privacy policies, consent flows, and storefront privacy/Data Safety disclosures synchronized.

## Current public website
| Component | Purpose | Data intentionally collected by Inactive Studios | Storage | Action |
|---|---|---|---|---|
| GitHub Pages site | Public studio/game information | None through forms/accounts | No studio website database | Re-review if analytics, forms, cookies, or tracking are added |
| Email links | Support/privacy/general contact | Information voluntarily emailed by sender | Business email provider | Retain only as needed for support/business/legal purposes |

## Product register
| Product | Player account DB | Cloud saves | Diagnostics | Advertising | Analytics | IAP | Status |
|---|---|---|---|---|---|---|---|
| Contact Imminent | None | None | Firebase Crashlytics planned for Google Play release | Google AdMob + UMP planned for Google Play release | Firebase Analytics not enabled | Google Play Billing supported/planned | Android release preparation |
| Dead Grid | None | None | Not yet declared | Not yet declared | Not yet declared | Not yet declared | Development |

## Contact Imminent — Google Play release baseline

### Application identity
- Android package/application ID: `com.inactivestudios.contactimminent`
- Developer/publisher: Inactive Studios LLC
- Product privacy policy: `https://inactivestudios.com/privacy/contact-imminent/`
- Privacy contact: `privacy@inactivestudios.com`
- Support contact: `support@inactivestudios.com`

### Planned services
- Google AdMob / Google Mobile Ads SDK — advertising.
- Google User Messaging Platform (UMP) — consent and privacy-choice messaging where applicable.
- Firebase Crashlytics — crash, ANR, and stability diagnostics.
- Firebase Installations — supporting Firebase installation identification.
- Firebase Sessions — supporting application/session diagnostics.
- Google Play Billing — digital purchase processing when in-app purchases are offered.
- Firebase Analytics — NOT enabled in the initial baseline unless separately reviewed and declared.

### Data-minimization baseline
- No Inactive Studios player accounts.
- No studio-hosted cloud saves.
- No intentional collection of contacts.
- No precise-location gameplay requirement.
- No health-data functionality.
- No SMS or call-log functionality.
- No microphone requirement.
- No camera requirement.
- Local gameplay/settings data may be stored on-device.
- Sensitive Android permissions are not to be added without privacy review.

### Release-state rule
The public Contact Imminent privacy policy may describe services planned for the Google Play release, but the Play Console Data Safety declaration must reflect the actual SDKs, permissions, configuration, and behavior of the AAB submitted for review. Before production submission, verify the final dependency tree and Android manifest against this register.

## SDK/service intake checklist
For every proposed SDK/service, record:
- Provider and SDK/version.
- Purpose.
- Data types accessed, collected, transmitted, or shared.
- Whether data is linked to identity.
- Whether data is used for advertising or tracking.
- Device identifiers used.
- Storage/provider and retention/deletion controls.
- Encryption/security behavior.
- Runtime permissions.
- Consent or prominent-disclosure requirements.
- Child-directed implications.
- Apple privacy-label impact.
- Google Play Data Safety impact.
- Privacy-policy changes.
- Owner and approval date.

## Release gate
Before every public store release:
1. Inventory direct and transitive SDK dependencies.
2. Inspect the final Android permissions/manifest or applicable platform entitlements.
3. Verify advertising and consent configuration.
4. Verify the product privacy policy matches the shipped build.
5. Verify Google Play Data Safety answers match the shipped build.
6. Verify Apple privacy answers when applicable.
7. Verify support/privacy URLs and email addresses.
8. Test in-app privacy/support links.
9. Verify account deletion requirements if accounts exist.
10. Confirm no secrets or user data are committed to Git.
