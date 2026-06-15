# homelab-k8s

Manifests Kubernetes du homelab, déployés en **GitOps via ArgoCD** sur le cluster k3s (lab).
Aucun secret ici — les Secrets k8s sont créés hors-bande sur le cluster (`kubectl`).

## Apps
- `apps/umami/` — Umami analytics (Umami + PostgreSQL). Service en LoadBalancer (MetalLB).

ArgoCD surveille ce repo : `git push` → synchro automatique sur le cluster.
