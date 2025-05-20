# Notes for Mod 2: Web and Cloud Development

## ✅ Topics Covered
- [x] Overview
- [x] Front-End Development
- [x] Back-End Development

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
