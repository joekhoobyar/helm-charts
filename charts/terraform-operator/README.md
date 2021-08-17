# terraform-operator

![Version: v0.1.17](https://img.shields.io/badge/Version-v0.1.17-informational?style=flat-square) ![AppVersion: v0.3.10](https://img.shields.io/badge/AppVersion-v0.3.10-informational?style=flat-square)

A Helm chart to deploy the terraform-operator Controller and CRD.

## TL;DR;

```console
$ helm repo add isaaguilar https://isaaguilar.github.io/helm-charts
$ helm install isaaguilar/terraform-operator --namespace tf-system
```

## Upgrading the Custom Resource Definition

Helm does not have support at this time for upgrading or deleting CRDs. Instead, update CRDs manually by running

```
kubectl apply -f crds/terraform.yaml
```

## Values

| Key | Description | Default |
|---|---|---|
| controller.affinity | `object` node/pod affinities | `{}` |
| controller.args | `list` additional arguments for the command | <a href="values.yaml#L22-L24">values.yaml</a> |
| controller.enabled | `bool` deploy the terraform-operator controller | `true` |
| controller.environmentVars | `object` key/value envs | `{}` |
| controller.image.pullPolicy | `string`  Set how kubernetes determines when to pull the docker image. | `"Always"` |
| controller.image.repository | `string` repo name without the tag | `"isaaguilar/terraform-operator"` |
| controller.image.tag | `string` tag of the image | `"v0.3.10"` |
| controller.nodeSelector | `object` node labels for pod assignment | `{}` |
| controller.replicaCount | `int` number of replicas | `1` |
| controller.resources | `object` CPU/Memory request and limit configuration | <a href="values.yaml#L28-L34">values.yaml</a> |
| controller.tolerations | `list` List of node taints to tolerate | `[]` |
