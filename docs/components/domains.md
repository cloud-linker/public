# Domains

In CloudLinker, domains are essential for configuring and managing services deployed within your infrastructure. Each domain is associated with an **Ingress**, and the configuration of this domain triggers the setup of other important resources, such as the **Certificate Manager** for securing connections. Domains allow you to manage both public and private services easily, providing flexibility in how you expose and secure your services.

### **What is a Domain in CloudLinker?**

A **domain** in CloudLinker represents a fully qualified domain name (FQDN) associated with your infrastructure or application. It is the public address used by external users to access your services. CloudLinker uses domains to map incoming requests to specific services and to facilitate secure access via TLS certificates.

#### **Domain Structure**

A domain in CloudLinker is represented by the following structure:

```json
{
  "domain": "cloudlinker.brandonguigo.com",
  "ingress_id": "67b300266e01faed8f380658"
}
```

* **domain**: The fully qualified domain name (FQDN) that external users will use to access your services. For example, `"cloudlinker.brandonguigo.com"`.
* **ingress\_id**: The ID of the ingress installation inside your cluster.

### **Wildcard Domains for Service Flexibility**

In CloudLinker, you don't need to manually add wildcard characters like `*.`. Simply provide the domain you wish to use (e.g., `toto.fr`), and CloudLinker will automatically handle the configuration of wildcard subdomains for both private and public services.

#### **Example Wildcard Domains**

* **Public Domain**: If you provide a domain like `toto.fr`, CloudLinker will automatically configure it to manage all subdomains under this domain (e.g., `service.toto.fr`, `api.toto.fr`).
* **Private Domain**: For private services, you can use a domain like `internal.toto.fr`, and CloudLinker will automatically handle services under subdomains like `service1.internal.toto.fr` or `service2.internal.toto.fr`.

This way, you only need to provide the root domain (e.g., `toto.fr` or `toto.internal.fr`), and CloudLinker will ensure all subdomains are configured properly without any manual work from you.

### **Domain Setup Process**

When you add a domain in CloudLinker, the following steps occur:

1. **Ingress Configuration**: CloudLinker automatically associates the domain with an Ingress resource. The Ingress is responsible for handling external HTTP(s) traffic and routing it to the appropriate internal services based on the domain and paths defined in your configuration.
2. **Certificate Management**: Once the domain is associated with an Ingress, CloudLinker triggers the setup of the **Certificate Manager**. The Certificate Manager provisions a TLS certificate to secure traffic for the domain, enabling HTTPS access.
3. **Resource Creation**: Other necessary resources (e.g., DNS records, firewall rules, etc.) are automatically set up as part of the domain setup process, assuming your domain registrar is properly configured. These resources ensure that the domain is properly configured and accessible.

#### **Automatic DNS Record Updates**

CloudLinker supports automatic updates to your **DNS records** if your **domain registrar** is configured. This means that once a domain is added, CloudLinker will automatically update the required DNS records (such as A or CNAME records) to point to the correct ingress controllers, making your domain accessible without the need for manual DNS configuration.

#### **Automatic TLS/SSL Certificate Provisioning**

CloudLinker uses the **Certificate Manager** to automatically manage TLS certificates for your domains. Upon domain creation, the Certificate Manager will request, renew, and configure certificates for secure communication over HTTPS.

#### **Key Features of Domain Management**

* **Secure HTTPS Access**: With the integration of Certificate Manager, all traffic to your domain is encrypted via TLS, ensuring security for your users.
* **Wildcard Support**: Easily manage multiple services under both private and public domains with wildcard domain support, without the need for manual wildcard configuration.
* **Automated Setup**: Domains are automatically linked to Ingress and Certificate Manager resources, minimizing manual configuration and reducing the chance of errors.
* **Scalability**: CloudLinker’s domain management system scales with your infrastructure, automatically handling additional domains and certificates as your services grow.

### **Adding a Domain to CloudLinker**

To add a new domain to your CloudLinker setup, follow these steps:

1. **Configure DNS Registrar**: Ensure that your domain registrar is configured to allow CloudLinker to manage your DNS records. This typically involves setting up API keys or access credentials for CloudLinker to make changes to your DNS settings.
2. **Add the Domain**: Use the CloudLinker CLI or dashboard to associate the domain with an Ingress. This will trigger the automatic creation of the necessary resources, including DNS record updates if your registrar is configured.
3. **Verify Setup**: After the domain is added, verify that the domain resolves correctly and that HTTPS is working by visiting the domain in your browser.

#### Example:

Here’s an example JSON structure for adding a domain to CloudLinker:

```json
{
  "domain": "toto.fr",
  "ingress_id": "ac58f3b2c19c72ef0d9374ea"
}
```

In this example, `toto.fr` is the public domain, and any subdomain (e.g., `service.toto.fr`) will be automatically managed by CloudLinker.

For a private service, you might use a domain like:

```json
{
  "domain": "internal.toto.fr",
  "ingress_id": "ac58f3b2c19c72ef0d9374ea"
}
```

Here, CloudLinker will automatically handle subdomains like `service1.internal.toto.fr` and `service2.internal.toto.fr` without any need for you to manually configure them.

### **Why Domains Are Key for Stable Infrastructure**

* **Routing and Load Balancing**: Domains serve as the entry points for all external traffic. By associating each domain with an Ingress, CloudLinker ensures that traffic is routed correctly to the right service, helping balance load and ensuring reliable performance.
* **Security**: With automatic TLS certificate provisioning via the Certificate Manager, CloudLinker ensures that all communication is secure, preventing eavesdropping and man-in-the-middle attacks.
* **Simplified Management**: Associating each domain with an Ingress and automatically provisioning the necessary resources reduces manual overhead and simplifies the management of multiple domains and services.

### **Conclusion**

Domains in CloudLinker are a fundamental component of infrastructure management, serving as the link between users and your services. With automatic configuration of Ingress resources, DNS record updates (via your registrar), wildcard domain support, and TLS certificates, CloudLinker simplifies domain management and enhances security. Whether you are adding a single domain, deploying multiple services, or scaling up your infrastructure with both private and public domains, CloudLinker provides the tools to manage them with ease and confidence.

For any issues or further assistance, consult the CloudLinker support documentation or contact the support team.
