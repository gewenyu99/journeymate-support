# JourneyMate support site

Public support and privacy pages for JourneyMate, an experimental travel
information app. This repository contains only the static website and its
GitHub Pages deployment workflow.

## Publication status

Created 2026-09-07. The website is **not deployed**. The source pages contain
clearly marked draft fields; the deployment workflow rejects those fields.
Repository creation and commits do not publish the website.

| Item | Status |
| --- | --- |
| Support and privacy HTML, responsive styles and logo | Prepared |
| Public support/privacy email | NEEDS_INPUT — owner will provide later |
| Operator name, policy effective date and support retention | NEEDS_INPUT — owner will provide later |
| Final policy matching the distributed app configuration | Complete before deployment |
| Live support/privacy URLs | Pending successful Pages deployment |
| Optional reference download package | Not included or hosted |

## Files and local preview

The website lives in `docs/appstore/site/`:

- `index.html` and `support.html`: identical support pages.
- `privacy.html`: privacy policy draft for an analytics-disabled app release.
- `styles.css` and `assets/journeymate-logo.svg`: local styles and artwork.

No framework, dependency install, database, paid domain or application server
is needed. Preview locally with Python:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory docs/appstore/site
```

Open `http://127.0.0.1:8000/`. This is a local preview, not a public deployment.

## Finish and publish

1. Fill the marked contact/operator/date/retention fields using owner-provided
   details. A personal Gmail address can serve as the support/privacy contact;
   a custom email domain is optional. Do not invent an address or identity.
2. Complete the policy for the actual distributed app configuration and chosen
   hosting. GitHub Pages records visitors' IP addresses for security; disclose
   the host's processing accurately. A static website does not imply no logs.
   See [GitHub's Pages documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages).
3. Remove the draft banners, editorial paragraphs, unresolved markers and
   `noindex,nofollow` tag only after their fields are resolved. Keep support and
   index identical. Use relative links between support and privacy pages.
4. The agent checks local navigation, phone layouts, keyboard access and light
   and dark appearance. Fix failures; do not assign manual testing to the owner.
5. Commit and push to `main`. In repository Settings → Pages, the build source
   must be **GitHub Actions**. Run **Publish support and privacy pages** from
   Actions, or use:

   ```sh
   gh workflow run publish-support-site.yml --repo gewenyu99/journeymate-support --ref main
   ```

6. The workflow stages only the intended public files. It runs only on manual
   dispatch and refuses unresolved draft fields. The agent must verify the
   deployed HTTPS pages load without authentication, then use those actual
   working URLs in the app and App Store Connect.

Expected Pages addresses, **not live until deployment succeeds**:

- Support: `https://gewenyu99.github.io/journeymate-support/support.html`
- Privacy: `https://gewenyu99.github.io/journeymate-support/privacy.html`

GitHub Pages is available for public repositories on GitHub Free. No custom
domain or paid hosting plan is required for this setup. Hosting availability
and limits follow [GitHub's Pages documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages).

## Optional static reference downloads

The app primarily uses the reference information bundled with each build.
An explicit **Pull latest** action may download a complete validated static
snapshot; app startup must not depend on this site. Sources and actual content
dates remain distinct from packaging and download timestamps.

A future agent can place a qualified `latest.json` and `latest.receipt.json`
pair under `docs/appstore/site/reference-data/`. The workflow requires matching
hashes and a passing phone/release QA qualification before including the pair.
Do not copy raw source observations, private QA artifacts or maintenance reports.
No reference endpoint is established by the current repository.
