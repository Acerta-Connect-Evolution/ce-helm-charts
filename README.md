# ce-helm-charts

![Release Charts](https://github.com/Acerta-Connect-Evolution/ce-helm-charts/workflows/Release%20Charts/badge.svg?branch=main)

GitHub Pages-powered Helm repository for charts needed by Connect Evolution.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.
Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Helm charts are stored on Harbor using oci.
https://harbor.toolsstg.acerta.io/
https://harbor.tools.acerta.io/

examples:
helm pull oci://harbor.toolsstg.acerta.io/acerta-snapshots/connect-evolution
helm show chart oci://harbor.tools.acerta.io/acerta-releases/connect-evolution

## Custom images

We defined some custom images that the charts refer to. They can be found in [ce-images](https://github.com/Acerta-Connect-Evolution/ce-images).

## Tip: Validating a chart up front

Check the syntactical correctness of a chart before publishing it. E.g., for chart 'keycloak-boot':

```console
# test rendering chart template locally
helm template --debug .\charts\keycloak-boot\

# let the server decide if the chart is valid
helm install --dry-run --debug keycloak-boot .\charts\keycloak-boot\

# are best-practices followed?
helm lint .\charts\keycloak-boot\
```
