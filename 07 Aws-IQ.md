### 76. What is Amazon EKS and why would you use it instead of self-managed Kubernetes?

**Amazon Elastic Kubernetes Service (EKS)** is a **managed Kubernetes
platform** provided by **AWS**, designed to simplify running
**containerized applications at scale**. **Kubernetes** itself is
powerful but requires managing **control plane components**, **security
updates**, and **high availability** when self-hosted.

With **EKS**, AWS manages the **orchestration layer**, including
**scheduling** and **cluster coordination**, which reduces **operational
burden**. Teams can focus on **deploying applications** instead of
maintaining **infrastructure**.

EKS also integrates directly with **AWS services** like **networking**
and **identity management**, enabling **secure** and **scalable
architecture design**. Organizations choose it because it provides
**reliability**, **automation**, and **reduced maintenance overhead**
compared to running Kubernetes manually.

This balance of **flexibility** and **operational simplicity** makes it
suitable for **production container workloads**.

------------------------------------------------------------------------

### 77. Explain EKS Architecture and its Components

**EKS architecture** is composed of a **managed control plane** and
**worker nodes**.

The **control plane** is responsible for **cluster management** and
**scheduling**. **Worker nodes** execute **application containers** and
communicate with the control plane for instructions.

**Networking components** allow communication across resources, while
**identity mechanisms** ensure **secure permissions management**.

This separation ensures **stability** because AWS maintains the
**orchestration layer** while users manage **application execution**.

Understanding architecture helps engineers **operate**, **scale**, and
**troubleshoot workloads** effectively.

------------------------------------------------------------------------

### 78. How does AWS manage the control plane in EKS?

AWS fully manages the **control plane infrastructure** behind the
scenes. It ensures **availability** by distributing components across
multiple **infrastructure zones**.

AWS handles **patching**, **scaling**, and **monitoring** automatically,
reducing **operational responsibility**.

This ensures the cluster remains **stable** and **secure** without
manual intervention.

Managed orchestration allows teams to focus on **application lifecycle**
rather than **infrastructure health**.

------------------------------------------------------------------------

### 79. Difference between EKS and ECS

**EKS** uses **Kubernetes orchestration**, enabling **compatibility with
open-source tools** and **portability**.

**ECS** is **AWS-native** and tightly integrated with AWS services,
offering **simplicity** and easier setup.

Choosing depends on **flexibility needs** versus **simplicity goals**.
Kubernetes-based workflows use EKS, while AWS-centric deployments may
prefer ECS.

Understanding both helps design suitable **container strategies**.

------------------------------------------------------------------------

### 80. How do worker nodes join an EKS cluster?

**Worker nodes** join by **registering with the control plane** during
initialization.

**Configuration instructions** enable communication between nodes and
orchestration services. Once registered, nodes receive **scheduling
instructions** and run workloads.

This automated process supports **cluster scalability** and **dynamic
resource allocation**.

It ensures workloads expand efficiently without **manual
configuration**.

------------------------------------------------------------------------

### 81. What is IAM Role for Service Account (IRSA)?

**IAM Roles for Service Accounts (IRSA)** allow **Kubernetes workloads**
to securely access **AWS services** without embedding credentials.

A **service account** maps to an **IAM role** that provides **temporary
permissions**.

When a pod uses that service account, AWS grants **access tokens
automatically**, improving **security** and enabling **fine-grained
access control**.

IRSA is widely used for accessing **storage**, **databases**, or
**messaging services** safely.

------------------------------------------------------------------------

### 82. How does networking work in EKS?

Networking relies on **AWS VPC infrastructure**. **Pods receive IP
addresses** from the VPC and communicate using **native networking
rules**.

**Security groups** and **routing configurations** control **traffic
flow** and isolate workloads.

This integration enables **high performance** and consistent
connectivity with **AWS services**.

Proper design ensures **reliable communication** between components.

------------------------------------------------------------------------

### 83. How do you expose services externally in EKS?

External exposure uses **load balancers** or **ingress controllers**.

Traffic routes through **managed entry points** before reaching
workloads.

**Routing rules** provide **access control** and **scalability**.

This allows **secure interaction** between users and backend services.

------------------------------------------------------------------------

### 84. How do you scale pods in EKS?

Scaling uses **Horizontal Pod Autoscaling** based on **performance
metrics**.

When usage increases, **additional pods launch**. When it decreases,
**pods terminate**.

This dynamic adjustment maintains **performance** and optimizes
**resource consumption**.

Scaling supports **unpredictable workload patterns**.

------------------------------------------------------------------------

### 85. How do you upgrade an EKS cluster safely?

Safe upgrades involve **staged planning** and **testing**.

**Control plane updates** are AWS-managed, while **worker nodes**
require coordinated replacement.

**Rolling updates** maintain **application continuity**.

Validation prevents **downtime** and ensures **compatibility**.

------------------------------------------------------------------------

### 86. How do you manage secrets in EKS?

**Secrets** are stored securely and injected into workloads when needed.

**Access controls** restrict visibility.

Secure handling protects **credentials** and **sensitive data**.

Proper management is fundamental for **system security**.

------------------------------------------------------------------------

### 87. How does auto scaling work with EKS nodes?

**Node auto scaling** adjusts **infrastructure capacity dynamically**.

Additional nodes launch when **demand rises**, and terminate when it
drops.

This maintains **efficiency** and prevents **resource waste**.

Dynamic scaling supports **fluctuating workloads**.
