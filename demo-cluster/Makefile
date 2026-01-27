GEN_DIR := .k8s-gen
MANIFESTS := $(GEN_DIR)/manifests.yaml

.PHONY: all generate clean

all: generate

generate: $(MANIFESTS)

$(MANIFESTS):
	@mkdir -p $(GEN_DIR)
	@echo "# Manifests générés (placeholder)" > $(MANIFESTS)
	@echo "# À remplacer par un appel à Helm, Kustomize, etc." >> $(MANIFESTS)
	@echo "apiVersion: v1" >> $(MANIFESTS)
	@echo "kind: Namespace" >> $(MANIFESTS)
	@echo "metadata:" >> $(MANIFESTS)
	@echo "  name: demo-team-platform" >> $(MANIFESTS)

clean:
	rm -rf $(GEN_DIR)

