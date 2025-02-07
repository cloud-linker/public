# Overview

### **What is a Cluster?**

A **Cluster** in CloudLinker is a **private Kubernetes cluster** that resides within a **Backbone**. It forms the core infrastructure for hosting and running containerized applications in a **secure, scalable, and production-grade environment**. Each cluster is designed to support not just infrastructure management, but also the collaboration tools needed by your team.

### **Key Characteristics**

✅ **Private by Default** – All clusters are private with no public IPs, ensuring complete isolation and security.\
✅ **Backbone-Integrated** – Every cluster is deployed inside a Backbone, inheriting its robust network, security, and VPN configurations.\
✅ **Standalone or Peered** – Clusters can function as standalone environments, or can be peered with other clusters for advanced use cases.\
✅ **Cross-Cloud Peering** – Clusters can communicate securely across different Backbones, even within separate cloud providers.\
✅ **Automated Scaling & High Availability** – CloudLinker clusters are optimized to scale automatically based on demand, ensuring performance at all times.\
✅ **Comprehensive Tooling** – Inside each cluster, you have everything needed to operate both the infrastructure and your applications, as well as tools to collaborate as a company.

### **Deployment Flexibility**

#### **1. Standalone Clusters**

* A **self-contained** environment for isolated workloads, independent applications, or single projects.
* Ideal for simpler use cases that don’t require inter-cluster communication.

#### **2. Peered Clusters (Future-Ready)**

* Multiple clusters can be **connected** securely within the same Backbone.
* **Cross-Backbone peering** allows clusters to communicate seamlessly, even across different cloud providers, to create a distributed and interconnected infrastructure.

### **The Complete Cluster Experience**

Inside each CloudLinker cluster, you not only get the necessary components to operate your infrastructure and applications, but also the tools your team needs to collaborate and manage the business:

* **Infrastructure Tools**: Everything needed to manage Kubernetes, scaling, monitoring, and security.
* **Application Tools**: Easily deploy, manage, and scale your apps across the cluster.
* **Company Collaboration Tools**: Integrated **virtual workspace**, **video/audio meetings**, **chat (Zulip - Slack alternative)**, and other communication tools to keep your team connected and productive.

### **How Clusters Fit Into CloudLinker**

1️⃣ **The Backbone is created first**, defining the secure networking and security policies.\
2️⃣ **Clusters are deployed inside the Backbone**, which provides networking, security, and automation to the cluster.\
3️⃣ **Clusters can operate independently**, or they can be **peered** across different cloud environments, enabling complex, cross-cloud architectures.\
4️⃣ **Collaboration tools** are seamlessly integrated, so your teams can work efficiently while managing infrastructure.
