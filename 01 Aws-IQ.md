# Cloud & AWS Interview Notes (Highlighted)

## 1. What is Cloud Computing?

Cloud computing means using **computing services like servers, storage,
databases, and networking over the internet** instead of maintaining
physical hardware locally.

Instead of buying and managing your own servers, you **rent resources
from cloud providers like AWS and pay only for what you use**. This
makes systems **scalable, flexible, and cost-effective**.

Cloud computing allows teams to **deploy applications faster**, **scale
automatically based on demand**, and improve reliability because
infrastructure is **distributed across multiple locations**.

There are also benefits like **high availability**, **disaster recovery
options**, and **reduced operational overhead** since the provider
manages hardware maintenance.

In real-world DevOps work, cloud computing enables **automation**,
**CI/CD pipelines**, **container deployments**, and **infrastructure as
code**, which significantly speeds up delivery and improves consistency.

------------------------------------------------------------------------

## 2. What is AWS?

AWS, or Amazon Web Services, is a **cloud platform that provides
on-demand infrastructure and services over the internet**.

It offers services for **computing, storage, networking, databases,
security, analytics, and DevOps automation**. Instead of managing
physical servers, we launch resources like **EC2 instances** or storage
like **S3** within minutes.

AWS operates on a global infrastructure model with **regions and
availability zones**, which helps build **highly available and
fault-tolerant applications**.

From a DevOps perspective, AWS integrates well with **automation tools,
CI/CD pipelines, monitoring, and Kubernetes**.

Overall, AWS allows organizations to **scale quickly**, **optimize
costs**, and **focus on application development**.

------------------------------------------------------------------------

## 3. What are IaaS, PaaS, and SaaS?

These are cloud service models that define **how much responsibility you
manage versus the provider**.

**IaaS --- Infrastructure as a Service**\
You control **virtual machines, storage, and networking** while the
provider manages hardware.\
Example: **AWS EC2**\
Used when you need **full control of environment setup**.

**PaaS --- Platform as a Service**\
Provider manages infrastructure and runtime environment, and you focus
on **application deployment**.\
Example: **Elastic Beanstalk**\
This reduces operational work and **speeds development**.

**SaaS --- Software as a Service**\
You simply use the application through a browser.\
Example: **Gmail or Salesforce**\
No infrastructure or platform management required.

Understanding these helps choose the right level of **control vs
convenience**.

------------------------------------------------------------------------

## 4. What is EC2?

Amazon EC2 is a compute service that provides **virtual servers in the
cloud**.

It allows launching instances with **different CPU, memory, and storage
configurations**. You can install applications, run services, or host
websites just like physical servers.

EC2 supports scaling using **Auto Scaling groups** and integrates with
**load balancers** for traffic distribution.

It offers pricing models like **On-Demand, Reserved, and Spot** to
optimize costs.

Used for **application hosting, CI/CD runners, container nodes, or
custom workloads** with full OS control.

------------------------------------------------------------------------

## 5. What are Key Pairs?

Key pairs are used for **secure login to EC2 instances**.

They consist of a **public key stored by AWS** and a **private key
stored by the user**. AWS verifies access using **cryptographic
authentication instead of passwords**.

This improves security and prevents **brute force attacks**.

If the private key is lost, accessing the instance becomes difficult, so
**key management and backups are important**.

------------------------------------------------------------------------

## 6. What is an AMI?

An Amazon Machine Image (AMI) is a **template used to launch EC2
instances**.

It contains the **operating system, installed software, configurations,
and permissions**.

Custom AMIs ensure **consistent deployments** and reduce setup time.

AMI versioning supports **immutable deployments and rollback
strategies** in CI/CD pipelines.

------------------------------------------------------------------------

## 7. What are EC2 Pricing Models?

AWS provides multiple pricing options:

**On-Demand** --- Pay per usage, **no commitment**\
**Reserved Instances** --- **Discounts for long-term commitment**\
**Spot Instances** --- **Lowest cost but interruptible**

Choosing correctly helps **optimize costs while maintaining
performance**.

------------------------------------------------------------------------

## 8. What is Amazon S3?

Amazon S3 is an **object storage service**.

It stores data as **objects inside buckets** and provides extremely
**high durability and availability**.

Used for **backups, static hosting, logs, media storage, data lakes**.

Supports **versioning, lifecycle management, replication, and
encryption**.

Common DevOps usage: **pipeline artifacts, Terraform state, assets
storage**.

------------------------------------------------------------------------

## 9. What is Default Storage Class in S3?

Default storage class = **Standard**

Provides: - **High durability** - **High availability** - **Low latency
access**

Lifecycle rules can **move data to cheaper storage classes
automatically**.

------------------------------------------------------------------------

## 10. What are S3 Storage Classes?

S3 offers multiple classes:

-   **Standard --- frequent access**
-   **Intelligent Tiering --- auto optimization**
-   **Standard IA --- infrequent access**
-   **One Zone IA --- lower cost single zone**
-   **Glacier --- archival**
-   **Glacier Deep Archive --- lowest cost long-term storage**

Used to **balance performance and cost optimization**.
