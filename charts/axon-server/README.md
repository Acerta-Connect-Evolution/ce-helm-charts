# Axon Server

Copied from https://github.com/jdlabsco/axon-server-helm because ingress used an apiVersion that was no longer supported
on kubernetes 1.22

[Axon Server](https://axoniq.io/product-overview/axon-server) is a zero-configuration message router and event store for the open-source [Axon Framework](https://axoniq.io/product-overview/axon-framework) for event-driven microservices and domain-driven design.

This chart eases the deployment of the Axon Server in a single-instance or high-availability ([Axon Server Enterprise](https://axoniq.io/product-overview/axon-server-enterprise)).

## Important

We are in the early stages of releasing our Helm chart for Axon and are actively working on this chart. Consider this
repository as being in an "alpha" state.
We expect to do a clean-up prior to an eventual `1.0` release. If you use this repository, your feedback is welcomed and
you can open GitHub issues to ask for help or suggest improvements.

## Quickstart

First, add the Helm chart repository (provided through GitHub Pages with the help of [Chart Releaser](https://github.com/helm/chart-releaser)):

```
helm repo add axon https://jdlabsco.github.io/axon-server-helm/repo
```

Then install the chart:

```
helm upgrade --install axon-server axon/axon-server -f your-values-file.yaml
```

## Vendor installation documentation references

AxonIQ provide thorough installation documentation which was used to structure the stateful sets and other
Kubernetes resources.

* Standard edition (SE): [installation documentation](https://docs.axoniq.io/reference-guide/axon-server/installation/docker-k8s/axon-server-se#kubernetes)
* Enterprise edition (EE): [installation documentation](https://docs.axoniq.io/reference-guide/axon-server/installation/docker-k8s/axon-server-ee#kubernetes)
