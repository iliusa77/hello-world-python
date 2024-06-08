docker_build("iliusa77/hello-world-python", ".")
k8s_yaml("k8s/deployment.yaml")
k8s_resource("hello-world-python-deployment", port_forwards='8080:8080')