# Agent instructions

This is the public JourneyMate website repository. Read README.md for current
publication status, owner fields and the deployment command.

- Keep this repository limited to public support/privacy HTML, styles, artwork,
  public maintenance instructions and the Pages workflow. Never copy app source
  history, signing material, secrets or private App Review contact details.
- Keep unknown identity, email and retention fields marked. The owner explicitly
  deferred these inputs; they are not manual-testing tasks. Do not invent them.
- Maintain index.html and support.html as identical pages. Use relative site
  links so the GitHub Pages project path works.
- The agent owns testing and fixes. Check local links and headless phone renders
  at narrow and standard widths, dark/light appearance, keyboard focus and
  scrolling after visual changes. Record actual evidence; no human signoff gate.
- Keep deployment manual. Preserve the placeholder rejection and restricted
  artifact staging in .github/workflows/publish-support-site.yml. A commit alone
  must not deploy unfinished pages. Verify live URLs after a successful deploy.
- Use static files and inexpensive Linux Actions. Avoid adding services,
  dependencies, analytics or recurring automation without a concrete need.
- Reference content is bundled in the app first. Optional Pull latest files
  must come from a validated QA-qualified export with matching receipt. Do not
  treat source-check, package or download times as factual verification dates.
- Use non-destructive commits to main. Never force-push or replace repository
  history. No mandatory manual user testing or screenshot approval.
