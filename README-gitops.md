# Démo GitOps – Structure de base

Ce dossier reprend une structure inspirée du dépôt `oss-japan-demo` (`[oss-japan-demo](https://github.com/qasmi/oss-japan-demo)`), simplifiée pour un exercice.

## Arborescence

```text
.
├── .github/
│   └── workflows/
│       └── gitops-ci.yaml
├── agents/
│   ├── github-mcp.yaml
│   └── gitops-agent.yaml
├── demo-cluster/
│   ├── Makefile
│   ├── team-platform/
│   │   └── README.md
│   └── .k8s-gen/
│       └── .gitkeep
├── gitops-chart/
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
│       └── README.md
└── playgrounds/
    └── kind/
        └── infra-setup/
            └── setup.sh
```

## Flux GitOps attendu

- **`demo-cluster/team-platform`** : tu mets ici la config déclarative de ton cluster/équipe (fichiers YAML Kubernetes, valeurs Helm, etc.).
- **`demo-cluster/Makefile`** : génère un bundle de manifests dans `demo-cluster/.k8s-gen/manifests.yaml` (similaire à l’exemple du dépôt d’origine).
- **`gitops-chart`** : chart Helm servant de base pour templater la config GitOps.
- **`agents`** : définitions YAML d’agents (par exemple un agent GitOps et un MCP GitHub).
- **`playgrounds/kind/infra-setup`** : scripts pour créer un cluster de démo en local (kind, par exemple).
- **`.github/workflows/gitops-ci.yaml`** : pipeline CI très simple qui valide/génère les manifests.

Tu peux maintenant adapter les fichiers (`Makefile`, manifests, chart Helm, etc.) à ton contexte réel (noms de cluster, namespaces, repos, clés, tokens…).

