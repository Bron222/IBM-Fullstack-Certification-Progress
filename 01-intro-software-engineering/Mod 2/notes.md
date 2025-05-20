# Notes for Mod 2: Web and Cloud Development

## ✅ Topics Covered
- [x] Overview
- [x] Front-End Development
- [x] Back-End Development
- [x] Frameworks / Libraries / Tools / APIs
- [x] Teams / Squads
- [x] CI/CD / Packages
- [x] Hand-on Lab




# Notes

## Webpage basics
- HTML - format / page structure
- CSS - flare / style
- JavaScript - interactivity and dynamic content

- Static vs Dynamic
 - Static - websites whose elements are stored (or previously stored) on the server
 - dynamic - generated each time they are requested by the client. can involve information from other systems and app like DBs
 - most websites have elements of both

- CLoud apps
 - similar to websites, request content that a server returns
 - build to work seamlessly with a cloud-based back-end infrastructure
 - contain cloud-based data storage and data processing, and other cloud services, making them scalable and resilient

- Front-end: what the client see and interacts with. HTML, CSS, JS, related frameworks/tools
- back-end: deal with the server before the code and data are sent to the client, handles the logic and funct. and authentication processes that keep data secure, back-end dev also work with DBs
- Full stack do both environments

- Tools
  - code editor
  - IDE (integrated dev enviornment)
  - IDE integrates with management and storage like GitHub
 
## Front-End Dev
- HTML
- CSS
- JS - OOP language
- SASS - Syntactically Awesome Style Sheets: An extension of CSS that is compatible with all versions of CSS, enable you to use things like variable, nested rules, inline imports to keep things organized
- SASS allows you to create style sheets faster and more easily
- Learner Style Sheers (LESS): enhances CSS, adding more styles and functions, backwards compatible with CSS
  - Less.js is a JS tool that converts the LESS styles to CSS styles
 
 Reactive or adaptive websites display the version of the website designed for a specific screen size.
- A website can provide more info if opened on a PC than when opened on a mobile device

- Responsive Design of a website means that it will auto resize to the device.
- will change sizes to the screen and still show you all the features

#### JS Frameworks
  - Angular Framework - open-source framework by Google. Allows websites to render HTML pages quickly and effeciently
    - built in tools for routing and form validation
  - React.js - by Facebook, is a JS library that builds and renders components for a web page
    - routing is not a part of this framework and will need to be added by 3rd party tool.
  - Vue.js - by community, focus is the view layer which includes user interface, buttons, visual components
    - flexible, scalable, and integrates well with other frameworks.
    - very adaptable - it can be a library, or it can be a framework

## Back-End Dev
- creates and managees resources needed to respond to client requests
- enables serves infra. to process requests, supply data and provide other services securely
- process the data you enter: login info, product searches, payment info
- write the parts of the app that process the inputs

#### APIs, routing, and endpoints
- requesting image, fill out form, input sensitive info all require a different service from the back-end server
- APIs, routes, and endpoints process requests from the front-end
- API - code that works with data - usually using .json or .xml
 - have set rules and structure
 - provide a way for Cloud Apps to access resources from the back-end
- Route - path to a website or page
- endpoint - may be an API or route
- Back-end devs create routes to direct requests to the correct service

#### Back-end languages and frameworks
- JavaScript
 - Frameworks: Node.js and Express
- Python: wide functionality
 - Frameworks: Django and Flask
- DBs: use SQL and ORM (Object Relational Mapping)

- Teamwork and Squads
 - squads - use agile, small team of up to 10 devs
 - squads - squad leaders, product devs, UX devs or designers
 - squads may practice in pair programming

- Pair Programming
  - 2 devs / 1 computer - work side by side on one computer either physically or shared screens /virtually
  - type of agile dev technique
  - styles: driver / navigator - driver types the code - nav review code as it's written
  - ping pong style: dev 1 writes the test, dev 2 writes code to pass the test, swap roles regularly
  - Strong style - pair a junior with experience dev. Senior is the navigator. Junior learns and driverr
  - benefits: shared knowledge, build soft skills, fewer typos/bugs/logical errors, code review on the fly, identify optimal solution early on, overall effeciency
  - Challenges: long periods of focus/exhausting, personal/work commitment issues, one person taking control, personality clash, noisy environment

