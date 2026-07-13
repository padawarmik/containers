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

For the current pinned ref `09573b64cadc`, the deployment should use immutable source SHA tags, e.g.:

```text
ghcr.io/padawarmik/ts6-manager-coom:backend-09573b64cadc
ghcr.io/padawarmik/ts6-manager-coom:frontend-09573b64cadc
ghcr.io/padawarmik/ts6-manager-coom:sidecar-09573b64cadc
```

Use the floating `backend`/`frontend`/`sidecar` tags only for ad-hoc testing.
