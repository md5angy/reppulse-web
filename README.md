# RepPulse Official Website

Independent static website project for RepPulse. It does not modify or build the Android project and has no backend, framework, tracker, cookie or external runtime dependency. The public controller is Miller Alberto Della Morte, an individual developer operating under Miller Lab, Italy; support and privacy contact is `millerlabchannel@gmail.com`.

## Local preview

From this directory run `python -m http.server 4173 --bind 127.0.0.1`, then open `http://127.0.0.1:4173/`.

## Public configuration

Edit only [`config/site-config.js`](config/site-config.js). It is the single public configuration source for product name, Miller Lab, support/privacy contact, controller identity, public URLs, publication status, app-ads.txt line and privacy update date. Empty values intentionally render as `TO BE PROVIDED`; publication stays conditionally blocked until the remaining legal, AdMob and deployment checks are completed. Never put Android credentials, private AdMob configuration or full internal identifiers here.

## Updating static resources

1. Complete and review `config/site-config.js`.
2. Copy the exact approved app-ads.txt line into `app-ads.txt`.
3. Replace the `[PUBLIC_SITE_URL]` tokens in `robots.txt` and `sitemap.xml`.
4. Complete the privacy controller, contact, retention, transfer and rights sections in both privacy pages.
5. Run the local preview and check desktop/mobile layouts, links, language toggle and demo.
6. Publish the whole project root so `privacy.html`, `app-ads.txt`, `robots.txt` and `sitemap.xml` remain direct static resources.

## GitHub Pages

Create a separate repository (for example `reppulse-web`), place these files at its root, push to the default branch and select **Settings → Pages → Deploy from a branch → main / root**. The project-site URL is normally `https://USERNAME.github.io/reppulse-web/`; use that exact origin in the configuration, robots and sitemap. Verify the public URLs after deployment. For AdMob app-ads.txt, follow the official AdMob hosting requirements; a custom domain or user-site root may be required depending on the app’s publisher setup. Do not publish until the checklist is unblocked.

Official app-ads.txt guidance: https://support.google.com/admob/answer/9363762

`app-ads.txt` is hosted separately at `https://md5angy.github.io/app-ads.txt` and is intentionally not duplicated in this repository. Before deployment, verify that URL returns HTTP 200, `text/plain`, the official Google line and no placeholder. AdMob’s crawl/verification status is a separate owner task.

Internal QA screenshots and audit reports are excluded from the deployable repository with `.gitignore`. Existing remote history contains earlier QA evidence; it is reported separately and is not rewritten automatically.

The homepage concept uses the official Android wordmark asset and labels the circular phone UI as a future Android theme preview, not as a current app screenshot. The former ultra-minimal phone concept remains available in the repository history/design direction; the current homepage uses Minimal Pulse.

## Evidence and scope

`assets/qa/` contains selected real Android QA captures copied from the Android repository. The phone shown on the homepage is explicitly a concept/demo SVG, not a real app screenshot. See [`docs/publication-checklist.md`](docs/publication-checklist.md) and [`docs/website-design-system.md`](docs/website-design-system.md).
