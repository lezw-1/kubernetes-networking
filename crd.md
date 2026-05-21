# Custom Resource Definitions (CRDs)

All CRDs in this project come from the Envoy Gateway helm chart (`gateway-helm` v1.4.0, `oci://docker.io/envoyproxy`) and are installed via the `charts/gateway-controller` chart.

## Envoy Gateway CRDs

| CRD Name | Kind | Group | Version | Scope |
|---|---|---|---|---|
| `backends.gateway.envoyproxy.io` | `Backend` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |
| `backendtrafficpolicies.gateway.envoyproxy.io` | `BackendTrafficPolicy` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |
| `clienttrafficpolicies.gateway.envoyproxy.io` | `ClientTrafficPolicy` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |
| `envoyextensionpolicies.gateway.envoyproxy.io` | `EnvoyExtensionPolicy` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |
| `envoypatchpolicies.gateway.envoyproxy.io` | `EnvoyPatchPolicy` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |
| `envoyproxies.gateway.envoyproxy.io` | `EnvoyProxy` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |
| `httproutefilters.gateway.envoyproxy.io` | `HTTPRouteFilter` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |
| `securitypolicies.gateway.envoyproxy.io` | `SecurityPolicy` | `gateway.envoyproxy.io` | `v1alpha1` | Namespaced |

## External CRDs (installed by other controllers)

These resources are used in `charts/gateway/templates/` but their CRDs are managed by separate controllers:

| Kind | CRD Source | Controller |
|---|---|---|
| `Gateway` | Kubernetes Gateway API | gateway.networking.k8s.io |
| `ClusterIssuer` | cert-manager | cert-manager.io |
| `Certificate` | cert-manager | cert-manager.io |
