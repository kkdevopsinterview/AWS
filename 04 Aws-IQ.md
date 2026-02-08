## 35. What are EBS Volume Types?

Amazon **Elastic Block Store** provides different **volume types**
designed for different **workloads**. Each type is optimized either for
**performance** or **cost**.

The most commonly used type is **General Purpose SSD**, which offers
**balanced performance** and is suitable for most applications like
**web servers** and **development workloads**. For more demanding
systems such as **databases**, **Provisioned IOPS SSD** is used because
it delivers **consistent high input/output performance**.

For large sequential workloads like **data processing** or **logging**,
**Throughput Optimized HDD** can be selected since it is designed for
**high throughput** rather than **low latency**. There is also **Cold
HDD**, which is more **cost-effective** for **infrequently accessed
data**.

Choosing the **right volume type** is important because **storage
performance** directly impacts **application performance**. In
real-world **DevOps work**, selecting proper storage ensures **efficient
resource usage**, **cost optimization**, and **system stability**.

------------------------------------------------------------------------

## 36. How Snapshot Works Internally?

An **EBS snapshot** is a **backup stored in S3** that captures the
**state of a volume** at a specific time. Internally, snapshots use an
**incremental mechanism**.

The **first snapshot copies all data blocks**. After that, only the
**blocks that change** are saved in **subsequent snapshots**. This makes
**backups faster** and more **storage-efficient**.

AWS also handles **replication** and **durability** automatically,
ensuring that snapshots remain **available** even if **infrastructure
failures** occur.

Snapshots are important for **disaster recovery**, **cloning
environments**, and **rollback strategies**. In **production
pipelines**, they enable **fast restoration** without rebuilding systems
from scratch.

This **incremental design** helps reduce **cost** while maintaining
**reliable data protection**.

------------------------------------------------------------------------

## 37. Can You Attach EBS Volume to Multiple Instances?

Typically, an **EBS volume** can be attached to only **one EC2
instance** at a time, ensuring **data consistency** and preventing
**corruption**.

However, certain volume types support **multi-attach capability**,
allowing connection to **multiple instances** within the same
**availability zone**. This requires applications to manage **concurrent
access** safely.

In many scenarios, shared storage services such as **Elastic File System
(EFS)** are more appropriate when multiple instances need access to the
same **data**.

Understanding this limitation helps architects choose proper **storage
strategies** for **distributed workloads**.

------------------------------------------------------------------------

## 38. How Do You Increase Volume Size?

Volume size can be increased **dynamically** without **recreating the
volume**. The process involves modifying the **volume configuration
through AWS** and then extending the **file system inside the
instance**.

This allows **storage scaling** with **minimal disruption**. Monitoring
**disk usage** helps determine when expansion is needed.

In **DevOps environments**, resizing storage supports **application
growth**, **log accumulation**, and **database expansion** without
**downtime**.

This flexibility ensures systems remain **operational** while adapting
to **changing storage requirements**.

------------------------------------------------------------------------

## 39. Difference Between EBS and Instance Store

**EBS** provides **persistent storage**, meaning **data remains** even
if the **instance stops or restarts**.

**Instance store**, on the other hand, provides **temporary storage**
physically attached to the **host machine**. Data is lost when the
**instance stops or terminates**.

EBS supports **backups**, **resizing**, and **encryption**, making it
suitable for **databases** or **application storage**. Instance store
offers **higher performance** but is used mainly for **temporary data**
such as **caches** or **buffers**.

Understanding this distinction helps choose the right **storage**
depending on **durability needs**.

------------------------------------------------------------------------

## 40. What is Volume Encryption?

**Volume encryption** ensures that **stored data** is protected using
**cryptographic techniques**.

AWS integrates encryption with **Key Management Service**, allowing
secure management of **encryption keys**. This protects **data at rest**
and during **snapshot operations**.

Encryption helps organizations meet **compliance requirements** and
**security standards**, ensuring **sensitive data** cannot be easily
accessed even if **compromised**.

In modern **cloud environments**, encryption is considered a **standard
best practice** rather than an **optional feature**.

------------------------------------------------------------------------

## 41. How Do You Back Up EBS Data?

Backing up **EBS volumes** is typically done using **snapshots**.

Snapshots can be **scheduled automatically**, stored **redundantly**,
and copied across **regions** for additional **safety**.

In **recovery situations**, volumes can be **recreated from snapshots**
quickly. This ensures **business continuity** and **disaster
preparedness**.

Proper **backup planning** is essential in **production systems** where
**data loss** can have serious **consequences**.

------------------------------------------------------------------------

## 42. Performance Tuning for EBS

Optimizing **storage performance** involves selecting the **right volume
type** and monitoring **usage metrics**.

Performance can be improved by balancing **workload distribution**,
adjusting **IOPS allocation**, and using **caching techniques**.

**Monitoring tools** help detect **bottlenecks** before they affect
**users**.

Effective tuning ensures applications run **efficiently** and maintain
**consistent response times**, which is critical for **production
reliability**.
