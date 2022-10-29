# Serverless Functions
## What is Serverless?
  - Serverless is a cloud application development and execution model that lets developers build and run code without managing servers, and without paying for idle cloud infrastructure.


## Serverless is more than just FaaS 
  - Serverless databases and storage
  - Event streaming and messaging
  - API gateways
 
 ## Serverless vs. PaaS, containers, and VMs
  1. Provisioning time: Measured in milliseconds for serverless, vs. minutes to hours for the other models.
  2. Administrative burden: None for serverless, compared to a continuum from light to medium to heavy for PaaS, containers and VMs respectively.
  3. Maintenance: Serverless architectures are managed 100% by the provider. The same is true for PaaS, but containers and VMs require significant maintenance including updating/managing operating systems, container images, connections, etc.
  4. Scaling: Auto-scaling—including auto-scaling to zero—is instant and inherent for serverless. The other models offer automatic but slow scaling that requires careful tuning of auto-scaling rules, and no scaling to zero.
  5. Capacity planning: None needed for serverless. The other models require a mix of some automatic scalability and some capacity planning.
  6. Statelessness: Inherent for serverless, which means scalability is never a problem; state is maintained in an external service or resource. PaaS, containers and VMs can leverage HTTP, keep an open socket or connection for long periods of time, and store state in memory between calls.
  7. High availability (HA) and disaster recovery (DR): Both are inherent in serverless with no extra effort and at no additional cost. The other models require additional cost and management effor
  8. Resource utilization: Serverless is 100% efficient because there are no such things thing as idle capacity—it is invoked only upon request. All other models feature at least some degree of idle capacity.
  9. Billing granularity and savings: Serverless is metered in units of 100 milliseconds. PaaS, containers and VMs are typically metered by the hour or the minute.

## Pros and cons of serverless 
#### Pros 
  1. Improved developer productivity
  2. Pay for execution only
  3. Develop in any language
  4. Streamlined development/DevOps cycles
  5. Cost-effective performance
 
#### Cons 
  1. Unacceptable latency for certain applications
  2. Higher costs for stable or predictable workloads
  3. Monitoring and debugging issues
## Use cases for serverless
  - Serverless and microservices : The most common use case of serverless today is supporting microservices architectures
  - API backends : Any action (or function) in a serverless platform can be turned into a HTTP endpoint ready to be consumed by web clients. When enabled for web, these actions are called web actions
  - Data processing 
  - Massively parallel compute/“Map” operations
  - Stream processing workloads


