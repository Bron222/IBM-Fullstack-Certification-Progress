# Notes for Mod 4: Software Architecture, Design, and Patterns

## ✅ Topics Covered
- [x] Overview
- [x] Software Design and Modeling
- [x] OOAD
- [x] Architectures




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
- Peer-to-peer: arch consists of a decentralized network of nodes that behave as both client and server
- Microservices: archs have apps composed of several loosely coupled services that communicate using APIs
- Event-driven: archs have consumers that send requests to producers
- two-tier: have clients that commnciates with a server
- three-tier: consist of 3 tiers - presentation, application, and data  

![image](https://github.com/user-attachments/assets/277099c5-fb37-4818-a43b-f58844425b30)  
![image](https://github.com/user-attachments/assets/c2688cab-cb33-417a-8100-d32219cec200)  
![image](https://github.com/user-attachments/assets/4fdeabee-45e9-4f19-9988-05ae67101326)
![image](https://github.com/user-attachments/assets/b3ddaa03-dbb3-4c2c-a58f-fe5f1db2763e)
![image](https://github.com/user-attachments/assets/d354fec9-7d86-4ec4-93bf-607968018d97)  

## App Arch

- Components:
![image](https://github.com/user-attachments/assets/b799057b-9f0c-44f4-8e18-fdd8e8623921)  

- component examples: API, Data Access Object, Controller
