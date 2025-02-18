# Certificate Manager

### Overview

Cert-Manager is a Kubernetes add-on that automates the management and issuance of TLS certificates. It integrates with **Let's Encrypt** to provide automatic HTTPS security for applications deployed in CloudLinker.

### How It Works

* Cert-Manager automatically requests and renews certificates for services exposed via Kubernetes Ingress.
* It uses **Let's Encrypt** as the default Certificate Authority (CA) to issue free, publicly trusted certificates.
* Certificates are generated and managed dynamically, ensuring secure communication for all exposed endpoints.

### Current Limitations

* **Single Certificate Issuer per Ingress**: Each ingress can only be associated with one certificate issuer.
* **Single Email for All Certificates**: Only one email address can be used for all certificates issued through the ingress.

### Deployment in CloudLinker

CloudLinker integrates Cert-Manager seamlessly to provide hassle-free SSL/TLS management. With automatic provisioning and renewal, users do not need to manually request or update certificates.
