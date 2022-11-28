# ce-helm-charts 
 
![Release Charts](https://github.com/Acerta-Connect-Evolution/ce-helm-charts/workflows/Release%20Charts/badge.svg?branch=main)

GitHub Pages-powered Helm repository for charts needed by Connect Evolution.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.
Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Once Helm is set up properly, add the repo as follows:
```console
helm repo add ce-helm https://acerta-connect-evolution.github.io/ce-helm-charts
```

You can then run `helm search repo ce-helm` to see the charts.

## Custom images

We defined some custom images that the charts refer to. They can be found in [ce-images](https://github.com/Acerta-Connect-Evolution/ce-images).

## Tip: Linting a chart

Useful when checking the syntactical correctness of a chart:

```console
helm lint .\keycloak-boot\
```
