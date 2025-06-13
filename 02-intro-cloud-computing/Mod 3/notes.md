# Notes for section 2 / mod 3: Cloud Infrastructure

# Infrastructure Overview
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
- Direct Connectivity: high-speed direct link from enterprise to cloud
- Building a Cloud Network entails creating a set of logical constructs that deliver networking functionality that is akin to the data center networks that all IT professionals have come to rely on for securing their environments and ensuring high-performing business applications.

## Containers
- Containers are an executable unit of software in which application code is packaged, along with its libraries and dependencies, in common ways so that it can be run anywhere, whether it be on desktop, traditional IT, or the cloud.
- small, fast, portable
- do not need to include a guest OS in every instance because they leverage the host's OS
![image](https://github.com/user-attachments/assets/79976eb7-7515-4df6-bf45-893dd12193ce)
- containers (like Docker):
  - first create a manifest (something that describes the container itself; in Docker, this would be a docker file or Cloud Foundry)
  - next, create an image (Docker image; or for Rocket would be ACI or app container image)
  - lastly, create the container itself (contains all the runtimes, libraries, and binaries needed to run the app)
- within a container (unlike a VM) instead of a hypervisor, you use a runtime engine (like Docker engine) 
- it recognizes and runs all the things in the container for the app to run without using a different VM instance OS each time you need to run the app in a different VM instance

## Summary of Cloud Infrastructure
- Cloud infrastructure consists of data centers, storage, networking components, and computing resources.

- Virtualization is the process of creating a software-based version of physical resources, made possible by hypervisors. 

- A few different types of Virtual Machines can be provisioned on the cloud. These include:

  - Shared or Public Cloud VMs that are provider-managed, multi-tenant deployments that can be provisioned on-demand with predefined sizes

  - Transient or Spot VMs that take advantage of unused capacity in a cloud data center

  - Reserved VMs that allow you to reserve capacity and guarantee resources for future deployments 

  - Dedicated hosts that offer single-tenant isolation

- Bare metal servers are single-tenant physical servers that are dedicated to a single customer. Bare metal servers fulfill the demanding needs of high-performance computing (HPC) and data-intense applications. They are ideal for applications that have a high degree of security or compliance requirements.

- Networking capabilities in the cloud are delivered as a service rather than in the form of rack-mounted devices. Cloud resources such as VMs (or VSIs), storage, network connectivity, and load balancers are deployed into subnets within Virtual Private Clouds (VPCs). Using private and public subnets allows users to deploy multi-tier enterprise applications securely. Load balancers distribute the traffic and allow applications to be responsive.

- Containers are executable units of software in which application code, its libraries, and its dependences are packaged in a common way, so that it can be run anywhere, from desktops, traditional IT, to the cloud. Containers are more lightweight and consume fewer resources than Virtual Machines, helping streamline the development and deployment of cloud native applications. 

# Cloud Storage and Content Delivery Network (CDNs)

## Basics of Storage in Cloud
- Save data files in the cloud
- Physical storage must connect to a storage node
- Cloud storage must connect to a public or private connection
- only pay for what you provision
- higher the read/write speed, higher the cost per gigabyte storage
  
- types of storage:
![image](https://github.com/user-attachments/assets/288da6b7-fbb2-47a7-8fc7-6d2dd6ce5713)
  - direct attached: referred to as local storage, within the same rack, fast, normally only for OS. Ephemeral (temporary), not shared with other nodes, its not as resilient
![image](https://github.com/user-attachments/assets/019e6306-f7fa-45a2-ba74-ad4f1321ca61)
  - file storage: NFS (network file system) - slower, use ethernet network, cheaper, attach to multiple servers, good for file systems
![image](https://github.com/user-attachments/assets/cde0a5c2-241d-4bc3-8b71-f05a6c2df471)
  - block storage: high speed fiber connections, faster read/write, good for DBs, stores in volumes, then mounted on a compute node which it sees as another HD, volumes can normally only be mount on one node at a time. IOPS (input/outputs operations per sec).
    - persistence (if set that way) when the compute node is ended. Can set to auto delete with the node.
    - can uses snapshots - fast to create, dont require downtime, record only changes to data, cannot recover individual files
![image](https://github.com/user-attachments/assets/26394e31-3abd-4a38-b959-118927ee00dd)
  - object storage: access rather an API (not attached to a compute node). cheapest and slowest read/write, infinite in size to end user, never fills ups (but pay for what you use)
  
## File Storage
![image](https://github.com/user-attachments/assets/d0ac6196-c40b-4ddb-9931-6ae8989468d0)
![image](https://github.com/user-attachments/assets/33de95a9-3468-4009-b748-eceb70647cb5)
- traffic and internet bandwidth can vary the speeds
- usually used where high speeds are not a requirement

## Block Storage
![image](https://github.com/user-attachments/assets/b7daef1c-f146-429e-9939-6ca858bb0baf)
![image](https://github.com/user-attachments/assets/37db39e7-c759-4465-be1d-fe064e6cd1ce)
![image](https://github.com/user-attachments/assets/9d276bbf-459f-45e5-87d5-d6d229e2df6e)
![image](https://github.com/user-attachments/assets/b820a7a0-82ce-4b38-a471-18cdfbcd6714)
![image](https://github.com/user-attachments/assets/155f59b9-e57e-4b77-afc6-34b176a9ac44)

## Object Storage

![image](https://github.com/user-attachments/assets/bc3cc0a5-54eb-4119-a9ae-73ba6b4dde5f)
![image](https://github.com/user-attachments/assets/ed8e3854-8d6d-4f02-bd02-116300bc1fef)
![image](https://github.com/user-attachments/assets/dcae7146-28ad-4b7d-892f-ae7662990999)
![image](https://github.com/user-attachments/assets/c1d7b1f7-dbd0-4352-8742-f3685132e712)
![image](https://github.com/user-attachments/assets/8e5234a6-7be9-402a-99c0-cc36b36c122f)
- buckets similar to a folder, but cannot be store in other buckets
![image](https://github.com/user-attachments/assets/a311dd0f-a3d4-483e-a9b8-09fb12547fd3)
- service provider manages resilience and ensures the buckets are highly available
![image](https://github.com/user-attachments/assets/5c0d05ed-0e38-481e-aa7d-5ef2918f9c43)
![image](https://github.com/user-attachments/assets/5a275449-2423-4844-b68b-6c584f5833ec)
![image](https://github.com/user-attachments/assets/8fc5b8c0-1383-4d24-9c67-f2c5806bd65e)

### Object Store - Tiers and APIs
- buckets are broken into tiers (or classes) depending on how frequently the data is accessed
![image](https://github.com/user-attachments/assets/742f61ec-2f0b-456e-9764-2fcd71c6016d)
![image](https://github.com/user-attachments/assets/e20c762a-1490-4a01-9db4-1e9ba41844fb)
![image](https://github.com/user-attachments/assets/7c71d844-bd8a-4e88-a936-9f9b1d550936)
![image](https://github.com/user-attachments/assets/c18d1eea-7035-43fd-88e1-400de700f5cc)
- uses objects metadata to determine when it should be archived
![image](https://github.com/user-attachments/assets/c6459419-6774-4b52-86fb-9b492c82a6cf)
![image](https://github.com/user-attachments/assets/af178e1b-479a-4cc2-ac57-9a30db2a9756)
![image](https://github.com/user-attachments/assets/0d1c42d8-154c-49de-82b9-e4fdecb4e927)
![image](https://github.com/user-attachments/assets/860c1055-9bd1-462f-819d-2f5b150b41ce)
![image](https://github.com/user-attachments/assets/afd1e83c-f959-4243-ba64-c2bdf6a95121)

### Content Delivery Network (CDN)
- just like a AWS edge location.
- used cached (AKA copies) of website content to user's based on geographic locations, closing the distance between content and end-users.
![image](https://github.com/user-attachments/assets/82146725-1739-4315-89d7-7f29a8f8ccb4)

## Summary of Cloud Storage
- Cloud storage is available in four main types–Direct Attached, File, Block, and Object Storage. These storage types differ in how they can be accessed, the capacity they offer, how much they cost, the types of data they are best suited to store, and their read-write speed.

- Direct Attached (or Local) Storage is storage that is presented directly to a cloud-based server and is effectively either within the host server chassis or within the same rack.

- File Storage is typically presented to compute nodes as a Network File System (NFS), which means that the storage is connected to compute nodes over a standard ethernet network.

- Block Storage is presented to compute nodes using high-speed fiber connections, typically provisioned in volumes, which are mounted onto a compute node.  

- Object Storage is accessed via an API and doesn’t need an underlying compute node. 

- Object Storage offers infinite capacity as you can keep adding files to it and just pay for what you use. Compared to the other storage types, object storage is slowest in terms of read and write speeds. 

- A Content Delivery Network (CDN) is a distributed server network that accelerates internet content delivery by delivering temporarily stored or cached copies of website or media content to users based on their geographic location. 
