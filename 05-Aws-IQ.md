🌐 VPC / Networking --- Continued

### 43. What is VPC?

A **Virtual Private Cloud (VPC)** is a **logically isolated network**
environment inside **AWS** where you launch your **resources**. It works
like your own **private data center** in the cloud, where you control
**IP ranges**, **routing**, and **security settings**.

Within a VPC, you define **subnets**, **gateways**, **routing rules**,
and **security controls** to structure how resources communicate. This
allows organizations to separate **application layers** such as
**frontend**, **backend**, and **databases**.

Using a VPC improves **security**, **traffic control**, and
**architecture flexibility**. For example, sensitive systems can run in
**private subnets** while **public-facing services** remain accessible
externally.

In real **DevOps scenarios**, **VPC design** is critical for **network
segmentation**, **compliance**, and **scalability**, ensuring resources
operate securely and efficiently.

------------------------------------------------------------------------

### 44. What Components Exist Inside a VPC?

A **VPC** includes several **components** that work together to manage
**connectivity**.

The main elements include **subnets** for **resource placement**,
**route tables** for **traffic direction**, **internet or NAT gateways**
for **external access**, and **security controls** such as **security
groups** and **NACLs**.

Each component has a defined **responsibility**. Subnets organize
**infrastructure tiers**, gateways control **internet connectivity**,
and security layers filter **traffic**.

Understanding these components helps engineers design **secure** and
**reliable cloud networks** that meet **application needs**.

------------------------------------------------------------------------

### 45. What is a Subnet?

A **subnet** is a subdivision of a **VPC network** that isolates
resources into smaller **segments**.

Subnets define how resources interact with the **internet** and other
systems. They help organize infrastructure logically and enforce
**security boundaries**.

For example, **application servers** might be placed in one subnet,
while **databases** remain in another for protection.

This segmentation improves **traffic control**, **security**, and
**scalability**, making it easier to manage **complex deployments**.

------------------------------------------------------------------------

### 51. What is a Route Table in VPC?

A **route table** defines how **network traffic** is directed within a
**VPC**.

It contains **rules** mapping **destinations** to **gateways or
targets**. Each **subnet** is associated with a route table that
controls **packet flow**.

For example, traffic destined for the **internet** might be sent to an
**internet gateway**.

Proper **routing** ensures **connectivity** while maintaining **security
isolation** between components.

------------------------------------------------------------------------

### 52. How Routing Decisions Are Made?

Routing decisions occur when **traffic** is evaluated against **route
table rules**.

The most **specific matching rule** determines where the traffic goes.

This process ensures **efficient data flow** across resources.

Misconfigured routing can lead to **connectivity failures**, making
proper **planning** and **monitoring** important.

------------------------------------------------------------------------

### 53. What is VPC Peering?

**VPC peering** connects two **VPC networks** privately.

This enables **secure communication** without sending traffic across the
**internet**.

It is used for connecting **environments**, sharing **services**, or
enabling **multi-account architectures**.

However, **routing** must be configured carefully and **overlapping
address ranges** must be avoided.

------------------------------------------------------------------------

### 54. When Do You Use VPC Peering?

Peering is useful when **applications** across different **VPCs** need
direct communication.

Examples include integrating **microservices** across environments or
connecting **staging** and **production systems**.

It improves **performance** and **security** compared to **public
networking methods**.

Understanding when to use peering helps design **scalable distributed
systems**.

------------------------------------------------------------------------

### 55. How Do You Control Security Inside VPC?

Security is enforced through multiple **layers**.

**Security groups** protect individual resources, while **NACLs**
control **subnet-level traffic**.

**IAM roles** restrict **administrative actions**, and **subnet design**
isolates workloads.

This layered approach follows the **defense-in-depth strategy**,
ensuring strong **protection** across infrastructure.

------------------------------------------------------------------------

### 58. NACL vs Security Groups

**NACLs** operate at **subnet level** and are **stateless**, while
**security groups** operate at **resource level** and are **stateful**.

NACLs provide **coarse filtering**, while security groups offer
**precise control**.

Using both creates **layered network defense**.

------------------------------------------------------------------------

### 59. How Do You Troubleshoot VPC Connectivity?

Troubleshooting involves checking **routing**, **security rules**,
**subnet configurations**, and **logs**.

Identifying **misconfigurations** step by step helps locate issues.

**Monitoring tools** provide visibility into **network behavior**.

Systematic analysis ensures **quick resolution** of connectivity
problems.

------------------------------------------------------------------------

### 60. What is ALB?

An **Application Load Balancer (ALB)** distributes **HTTP** and **HTTPS
traffic**.

It supports **advanced routing decisions** based on **request details**.

It improves **availability** by balancing requests across **multiple
targets**.

This ensures **scalable application performance**.

------------------------------------------------------------------------

### 62. How Load Balancing Works Internally?

Incoming **traffic** is distributed across resources based on
**algorithms**.

**Health checks** ensure only **available resources** receive requests.

This prevents **overload** and maintains **responsiveness**.

It also supports **scaling**.

------------------------------------------------------------------------

### 63. Health Checks in Load Balancer

**Health checks** monitor **resource availability**.

**Unhealthy instances** are removed automatically.

This improves **service reliability**.

Monitoring ensures traffic reaches **healthy targets**.

------------------------------------------------------------------------

### 64. TLS Termination at ALB

**TLS termination** decrypts traffic at the **load balancer**.

This reduces **backend workload** and centralizes **certificate
management**.

It enhances **security** and **efficiency**.

------------------------------------------------------------------------

### 65. How Do You Isolate Environments Using VPC?

Isolation is achieved through separate **subnets** or **VPCs**.

Different **routing** and **policies** restrict access.

This prevents **cross-environment impact**.

It ensures **deployment safety**.

------------------------------------------------------------------------

### 66. How Do You Monitor VPC Traffic?

**Monitoring tools** provide visibility into **network flow**.

**Logs** capture **traffic metadata**.

**Alerts** detect **anomalies**.

This enables **proactive security** and **performance management**.
