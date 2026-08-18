# gmterminal.today — Domain Migration Plan

**สถานะ:** PLANNED — NO DNS CHANGE

## Current State Verified

The GitHub account contains a private repository named `delucksy-afk/gmterminal` with a single `index.html` at repository root. The page title is currently `Smart Trading Academy - Grandmaster v9.3`, so this repository is not yet a neutral Content AI OS frontend.

## Decision

We will **reuse the domain** `gmterminal.today` for Content AI OS, but we will not immediately repoint the domain or overwrite the existing site.

## Why

The existing domain already has a web asset, while Content AI OS needs a new Public Web Layer. A direct replacement without a staging and rollback path could cause unnecessary downtime or loss of the existing site.

## Target

```text
gmterminal.today
      ↓
Content AI OS Public Web
      ↓
Authenticated / scoped API layer
      ↓
n8n Runtime
      ↓
Content AI OS Core
```

## Migration Options

### Option A — Replace current root site

Use `gmterminal.today` directly for the Content AI OS web UI.

**Use only after staging and backup.**

### Option B — Keep current root and use a subdomain

Example architecture:

```text
gmterminal.today        → existing public site
app.gmterminal.today    → Content AI OS
```

This is the safest transition if the existing site still has value.

### Option C — Rebuild the existing site as the Public Web Layer

Retain useful UI concepts/assets, but rewrite the frontend around Content AI OS requirements.

## Recommended v0.1

**Option B first**, then decide whether the Content AI OS interface should eventually become the root domain.

## DNS / Hosting Gate

Before any DNS change:

- confirm current DNS provider
- confirm current hosting target
- back up existing site
- create staging deployment
- test HTTPS
- test mobile layout
- test authentication boundaries
- confirm API does not expose privileged credentials
- define rollback target

## Important

This repository does not currently change DNS. Domain configuration must be performed at the actual DNS / hosting provider after the migration gate is approved.
