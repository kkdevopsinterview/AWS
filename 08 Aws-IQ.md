## 88. What is API Gateway?

An API Gateway is a service that acts as a single entry point for client
requests to backend services. Instead of clients directly calling
multiple microservices, all requests go through the gateway.

It performs important responsibilities like:

-   routing requests to correct services
-   authentication and authorization
-   rate limiting
-   request validation
-   logging and monitoring

This centralizes API management and simplifies system design.

In cloud platforms like AWS, API Gateway is fully managed, meaning we
don't manage servers or scaling. It automatically handles traffic spikes
and integrates with services like Lambda or containers.

#### Real-World Example

In an e-commerce system, mobile apps send requests only to API Gateway.
The gateway routes them to services like payment, inventory, or orders.

#### Interview Punch Lines

"API Gateway acts as the front door to backend services."\
"It centralizes security, routing, and monitoring."

------------------------------------------------------------------------

## 89. Difference between REST and HTTP API Gateway types

API Gateway typically provides REST APIs and HTTP APIs, each designed
for different needs.

#### REST APIs

-   More features
-   Advanced authorization
-   API keys and usage plans
-   Request/response transformation
-   Higher cost and latency

#### HTTP APIs

-   Lightweight and faster
-   Lower cost
-   Simpler configuration
-   Limited advanced features

Choosing between them depends on whether you need advanced control or
simple high-performance routing.

#### Real-World Example

Banking system → REST API for strict control\
Simple microservice → HTTP API for speed and cost savings

#### Interview Punch Line

"REST APIs provide capability, HTTP APIs provide efficiency."

------------------------------------------------------------------------

## 90. How does API Gateway integrate with Lambda?

API Gateway integrates with Lambda by acting as the trigger for
serverless execution.

#### Flow

1.  Client sends HTTP request\
2.  API Gateway receives request\
3.  Gateway invokes Lambda function\
4.  Lambda processes logic\
5.  Response returned to client

This removes the need for managing servers and enables event-driven
architecture.

Scaling is automatic --- Lambda runs more instances when traffic
increases.

#### Real-World Example

Uploading a profile picture triggers Lambda through API Gateway to
process and store the image.

#### Interview Punch Line

"API Gateway turns HTTP requests into Lambda events."

------------------------------------------------------------------------

## 91. How do you secure APIs?

API security requires multiple layers:

-   Authentication (who are you?)
-   Authorization (what can you access?)
-   Encryption using HTTPS
-   Rate limiting
-   Monitoring and logging

API Gateway provides built-in tools like:

-   IAM policies
-   OAuth/JWT
-   API keys

Security protects data integrity and prevents misuse.

#### Real-World Example

Only authenticated users can access payment endpoints.

#### Interview Punch Line

"API security combines identity verification, encryption, and
monitoring."

------------------------------------------------------------------------

## 92. What is throttling in API Gateway?

Throttling controls how many requests a client can send within a time
window.

It protects backend services by:

-   preventing overload
-   stopping abuse
-   maintaining performance

Limits can be set per user or per API.

If limits are exceeded, requests are rejected.

#### Real-World Example

Preventing bots from sending thousands of login requests.

#### Interview Punch Line

"Throttling maintains system stability under heavy traffic."

------------------------------------------------------------------------

## 93. How do you monitor API usage?

Monitoring tracks how APIs are being used and helps detect issues.

We monitor:

-   request counts
-   latency
-   errors
-   traffic patterns

Tools provide logs and metrics dashboards.

Monitoring helps:

-   optimize performance
-   detect failures
-   plan scaling

#### Real-World Example

Detecting increased errors after deployment.

#### Interview Punch Line

"Monitoring provides visibility into API health and usage."

------------------------------------------------------------------------

## 94. What is request transformation?

Request transformation modifies incoming requests before sending them to
backend services.

This helps:

-   adapt data formats
-   add headers
-   map fields
-   maintain compatibility

It allows integration between systems with different interfaces.

#### Real-World Example

Client sends JSON but backend expects another structure --- gateway
converts it.

#### Interview Punch Line

"Transformation enables flexible system integration."

------------------------------------------------------------------------

## 95. How do you handle versioning?

Versioning ensures new API changes do not break existing clients.

Common methods:

-   URL versioning (/v1/, /v2/)
-   header versioning

This allows:

-   gradual migration
-   backward compatibility

Clients continue using older versions until ready to upgrade.

#### Real-World Example

Mobile apps still calling old endpoints while web uses new version.

#### Interview Punch Line

"Versioning protects clients from breaking changes."

------------------------------------------------------------------------

## 96. Difference between API Gateway and Load Balancer

#### API Gateway

-   Application-level routing
-   Authentication
-   Rate limiting
-   Request transformation
-   Monitoring

#### Load Balancer

-   Distributes traffic across servers
-   Operates at network/transport level
-   Improves availability

They solve different problems.

#### Real-World Example

Gateway routes request to service; load balancer spreads traffic across
instances.

#### Interview Punch Line

"Gateway manages API logic, load balancer manages traffic distribution."
