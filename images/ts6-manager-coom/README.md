# ts6-manager-coom

Builds the TS6 Manager images from [`coom/ts6-manager`](https://github.com/coom/ts6-manager).

The workflow builds three components from the fork's Dockerfiles:

| Component | Dockerfile |
| --- | --- |
| `backend` | `Dockerfile.backend` |
| `frontend` | `Dockerfile.frontend` |
| `sidecar` | `Dockerfile.sidecar` |

## Tagging

For each component the workflow publishes four tags:

```text
ghcr.io/padawarmik/ts6-manager-coom:<component>-<source-short-sha>
ghcr.io/padawarmik/ts6-manager-coom:<component>-<requested-ref>
ghcr.io/padawarmik/ts6-manager-coom:<component>-<utc-date-YYYYMMDD>
ghcr.io/padawarmik/ts6-manager-coom:<component>
```

Expected tags for the pinned ref plus the homelab runtime patch:

```text
ghcr.io/padawarmik/ts6-manager-coom:backend-83a0635b37fb-homelab1
ghcr.io/padawarmik/ts6-manager-coom:frontend-83a0635b37fb-homelab1
ghcr.io/padawarmik/ts6-manager-coom:sidecar-83a0635b37fb-homelab1
```

Use the floating `backend`/`frontend`/`sidecar` tags only for ad-hoc testing.
