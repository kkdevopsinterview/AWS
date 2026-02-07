## 11. Explain S3 Lifecycle Rules

S3 lifecycle rules help automatically manage objects throughout their
lifetime. Instead of manually moving or deleting files, we define
**policies that transition data between storage classes or remove it
after a certain period**.

For example, frequently accessed data can stay in **Standard storage**,
then move to **Infrequent Access after 30 days**, and later archive to
**Glacier**. Old logs can also be **automatically deleted after a
retention period**.

This helps **optimize costs and maintain compliance without manual
work**.

In DevOps environments, lifecycle rules are commonly used for **log
management, backup retention, and artifact cleanup**, ensuring storage
remains efficient and cost-controlled.

------------------------------------------------------------------------

## 12. How does Cross-Region Replication work in S3?

Cross-region replication copies objects automatically from one bucket to
another bucket in a different AWS region.

It is used for **disaster recovery, data locality, or compliance
requirements**. When enabled, new objects uploaded to the source bucket
are **asynchronously replicated** to the destination bucket.

**Versioning must be enabled on both buckets**, and proper **IAM
permissions must be configured**.

This feature improves resilience because **data remains available even
if one region becomes unavailable**.

In production systems, replication supports global applications and
backup strategies where **data durability and availability are
critical**.

------------------------------------------------------------------------

## 13. What is IAM?

IAM, or Identity and Access Management, controls **who can access AWS
resources and what actions they can perform**.

It allows creation of **users, groups, roles, and policies**. Policies
define permissions, and roles allow services or users to assume
**temporary access**.

This helps enforce security best practices such as **least privilege
access**, ensuring users only get permissions necessary for their tasks.

In DevOps workflows, IAM is used to **grant pipeline access, manage
instance permissions, and securely connect services without sharing
credentials**.

Proper IAM configuration is essential for **maintaining security and
auditability** in cloud environments.

------------------------------------------------------------------------

## 14. What is Amazon EBS?

Amazon Elastic Block Store provides **persistent block storage volumes
for EC2 instances**.

These volumes behave like **physical hard drives attached to servers**,
allowing applications to store data that survives instance restarts.

EBS supports **multiple volume types optimized for performance or
cost**, and they can be resized or backed up through **snapshots**.

In DevOps use cases, EBS is commonly used for **databases, application
data, and boot volumes**.

It integrates well with automation and scaling, providing **reliable and
flexible storage** for compute workloads.

------------------------------------------------------------------------

## 15. What is an EBS Snapshot?

An EBS snapshot is a **backup of a volume stored in S3**.

Snapshots capture volume data **at a point in time** and allow
restoration later. They are **incremental**, meaning only changed data
is saved after the first snapshot.

Snapshots are used for **disaster recovery, cloning environments, or
migrating data**.

In automation pipelines, snapshots enable **quick rollback and
environment replication**.

They are a key part of **backup strategies for maintaining
reliability**.

------------------------------------------------------------------------

## 16. What is NAT Instance and NAT Gateway?

Both allow instances in private subnets to **access the internet without
exposing them directly**.

A NAT Instance is a **manually configured EC2 instance** that performs
network address translation. It requires maintenance and scaling
management.

A NAT Gateway is a **managed AWS service** that performs the same
function but is **highly available, scalable, and easier to manage**.

Modern architectures prefer NAT Gateway because it **reduces operational
overhead and improves reliability**.

These components are essential for **secure VPC network design**.

------------------------------------------------------------------------

## 17. How do you connect an EBS volume to multiple instances?

Normally, an EBS volume attaches to **one instance at a time**.

However, certain volume types support **multi-attach**, allowing
connection to multiple instances in the same availability zone.

Applications must handle concurrency properly to **avoid corruption**.

Alternatively, shared storage solutions like **EFS** are often better
for multi-instance access.

Understanding storage access patterns helps **choose the right
architecture**.

------------------------------------------------------------------------

## 18. What is VPC Route Table?

A route table controls **how network traffic flows within a VPC**.

It contains rules defining where traffic should go, such as sending
internet-bound traffic to an **Internet Gateway** or directing private
traffic through **NAT**.

Each subnet is associated with a route table.

Proper routing configuration ensures **connectivity and security
boundaries**.

Route tables are fundamental to **AWS networking architecture**.

------------------------------------------------------------------------

## 19. Public vs Private Subnet Usage

- A public subnet allows **direct internet access through an Internet
Gateway**, typically used for **load balancers or bastion hosts**.

- A private subnet has **no direct internet access** and is used for
**databases or backend services** to improve security.

- This separation reduces exposure of critical systems and follows **best
practice architecture design**.

- DevOps teams design subnet layouts based on **application tiers and
security needs**.

------------------------------------------------------------------------

## 20. What is Internet Gateway?

An Internet Gateway connects a VPC to the **public internet**.

It enables communication between **public resources and external
users**.

It works alongside route tables to **direct traffic**.

Without an IGW, instances cannot communicate with the internet.

It is a basic component of **public-facing architectures**.

------------------------------------------------------------------------

## 21. Types of Load Balancers in AWS

AWS provides three main types:

**Application Load Balancer --- layer 7 routing for HTTP/HTTPS
traffic**\
**Network Load Balancer --- high-performance layer 4 routing**\
**Classic Load Balancer --- legacy option**

Load balancers distribute traffic across multiple instances to **improve
availability and reliability**.

They also perform **health checks and support auto scaling
integration**.

Load balancing is critical for **scalable production systems**.

------------------------------------------------------------------------

## 22. What is NACL?

Network Access Control List is a **subnet-level firewall controlling
inbound and outbound traffic**.

It works using **numbered rules** and is **stateless**, meaning return
traffic must be explicitly allowed.

NACLs provide an additional **security layer beyond security groups**.

They are typically used for **broad traffic filtering policies**.

------------------------------------------------------------------------

## 23. What are Security Groups?

Security groups act as **instance-level firewalls controlling traffic**.

They are **stateful**, meaning allowed inbound traffic automatically
allows outbound response.

Rules define permitted **ports, protocols, and IP ranges**.

They are widely used to secure **EC2, load balancers, and databases**.

Correct configuration ensures **controlled access to resources**.

------------------------------------------------------------------------

## 24. What is Amazon RDS?

Amazon RDS is a **managed relational database service**.

It automates **setup, patching, backups, scaling, and failover**.

This reduces operational effort compared to **self-hosting databases**.

RDS supports multiple engines and **high availability through Multi-AZ
deployments**.

It is widely used for **application data storage with minimal
administrative overhead**.

------------------------------------------------------------------------

## 25. What is DynamoDB?

DynamoDB is a **fully managed NoSQL database designed for fast and
scalable performance**.

It stores data as **key-value pairs** and automatically scales
throughput.

It is used for **high-volume applications requiring low latency
access**.

DevOps teams use it for **session data, metadata storage, or
event-driven workloads**.

Its serverless model simplifies **operations and scaling**.
