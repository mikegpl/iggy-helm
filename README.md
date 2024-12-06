![Helm: v3](https://img.shields.io/static/v1?label=Helm&message=v3&color=informational&logo=helm)

# iggy-helm
Official Helm chart for Iggy.rs

## Installing the chart

Export default values of `iggy-rs` chart to file `values.yaml`:


```console
helm show values iggy-rs-1.0.tgz > values.yaml
```

Change the values according to the need of the environment in ``values.yaml`` file.

Test the installation with command:

```console
helm install iggy-rs iggy-rs-1.0.tgz -f values.yaml -n NAMESPACE --debug --dry-run
```


Install chart with command:

```console
helm install iggy-rs iggy-rs-1.0.tgz -f values.yaml -n NAMESPACE
```

## Validate installation

Get the pods lists by running these commands:

```console
kubectl get pods -A | grep 'iggy-rs'

# or list all resorces of victoria-metrics

kubectl get all -n NAMESPACE | grep iggy
```

Get the application by running this commands:

```console
helm list -f iggy-rs -n NAMESPACE
```

See the history of versions of ``iggy-rs`` application with command.

```console
helm history iggy-rs -n NAMESPACE
```

## How to uninstall IggyRs

Remove application with command.

```console
helm uninstall iggy-rs -n NAMESPACE
```

## Kubernetes compatibility versions

Supported versions

| Kubernetes version | Supported |
| ------------------ | --------- |
| 1.30               | Yes       |
