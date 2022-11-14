- [Nginx Unit + Static Files Helm Chart](#nginx-unit--static-files-helm-chart)
  - [Requirements](#requirements)
  - [Installation](#installation)
    - [Healthchecks](#healthchecks)

# Nginx Unit + Static Files Helm Chart

Containerize & Orchestrate your static websites with this simple Helm chart

## Requirements

- Kubernetes v1.22+

## Installation

To create a Nginx Unit + Static Files project image for Docker, head over to [jd1378/static-serve-demo](https://github.com/jd1378/static-serve-demo) to get started. The Dockerfile differs based on the project you want to deploy, and there you will find a demo application to run to understand the basics.

Install the Helm chart repository:

```bash
helm repo add jd1378 https://jd1378.github.io/helm-charts
helm repo update
```

Install Nginx Unit + Static Files chart:

```bash
$ helm upgrade static-webapp \
    --install \
    --version=1.0.0 \
    jd1378/static-serve
```

Check `values.yaml` for additional available customizations.

### Healthchecks

Healthchecks are set up and enabled for `/health` on the container on the `/` path by default.
