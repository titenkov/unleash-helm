# unleash-helm

[Unleash](https://github.com/Unleash/unleash) is a open source feature flag & toggle system, that gives you a great overview over all feature toggles across all your applications and services. It comes with official client implementations for Java, Node.js, Go, Ruby, Python and .NET Core.

## Introduction

This chart bootstraps a [Unleash](https://github.com/Unleash/unleash) deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.12+
- Helm 2.11+ or Helm 3.0+

## Chart

The current chart config contains a basic deployment template in the `templates` directory. 

The `values.yaml` contains the default values for the chart.
The `requirements.yaml` contans the dependency on the [Postgresql](https://github.com/bitnami/charts/tree/master/bitnami/postgresql).

To modify the Unleash version used in this chart you can specify a [valid image tag](https://hub.docker.com/r/unleashorg/unleash-server/tags/) using the `image.tag` parameter. For example, `image.tag=3.2` or update it in the `values.yaml` file.

## Setup

You need to be connected to a kubernetes cluster, which is either running locally (f.e. `minikube`) or remotely.

You also need to have `helm` installed ([installation guide](https://helm.sh/docs/intro/install/)).

## Installing the Chart
To install the chart with the release name `unleash`, run the following command in the root of the project:

```console
$ helm install unleash .
```

The command deploys Unleash on the Kubernetes cluster in the default configuration

> **Tip**: List all releases using `helm ls`

## Uninstalling the Chart

To uninstall/delete the `unleash` deployment:

```console
$ helm delete unleash
```

The command removes all the Kubernetes components associated with the chart and deletes the release.
