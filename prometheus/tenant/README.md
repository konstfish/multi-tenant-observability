# Tenant Manifests

## [role.yaml](role.yaml) 

Create a Role with view rights on `namespace/metrics` as configured for the `kube-rbac-proxy` in [config.yaml](../querier-frontend/config.yaml).

## [sa.yaml](sa.yaml) & [token.yaml](token.yaml)

Create a Service Account, bind it to the Role & create a `kubernetes.io/service-account-token` Secret referencing the SA. The JWT populated in the secret will then provide access to the querier frontend.

## [datasource.yaml](datasource.yaml)

Assumes you have the [Grafana Operator](https://grafana.github.io/grafana-operator/) installed to manage datasources.
