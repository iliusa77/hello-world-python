# Hello, World (Python/Flask)

This is a Python/Flask template for building a microservice in Kubernetes and Docker. This template is designed for use with [Forge](https://forge.sh), [Telepresence](https://www.telepresence.io), and [Ambassador](https://www.getambassador.io).

# Repository structure

The main files in this repository are:

* `Dockerfile` specifies how the application is built and packaged
* `k8s/deployment.yaml` contains a templated Kubernetes manifest, with additional annotations for configuring Ambassador
* `service.yaml` contains values (typically configured by a developer) that will be instantiated into the Kubernetes manifest
* `app.py` is the actual Python/Flask application

# Helm chart
Enable ingress controller Nginx (minikube)
```
minikube addons enable ingress
```

Installation
```
cd k8s/helm
helm upgrade hello-world-python hello-world-python/ --install --namespace hello-world-python --create-namespace
```

Removing
```
helm del hello-world-python --namespace hello-world-python
```


# License

Licensed under Apache 2.0. Please see [LICENSE](LICENSE) for details.

# Tilt
```
tilt up
```

Open in browser http://localhost:10350/
![alt text](tilt.png)
