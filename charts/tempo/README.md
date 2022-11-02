# Grafana Tempo

![Version: 0.16.3](https://img.shields.io/badge/Version-0.16.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.5.0](https://img.shields.io/badge/AppVersion-1.5.0-informational?style=flat-square)

Is a patched version of official chart <https://github.com/grafana/tempo>, release 0.16.3.

[service.yaml](./templates/service.yaml) now contains 2 services instead of just 1:
* one for the main (grpc 4317); type LoadBalancer so that it can be exposed to the outside world without having to use NGINX
* one for the query api (3100); type ClusterIP; can be exposed via NGINX ingress 

Reason: when using the LoadBalancer service type, you can only expose a SINGLE port/protocol. So I created a SEPARATE Service and removed all other ports from it.

