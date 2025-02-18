# Networking

### Overview

CloudLinker provides built-in networking capabilities to ensure secure and efficient traffic management within your Kubernetes clusters. Currently, the only supported ingress controller is **NGINX Ingress Controller**.

All ingress configurations can be set as either **public** or **private**, allowing you to control access to your services based on security requirements.

### Supported Providers

| **NGINX Ingress Controller** | A widely used and flexible ingress controller for managing HTTP(S) traffic into Kubernetes clusters. |
| ---------------------------- | ---------------------------------------------------------------------------------------------------- |

### Public vs. Private Ingress

* **Public Ingress**: Allows external access to services from the internet. Typically used for web applications, APIs, and externally accessible workloads.
* **Private Ingress**: Restricts access to internal networks only, ensuring that services are only reachable from within a VPN, VPC, or internal corporate network.

### Domains & SSL

One Certificate Issuer is associated per Ingress Controller to generate on-the-fly SSL Certificates with Let's Encrypt. For now, you can only associate one Certificate Issuer and so, have only one email for all the SSL Certificates.

### Configuration

When deploying a Backbone, CloudLinker automatically provisions **NGINX Ingress Controller** as the default ingress solution. You can define whether an ingress should be **public** or **private** based on your security needs.

### Future Expansions

Support for additional ingress controllers (such as Traefik, HAProxy, and cloud-native solutions) is planned in upcoming releases.
