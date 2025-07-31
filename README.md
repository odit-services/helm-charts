# helm-charts

A collection of different helm charts we created for ourselves or upon customers' request.

Charts can be pulled via:

- HTTPS: `helm repo add odit https://odit-services.github.io/helm-charts/`

## Charts

### App with Autoupdate (through Flux) and Traefik Ingress

A simple helm chart that deploys your stateless application with an autoupdate feature through FluxCD and ingress via Traefik with Cert-Manager TLS certificates.

```shell
helm repo add odit https://odit-services.github.io/helm-charts/
helm upgrade --install myapp odit/app-with-autoupdate-and-traefik-ingress \
  --set image.repository=nginx \
  --set image.tag=latest
```
