<<<<<<< HEAD
# Notes for Mod 4: Software Architecture, Design, and Patterns
=======
# Notes for mod 5: Software Engineering
>>>>>>> 75d3029a2a7ec1b7a26b95465021cecfc63146e1

## ✅ Topics Covered
- [x] Overview
- [x] Software Design and Modeling
- [x] OOAD
- [x] Architectures

<<<<<<< HEAD



# Notes

## Software Architecture and Design

- why is it important?
    - communication, earliest deign decisions, flexibility, increases lifespan
 
- software deign is a process to document:
    - structural compenents
    - behavioral attributes - describes what the system does, but not how - UMLs can do this (state transition diagram and interaction diagram)
- expressed using diagrams/flowcharts/UML
- structural elements: modules and sub modules
    - cohesive and loosely coupled
        - cohesive: all funtionally related elements are grouped together
        - loosely coupled: modules are weakly associated so changes in one have minimal effect on others
        - 
![image](https://github.com/user-attachments/assets/f514bc50-0f4c-4a5d-a1e0-1fce9a733e39)

- Unified Modeling Language (UML): visual representations to communicate arch, design, and implementation
    - can be structural or behavioral
    - programming language agnostic
    - advantages: plans, comunicates, saves time/money, bring team up to speed quickly, navigate source code
    - 
![image](https://github.com/user-attachments/assets/30248a4f-c7b3-4763-aa45-b60683c269ad)  
![image](https://github.com/user-attachments/assets/cf8a6230-0860-43c1-949e-2e21730dd927)  

## Object-oriented analysis and design (OOAD)
- OOP languages: C++. Java, Python
- objects contain data and perform actions
- Classes: blueprint for an object
- Properties/attributes/fields(variables): objects data
- Methods: object's actions
- instantiation: instance of an object is created  

- OOAD allow devs to work on different aspects of the same app at the same time
- Class diagram (UML)

![image](https://github.com/user-attachments/assets/8126b239-51f8-409d-a49c-05ce349280de)  

- subclasses: inheret the data/methods of their parent classes (the superclass)

## Architectures
- are not mutually exclusive entirely. can be combined to a degree given the restraints of logic
- Peer-to-peer: arch consists of a decentralized network of nodes that behave as both client and server
- Microservices: archs have apps composed of several loosely coupled services that communicate using APIs
- Event-driven: archs have consumers that send requests to producers
- two-tier: have clients that commnciates with a server
- three-tier: consist of 3 tiers - presentation, application, and data  

![image](https://github.com/user-attachments/assets/277099c5-fb37-4818-a43b-f58844425b30)  

- Microservices are an approach to building an application that breaks its functionality into modular components called services. An application programming interface, also called an API, is the part of an application that communicates with other applications. An API defines how two applications share and modify each other’s data. APIs can be used to create a microservices-based architecture. The API Gateway routes the API from the client to a service. Orchestration handles communication between services.
    - ex: social media sites

![image](https://github.com/user-attachments/assets/c2688cab-cb33-417a-8100-d32219cec200)  

- Peer 2 Peer: nodes share resources among each other
- useful for file sharing, collaboration, Instant messageing, and high performance computing
    - ex: Cyrptocurrency

![image](https://github.com/user-attachments/assets/4fdeabee-45e9-4f19-9988-05ae67101326)

- 2 Tier: server hosts most of the resources to one or more clients over a network
    - ex: messaging apps, DB clients connecting with DB servers

![image](https://github.com/user-attachments/assets/b3ddaa03-dbb3-4c2c-a58f-fe5f1db2763e)  

- event: anything that results in a change of state. action that is triggered by end-user or the program.
- Event-driven architecture focuses on producers and consumers of events. Producers listen for and react to triggers while consumers process an event. The producer publishes the event to an event router. The router determines which consumer to push the event to. The triggering event generates a message, called an event notification, to the consumer which is listening for the event. The components in event-driven architectures are loosely coupled making the pattern appropriate for use with modern, distributed systems.
    - Ride sharing app

![image](https://github.com/user-attachments/assets/d354fec9-7d86-4ec4-93bf-607968018d97)  

- 3 Tier (N-Tier): most common - The 3-tier architecture is composed of several horizontal tiers that function together as a single unit of software. A tier only communicates with other tiers located directly above and below it. Related components are placed within the same tier. Changes in one tier do not affect the other tier.
    - ex: web apps: a web server for processing UI, app server to process user input, and DB server for data management  
   

    - presentation tier: user view
    - (firewall starts here)
    - web tier: web load balancer
    - app server tier: app load balancer / proxy server - routes to different app servers
    - DB tier: now the directed app requests data from the DB server \
    - (firewall ends here)
 

## App Arch

- Components:
![image](https://github.com/user-attachments/assets/b799057b-9f0c-44f4-8e18-fdd8e8623921)  

    - component examples:
        - API, Data Access Object, Controller  

- services:
    - designed to be deployed independently and resused by multiple systems. Solution to a business need. Has one uniques, always running instance with whom multplie clients communicate
    - ex: checking a customer's credit, calc monthly loan payment, processing application
    - Service-oriented architecture: loosley coupled services that communicate over a network  

- Distrubted system:
    - multiple services located on different machine and coordinate interactions via a communication protocol (such as HTTP). Appears tot he end-user as a single coherent system
    - characteristics: shared resources, fault-tolerant, multi-activities run concurrently, scalable, runs on a variety of comp (doesn't need same hardware or OS), programmed in various langs.
    - use 1 or more of these archs: client-server, Peer2Peer, 3Tier, microservices 

- Nodes:
![image](https://github.com/user-attachments/assets/e5ef1dfa-58b3-431b-bffe-cc2c2866bf78)  

## Application enviroments
![image](https://github.com/user-attachments/assets/73f828fc-1ffb-4a1c-8a82-a05ad36308b4)  
![image](https://github.com/user-attachments/assets/500a4b0d-8e52-4a3a-9917-23422c80d3cb)
![image](https://github.com/user-attachments/assets/8a25af01-f5a7-4111-8f8c-347d7c865359)
![image](https://github.com/user-attachments/assets/1d83e67c-3cde-4a48-bd67-5fd38b47f2f5)

## Production Deployment Components

![image](https://github.com/user-attachments/assets/91025c5f-b92f-4be0-9f06-d498eaf2cf95)

- firewall: monitors traffic between int and out of networks. permits or blocks data base on set of rules. barrier between networks to block viruses and hackers from accessing internal network
- load balancer: directs netowrk traffic efficiently amongst multi servers
    - prevents overloading of servers

![image](https://github.com/user-attachments/assets/d1225282-e3f6-487f-bbbe-369c55c79087)

- proxy server:
![image](https://github.com/user-attachments/assets/f5b2601f-247f-4bb5-b273-8453da85746a)


=======
#  Notes

## Roles

- Junior
- Senior

- Daily routine: 
- check messages about status of code merge request and get feedback from mentor


-Stand up meetings: 





>>>>>>> 75d3029a2a7ec1b7a26b95465021cecfc63146e1
