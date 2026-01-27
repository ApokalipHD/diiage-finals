# Team Platform

Place ici la configuration GitOps spécifique à ton équipe / ton cluster.

Exemples (à adapter) :

- Fichiers YAML Kubernetes pour les namespaces, quotas, RBAC, ingress…
- Valeurs Helm (`values-*.yaml`) consommées par le chart `gitops-chart`.
- Structuration par environnement (`dev/`, `staging/`, `prod/`).

Ces fichiers seront agrégés par le `Makefile` de `demo-cluster` dans `.k8s-gen/manifests.yaml`.

