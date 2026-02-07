## 1. What is Cloud Computing?

Answer (speak like this):

Cloud computing means using computing services like servers, storage,
databases, and networking over the internet instead of maintaining
physical hardware locally.

Instead of buying and managing your own servers, you rent resources from
cloud providers like AWS and pay only for what you use. This makes
systems scalable, flexible, and cost-effective.

Cloud computing allows teams to deploy applications faster, scale
automatically based on demand, and improve reliability because
infrastructure is distributed across multiple locations.

There are also benefits like high availability, disaster recovery
options, and reduced operational overhead since the provider manages
hardware maintenance.

In real-world DevOps work, cloud computing enables automation, CI/CD
pipelines, container deployments, and infrastructure as code, which
significantly speeds up delivery and improves consistency.

------------------------------------------------------------------------

## 2. What is AWS?

AWS, or Amazon Web Services, is a cloud platform that provides on-demand
infrastructure and services over the internet.

It offers services for computing, storage, networking, databases,
security, analytics, and DevOps automation. Instead of managing physical
servers, we launch resources like EC2 instances or storage like S3
within minutes.

AWS operates on a global infrastructure model with regions and
availability zones, which helps build highly available and
fault-tolerant applications.

From a DevOps perspective, AWS is widely used because it integrates well
with automation tools, CI/CD pipelines, monitoring, and container
orchestration platforms like Kubernetes.

Overall, AWS allows organizations to scale quickly, optimize costs, and
focus on application development instead of infrastructure management.

------------------------------------------------------------------------

## 3. What are IaaS, PaaS, and SaaS?

These are cloud service models that define how much responsibility you
manage versus the provider.

IaaS --- Infrastructure as a Service\
You control virtual machines, storage, and networking while the provider
manages hardware.\
Example: AWS EC2\
Used when you need full control of environment setup.

PaaS --- Platform as a Service\
Provider manages infrastructure and runtime environment, and you focus
on application deployment.\
Example: Elastic Beanstalk\
This reduces operational work and speeds development.

SaaS --- Software as a Service\
You simply use the application through a browser.\
Example: Gmail or Salesforce\
No infrastructure or platform management required.

Understanding these helps choose the right level of control vs
convenience depending on project needs.

------------------------------------------------------------------------

## 4. What is EC2?

Amazon EC2 is a compute service that provides virtual servers in the
cloud.

It allows us to launch instances with different CPU, memory, and storage
configurations depending on workload requirements. You can install
applications, run services, or host websites just like on physical
servers.

EC2 supports scaling using Auto Scaling groups and integrates with load
balancers for traffic distribution.

It offers multiple pricing models like On-Demand, Reserved, and Spot to
optimize costs.

From a DevOps perspective, EC2 is often used for application hosting,
CI/CD runners, container nodes, or custom workloads where full OS-level
control is needed.

It provides flexibility, scalability, and automation capability through
APIs and scripts.

------------------------------------------------------------------------

## 5. What are Key Pairs?

Key pairs are used for secure login to EC2 instances.

They consist of a public key stored by AWS and a private key stored
securely by the user. When connecting via SSH, AWS verifies access using
cryptographic authentication instead of passwords.

This improves security and prevents brute force attacks.

If the private key is lost, accessing the instance becomes difficult,
which is why proper key management and backups are important.

In DevOps environments, key access is often replaced or supplemented by
IAM roles or session managers for better centralized control.

------------------------------------------------------------------------

## 6. What is an AMI?

An Amazon Machine Image, or AMI, is a template used to launch EC2
instances.

It contains the operating system, installed software, configurations,
and permissions required to start a virtual machine.

Teams create custom AMIs to ensure consistent deployments. For example,
a preconfigured AMI with application dependencies installed reduces
setup time and improves reliability.

AMI versioning is useful in CI/CD pipelines for immutable deployments
and rollback strategies.

Essentially, AMIs help standardize infrastructure and speed up
provisioning.

------------------------------------------------------------------------

## 7. What are EC2 Pricing Models?

AWS provides multiple pricing options to balance flexibility and cost.

On-Demand:\
Pay per usage with no commitment. Best for unpredictable workloads.

Reserved Instances:\
Commit for long-term usage for significant discounts. Suitable for
stable workloads.

Spot Instances:\
Use spare AWS capacity at very low cost but may be interrupted. Ideal
for batch jobs or fault-tolerant tasks.

Choosing the right model helps optimize operational expenses while
maintaining performance needs.

DevOps teams often mix these models depending on workload type.

------------------------------------------------------------------------

## 8. What is Amazon S3?

Amazon S3 is an object storage service used to store and retrieve data
from anywhere.

It stores data as objects inside buckets and provides extremely high
durability and availability.

S3 is commonly used for backups, static website hosting, logs, media
storage, and data lakes.

It supports versioning, lifecycle management, replication, and
encryption for data protection.

From a DevOps perspective, S3 is often used to store pipeline artifacts,
Terraform state files, and application assets.

Its scalability and reliability make it a core AWS storage service.

------------------------------------------------------------------------

## 9. What is Default Storage Class in S3?

The default storage class in S3 is Standard.

It provides high durability, availability, and low latency access.

This class is suitable for frequently accessed data like application
assets, logs, and active datasets.

If cost optimization is needed, lifecycle rules can transition data to
lower-cost classes like Glacier or Infrequent Access automatically.

Understanding storage classes helps balance performance and cost.

------------------------------------------------------------------------

## 10. What are S3 Storage Classes?

S3 offers multiple classes based on access frequency and cost:

Standard --- frequent access\
Intelligent Tiering --- automatic cost optimization\
Standard IA --- infrequent access\
One Zone IA --- cheaper but single zone\
Glacier --- archival storage\
Glacier Deep Archive --- lowest cost long-term storage

Choosing the right class depends on retrieval needs, performance
requirements, and budget considerations.

Lifecycle policies often automate movement between classes.
