# Web365 27B Blocklist Check

Static GitHub Pages app that shows the community full-blocklist wallets behind the 26 Aug 2026 **~26.972B BDAG** figure.

The page ships with a verified snapshot. If a community RPC allows browser calls, **Refresh live** re-reads `isBlocked` and balances.

## What you get

- 13 fully blocked addresses
- Live or snapshot balances
- Sum compared with the published ~26.972B figure
- JSON at `data/frozen-wallets.json`
- CSV export

## Publish

```bash
git init
git add .
git commit -m "Web365 27B Blocklist Check"
git branch -M main
git remote add origin git@github.com:<you>/web365-27b-blocklist-check.git
git push -u origin main
```

Then: repo **Settings → Pages → Deploy from branch → main / root**.

URL: `https://<you>.github.io/web365-27b-blocklist-check/`

No build. No Node. No backend.

## On-chain source

| Item | Value |
|---|---|
| Chain ID | 1404 |
| Full blocklist | `0xe628505d5cB6F5F4f9a25Cd5c80Caa198cc645a0` |
| `isBlocked(address)` selector | `0xe5962195` |
| Owner | `0xe9ce34eda6a4554420ca871d7057edaec32e9e9c` |
| Snapshot RPC | `https://rpc.capedag.com` |

Public RPCs do not serve historical state at block 18,955,000. The published total matches the live blocked set.
