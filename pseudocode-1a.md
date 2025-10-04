# Flowchart + ~English Revised: Iterative Pseudocode Polyglot

A metalanguage for algorithm design, visualization, and print debugging that combines executable natural language programming with flowchart semantics.

## Overview

This system is an **iterative pseudocode polyglot** that merges two esoteric programming languages:

- **[~English Revised](https://esolangs.org/wiki/~English)** - Natural language programming with executable syntax
- **[Flowchart](https://esolangs.org/wiki/Flowchart)** - Visual flowchart-based programming

The result is self-documenting pseudocode that describes algorithm behavior while being executable for print debugging.

## Key Features

- ✅ **Executable Documentation** - Code that runs and explains what it does
- ✅ **Algorithm Visualization** - Maps directly to flowchart diagrams
- ✅ **Print Debugging** - Traces execution by describing operations
- ✅ **Teaching Tool** - Ideal for algorithm education and understanding
- ✅ **Literate Programming** - Code and documentation unified

## File Type System

Every file begins with a type declaration showing source format and build output:

```
Note: File Type: source: <source-type> → build: <build-type>
```

### Source File Types

```
source: c-txt       = C source code (text)
source: h-txt       = C header file (text)
source: py-txt      = Python source code (text)
source: m-txt       = Makefile (text)
source: md-txt      = Markdown documentation (text)
source: dev-ini-txt = Embarcadero Dev-C++ project file (text)
source: lay-ini-txt = Embarcadero Dev-C++ layout file (text)
source: gny-ini-txt = Geany IDE project/config (text)
```

### Build Output Types

```
build: exe-hs-bin   = Executable program (header-structured binary)
build: lib-hs-bin   = Static Library (header-structured binary)
build: dll-hs-bin   = Dynamic Link Library (header-structured binary)
build: none         = No build output (source only)
```

**Structure Notation:**
- `hs` = Header-Structured (metadata at start)
- `fs` = Footer-Structured (metadata at end)
- `bin` = Binary format
- `txt` = Text format

## Command Reference

### Control Flow Commands (CF)

Mapped to traditional flowchart symbols:

#### Terminal Operations
```
CF-()-s    = ● Terminal Start Oval (program entry point)
CF-()-e    = ● Terminal End Oval (program exit point)
```

#### Process Operations
```
CF-[]      = ▭ Process Rectangle (general computation/operation)
CF-clr-<>  = ▭ Clear/Reset Operation (memory/state clearance)
```

#### Data Operations
```
CF-//      = ▱ Input Parallelogram (receive data from external source)
CF-\\      = ▱ Output Parallelogram (send data to external destination)
```

#### Decision Operations
```
CF-<>      = ◇ Decision Diamond (binary true/false conditional)
CF-swch-{} = ◇ Switch Statement (multi-way branch with cases)
```

### Data Structure Commands (DS)

#### Stack Operations
Stack operations use register semantics with the currently selected deque:

```
DS-s-\[ ]/  = Push Top (clear register, push value to top)
DS-s-/[ ]\  = Push Bottom (clear register, push value to bottom)
DS-s-\{ }/  = Pop Top (clear register, pop top value to register)
DS-s-/{ }\  = Pop Bottom (clear register, pop bottom value to register)
```

#### Queue Operations
```
DS-q-<]  = Queue Switch Left (select previous deque in circular buffer)
DS-q-[>  = Queue Switch Right (select next deque in circular buffer)
```

#### Other Data Structures
```
DS-a   = Array (indexed linear collection)
DS-h   = Hash Table (key-value mapping)
DS-ll  = Linked List (node-based sequential collection)
```

### Combined Command Patterns

Commands can be combined with `+` to show multiple operations:

```
CF-[] + DS-s + DS-a           = Process using stack and array
CF-[] + DS-s-\[ ]/            = Process with push to stack top
CF-[] + DS-s-\{ }/            = Process with pop from stack top
CF-swch-{} + DS-a + DS-s-\{ }/ = Switch with array and stack pop
```

## Syntax Guide

### ~English Revised Syntax

#### Basic Statements

```
Display "text" and a newline.              # Output
Create variable_name.                      # Variable declaration
Set variable_name to value.                # Assignment
Stop the program.                          # Program termination
```

#### Control Structures

```
While condition:                           # Loop start
    statements
That's all.                                # Loop end

For each item in collection:               # For-each loop
    statements
End for.                                   # Loop end

If condition:                              # Conditional
    statements
Else:                                      # Else clause
    statements
That's all.                                # Conditional end
```

#### Comments

```
Note: This is a comment
```

### Annotation Format

Each line of executable code should have aligned annotations:

```
Display "CF-()-s Program Started" and a newline.    # CF-()-s
While calculator is running:                        # CF-<> + DS-s
    Display "CF-[] Processing" and a newline.       # CF-[] + DS-a
End while.
```

**Alignment Rules:**
- All `#` symbols vertically aligned in right margin
- Consistent spacing for readability
- Annotations describe flowchart operations

## Example: RPN Calculator

```
Pseudocode for file rpn_calculator.c (begins here)
Note: File Type: source: c-txt → build: exe-hs-bin

To demonstrate rpn calculator in c:                            # CF-[] + DS-s + DS-a
    Display "CF-()-s RPN Calculator Started" and a newline.    # CF-()-s
    
    Note: Initialize calculator state
    Display "CF-[] Initialize calculator stack" and a newline.  # CF-[] + DS-s
    
    While calculator is running:                                # CF-<> + DS-s
        Display "CF-<> Continue calculating?" and a newline.
        
        Note: Get user input
        Display "CF-// Enter RPN expression:" and a newline.    # CF-// + DS-a
        Create input_buffer array.                              # DS-a
        Set input_buffer to user input.
        
        For each token in input_buffer:                         # CF-[] + DS-a
            Display "CF-[] Processing token" and a newline.     # CF-[] + DS-a
            
            Note: Number handling - push to stack
            If token is number:                                 # CF-<> + DS-s
                Display "CF-[] DS-s-\[ ]/ Push to stack" and a newline.  # CF-[] + DS-s-\[ ]/
            
            Note: Operator handling - pop operands
            Else if token is operator:                          # CF-<> + DS-s
                Display "CF-[] DS-s-\{ }/ Pop operand2" and a newline.   # CF-[] + DS-s-\{ }/
                Display "CF-[] DS-s-\{ }/ Pop operand1" and a newline.   # CF-[] + DS-s-\{ }/
                Display "CF-[] Perform operation" and a newline.          # CF-[]
                Display "CF-[] DS-s-\[ ]/ Push result" and a newline.    # CF-[] + DS-s-\[ ]/
            That's all.
        End for.
        
        Note: Display final result
        Display "CF-[] DS-s-\{ }/ Pop result" and a newline.    # CF-[] + DS-s-\{ }/
        Display "CF-\\ Output result to user" and a newline.    # CF-\\ + DS-s
    End while.
    
    Display "CF-()-e Calculator terminated" and a newline.      # CF-()-e
    Stop the program.

Pseudocode for file rpn_calculator.c (ends here)
```

## Use Cases

### 1. Algorithm Design
Write algorithms in natural language with structural annotations before implementing in a production language.

### 2. Print Debugging
Execute the pseudocode to see a trace of what operations would occur, helping identify logic errors.

### 3. Documentation
Create self-documenting code that explains both what it does and how data flows through structures.

### 4. Teaching
Help students understand algorithms by showing explicit control flow and data structure operations.

### 5. Code Review
Provide clear algorithmic specifications that reviewers can understand without language-specific knowledge.

## Project Structure

Organize files with folder and file declarations:

```
Fo: project_root/
    Fi: main.c
    Fi: calculator.c
    Fi: calculator.h
    Fo: docs/
        Fi: README.md
        Fi: algorithm_spec.txt
```

**Structure Notation:**
- `Fo:` = Folder declaration
- `Fi:` = File declaration
- `Parent:` = Parent directory context (when needed)

### Complete Multi-Folder Example: Calculator Project

```
Fo: rpn_calculator/
    Fi: README.md
    Fi: Makefile
    Fi: rpn_calculator.dev
    Fi: rpn_calculator.layout
    
    Fo: src/
        Fi: main.c
        Fi: stack.c
        Fi: parser.c
        Fi: evaluator.c
    
    Fo: include/
        Fi: stack.h
        Fi: parser.h
        Fi: evaluator.h
        Fi: common.h
    
    Fo: tests/
        Fi: test_stack.c
        Fi: test_parser.c
        Fi: test_evaluator.c
        Fi: run_tests.py
    
    Fo: docs/
        Fi: architecture.md
        Fi: algorithm_specs.txt
        
        Fo: pseudocode/
            Fi: main_flow.txt
            Fi: stack_operations.txt
            Fi: expression_parser.txt
    
    Fo: build/
        Fi: .gitkeep
    
    Fo: lib/
        Fi: libstack.a
```

#### File: src/main.c
```
Pseudocode for file main.c (begins here)
Note: File Type: source: c-txt → build: exe-hs-bin
Parent: rpn_calculator/src/

To demonstrate main program entry point:                       # CF-[] + DS-s
    Display "CF-()-s Main Program Started" and a newline.     # CF-()-s
    
    Note: Initialize application
    Display "CF-[] Initialize stack module" and a newline.     # CF-[]
    Display "CF-[] Initialize parser module" and a newline.    # CF-[]
    Display "CF-[] Initialize evaluator module" and a newline. # CF-[]
    
    Note: Main program loop
    While program is running:                                   # CF-<> + DS-s
        Display "CF-// Get user input" and a newline.          # CF-//
        Create input_string variable.                           # DS-a
        
        Note: Check for exit command
        If input_string equals "quit":                          # CF-<>
            Display "CF-[] Break loop" and a newline.          # CF-[]
            Break from loop.
        That's all.
        
        Note: Parse and evaluate expression
        Display "CF-[] Call parse_expression()" and a newline. # CF-[]
        Display "CF-[] Call evaluate_rpn()" and a newline.     # CF-[]
        Display "CF-\\ Output result" and a newline.           # CF-\\
    End while.
    
    Display "CF-() Cleanup and exit" and a newline.            # CF-()-e
    Stop the program.

Pseudocode for file main.c (ends here)
```

#### File: src/stack.c
```
Pseudocode for file stack.c (begins here)
Note: File Type: source: c-txt → build: lib-hs-bin
Parent: rpn_calculator/src/

To demonstrate stack_init function:                             # CF-[] + DS-s
    Display "CF-()-s stack_init() called" and a newline.       # CF-()-s
    
    Note: Allocate stack memory
    Display "CF-[] Allocate stack structure" and a newline.    # CF-[]
    Display "CF-[] Set stack->top to -1" and a newline.        # CF-[] + DS-s
    Display "CF-[] Set stack->capacity to MAX_SIZE" and a newline. # CF-[] + DS-s
    
    Display "CF-()-e Return stack pointer" and a newline.      # CF-()-e

To demonstrate stack_push function:                             # CF-[] + DS-s-\[ ]/
    Display "CF-()-s stack_push() called" and a newline.       # CF-()-s
    
    Note: Check if stack is full
    If stack->top equals capacity minus one:                    # CF-<> + DS-s
        Display "CF-\\ Error: Stack overflow" and a newline.   # CF-\\
        Display "CF-()-e Return error code" and a newline.     # CF-()-e
    That's all.
    
    Note: Push value to stack
    Display "CF-[] Increment stack->top" and a newline.         # CF-[] + DS-s
    Display "CF-[] DS-s-\[ ]/ Push value to stack[top]" and a newline. # CF-[] + DS-s-\[ ]/
    
    Display "CF-()-e Return success code" and a newline.        # CF-()-e

To demonstrate stack_pop function:                              # CF-[] + DS-s-\{ }/
    Display "CF-()-s stack_pop() called" and a newline.        # CF-()-s
    
    Note: Check if stack is empty
    If stack->top is less than zero:                            # CF-<> + DS-s
        Display "CF-\\ Error: Stack underflow" and a newline.  # CF-\\
        Display "CF-()-e Return error value" and a newline.    # CF-()-e
    That's all.
    
    Note: Pop value from stack
    Display "CF-[] DS-s-\{ }/ Pop value from stack[top]" and a newline. # CF-[] + DS-s-\{ }/
    Display "CF-[] Decrement stack->top" and a newline.         # CF-[] + DS-s
    
    Display "CF-()-e Return popped value" and a newline.        # CF-()-e

Pseudocode for file stack.c (ends here)
```

#### File: src/parser.c
```
Pseudocode for file parser.c (begins here)
Note: File Type: source: c-txt → build: lib-hs-bin
Parent: rpn_calculator/src/

To demonstrate parse_expression function:                       # CF-[] + DS-a
    Display "CF-()-s parse_expression() called" and a newline. # CF-()-s
    
    Note: Tokenize input string
    Display "CF-[] Create token array" and a newline.          # CF-[] + DS-a
    Create tokens array.                                         # DS-a
    Set token_count to zero.
    
    Note: Split string by whitespace
    While input has more characters:                             # CF-<> + DS-a
        Display "CF-// Read next character" and a newline.      # CF-//
        
        Note: Check token type with switch
        Display "CF-swch-{} Determine token type:" and a newline. # CF-swch-{}
        Display "  Case: Digit (0-9)" and a newline.
        Display "  Case: Operator (+, -, *, /)" and a newline.
        Display "  Case: Whitespace" and a newline.
        Display "  Default: Invalid character" and a newline.
        
        If character is digit:                                   # CF-<>
            Display "CF-[] Parse number" and a newline.         # CF-[]
            Display "CF-[] DS-a Store in tokens[count]" and a newline. # CF-[] + DS-a
            Display "CF-[] Increment token_count" and a newline. # CF-[]
        Else if character is operator:                           # CF-<>
            Display "CF-[] DS-a Store operator in tokens[count]" and a newline. # CF-[] + DS-a
            Display "CF-[] Increment token_count" and a newline. # CF-[]
        That's all.
    End while.
    
    Display "CF-()-e Return token array" and a newline.         # CF-()-e

Pseudocode for file parser.c (ends here)
```

#### File: src/evaluator.c
```
Pseudocode for file evaluator.c (begins here)
Note: File Type: source: c-txt → build: lib-hs-bin
Parent: rpn_calculator/src/

To demonstrate evaluate_rpn function:                           # CF-[] + DS-s + DS-a
    Display "CF-()-s evaluate_rpn() called" and a newline.     # CF-()-s
    
    Note: Initialize evaluation stack
    Display "CF-[] Call stack_init()" and a newline.           # CF-[] + DS-s
    Create eval_stack.                                          # DS-s
    
    Note: Process each token
    For each token in tokens array:                             # CF-[] + DS-a
        Display "CF-[] Processing token" and a newline.         # CF-[] + DS-a
        
        Note: Handle different token types
        If token is number:                                      # CF-<>
            Display "CF-[] Convert to double" and a newline.    # CF-[]
            Display "CF-[] DS-s-\[ ]/ Push to eval_stack" and a newline. # CF-[] + DS-s-\[ ]/
        
        Else if token is operator:                               # CF-<>
            Note: Pop two operands
            Display "CF-[] DS-s-\{ }/ Pop right operand" and a newline. # CF-[] + DS-s-\{ }/
            Display "CF-[] DS-s-\{ }/ Pop left operand" and a newline.  # CF-[] + DS-s-\{ }/
            
            Note: Perform operation based on operator
            Display "CF-swch-{} Select operation:" and a newline. # CF-swch-{}
            Display "  Case '+': Add operands" and a newline.
            Display "  Case '-': Subtract operands" and a newline.
            Display "  Case '*': Multiply operands" and a newline.
            Display "  Case '/': Divide operands" and a newline.
            Display "  Default: Error" and a newline.
            
            Display "CF-[] Perform calculation" and a newline.   # CF-[]
            Display "CF-[] DS-s-\[ ]/ Push result to eval_stack" and a newline. # CF-[] + DS-s-\[ ]/
        That's all.
    End for.
    
    Note: Get final result
    Display "CF-[] DS-s-\{ }/ Pop final result" and a newline.  # CF-[] + DS-s-\{ }/
    Display "CF-()-e Return result" and a newline.               # CF-()-e

Pseudocode for file evaluator.c (ends here)
```

#### File: include/stack.h
```
Pseudocode for file stack.h (begins here)
Note: File Type: source: h-txt → build: none
Parent: rpn_calculator/include/

Note: Stack structure definition
Display "CF-[] Define Stack structure" and a newline.           # CF-[]
Display "  - double* data array" and a newline.
Display "  - int top (stack pointer)" and a newline.
Display "  - int capacity" and a newline.

Note: Function declarations
Display "CF-[] Declare stack_init()" and a newline.            # CF-[]
Display "CF-[] Declare stack_push()" and a newline.            # CF-[]
Display "CF-[] Declare stack_pop()" and a newline.             # CF-[]
Display "CF-[] Declare stack_peek()" and a newline.            # CF-[]
Display "CF-[] Declare stack_is_empty()" and a newline.        # CF-[]
Display "CF-[] Declare stack_is_full()" and a newline.         # CF-[]
Display "CF-[] Declare stack_destroy()" and a newline.         # CF-[]

Pseudocode for file stack.h (ends here)
```

#### File: tests/test_stack.c
```
Pseudocode for file test_stack.c (begins here)
Note: File Type: source: c-txt → build: exe-hs-bin
Parent: rpn_calculator/tests/

To demonstrate test_stack_push_pop function:                    # CF-[] + DS-s
    Display "CF-()-s test_stack_push_pop() started" and a newline. # CF-()-s
    
    Note: Setup test
    Display "CF-[] Create test stack" and a newline.           # CF-[] + DS-s
    Display "CF-[] Push test values: 1.0, 2.0, 3.0" and a newline. # CF-[] + DS-s-\[ ]/
    
    Note: Verify operations
    Display "CF-[] DS-s-\{ }/ Pop and verify: 3.0" and a newline. # CF-[] + DS-s-\{ }/
    If popped_value equals 3.0:                                  # CF-<>
        Display "CF-\\ Test PASSED" and a newline.              # CF-\\
    Else:                                                        # CF-<>
        Display "CF-\\ Test FAILED" and a newline.              # CF-\\
    That's all.
    
    Display "CF-()-e test_stack_push_pop() completed" and a newline. # CF-()-e

To demonstrate test_stack_overflow function:                     # CF-[] + DS-s
    Display "CF-()-s test_stack_overflow() started" and a newline. # CF-()-s
    
    Note: Fill stack to capacity
    Display "CF-[] Create stack with capacity 10" and a newline. # CF-[] + DS-s
    
    For i from zero to ten:                                      # CF-[]
        Display "CF-[] DS-s-\[ ]/ Push value" and a newline.    # CF-[] + DS-s-\[ ]/
    End for.
    
    Note: Attempt overflow
    Display "CF-[] Attempt to push to full stack" and a newline. # CF-[]
    If push returns error:                                       # CF-<>
        Display "CF-\\ Test PASSED: Overflow detected" and a newline. # CF-\\
    Else:                                                        # CF-<>
        Display "CF-\\ Test FAILED: Should have failed" and a newline. # CF-\\
    That's all.
    
    Display "CF-()-e test_stack_overflow() completed" and a newline. # CF-()-e

Pseudocode for file test_stack.c (ends here)
```
## Project Structure Examples - Part 2

### File: Makefile
```
Pseudocode for file Makefile (begins here)
Note: File Type: source: m-txt → build: exe-hs-bin
Parent: rpn_calculator/

Note: Build configuration
Display "CF-[] Set CC = gcc" and a newline.                     # CF-[]
Display "CF-[] Set CFLAGS = -Wall -Wextra -std=c11" and a newline. # CF-[]
Display "CF-[] Set INCLUDES = -Iinclude/" and a newline.       # CF-[]

Note: Build targets
Display "CF-[] Target: all (default)" and a newline.            # CF-[]
Display "  Dependencies: rpn_calculator libstack.a" and a newline.

Display "CF-[] Target: rpn_calculator" and a newline.           # CF-[]
Display "  Compile src/main.c src/parser.c src/evaluator.c" and a newline.
Display "  Link with lib/libstack.a" and a newline.

Display "CF-[] Target: libstack.a" and a newline.               # CF-[]
Display "  Compile src/stack.c to object" and a newline.
Display "  Archive into lib/libstack.a" and a newline.

Display "CF-[] Target: test" and a newline.                     # CF-[]
Display "  Compile and run all test files" and a newline.

Display "CF-clr-<> Target: clean" and a newline.               # CF-clr-<>
Display "  Remove all .o files" and a newline.
Display "  Remove executables" and a newline.
Display "  Remove library files" and a newline.

Pseudocode for file Makefile (ends here)
```

### File: rpn_calculator.dev
```
Pseudocode for file rpn_calculator.dev (begins here)
Note: File Type: source: dev-ini-txt → build: none
Parent: rpn_calculator/

Note: Dev-C++ Project Configuration
Display "CF-[] Project Name: RPN Calculator" and a newline.     # CF-[]
Display "CF-[] Project Type: Console Application" and a newline. # CF-[]
Display "CF-[] Compiler: TDM-GCC" and a newline.               # CF-[]

Note: File list
Display "CF-[] Add src/main.c to project" and a newline.        # CF-[]
Display "CF-[] Add src/stack.c to project" and a newline.       # CF-[]
Display "CF-[] Add src/parser.c to project" and a newline.      # CF-[]
Display "CF-[] Add src/evaluator.c to project" and a newline.   # CF-[]
Display "CF-[] Add include/ directory to includes" and a newline. # CF-[]

Note: Build settings
Display "CF-[] Set optimization level: -O2" and a newline.      # CF-[]
Display "CF-[] Enable warnings: -Wall -Wextra" and a newline.   # CF-[]
Display "CF-[] Output: build/rpn_calculator.exe" and a newline. # CF-[]

Pseudocode for file rpn_calculator.dev (ends here)
```

### File: rpn_calculator.layout
```
Pseudocode for file rpn_calculator.layout (begins here)
Note: File Type: source: lay-ini-txt → build: none
Parent: rpn_calculator/

Note: Dev-C++ IDE Layout Configuration
Display "CF-[] Window layout: Standard" and a newline.          # CF-[]
Display "CF-[] Editor tabs position: Top" and a newline.        # CF-[]

Note: Open files
Display "CF-[] Open file: src/main.c (active)" and a newline.   # CF-[]
Display "CF-[] Open file: src/stack.c" and a newline.           # CF-[]
Display "CF-[] Cursor position: Line 45, Column 12" and a newline. # CF-[]

Note: Breakpoints
Display "CF-[] Breakpoint: src/evaluator.c, line 78" and a newline. # CF-[]
Display "CF-[] Breakpoint: src/stack.c, line 34" and a newline. # CF-[]

Note: Watch variables
Display "CF-[] Watch: eval_stack->top" and a newline.           # CF-[]
Display "CF-[] Watch: token_count" and a newline.               # CF-[]

Pseudocode for file rpn_calculator.layout (ends here)
```

### File: docs/architecture.md
```
Pseudocode for file architecture.md (begins here)
Note: File Type: source: md-txt → build: none
Parent: rpn_calculator/docs/

Note: Project Architecture Documentation
Display "CF-[] Title: RPN Calculator Architecture" and a newline. # CF-[]

Display "CF-[] Section: Overview" and a newline.                # CF-[]
Display "  Modular design with separated concerns" and a newline.
Display "  Stack-based evaluation engine" and a newline.
Display "  Token-based parsing system" and a newline.

Display "CF-[] Section: Module Dependencies" and a newline.     # CF-[]
Display "  main.c depends on: parser, evaluator, stack" and a newline.
Display "  evaluator.c depends on: stack" and a newline.
Display "  parser.c: independent" and a newline.
Display "  stack.c: independent" and a newline.

Display "CF-[] Section: Data Flow" and a newline.               # CF-[] + DS-s + DS-a
Display "  Input → Parser → Token Array → Evaluator → Stack → Output" and a newline.

Pseudocode for file architecture.md (ends here)
```

---

## Use Cases

### 1. Algorithm Design
Write algorithms in natural language with structural annotations before implementing in a production language.

### 2. Print Debugging
Execute the pseudocode to see a trace of what operations would occur, helping identify logic errors.

### 3. Documentation
Create self-documenting code that explains both what it does and how data flows through structures.

### 4. Teaching
Help students understand algorithms by showing explicit control flow and data structure operations.

### 5. Code Review
Provide clear algorithmic specifications that reviewers can understand without language-specific knowledge.

---

## Troubleshooting

### Common Questions

**Q: Do I need to install both ~English Revised AND Flowchart interpreters?**

A: No! This is a text-based system. You only need ~English Revised to execute. The Flowchart annotations are comments for humans to understand the structure - they map to flowchart symbols but don't require a separate interpreter.

**Q: What if my annotations don't align properly?**

A: Use spaces (not tabs) and count characters carefully. All `#` symbols should be in the same column. Most text editors have a "show whitespace" feature that can help you align them properly.

**Q: Can I write this without the annotations?**

A: Yes! The ~English Revised code works alone. Annotations add flowchart documentation but aren't required for execution. You can start without them and add them later for clarity.

**Q: How do I execute this?**

A: Use the ~English Revised interpreter from GitHub. The pseudocode is executable ~English Revised code. When you run it, it will output the trace of operations.

**Q: What's the difference between `CF-[]` and `CF-()-s`?**

A: `CF-()-s` is specifically for program start (entry point) - use it once at the beginning. `CF-[]` is for general operations/processes - use it for most computational steps.

**Q: Why use `\[ ]/` instead of just writing "push"?**

A: The symbols visually represent the direction of data flow. `\[ ]/` looks like an arrow pointing down into a stack (push), while `\{ }/` looks like an arrow coming up from a stack (pop). This makes the data movement clearer at a glance.

**Q: Do I have to use "Display" and "and a newline" every time?**

A: In ~English Revised, yes - this is the syntax for output. But remember, the system is designed to describe program behavior, so this verbosity is intentional to make execution traces clear.

**Q: Can I use this for languages other than C?**

A: Absolutely! Just change the file type notation. Use `source: py-txt` for Python, or create your own conventions. The system is language-agnostic.

### Common Mistakes

**Mistake 1: Forgetting to close control structures**
```
Wrong:
While condition:
    Display "CF-[] Do something" and a newline.
# Missing: That's all.

Correct:
While condition:
    Display "CF-[] Do something" and a newline.
That's all.
```

**Mistake 2: Misaligned annotations**
```
Wrong:
Display "CF-()-s Started" and a newline.  # CF-()-s
Display "CF-[] Process" and a newline.    # CF-[]
Display "CF-\\ Output" and a newline. # CF-\\

Correct:
Display "CF-()-s Started" and a newline.  # CF-()-s
Display "CF-[] Process" and a newline.    # CF-[]
Display "CF-\\ Output" and a newline.     # CF-\\
```

**Mistake 3: Using wrong stack symbols**
```
Wrong:
Display "CF-[] Push to stack" and a newline.  # CF-[] + DS-s

Better:
Display "CF-[] DS-s-\[ ]/ Push to stack" and a newline.  # CF-[] + DS-s-\[ ]/
```

---

## Workflow

### Step-by-Step Process

1. **Design Phase**
   - Write algorithm in ~English Revised
   - Add Flowchart annotations
   - Focus on logic, not implementation details

2. **Debug Phase**
   - Execute pseudocode with ~English Revised interpreter
   - Review output trace for logical errors
   - Refine algorithm as needed

3. **Visualize Phase**
   - Map annotations to actual flowchart diagram (optional)
   - Use for presentations or documentation

4. **Implement Phase**
   - Translate to production language (C, Python, Java, etc.)
   - Use pseudocode as specification reference

5. **Document Phase**
   - Keep pseudocode as living documentation
   - Update when algorithm changes

### Example Workflow

```
Start: Need to implement a sorting algorithm

Step 1 - Design:
Write in ~English Revised with annotations
"To demonstrate bubble sort..."

Step 2 - Execute:
Run interpreter, see output:
"CF-()-s Sort Started
CF-[] Compare elements
CF-<> If out of order
..."

Step 3 - Debug:
Notice logic error in swap condition
Fix pseudocode, run again

Step 4 - Implement:
Translate to C code
Use pseudocode as guide

Step 5 - Document:
Commit pseudocode to docs/ folder
Reference in code comments
```

---

## Benefits

### For Developers
- **Language Agnostic** - Design algorithms independent of implementation language
- **Quick Prototyping** - Test logic without writing actual code
- **Self-Documenting** - Code explains itself through natural language
- **Debugging Aid** - Trace execution before implementation

### For Students
- **Clear Learning** - See exactly what each step does
- **Visual Connection** - Links to flowchart concepts
- **Natural Language** - No syntax barriers to understanding
- **Step-by-Step** - Explicit operation sequences

### For Teams
- **Better Communication** - Non-programmers can understand algorithms
- **Code Review** - Review logic before implementation
- **Consistent Documentation** - Standard format across projects
- **Onboarding** - New team members understand architecture quickly

---

## Implementation Notes

- ~English Revised interpreter available on GitHub
- Flowchart esolang uses 2D visual representation
- This polyglot combines both for text-based workflow
- Annotations serve as bridge between natural language and flowchart semantics
- System is extensible - add your own data structure annotations as needed

---

## Resources

### Official Documentation
- [~English on Esolangs Wiki](https://esolangs.org/wiki/~English)
- [Flowchart on Esolangs Wiki](https://esolangs.org/wiki/Flowchart)
- [~English Revised GitHub Repository](https://github.com/AnotherTest/english)

### Related Concepts
- [Literate Programming (Knuth)](https://en.wikipedia.org/wiki/Literate_programming)
- [Pseudocode on Wikipedia](https://en.wikipedia.org/wiki/Pseudocode)
- [Flowchart on Wikipedia](https://en.wikipedia.org/wiki/Flowchart)

### Tools
- Text editors with column alignment features
- Flowchart drawing tools (for visualization phase)
- ~English Revised interpreter (for execution)

---

## License

This documentation describes a metalanguage combining two esoteric programming languages. Refer to individual language implementations for their respective licenses.

---

**Created for algorithm design, visualization, and iterative development through executable pseudocode.**

*For questions, issues, or contributions, please refer to the respective esolang wiki pages or GitHub repositories.*