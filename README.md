# Platform-Shared-Service

GitOps repository for deploying applications using Argo CD.

## Secret handling

- Docker registry credentials are created manually in the cluster.
- Secret name expected per namespace:
  - ghcr-cred
- ServiceAccounts reference imagePullSecrets.
- Git never stores secret values.

If the secret is missing, pods will fail with ImagePullBackOff.