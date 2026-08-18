# Almost Clever Games — Public Pages

Public GitHub Pages website, support contact, game artwork, and privacy policies for games published by **Almost Clever Games**.

## Website

- [Almost Clever Games home page](https://dmlapteacru.github.io/almost-clever-pages/)

## Games

| Game | Platform / services | Public page |
|---|---|---|
| ![Merge Orbit icon](assets/merge-orbit-icon.svg) **Merge Orbit** | Android · Offline | [Privacy Policy](https://dmlapteacru.github.io/almost-clever-pages/merge-orbit/privacy-policy.html) |
| ![Puff Up icon](assets/puff-up-icon.png) **Puff Up!** | Android · Play Games leaderboards · Saved Games | [Privacy Policy](https://dmlapteacru.github.io/almost-clever-pages/puff-up/privacy-policy.html) |
| ![Lucky Ticket icon](assets/lucky-ticket-icon.png) **Lucky Ticket** | Android · Play Games Saved Games · Google Play Billing | [Privacy Policy](https://dmlapteacru.github.io/almost-clever-pages/lucky-ticket/privacy-policy.html) |

Merge Orbit is designed as an offline game. Puff Up! keeps its core gameplay offline-capable but uses Google Play Games Services for player sign-in, weekly/all-time leaderboards, and Saved Games cloud synchronization. Puff Up! currently has no ad SDK, no real-money billing SDK, and no developer-operated third-party analytics service. Lucky Ticket uses Google Play Games Services for player sign-in and Saved Games cloud synchronization and Google Play Billing for optional in-app purchases; its current version has no advertising SDK and no developer-operated third-party analytics service.

## Repository structure

```text
index.html                          Main public landing page
assets/                             Shared branding and game-card artwork
assets/puff-up-icon.png             Puff Up! production app artwork
assets/lucky-ticket-icon.png        Lucky Ticket production app artwork
merge-orbit/privacy-policy.html     Merge Orbit privacy policy
puff-up/privacy-policy.html         Puff Up! privacy policy
lucky-ticket/privacy-policy.html    Lucky Ticket privacy policy
```

## Privacy-policy maintenance

Privacy pages must stay consistent with the corresponding shipped game and Play Console Data safety declarations. Update the relevant policy effective date whenever data handling, platform services, advertising/analytics, purchases, account behavior, leaderboards, or cloud storage changes.

The public policy should describe the categories of data handled, why they are used, the relevant service providers, retention/deletion, and security. It should not expose internal implementation algorithms unless they are necessary to explain a user-facing data practice.

**Audit baseline — 2026-08-19:**

- Lucky Ticket was checked against `v3-redesign` (version `1.0.0+1`): Google Play Games sign-in/Saved Games and Google Play Billing are active code paths; there is no advertising SDK, separate player-account backend, or developer-operated third-party analytics SDK.
- Puff Up! was checked against `release/5.0` (version `5.0.0+14`): Google Play Games sign-in, weekly/all-time leaderboards, and Saved Games are active; production has no advertising SDK, no real-money billing integration, and no developer-operated third-party analytics service.

Puff Up! contains code seams for possible future rewarded ads and premium monetization, but the current production build activates neither; the privacy policy and Play Data Safety declarations must be updated before either is enabled.

Lucky Ticket's current architecture stores purchase-related delivery identifiers with its game state so consumable purchases can be delivered safely. The public policy intentionally describes this at the user-data level rather than documenting the internal purchase-delivery algorithm. If the planned future cross-platform/backend architecture is implemented, the policy must be revised before that data path ships.

## Artwork conventions

Game-specific public surfaces should use the corresponding game artwork from `assets/` (for example `puff-up-icon.png` for Puff Up! and `lucky-ticket-icon.png` for Lucky Ticket). Almost Clever Games branding such as the site header, publisher logo and shared developer banner continues to use the ACG assets.

## Contact

Support: [lector3run@gmail.com](mailto:lector3run@gmail.com)

This repository contains public website content only. Game source code, Android signing material, secrets, APK files, and release bundles are not stored here.

Copyright © 2026 Almost Clever Games. All rights reserved.
