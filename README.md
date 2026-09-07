# JourneyMate public support site

Support, privacy policy and static reference-download hosting for JourneyMate,
an experimental travel information app. Operator: **Vincent Ge**. Contact:
[vge2606@gmail.com](mailto:vge2606@gmail.com).

- [Support](https://gewenyu99.github.io/journeymate-support/support.html)
- [Privacy policy](https://gewenyu99.github.io/journeymate-support/privacy.html)

GitHub Pages uses GitHub Actions with HTTPS enforced. The pages contain no
analytics, ads, forms or tracking scripts. GitHub's request handling and Gmail
support correspondence are disclosed in the privacy policy dated September 7, 2026.
Publication status and agent checks are recorded in `VALIDATION.md`.

## Maintenance

Website source is `docs/appstore/site/`. Keep `index.html` and `support.html`
identical; share styles and the local logo. No framework or dependency install
is needed. Preview with:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory docs/appstore/site
```

The agent checks local links, keyboard access, phone layouts, light/dark
appearance and exact public email/identity before committing. No user testing
or screenshot signoff is required. Keep policy, app behavior and actual data
handling consistent; do not add unreviewed private files or credentials.

Push to `main`, then explicitly deploy:

```sh
gh workflow run publish-support-site.yml --repo gewenyu99/journeymate-support --ref main
```

The manual workflow rejects unfinished fields and stages only intended site
files. Ordinary pushes do not publish. The agent verifies successful deployment
and actual unauthenticated HTTPS responses before claiming a change is live.

## Reference snapshots

The app uses reference data bundled with each build. **Pull latest** explicitly
downloads `reference-data/latest.json` when requested; app startup does not
depend on this site. The app validates the complete snapshot before replacing
its saved data and keeps the existing data if the download fails. Source/content
dates remain separate from package and download timestamps.

Publish only an exported `latest.json` and its matching `latest.receipt.json`
under `docs/appstore/site/reference-data/`. The workflow verifies matching
hashes and passing phone/release QA qualification. No source-check result or
new package date is a guarantee that every fact is current. Raw source
observations, private QA artifacts and maintenance reports do not belong here.

GitHub Pages is available for public repositories on GitHub Free; a custom
domain is optional. See [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages).
