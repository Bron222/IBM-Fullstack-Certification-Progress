# Notes for mod 1
## ✅ Topics Covered
- [x] Software Engineer vs. Developer
- [x] SDLC
- [x] Building Quality Software

## Notes
- Engineer focuses more on design aspects, larger picture
- Developer focuses on feature management

# SDLC
- SDLC phases: 1. Planning 2. Design 3. Development 4. Testing 5. Deloyment 6. Maintenance
- Planning: requirement are gathered, analyzed, documented, prioritized. 
  - May produce prototypes to get requirements. 
  - Create the Software Requirements Specification (SRS document).
- Design: software architecture is developed and reviewed. 
  - Prototypes can be disigned. 
  - Design document created.
- Development: Start coding process using design document.
- Testing: Code is tested for stability, security, and meets requirements from the SRS. 
  - Bugs are reported, tracked, fixed.
- Deployment: launched to production environement users.
  - user acceptance testing (UAT).
  - after sign-off of customer, it is released to production.
- Maintenance: support, fix other bugs, code enhancements, new or change requirements, feedback.

- system requirements are classified:
  - Functional
  - external & user interface
  - system features
  - nonfunctioanl
 
- Quality code attributes:
  - Maintainability
  - Readability
  - Testability
  - Security
  - Well documented, clean and consistent, effiecent, without defects, follows coding standards
  - use linters to dected errors

- Testing:
  - Unit testing: testing small snippet of code
  - Integration test: testing that unit when merged with product
  - UAT or Beta testing

- Releases:
  - Alpha: first functioning version, may contain errors, design changes may occur, select stakeholders
  - Beta: all stakeholders, user testing, meets requirements
  - General Availability: Stable, all users
 
- Documenting:
  - system docs - explains how the system works, maintenance, README files, inline comments, arch and design, (technical documents)
  - User docs - user guides, instructional vids, manuals, online and inline help (non tech docs)

# Models of Software development
- Waterfall method

- v-shaped model - sequential like waterfall. 
  - plan, system design, architecture design, module design, coding (the point of the V), unit testing integration testing, system testing, acceptance testing
  - verification going down to coding, then up with validation

- agile - iterative approach. teams work in cycles with sprints with tesing during for assurance.
  - plan, design, develop, test, deploy, feedback, back to plan again. Sprint demo happens to show stakeholders
  - MVP - minimum viable product - developed so stakeholders can give feedback

  # Software versions
  - version numbers - vary in length and meaning
  - indicated when it was released, if it was updated, patched, etc.
  - betas can be before one 0.9
  - some use dates in versioning
  - semanitc numbering has 4 parts
    - 1: major software changes
    - 2: minor changes (possibly updates)
    - 3: patches or bug fixes
    - 4: indicated build numbers, dates, less sigificant changes
  - in about section of software

# Software testing
- functional testing: black box testing - testing without touching the code. only concerened with input and outputs of the test. can be manual or automated. testing the application, system under test (SUT)
- non-functional testing: tests performance, security, scallability, availability
  - how does it the software behave under stress, what happens when many users log in at once, are instructions consistent with behavior
  - does it behave the same in diferent OS
- Regression testing: tests if bug fixes don't break the application, occurs after fixes occur

- TESTING LEVELS
  - Unit: test a moduke of code, tested during dev phase, eliminatate construction erros before integration with other modules
  - integration: seeks erros with two modules are combined. other kind of black box testing. Occurs after integrated to system to ensure bugs don't occur
  - system: occurs after integration testing and is conducted on a complete integrated system to ensure the system meets all requirements, validates it as a completed product, completed in a staging environment
  - acceptance: formal testing with respect to users, customers, and stakeholder to meet their requirements and needs
