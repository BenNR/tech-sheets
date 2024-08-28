helm repo add hashicorp https://helm.releases.hashicorp.com
helm search repo hashicorp/vault

helm show values codecentric/keycloak > keycloak-values.yaml


helm repo add keycloak 'https://raw.githubusercontent.com/codecentric/helm-charts/tree/master/'
