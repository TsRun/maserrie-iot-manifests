# maserrie-iot-manifests

Manifests deployed by Argo CD for Inception-of-Things, part 3.

| File | Role |
| --- | --- |
| `deployment.yaml` | the `playground` application, 1 replica, port 8888 |
| `service.yaml` | ClusterIP service in front of it |
| `ingress.yaml` | exposes it on the cluster ingress |

Argo CD watches this repository and keeps the `dev` namespace in sync with it.
Changing the image tag here is enough to roll out a new version.
