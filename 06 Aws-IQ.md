### 67. What is Amazon RDS?

**Amazon Relational Database Service (RDS)** is a **managed service**
for running **relational databases** in **AWS**. Instead of installing
and maintaining **database software manually**, AWS handles tasks such
as **setup**, **patching**, **backups**, **monitoring**, and
**scaling**.

It supports popular engines like **MySQL**, **PostgreSQL**, and others,
allowing applications to store **structured data reliably**. By using
**RDS**, teams focus on **application logic** rather than
**infrastructure maintenance**.

RDS also provides **high availability options**, **automated
snapshots**, and **performance monitoring**, making it suitable for
**production workloads**. In **DevOps environments**, this reduces
**operational burden** and improves **deployment consistency**.

Overall, RDS simplifies **database management** while providing
**reliability**, **scalability**, and **security**.

------------------------------------------------------------------------

### 68. Difference Between RDS and EC2-Hosted Database

Running a database on **EC2** gives **full control** over configuration
and environment, but requires **manual management** of **backups**,
**patching**, **scaling**, and **failover**.

**RDS** removes much of this **operational responsibility** by
**automating** these tasks. This allows **faster deployment** and
reduced **risk of misconfiguration**.

However, **EC2-hosted databases** may be chosen when **deep
customization** or **specific tuning** is required.

In most **standard application scenarios**, **RDS is preferred** because
it balances **performance** with reduced **management effort**. Choosing
between them depends on **control versus convenience**.

------------------------------------------------------------------------

### 69. What is Multi-AZ in RDS?

**Multi-AZ deployment** creates a **standby database replica** in
another **availability zone**.

Data is **synchronously replicated**, and if the **primary instance
fails**, AWS automatically switches to the **standby**.

This improves **fault tolerance** and **uptime** without **manual
intervention**.

Multi-AZ is used mainly for **availability** rather than **performance
scaling**. It ensures **critical applications remain accessible** even
during **infrastructure failures**.

Implementing **redundancy** like this is a **best practice** for
**production systems**.

------------------------------------------------------------------------

### 70. What is Read Replica?

**Read replicas** are copies of a database designed to handle
**read-heavy workloads**.

They receive data **asynchronously** from the **primary database** and
allow applications to distribute **read queries** across **multiple
instances**.

This improves **performance** and reduces **load** on the **main
database**.

They are commonly used for **reporting**, **analytics**, or **scaling
web applications**.

Unlike **Multi-AZ**, replicas are mainly for **performance** rather than
**failover**, though they can be **promoted manually** if needed.

------------------------------------------------------------------------

### 71. What is Amazon DynamoDB?

**Amazon DynamoDB** is a **fully managed NoSQL database service**
designed for **high speed** and **scalability**.

It stores data as **key-value** or **document structures** and
automatically adjusts **capacity** based on **demand**.

Because AWS manages **infrastructure** and **replication**, developers
do not handle **server provisioning**.

It is ideal for applications needing **low latency** and **high
throughput**, such as **gaming platforms**, **mobile apps**, or
**real-time analytics**.

This **serverless model** simplifies **operations** while maintaining
**performance** and **availability**.

------------------------------------------------------------------------

### 72. When Would You Use DynamoDB?

**DynamoDB** is best used when applications require **rapid scaling**,
**unpredictable traffic handling**, and **fast response times**.

It suits workloads where **relational joins** are unnecessary and
**access patterns** are based on **keys**.

Examples include **session storage**, **event tracking**, and **IoT
data**.

Using DynamoDB allows teams to focus on **application logic** rather
than **database scaling**.

Selecting the correct **database type** ensures **efficient architecture
design**.

------------------------------------------------------------------------

### 73. What is Partition Key?

A **partition key** determines how **data is distributed** across
**storage partitions** in **DynamoDB**.

Each item uses a **key value** that helps decide where it is stored
internally.

Choosing a well-distributed key prevents **bottlenecks** and ensures
**consistent performance**.

Poor key selection can **overload specific partitions**.

Understanding **key design** is essential for **scalability** and
**efficient data access**.

------------------------------------------------------------------------

### 74. How Scaling Works in DynamoDB?

**DynamoDB** supports scaling through **provisioned** or **on-demand
capacity modes**.

**Provisioned mode** allows configuration of **read and write limits**,
while **on-demand** automatically adjusts capacity based on **usage**.

AWS also distributes **data** across infrastructure for
**availability**.

This ensures **stable performance** during **traffic changes**.

Automatic scaling reduces **operational complexity** while maintaining
**responsiveness**.

------------------------------------------------------------------------

### 75 . What is Amazon Redshift Used For?

**Amazon Redshift** is AWS's **managed data warehousing platform**.

It processes **large datasets quickly** using **optimized query
execution**.

It integrates with **analytics tools** for **visualization** and
**reporting**.

Organizations use it to extract **insights from historical data**.

Redshift supports **business intelligence**, **forecasting**, and
**strategic planning** by enabling **deep data analysis**.
