# gmterminal.today DNS Cutover

**Status:** READY FOR DNS ACTION — USER ACTION REQUIRED

## Target

`gmterminal.today` → GitHub Pages deployment for `Content-ai-os` Public Web v0.1.

## GitHub Side

- Pages deployment workflow is present at `.github/workflows/public-web-pages.yml`
- Custom-domain declaration is present at `15 Public Web Layer/web/CNAME`

## DNS Side

The GitHub connector cannot modify the user's DNS provider from this repository.

At the DNS provider, configure the apex domain according to the current GitHub Pages custom-domain guidance. For an apex domain, this normally means the GitHub Pages A/AAAA records published by GitHub. Do not guess or copy stale IP addresses from old documentation; verify the current values in GitHub's documentation/settings before saving DNS changes.

## Cutover Procedure

1. Confirm the Pages workflow has completed successfully.
2. Open the repository Pages settings and confirm the custom domain is accepted.
3. Configure DNS for `gmterminal.today` at the domain/DNS provider.
4. Wait for DNS propagation.
5. Verify HTTPS certificate issuance.
6. Smoke test the site on desktop and mobile.
7. Confirm the old `gmterminal` site is no longer being served.
8. Only after successful verification, archive/delete the obsolete `gmterminal` repository.

## Rollback

Before deleting the old repository, record the previous DNS configuration and hosting target. Rollback means restoring the previous DNS records if the new deployment fails.

## Security

- Do not add API keys to the static site.
- Do not expose n8n credentials in frontend code.
- Public Web must not call privileged APIs directly.
