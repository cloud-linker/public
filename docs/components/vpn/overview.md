# Overview

### **What is the VPN Integration?**

A **VPN** (Virtual Private Network) integration is required to access and configure your CloudLinker infrastructure before it can serve any public-facing platform. This adds an extra layer of security to ensure that only authorized users can manage and interact with the infrastructure, protecting sensitive data and configurations.

### **VPN Requirements**

* **One VPN integration is mandatory**: A VPN integration is necessary for every CloudLinker deployment to enable secure access and configuration.
* **Secure Access to Clusters**: The VPN is used to access your **Kubernetes clusters** and configure them privately.
* **Access Control**: **RBAC (Role-Based Access Control)** is enforced to ensure only authorized personnel have access to manage your infrastructure.

### **Supported VPN Providers**

| **Feature**                 | **Twingate**                                                        |
| --------------------------- | ------------------------------------------------------------------- |
| **RBAC Support**            | ✔️ Role-Based Access Control for detailed, secure user permissions. |
| **Strong Security**         | ✔️ Enterprise-grade security for cloud infrastructure.              |
| **Cost-Effective**          | ✔️ Free or low-cost plans for companies of all sizes.               |
| **Easy Setup**              | ✔️ Simplified integration process.                                  |
| **Cross-Cloud Integration** | ✔️ Define Remote Networks & Resources for each provider             |
| **Scalability**             | ✔️ Supports scaling to accommodate growing infrastructure.          |
| **VPN Protocols Supported** | ✔️ IPsec, SSL, etc.                                                 |

### **How the VPN Works**

1️⃣ **Twingate Integration**: Once you set up Twingate, it establishes a secure connection between your local environment and the CloudLinker infrastructure.\
2️⃣ **Accessing the Cluster**: Use the VPN to securely access your CloudLinker infrastructure and configure your Kubernetes clusters, ensuring that no public exposure occurs during setup.\
3️⃣ **Securing the Entire Workflow**: With VPN access, your team can securely interact with both the infrastructure and the internal collaboration tools (e.g., monitoring, management, etc.) without the risk of exposure to the public network.
