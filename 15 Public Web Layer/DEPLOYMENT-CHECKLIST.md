# Public Web Deployment Checklist

**Target:** `gmterminal.today`
**Current:** STAGING REQUIRED

## Build

- [x] Public Web v0.1 shell exists
- [x] No secrets in frontend
- [x] No privileged API calls
- [x] Mobile viewport supported
- [x] Basic metadata included

## Staging Gate

- [ ] Deploy static site
- [ ] Verify HTTPS
- [ ] Verify desktop
- [ ] Verify mobile
- [ ] Verify all internal anchors
- [ ] Verify no console/runtime errors
- [ ] Verify repository/source boundary
- [ ] Verify API boundary before adding integrations

## DNS Cutover Gate

Do not change DNS until all staging checks pass.

After cutover:

- [ ] `gmterminal.today` resolves to new site
- [ ] HTTPS works
- [ ] Old site is no longer served
- [ ] Smoke test passes
- [ ] Rollback target is known

## Cleanup Gate

Only after successful DNS cutover and smoke test:

- [ ] Archive old `gmterminal` repository
- [ ] Preserve only any explicitly required legal/audit record
- [ ] Remove obsolete source from active workflow
- [ ] Record migration in CHANGELOG

## Note

GitHub connector does not control the user's DNS provider. DNS changes must be performed through the domain/DNS hosting account.