# RepPulse website publication checklist

**Status: BLOCKED UNTIL FINAL LEGAL/SDK REVIEW AND PUBLIC DEPLOYMENT**

The checklist must not be marked complete while any placeholder remains in the public configuration, privacy policy, app-ads.txt, robots.txt or sitemap.

## Owner-provided information still required

- Public support email: configured as `millerlabchannel@gmail.com`.
- Controller identity: configured as Miller Alberto Della Morte, individual developer operating under Miller Lab, Italy.
- Legal review/approval of the controller wording and rights procedure.
- Legal contact details beyond the published email, if required by the final legal review.
- Final public deployment verification for the configured website and privacy URLs.
- Final Google Play Store URL once the app is published.
- Exact official app-ads.txt line from AdMob.
- Privacy Policy update date is set to 24 November 2026, pending final legal approval.
- Final retention, recipients/processors, transfer safeguards, rights procedure and deletion procedure for the actual release configuration.

## Before publication

- [ ] Complete `config/site-config.js`.
- [ ] Replace the app-ads.txt placeholder with the exact AdMob line.
- [ ] Replace all `[PUBLIC_SITE_URL]` tokens.
- [ ] Review both privacy pages against the released Android SDK configuration.
- [ ] Verify static direct URLs for privacy, app-ads.txt, robots and sitemap.
- [ ] Test at 360×800, 390×844, 768×1024, 1280×720 and 1920×1080.
- [ ] Verify no horizontal overflow, broken links or console errors.
- [ ] Configure GitHub Pages and verify the public origin.
- [ ] Complete owner/legal review. Do not claim definitive GDPR compliance from this template alone.

## Deployment-specific checks

- [x] External `app-ads.txt` verified at `https://md5angy.github.io/app-ads.txt`: HTTP 200, `text/plain`, Google line present, no placeholder.
- [x] `app-ads.txt` is not duplicated in this repository.
- [x] `robots.txt` and `sitemap.xml` point to the configured project-site URL.
- [x] `.nojekyll` added for plain static hosting.
- [ ] GitHub Pages configured on `main` / repository root.
- [ ] Public project-site URLs return HTTP 200 after deployment.
- [ ] Review/decision on earlier remote history containing QA screenshots and internal audit documents.

## Google Play Data Safety handoff

- [x] Local workout, Countdown, Multi Countdown, language and feedback storage identified from Android source.
- [x] No RepPulse backend, Firebase Analytics, Crashlytics or Play Billing references found in the reviewed source.
- [x] UMP and Google Mobile Ads integrations identified, including `canRequestAds()` gating and OFF/SIMULATED behavior.
- [x] `VIBRATE` permission and SDK-contributed advertising/network permissions documented for review.
- [x] Android manifest declares backup enabled; final backup/data-extraction behavior still requires release verification.
- [ ] Confirm final AdMob/UMP console configuration and Google disclosures.
- [ ] Confirm advertising data categories, sharing, purposes and retention in Play Console.
- [ ] Confirm final release merged manifest and Data Safety answers.
