# Notes for sec 2 mod 5: Cloud Infrastructure

## Infrastructure Overview
- is the foundation of the cloud. This layer consists of physical resources that are housed in Regions, Zones and Data Centers.
- A Cloud provider’s IT environment is typically distributed across many Regions around the world.
- A cloud Region, is a geographic area or location where a Cloud provider’s infrastructure is clustered, and may have names like NA South or US East.
- Each Cloud Region can have multiple Zones (or Availability Zones or AZ for short), which are typically distinct Data Centers with their own power, cooling and networking resources.
- Computing resources
  - Virutal servers - (VMs) Software based servers
  - Bare Metal Servers - Physical Servers
  - "Serverless" - Abstraction layer on top of VMs
- Networking:
  - Routers
  - Switches
  - SDN - Software Defined Networking: options where certain networking resources are virtualized or made available programmatically, through APIs.
- Public vs Private Interfaces
- Networking: ACLs, Security Groups, VLANs, VPC, VPNs, Gateways, load balancers, firewalls, subnets, IP addresses, traffic analyzers, CDNs (content delivery networks; distribute content from multiple points around the world "like 'edge connection' networks in AWS")

## Virtualization and Virtual Machines

![image](https://github.com/user-attachments/assets/edfa631c-9910-44fe-86ed-0c20c4ddae61)
- Hypervisor type 1: bare metal - runs directly on top of the resources (most common and effecient)
- Hypervisor type 2: hosted - runs on top of an OS (like VirtualBox; mostly used by end users)
- since Virtual Machines are software based, they can be moved very easily to another hypervisor on another system.

## Types of Virtual Machines (VMs)
- also called Virtual Servers, Virtual Instances, or just Instances (names are cloud provider dependent)

### Shared or Public Cloud VMs
- multi-tenant - underlying server is a virtual server, and shared across other tenants (users), lots of predefined configurations, can cunstomers too. can be prices hourly/monthly/minutes/sec
- singe tenant

### Transient or Spot VMs
- take advantage of unused capacity in a cloud data center
- lower cost
- Cloud provider can take them take back if they need them
- great for non-production, testing, developing, and running stateless workloads, testing scalability
- running big data and HPC (high perforance computing) workloads at a lower cost

### Reserved Capacity VMs
- reserved capacity and guarantee resources for future deployment
- choose a term. Longer term = lower cost.
- if you exceed capacity, you can provision monthly or hourly VMs. but not all predefined VM families or configurations may be available as reserved

### Dedicated Hosts
- single tenant isolation
- exclusive use of resources
- only your VMs run on a given host
- when provisioning, must specify data center and pod
- then assign instances to the host
- maximum control over workload placement
- often used to meet compliance, laws, and lisencing terms

## Bare Metal Servers
- is a single tenant, dedicated physical server. In other words, it's dedicated to a single customer.
- The Cloud provider actually takes the physical server and plugs it into a rack in a data center for customers.
- The Cloud provider manages the server up to the OS
- preconfigured or custom-configured
- can add GPUs: for accelerating scientific computation, data analytics, and rendering professional grade virtualized graphics
- take longer to provision
- tend to be more expensive
- not all providers grant bare metal servers
- Characteristic/workloads: no hypervisor required
![image](https://github.com/user-attachments/assets/d2baf915-6859-4444-9e6d-7eadadf21876)
- Since there is no sharing underlying server hardware with other customers, bare metal servers fulfill the demanding needs of high-performance computing or HPC, and data intense applications that require minimal latency related delays.
- These servers also excel in big data analytics applications and GPU-intensive solutions.
- Some workload examples that bare metal servers satisfy are ERP, CRM, AI, deep learning, and virtualization.
![image](https://github.com/user-attachments/assets/766ad9b6-e17b-4a78-aa73-2fa1e95bcca6)

## Secure Networks in Cloud
![image](https://github.com/user-attachments/assets/0c3bac81-8745-4fd2-a165-32b68b5e14d0)
![image](https://github.com/user-attachments/assets/c1c21a04-0ffa-49ec-bbd2-993310170352)

- Cloud networks are deployed in networking spaces that are logically separated segments of the networks using options including Virtual, Private Cloud, or VPC that in turn can be divided into smaller segments called subnets. Logically segmented cloud networks are private carveout of the cloud that offer customers the security of private clouds and the scalability of public clouds. Cloud resources such as VMs or Virtual Server Instances, VSIs, storage, network connectivity, and load balancers are deployed into subnets.
  -  Subnets are also the main area where security is implemented in the Cloud. Every subnet is protected by access control lists or ACLs that serve as a subnet-level firewall.
  -  Within the subnet, one could create security groups that provide security at the instance level, such as VSIs. Once you build a subnet, then it is time to add some VSIs and storage to it so that you could run your applications.
  -  Then you can group each VSI into security groups
  -  for web facing VSIs, use can use a public gateway and VPN gateways for securely gaining access to the internet for these VSIs
