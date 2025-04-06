# Custom Compiler Project

## Overview
This repository documents a custom compiler project I developed as part of CSE 340 - Principles of Programming Class at ASU. The project involved building a complete compiler for a simple programming language that generates an intermediate representation (IR) which is then executed by an interpreter.

⚠️ **Note:** Due to academic integrity policies, the actual source code for this project cannot be shared publicly. However, this documentation provides comprehensive details about the project's architecture, implementation approach, and features. If you're interested in discussing this project in more depth, please feel free to contact me at smitdesai129@gmail.com.

## Project Accomplishments
- ✅ Designed and implemented a fully functional compiler
- ✅ Created a custom lexical analyzer for tokenizing input programs
- ✅ Built a parser to generate an intermediate representation
- ✅ Implemented an execution engine that interprets the IR
- ✅ Successfully handled various statement types (assignment, if, while, switch, for)
- ✅ Received a perfect score on the project evaluation

## Language Features
The compiler supports a simple programming language with the following features:

- **Variables and Assignments**: Integer variables with assignment operations
- **Arithmetic Operations**: Basic arithmetic operations (+, -, *, /)
- **Control Flow Statements**:
  - `if` statements with boolean conditions
  - `while` loops
  - `switch` statements with multiple cases
  - `for` loops with initialization, condition, and update expressions
- **I/O Operations**:
  - `input` statements for reading integer values
  - `output` statements for displaying values

## Compiler Architecture

### 1. Lexical Analyzer
- Processes the input program and breaks it down into tokens
- Identifies keywords, identifiers, operators, and literals
- Handles whitespace and comments
- Reports lexical errors

### 2. Parser
- Implements a recursive descent parser
- Builds syntax trees for program statements
- Validates program structure according to the language grammar
- Creates intermediate representation nodes

### 3. Intermediate Representation (IR)
- Represents the program as a linked list of instruction nodes
- Each node contains:
  - Instruction type (NOOP, ASSIGN, JMP, CJMP, IN, OUT)
  - Operand indices
  - Additional metadata specific to each instruction type
- Special handling for control flow statements using conditional jumps

### 4. Execution Engine
- Traverses the IR node by node
- Maintains a memory model for variable values
- Executes each instruction based on its type
- Handles jumps and conditional execution
- Produces the program output

## Implementation Highlights

### Control Flow Handling
- **If Statements**: Implemented using conditional jumps (CJMP)
- **While Loops**: Created using a combination of conditional jumps and unconditional jumps
- **Switch Statements**: Implemented as a series of conditional jumps with appropriate targets
- **For Loops**: Structured as a combination of assignment, conditional check, body execution, and update statements

### Memory Management
- Variables stored in an indexed memory array
- Constant values handled efficiently
- Location table maintains mapping between variable names and memory locations

### Notable Challenges Overcome
- Implementing proper nesting of control structures
- Handling complex boolean expressions in conditions
- Designing an efficient intermediate representation
- Managing jump targets in the linked instruction list
- Supporting both direct and computed memory addresses

## Project Grading
The project was evaluated based on the following criteria, with a total score of 100/100:
- Assignment statements: 20/20
- If statements: 20/20
- While statements: 30/30
- Switch statements: 20/20
- For statements: 10/10

## Learning Outcomes
Through this project, I gained valuable experience in:
- Compiler design principles and implementation techniques
- Language parsing and grammar specification
- Intermediate code generation strategies
- Execution semantics and memory management
- Testing and debugging complex systems

## Future Enhancements
If this were to be extended, potential improvements could include:
- Support for additional data types (strings, floats, arrays)
- Function definitions and calls
- Optimization passes on the intermediate representation
- Error recovery mechanisms
- A more sophisticated type system

## Contact
For more information about this project or to discuss compiler design in general, please reach out to me at smitdesai129@gmail.com.
