# containers

Central place for building and publishing container images used by the homelab.

Images are published to GHCR under this GitHub owner, for example:

```text
ghcr.io/padawarmik/ts6-manager-coom:<tag>
```

## TS6 Manager coom fork

Workflow: `.github/workflows/ts6-manager-coom.yml`

Default fork ref:

```text
83a0635b37fb
```

Expected tags for the pinned ref plus the homelab runtime patch:

```text
ghcr.io/padawarmik/ts6-manager-coom:backend-83a0635b37fb-homelab1
ghcr.io/padawarmik/ts6-manager-coom:frontend-83a0635b37fb-homelab1
ghcr.io/padawarmik/ts6-manager-coom:sidecar-83a0635b37fb-homelab1
```

The workflow also publishes moving convenience tags:

```text
ghcr.io/padawarmik/ts6-manager-coom:backend
ghcr.io/padawarmik/ts6-manager-coom:frontend
ghcr.io/padawarmik/ts6-manager-coom:sidecar
```

Manual run:

1. Open Actions → `Build ts6-manager-coom images`.
2. Run workflow.
3. Keep the default ref, or pass any commit/branch/tag from `coom/ts6-manager`.
