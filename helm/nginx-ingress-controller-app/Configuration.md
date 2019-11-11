# nginx-ingress-controller

This chart installs nginx-ingress-controller and its dependencies as managed applications. An Ingress Controller is a daemon, deployed as a Kubernetes Pod, that watches the apiserver's /ingresses endpoint for updates to the Ingress resource. Its job is to satisfy requests for Ingresses.


## Configuration

The following table lists the configurable parameters of the nginx-ingress-controller chart, its dependencies and default values.

Parameter | Description | Default
--- | --- | ---
`baseDomain` | Cluster base domain. Dynamically calculated during cluster creation. Manual change doesn't affect this value | 'aws'
`provider` | Provider identifier (`aws`/`azure`/`kvm`) | 'kvm'
`configmap.ingress-class` | Ingress class, which controller processes | `nginx`
`controller.service.enabled` | If true, create service | `true`
`controller.service.type` | Applies only to `provider=aws` (`external`/`internal`) | `external`