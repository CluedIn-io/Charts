# Charts

This repository contains a collection of CluedIn Helm charts that can be used to install the CluedIn application into a Kubernetes cluster.

Information on Helm and how to use it can be found here: https://helm.sh/docs/intro/using_helm/

Current charts:

* CluedIn - The whole cluedin application + all dependant services.

## Using charts from the CluedIn chart repository

Before you can install the CluedIn chart you need to add the chart repository to your local collection so that Helm knows where to retrieve the chart from.

Adding the `cluedin` chart repository to your local repository collection.

```shell
$ helm repo add cluedin https://cluedin-io.github.io/Charts/
```

List all repositories currently installed.

```shell
$ helm repo list
```

## Examples of Helm usage

Search repositories for charts called `cluedin` in the chart repository and display the versions.

```shell
$ helm search repo cluedin
```

Search repositories for charts called `cluedin` but include pre-release/development versions of the charts.

```shell
$ helm search repo cluedin --devel
```

Installing the chart into a release called `cluedin` into the cluster.

```shell
$ helm install cluedin cluedin/cluedin
```

Installing with a custom `values.yaml`.

```shell
$ helm install cluedin cluedin/cluedin --values values.yaml
```

Installing a specific version of the chart.

```shell
$ helm install cluedin cluedin/cluedin --version 3.2.0
```

## Cleanup

Uninstall the `cluedin` release from the cluster.

```shell
$ helm uninstall cluedin
```

Remove `cluedin` repository from your local repository collection.

```shell
$ helm repo rm cluedin
```

