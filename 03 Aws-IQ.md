## 26. Difference between IAM User, Role, and Group

IAM provides multiple identity types to control access in AWS.

- An IAM User represents an individual identity --- typically a human or
application --- with long-term credentials like passwords or access
keys. Users are assigned permissions directly or through groups.

- An IAM Group is a collection of users that share the same permissions.
Instead of assigning policies to each user, permissions are applied once
to the group. This simplifies management and enforces consistent access
control.

- An IAM Role is different because it doesn't represent a person. It
provides temporary credentials that can be assumed by users, AWS
services, or external systems. Roles are widely used for secure
service-to-service access without storing credentials.

In DevOps environments, users manage access, groups organize
permissions, and roles enable secure automation workflows.

---
## 27. What are IAM Policies?

IAM policies are JSON documents that define what actions are allowed or
denied on which resources.

They specify permissions such as read access to S3 or instance
management rights in EC2. Policies can be attached to users, groups, or
roles.

They enforce access control and are central to AWS security design.
Using properly structured policies ensures resources remain protected
while allowing necessary operations.

In production environments, policies are audited and maintained to align
with least privilege principles and compliance standards.

---
## 28. Managed vs Inline Policies

Managed policies are reusable permission sets created and maintained
either by AWS or by the organization. They can be attached to multiple
identities and updated centrally.

Inline policies are embedded directly into a specific user, group, or
role and apply only there. They are tightly coupled and not reusable.

Managed policies simplify large-scale permission management, while
inline policies are useful for very specific access scenarios.

---
## 29. What is Least Privilege Principle?

Least privilege means granting only the minimum permissions required to
perform a task --- nothing more.

This reduces security risk by limiting the impact of compromised
credentials or accidental misuse.

In cloud environments, following least privilege helps prevent
unauthorized access and protects sensitive resources. It is considered a
core best practice in DevOps security and compliance.

---
## 30. What is MFA in AWS?

Multi-Factor Authentication adds an extra verification step beyond
passwords.

Users must provide a second factor such as a time-based code from a
mobile device. This protects accounts even if credentials are exposed.

MFA is especially critical for privileged users and production
environments.

---
## 31. What is Role Assumption?

Role assumption is the process of temporarily gaining permissions
associated with an IAM role.

Instead of permanent credentials, temporary tokens are issued. This
improves security by limiting exposure.

Common examples include applications accessing AWS services or
cross-account access scenarios.

---
## 32. How Do Services Access Other Services Securely?

AWS services typically use IAM roles.

For example, an EC2 instance can assume a role that allows access to S3
without storing credentials. AWS automatically rotates temporary
credentials.

This approach eliminates hardcoded secrets and improves security
posture.

---
## 33. How Do You Audit IAM Usage?

Auditing is done using AWS CloudTrail logs and IAM access analysis
tools.

These track actions performed by identities, enabling review of
permission usage and detection of anomalies.

Regular auditing ensures compliance and strengthens governance.

---
## 34. Best Practices for IAM Security

Best practices include:

Enforcing least privilege
Using roles instead of access keys
Enabling MFA
Rotating credentials
Monitoring logs

Applying these practices ensures strong security in cloud deployments.
