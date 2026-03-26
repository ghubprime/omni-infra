# omni-infra
The foundational infrastructure repository providing generic configurations, baseline Helm charts, and custom patches supporting the overarching `k8s-scots-lab` environment.

## Repository Overview
While `k8s-cluster` acts as the primary deployment definition representing the actual endpoints and core cluster base, `omni-infra` serves as an environment detailing shared, reusable Helm charts, generic Kustomize components, and declarative patches across the Sidero Omni physical footprint.

### Key Components
- `helm/`: Custom or modified Helm charts utilized in the infrastructure deployments.
- `kustomize/overlays/scots-lab/`: Environment-specific implementations and custom patches for the primary infrastructure.
- `manifests/`: Raw YAML definitions required for standard infrastructure setups.
- `patches/`: Configuration variations and generalized patch components to be consumed by deployments.

## Dependency Management

The `omni-infra` repository is integrated with **Mend.io** (formerly WhiteSource/Renovate) for automated dependency and vulnerability management. 

Mend.io continuously scans the repository's Helm charts, Kustomize bases, and container image references. When an update is available, Mend generates automated Pull Requests with the necessary configuration bumps. A central "Dependency Dashboard" issue is maintained by the bot to track the status of all available upgrades and pending auto-PRs. These PRs should be reviewed and merged regularly to maintain security and feature currency across the cluster.
