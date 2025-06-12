# Notes for section 2 mod 2: Overview of Cloud Service Models

## 3 Service Models
- MODELS: from most complex to least complex
- IaaS - Infrastucture services - users: system/IT admin
- Paas - services from infrastructure - users: developer
- Saas - software host over internet - users: everyone

- Car Metaphor
  - IaaS: leasing - pay for the gas, care about the specs, color, and details
  - PaaS: renting - don't care about specs, but still paying for the gas
  - SaaS: taxi - don't care about the details, you're not driving, don't pay gas

![image](https://github.com/user-attachments/assets/87ed58cd-ac13-40b3-a8b9-7eb99f64f2bf)
![image](https://github.com/user-attachments/assets/ea5bbec3-90d7-4d88-bc69-53d005853266)
![image](https://github.com/user-attachments/assets/b5d4f94f-1e4c-45fd-8d29-93c44dcbced4)

## Infrastructure as a service (IaaS)

 ![image](https://github.com/user-attachments/assets/88291a3f-0522-4f50-b4d6-07edcc630fb8)

- customers can create or provision VMs in their choice of Region and Zone available from the Cloud provider
- these VMs ususally come pre-installed with the customer's choice of OS
- then they can deploy middleware, apps, and run workloads on these VMs
- storage for backups/workloads
- give ability to track and monitor performance ans usage and manage distaster recovery

- Physical: in most IaaS, users do not interact with the physical infra., it is a service provided to them
- Compute: IS providers manage the hypervisors, and users provision the amount of meemory, compute capacity, and storage
  - comes with supporting services like auto scaling and load balancing
- Network: users get access to networking resources through virtualization or programmatically through APIs
- Storage:
  - object: most common - highly distributed and resilient.
  - file:
  - block:

- IaaS is the fastest growing model today

## Platform as a Service (PaaS)

![image](https://github.com/user-attachments/assets/1b39ae33-b409-45e9-b245-1288c6c9be0b)
![image](https://github.com/user-attachments/assets/9da2fb74-ee5f-42f7-8f09-8270c55862f5)

- in IaaS, user manages all components; in PaaS, the user manages everything past the OS like apps and data.

![image](https://github.com/user-attachments/assets/176639f4-aa01-4c6f-9fb2-37127b78e97c)

- USE CASE for PaaS is strategic: build, test, deploy, enchance, and scale apps rapidly and cost-effectively
 
![image](https://github.com/user-attachments/assets/9a9a2e0f-e78f-4586-8357-85fde211697f)

- Advantages of PaaS
  - scalability
  - faster time to market
  - greater agility and innovation - can use a great range of tools and languages without having to invest in these resources. Prototype with less risk exposure

![image](https://github.com/user-attachments/assets/8833bac7-4d93-4a14-bb86-d0dd2d80ec0f)
- side note: OpenShift RedHat is what is indicated above

- Risks of PaaS:
  - information security threats
  - dependency of service provider's infra.
  - customers lack control over changes in provider's strategy, offerings, or tools

## Software as a Service (SaaS)
