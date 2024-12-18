# ClickhouseDB Helm Chart

This chart deploys ClickhouseDB to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage in Teknoir platform
Use the HelmChart to deploy the ClickhouseDB to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: clickhouse
  namespace: default
spec:
  repo: https://teknoir.github.io/clickhouse-helm
  chart: clickhouse
  targetNamespace: default
  valuesContent: |-
    # Example for minimal configuration
    
```

## Adding the repository

```bash
helm repo add teknoir-clickhouse https://teknoir.github.io/clickhouse-helm/
```

## Installing the chart

```bash
helm install clickhouse teknoir-clickhouse/clickhouse -f values.yaml
```