# Mini C++ Compiler showing if-else, for loop

Our problem statement is to design and implement a compiler for a simple programming 
C++-like language using the Lex and Yacc compiler generating packages and a simple GUI 
using C++. 

This project for a Mini Compiler for the C++ programming language was made for the course title Compiler Design. The project focuses on generating an intermediate code for the language for specific constructs. It works for constructs such as conditional statements, loops, and the ternary operator. The main functionality of the project is to generate an optimized intermediate code for the given C++ source code. This is done using the following steps:

* Generate symbol table after performing expression evaluation 
* Generate Abstract Syntax Tree for the code 
* Generate 3 address code followed by corresponding quadruples 
* Perform Code Optimization 

<p> The main tools used in the project include LEX which identifies predefined 
patterns and generates tokens for the patterns matched and YACC which parses the input 
for semantic meaning and generates an abstract syntax tree and intermediate code for the 
source code. PYTHON is used to optimize the intermediate code generated by the parser. </p>

## DESIGN STRATEGY
 ### SYMBOL TABLE CREATION
In our symbol table, we have handled error detection as well as expression evaluation. We 
have also covered handling undeclared variables, detecting redeclaration of variables, and 
syntax errors like semicolon missing.

### INTERMEDIATE CODE GENERATION
Intermediate code generator receives input from its predecessor phase, semantic analyser, 
in the form of an annotated syntax tree. That syntax tree then can be converted into a 
linear representation. Intermediate code tends to be machine independent code.

###  CODE OPTIMIZATION
The code optimizer maintains a key-value mapping that resembles the symbol table 
structure to keep track of variables and their values (possibly after expression evaluation). 
This structure is used to perform constant propagation and constant folding in sequential 
blocks followed by dead code elimination.

### ERROR HANDLING
As part of our syntax validation, we have made use of an abstract syntax tree. Abstract 
syntax trees are data structures widely used in compilers to represent the structure of 
program code. An AST is usually the result of the syntax analysis phase of a compiler. It 
often serves as an intermediate representation of the program through several stages that 
the compiler requires, and has a strong impact on the final output of the compiler.
Here, our tree that is representing the syntactic flow of our code is generated.
We have made use of %left and %right fields (types of grammar symbols)
We made use of the AST so that we can separate the parsing and validation logic from the 
implementation piece. We used the AST as part of our syntax validation phase so that when 
there is a problem parsing some strange syntax you can just look at the AST parser, where if 
a piece of code is not producing the expected results than you look at the code that 
interprets the AST.

# Team Members
1. Sunad Suhas
2. Eshan Naik
3. Ishita Datta