## Application Development Tools
- Tools for Cloud app dev: Version control, libraries, frameworks
- Version Control: track changes (who/when/what), resolves change conflicts, creates a way to revdert to an older version

#### Libraries
- Libraries - collections of reusable code
- Multiple code libararies can be integrated into a project and help solve specific problems
- use anytime

#### Frameworks
- Frameworks - provide standard way to build and deploy applications
- like a skeleton you extend by adding your own code
- should be used from the beginning. new frameworks can't be added into an existing project. needs to be use at the beginning of project
- dictates the architecture of the app
- specific structure you must follow
- Framework calls on your code
- less control, more standardization and effieciency
- AngularJS - Js Framework for dynamic web apps
- VUE.js - JS Framework for user interface
- Django - Python framework for web development
- Inversion of Control - makes the framework extensible. Makes you feel like you have less control over development
- Frameworks with lots of control are called "Opinionated"
- Frameworks sometimes used their own libraries

#### CI/CD
- continuous integration with continuous delivery / continous deployment
- enable developers to deliver frequent changes reliably
- implemented through a build-automation server
- CI auto builds and tests code
- CD deploys the changes

#### Build tools
- transform source code into binaries for installation 
- Important in environments with many inter-connected projects and multi-developers
- Automate tasks like: downloading dependencies, compiling into binary, packaging that binary code, running tests, deployment to production systems
- Initiate a build rom the command line or from an IDE
- Two categories that widely use: build-auto utilities & build-auto servers
- ex: webpack - module bundler for JS
- ex: Babel - JS compiler
- ex: Web Assembly - binary instruction format that runs in browser

#### Packages
- make apps easy to install
- contain app files and instructions for install
- metadata
- Once bundles into package, use PACKAGE MANAGER to distrubte it
- Package Managers - make working with packages easier, coordinate with file archivers to extract package archives, verify checksums and digital certs to ensure integrity and authenticity, locate/download/install/update existing software from a software repository, manage dependencies to ensure a package is installed with all packages it requires
- Linux examples of package managers:
  - ex: Debian Package Management System (DPKG)
  - Red Hat Package Manager (RPM)
- Windows:
  - Chocolately
- Android:
  - Package Manager
- MacOS
  - Homebrew
  - MacPorts

- Libraries and uitility code are managed with cloud app package managers
Node.js/JS: npm
Java: Gradle, Maven
Ruby: RubyGems
Python: Pip, Conda

#### Software Stacks
- upper portion of stacks interact with user
- lower portion interact with hardware
- typically include: front-end tech, back-end tech
- Parts / Layers: Presentation layer, logic layer, data layer, (security layer, virtualization layer, orchestration layer <-- if more complex)
- can be made up of internal sources, 3rd party, or cloud technologies, no formal definition
- can use all of a stack or just parts you need

- popular stacks:
  - Python-Django
  - Ruby on Rails
  - ASP .NET
  - LAMP, MEAN, MEVN, MERN

- LAMP stack: Linux, Apache, MySQL, PHP
  - early example of stack, loosely coupled, so can interchange techs easily
- MEAN stack: MongoDB, Express.js, Angular.js, Node.js
  - platform agnostic, free/open-source, React - MERN, Vue.js - MEVN

- COMPARE:
  - MEAN: all just JS, lots of docs and resuable code, not suited for large-scal apps or relational DB
  - MEVN: similar to MEAN, WEB stack, Less reusable libraries
  - LAMP: lots of resuable code and support, only on Linux, isn't as flexible as MERN/MERV, not suited for non-realtional DB, uses different languages


## HANDS-ON LAB
- used Skills Network Cloud IDE to create and run a simple Python app
 - In this lab, you will become familiar with using an Integrated Development Environment (IDE). The IDE that you will be using is called Skills Network Cloud IDE which is based on an open-source project called Theia. This IDE is very similar to the popular Visual Studio (VS) Code IDE. In this lab, you will explore the IDE and use it to create and run a simple Python application. You will create a code file, save it, and edit it to make changes.




















































































