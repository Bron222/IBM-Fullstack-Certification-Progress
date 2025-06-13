# Notes for section 2 / mod 2: Overview of Cloud Service Models

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

 - SaaS: cloud offering that provides access to a service provider's cloud-based software

 - Supports:
  - email and collaboration
  - CRM - customer relationship management
  - HRM - human resource management
  - financial management
  - billing and collaboration
   
- Key characteristics:
  - Multitenant architecture
  - easy for users to manage privileges and monitor data use
  - offers security, compliance, and maintenance
  - customize applications, but may have limited control
  - subscription model
     
- key Benefits
  - greatly reduce the time from decision to value
  - increase workforce prod and eff.
  - users can access core business apps from anywhere
  - spread out software costs over time
   
![image](https://github.com/user-attachments/assets/9588273a-7739-4af4-8bac-882ba68f3f0e)

- Concerns:
  - data ownership and data safety
  - 3rd party maintains business-critical data
  - needs good network connection

## Deloyment Models

### Public Cloud model

 ![image](https://github.com/user-attachments/assets/d9afc863-55cc-454c-bbf0-e515759c29fa)
- like water, energy, gas in homes, we don't manage the resources, only pay for our usage
- public cloud = cost savings
- in a public cloud pay for the services you use but do not control the computing environment
- Providers: AWS, Azure, IBM Cloud, Google Cloud, Alibaba Cloud
  
- Characteristic of Public Cloud:
  - virtualized Multi-tenant architecture enabling the tenants or users to share computijng resources
  - cloud providers pool of resources, including infra, platforms, and software are NOT dedicated for use by a single tenant or organization.
  - variety of different pay-as-you-go models with different features

![image](https://github.com/user-attachments/assets/77ab3f91-a747-4527-8258-fc1c8a611518)
  
- concers: 
  - security: data breaches, data loss, account hijacking, lack of due dilligence, and system/app vulnerability
  - Data sovereignty: increasingly difficulty for companies to be compliant with data sov. regulations governing the storage, transfer, and security of data
 
![image](https://github.com/user-attachments/assets/a83e984f-58aa-41fb-8874-507408ce4a8c)

### Private Cloud model

- exclusively used by a single organization with multiple consumers
- owned, managed and operated by organizations, 3rd party, or combination
- can be external or internally hosted
  - external: private cloud, but hosted by a service provider
    - VPC (virtual private cloud) - a private cut of the public cloud
  - internal: manaaged by the organization

![image](https://github.com/user-attachments/assets/9a2ba34d-6083-47e9-8964-abab616fc383)
  
![image](https://github.com/user-attachments/assets/6d32d80e-d55b-43d5-b228-14f450f27f67)

### Hybrid Cloud model

- connects an organizations' on-premise private cloud and 3rd party public cloud
- workloads hosted in either public or private cloud depending on needs
  - flexibility
  - workloads move freely
  - leverage public and private clouds: when you need to temporarily expand your private cloud resources, you can utilize the public cloud to help (like during a surge). This is called "Cloud Bursting"
  
![image](https://github.com/user-attachments/assets/bddef5f9-8165-4d01-b947-10b477fa2dc4)
  
![image](https://github.com/user-attachments/assets/857e9b15-fb66-4aae-a2ae-ca679e8ace90)

![image](https://github.com/user-attachments/assets/3958cde8-35d3-4d44-80a1-98ff8ab8f83e)

![image](https://github.com/user-attachments/assets/5ac742dd-393d-4352-b10e-856972afff32)

### Community Cloud model
- Cloud infrastructure [that] is provisioned for exclusive use by a specific community of consumers from organizations that have shared concerns (e.g., mission, security requirements, policy, and compliance considerations). It may be owned, managed, and operated by one or more of the organizations in the community, a third party, or some combination of them, and it may exist on or off premises
  
- Why community cloud?
  - Community cloud approach is used by organizations for the following reasons:

  - The community cloud members work under the same set of security controls.

  -  The approach provides the members the same attributes like citizenship and authorization controls while giving limited physical and/or logical access to resources.

  - It also supports data localization and some data sovereignty requirements based on the location of the community cloud’s data centers. 

  - The approach defines a perimeter security model encompassing the community cloud.
  
- Benefits of a software-defined community cloud
  - The approach Google Cloud has taken brings multiple benefits such as meeting security and compliance requirements.
  - New hardware, new services, and improvements to existing services are accessed faster than in traditional community clouds.
  - The process by which new cloud technology can be onboarded and made available is also faster.
  - Overall efficiency is improved in this model due to the scale of infrastructure available to the community; this can translate to improved availability and performance.
  - Security enhancements can be scaled and implemented more quickly.  
