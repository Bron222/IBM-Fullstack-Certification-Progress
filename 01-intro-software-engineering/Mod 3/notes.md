# Notes for Mod 2: Web and Cloud Development

## ✅ Topics Covered
- [x] Interpreted and Compiled Languages
- [x] High lang vs low lang
- [x] database lang
- [x] Programming logic and structures
- [x] Functions
- [x] Objects




# Notes

## Programming Languages
- interpreted Lang
  - scripting lang.
  - operates through interpreter on comp or browser
  - ex: JS, Python, Lua (game scripting), HTML
- Compiled Lang
  - programs are packaged/compiled into 1 executable file, usually larger, often used locally on a computer
  - programming lang
  - run faster and more repeatablyi
  - ex: C, C++, C#, Java

- High level langs
  - more sophisticated
  - common English
  - ex: SQL (Structured Query Language), Pascal, Python

- Low level langs
  - more sophisticated
  - used simple symbols to represent machine code (0s and 1s)
  - assembly: closely tied to CPU architecture; each CPU type has its own assembly lang
  - ex: ARM, MIPS, X86
  - simple readable format, entered one line at a time, one statement per line
  - {label} mnemonic {operand list} {;comment}
  - mov TOTAL, 212
  - assembly translated by an assembler using mnemonics like: input (INP) output (OUT) load (LDA) store (STA) add (ADD)

- Query Lang
   - request send to a database 
   - SQL, AQL, CQL datalog, DMX
   - CRUD: create read update delete

 - NoSQL
    - (Not Only SQL) a non-relational DB, whereas SQL is relational

 - query statements
    - select, where, order by, update, insert into, alter table, create, drop, sum, count, avg
    - SELECT * FROM table_name;

- CODE ORGANIZATION METHODS
    - organizing code: Pseudocode vs Flowcharts
        - FlowChart programs include: Microsoft Visio, Lucidchart, Draw.io, DrawAnywhere

## Programming Logic and Constructs
- boolean logic: true / false
- variables: value that can change
- braching logic:
    - decision making, no limit to complex branching
- if/then/else statement, switch statement (selection control construct), loop
- loops: for loop, while loop, do-while (exit controlled loop) loop

- identifiers: store value, method, interfaces, classes
    - constant or variable
        - contants are defined when declared
        - easy of readability, only need to change in one place
        - Variable: can change; best for values that is unknown to you
        - containers: special type of indentifier to reference multiple program elements
            - no need to create a variable for every  element
            - faster and more effecient
            - Arrrys and Vectors
                - Array:
                - fixed number of elements stored in sequental order, starting at 0
                - specify the max number of elements it can contain
                - int my_array [50];
            - Vector:
                - dynamic size, change sizes when adding or subtracting elements; "dynamic arrays"
                - take up more memory than array, and longer to access data within (not store sequentially)
                - vector <int> my_vector;

## Function
- structured modular code that is reusable.
    - also called methods, procedures, subroutines, modules
- types of functions
    - standard library functions - built in functions
    - user identified functions
- using functions
    - define the function
    - call the function
    - delcare a function (some cases like c, c++)
 
## OBJECTS
- used in OOP
- contain data in the form of attributes, and code in the form of procedures (methods)





































































