# class 13

## Serverless

----------------------

### Serverless is a cloud application development and execution model that lets developers build and run code without managing servers, and without paying for idle cloud infrastructure.

### Serverless lets developers put all their focus into writing the best front-end application code and business logic they can. All developers need to do is write their application code and deploy it to containers managed by a cloud service provider. The cloud provider handles the rest, provisioning the cloud infrastructure required to run the code and scaling the infrastructure up and down on demand as needed. The cloud provider is also responsible for all routine infrastructure management and maintenance such as operating system updates and patches, security management, capacity planning, system monitoring and more.

### Also important: With serverless, developers never pay for idle capacity. The cloud provider spins up and provisions the required computing resources on demand when the code executes, and spins them back down again—called ‘scaling to zero’—when execution stops. The billing starts when execution starts, and ends when execution stops; typically, pricing is based on execution time and resources required.

----------------------

## Serverless does not mean 'no servers'

### The name notwithstanding, there are most definitely servers in serverless computing. 'Serverless' describes the developer’s experience with those servers—they are are invisible to the developer, who doesn't see them, manage them, or interact with them in any way.

----------------------

## Serverless is more than just FaaS

### Function-as-a-service, or FaaS, is a cloud computing service that enables developers to run code or containers in response to specific events or requests, without specifying or managing the infrastructure required to run to code.

----------------------

## Serverless vs. PaaS, containers, and VMs

### Because serverless, platform as a service (PaaS), containers, and virtual machines (VMs) all play a critical role in the cloud application development and compute ecosystem, it’s useful to compare how serverless compares to the others across some key attributes.

- Provisioning time: Measured in milliseconds for serverless, vs. minutes to hours for the other models.

- Administrative burden: None for serverless, compared to a continuum from light to medium to heavy for PaaS, containers and VMs respectively.

- Maintenance: Serverless architectures are managed 100% by the provider. The same is true for PaaS, but containers and VMs require significant maintenance including updating/managing operating systems, container images, connections, etc.

- Scaling: Auto-scaling—including auto-scaling to zero—is instant and inherent for serverless. The other models offer automatic but slow scaling that requires careful tuning of auto-scaling rules, and no scaling to zero.

- Capacity planning: None needed for serverless. The other models require a mix of some automatic scalability and some capacity planning.

- Statelessness: Inherent for serverless, which means scalability is never a problem; state is maintained in an external service or resource. PaaS, containers and VMs can leverage HTTP, keep an open socket or connection for long periods of time, and store state in memory between calls.

- High availability (HA) and disaster recovery (DR): Both are inherent in serverless with no extra effort and at no additional cost. The other models require additional cost and management effort. In the case of both VMs and containers, infrastructure can be restarted automatically.

- Resource utilization: Serverless is 100% efficient because there are no such things thing as idle capacity—it is invoked only upon request. All other models feature at least some degree of idle capacity.

- Billing granularity and savings: Serverless is metered in units of 100 milliseconds. PaaS, containers and VMs are typically metered by the hour or the minute.
