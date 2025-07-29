# Pseudocode System

> **Natural Language Programming with Embedded Flowchart Documentation**

[![Version](https://img.shields.io/badge/version-2.0-blue.svg)](https://github.com/user/repo)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Documentation](https://img.shields.io/badge/docs-complete-brightgreen.svg)](#documentation)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Core Principles](#core-principles)
- [Statement Types](#statement-types)
- [Built-in Functions & Constants](#built-in-functions--constants)
- [Flowchart Notation System](#flowchart-notation-system)
- [System Error Handling Protocol](#system-error-handling-protocol)
- [Syntax Features](#syntax-features)
- [File System Structure Documentation](#file-system-structure-documentation)
- [Complete Project Examples](#complete-project-examples)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

This pseudocode system is based on the ~English revised esolang syntax, designed to create algorithms that read like natural English while maintaining proper control flow documentation through embedded flowchart notation in comments.

The system bridges the gap between human-readable documentation and executable pseudocode, making it ideal for:
- **Educational contexts** where beginners need to understand programming logic
- **Algorithm documentation** that remains readable by non-technical stakeholders
- **System design** where complex workflows need clear documentation
- **Rapid prototyping** before implementing in production languages

---

## 🚀 Core Principles

| Principle | Description |
|-----------|-------------|
| **🗣️ Natural Language** | Code reads like English sentences |
| **🔄 Loose Syntax** | Flexible sentence structure with multiple keyword synonyms |
| **📊 Embedded Flow Documentation** | Flowchart symbols embedded in comments for structure clarity |
| **🔢 Optional Numbering** | Simple sequential numbering system for complex algorithms |

---

## 📝 Statement Types

### 1. Declaration
Creates new variables/objects with generic types.

```pseudocode
Create a variable named username.
Make another variable called age.
Declare a new object named userProfile.
```

### 2. Display/Output
Shows numbers, strings, or data to user.

```pseudocode
Display "Hello world!" and a newline.
Show "Your name is ", the username, "." and a newline.
Print the age and another newline.
```

### 3. Function Calls
Calls built-in or user-defined functions.

```pseudocode
Set the value of age to call function "to number" with call another function "ask".
Vary the value of username by call the function "ask".
```

### 4. While Loops
Provides loop functionality.

```pseudocode
While the age is smaller than 0 do:
    Display "Invalid age entered." and a newline.
That's all.
```

### 5. If...Else Conditionals
Conditional branching statements.

```pseudocode
If the username equals "admin" then:
    Display "Welcome administrator!" and a newline.
That's all.
Else, then:
    Display "Welcome user!" and a newline.
That's all.
```

### 6. Stop
Terminates the program.

```pseudocode
Stop the program.
Stop this program.
```

### 7. Comments/Notes
Documentation and flowchart notation.

```pseudocode
Note: This validates user input
Note: [DECISION] Check if username exists
```

---

## 🛠️ Built-in Functions & Constants

### Functions
- `ask` - Prompt user for input
- `get input` - Get user input
- `to number` - Convert to numeric type
- `to string` - Convert to string type

### Constants
- `one` instead of 1
- `zero` instead of 0
- Other numeric words as needed

### Special References
- `it` - References the last-used variable
- `its` - Possessive form for object members

---

## 📊 Flowchart Notation System

### Basic Symbols
Embedded within Note statements to document control flow:

| Symbol | Meaning | Usage Example |
|--------|---------|---------------|
| `[START]` | Program beginning | `Note: [START] Initialize application` |
| `[END]` | Program termination | `Note: [END] Close application` |
| `[INPUT]` | Data input operations | `Note: [INPUT] Get user credentials` |
| `[OUTPUT]` | Data output operations | `Note: [OUTPUT] Display results` |
| `[PROCESS]` | General processing | `Note: [PROCESS] Calculate total` |
| `[DECISION]` | Conditional branching | `Note: [DECISION] Valid password?` |
| `[DOCUMENT]` | Reports/printouts | `Note: [DOCUMENT] Generate user report` |
| `[MANUAL]` | Manual input prompt | `Note: [MANUAL] Wait for user confirmation` |
| `[CONNECTOR]` | On-page flow connection | `Note: [CONNECTOR] Continue main flow` |
| `[OFF-PAGE]` | Off-page connection | `Note: [OFF-PAGE] See validation module` |

### Control Statement Notation

| Symbol | Meaning | Usage Example |
|--------|---------|---------------|
| `[CS-SS]` | Selection Statement | `Note: [CS-SS] If-else condition block` |
| `[CS-IS]` | Iteration Statement | `Note: [CS-IS] While/for loop structure` |
| `[CS-JS]` | Jump Statement | `Note: [CS-JS] Break, continue, or goto` |

### File System and Build Notation

| Symbol | Meaning | Usage Example |
|--------|---------|---------------|
| `[FOLDER]` | Directory/folder operations | `Note: [FOLDER] Create project structure` |
| `[FILE]` | File operations | `Note: [FILE] Generate source code` |
| `[INI]` | Configuration file content | `Note: [INI] IDE project settings` |
| `[BFB]` | Batch File Begin | `Note: [BFB] Start Windows batch script` |
| `[BFE]` | Batch File End | `Note: [BFE] End Windows batch script` |
| `[MFB]` | Makefile Begin | `Note: [MFB] Start Makefile content` |
| `[MFE]` | Makefile End | `Note: [MFE] End Makefile content` |

### Optional Numbering System
For complex algorithms requiring clear execution order:

```pseudocode
Note: [1-START] Begin user authentication
Note: [2-INPUT] Collect username and password
Note: [3-DECISION] Credentials valid?
Note: [3A-PROCESS] Grant access (if valid)
Note: [3B-OUTPUT] Show error message (if invalid)
Note: [4-END] Complete authentication process
```

**Numbering Guidelines:**
- Use simple sequential numbers (1, 2, 3...)
- Use letters for branches (3A, 3B, 3C...)
- Keep numbering simple to maintain readability
- Consider renumbering complexity when inserting steps

---

## ⚠️ System Error Handling Protocol

> **🔒 All programs written in the ~English Revised Pseudocode System follow a standardized error handling protocol to ensure consistent error management and debugging across all implementations.**

### Error Response Procedure

1. **🚨 On Error**: When any error condition is detected during program execution
2. **⏸️ Pause Program**: Immediately halt program execution to prevent cascading failures
3. **🔍 Self Diagnosis**: If the program has diagnostic capabilities, perform automated system checks to gather additional context about the error state
4. **👤 User Interaction**: Prompt the user for input and feedback regarding the error condition, including:
   - What operation was being performed when the error occurred
   - Any unusual circumstances or recent changes
   - User's assessment of the error severity and impact
5. **📋 Report Generation**: Create a comprehensive error report containing:
   - Complete error details and stack trace information
   - User feedback and input collected in step 4
   - Current date and timestamp
   - System environment information
   - Program state and variable values at time of error
   - Relevant configuration settings and file paths
6. **📤 Repository Logging**: Automatically commit the error report to `error_log.md` in the appropriate folder of the relevant GitHub repository for the project

### Error Report Format
Error reports should be structured as markdown entries in `error_log.md` with consistent formatting for easy analysis and tracking of recurring issues.

### Protocol Benefits

- ✅ **Consistent Error Handling**: All programs behave predictably when errors occur
- 🤝 **User Engagement**: Users become active participants in the debugging process
- 📚 **Comprehensive Documentation**: Every error is properly logged with full context
- 🔗 **Repository Integration**: Error tracking becomes part of the project's version control history
- 📈 **Continuous Improvement**: Error patterns can be analyzed over time to improve system reliability

---

## ✨ Syntax Features

### Flexible Punctuation
Sentences can end with:
- Period (.)
- Exclamation mark (!)
- Question mark (?)

### Keyword Synonyms
Multiple ways to express the same concept, with semantic meaning based on context:

#### Output Operations
- **`Display`** → Print debugging, temporary output, informal logging
- **`Show`** → Formal program output, user interface elements  
- **`Print`** → Reports, formatted output, final results

**Example Usage:**
```pseudocode
Display "Debug: username is ", username, "."     // Temporary debug output
Show "Your account balance is $", balance, "."   // User interface display
Print "Monthly Report - Generated ", date, "."   // Formal document output
```

#### Variable Operations  
- **`Create/Make/Declare`** → Variable initialization
- **`Set/Vary/Change`** → Variable modification

#### Programming Context
The natural language approach means keyword choice carries semantic meaning about the programmer's intent. `Display` statements naturally stand out when scanning code for debug statements to remove, while `Show` and `Print` indicate more permanent program functionality.

### Natural Language Flow
Code should read as naturally as possible:

```pseudocode
Note: [START] Begin password validation
Create a variable named password.
Note: [INPUT] Get user password
Display "Enter your password: " and a newline.
Set the value of password to call function "ask".
Note: [CS-SS] Selection statement for password validation
Note: [DECISION] Check password strength
If the password length is less than 8 then:
    Note: [OUTPUT] Inform user of requirements
    Display "Password must be at least 8 characters." and a newline.
    Note: [CS-JS] Jump back to input (implied goto)
    Note: [CONNECTOR] Return to input
That's all.
Note: [END] Password validation complete
```

---

## 📁 File System Structure Documentation

### Folder and File Tree Notation
The system supports nested folder/file structure documentation for creating complete project hierarchies:

```pseudocode
Note: [FOLDER] Project root directory structure
Create a folder named MyProject.
    Note: [FOLDER] Source code directory
    Inside MyProject, create a folder named src.
        Note: [FILE] Main application file
        Inside src, create a file named main.c.
        Note: [FILE] Utility functions
        Inside src, create a file named utils.c.
    Note: [FOLDER] Header files directory
    Inside MyProject, create a folder named include.
        Note: [FILE] Function declarations
        Inside include, create a file named utils.h.
    Note: [FOLDER] Build output directory
    Inside MyProject, create a folder named build.
        Note: [FOLDER] Object files subdirectory
        Inside build, create a folder named obj.
        Note: [FOLDER] Executable files subdirectory
        Inside build, create a folder named bin.
    Note: [FOLDER] Configuration directory
    Inside MyProject, create a folder named config.
        Note: [INI] IDE project configuration
        Inside config, create a file named project.ini.
```

> **💡 This notation allows programs like Manus to automatically generate complete file/folder trees in the correct order for platforms like GitHub.**

---

## 🛠️ IDE Configuration Files

### INI File Content Notation
For IDE-specific configuration files used by Embarcadero, Geany, and similar development environments:

```pseudocode
Note: [INI] Embarcadero C++ Builder project configuration
Set the contents of project.bpr to include these configuration sections:
    Display "[Compiler]" as a line.
    Display "Defines=" as a line.
    Display "IncludePath=include;src" as a line.
    Display "LibraryPath=lib;build" as a line.
    Display "OutputDir=build\\bin" as a line.
    Display "" as a line.
    Display "[Linker]" as a line.
    Display "Libraries=user32.lib;kernel32.lib" as a line.
    Display "OutputFile=MyProject.exe" as a line.

Note: [INI] Geany project configuration
Set the contents of MyProject.geany to include these settings:
    Display "[project]" as a line.
    Display "name=MyProject" as a line.
    Display "base_path=." as a line.
    Display "description=C Project with Build Automation" as a line.
    Display "" as a line.
    Display "[build-menu]" as a line.
    Display "FT_00_LB=_Compile" as a line.
    Display "FT_00_CM=gcc -c \"%f\" -Iinclude -o build/obj/\"%e.o\"" as a line.
    Display "FT_01_LB=_Build" as a line.
    Display "FT_01_CM=make -f Makefile" as a line.
    Display "FT_02_LB=_Execute" as a line.
    Display "FT_02_CM=./build/bin/MyProject" as a line.
```

---

## 🚀 Build Automation Scripts

### Batch File Content
Windows batch files that automatically execute Makefiles when double-clicked or run from CMD:

```pseudocode
Note: [BFB] Windows build automation batch file
Create a file named build.bat.
Set the contents of build.bat to include these commands:
    Display "@echo off" as a line.
    Display "echo Starting automated build process..." as a line.
    Display "if not exist build mkdir build" as a line.
    Display "if not exist build\\obj mkdir build\\obj" as a line.
    Display "if not exist build\\bin mkdir build\\bin" as a line.
    Display "echo Executing Makefile..." as a line.
    Display "make -f Makefile" as a line.
    Display "if %errorlevel% equ 0 (" as a line.
    Display "    echo Build completed successfully!" as a line.
    Display "    echo Executable created: build\\bin\\MyProject.exe" as a line.
    Display ") else (" as a line.
    Display "    echo Build failed with errors!" as a line.
    Display "    pause" as a line.
    Display "    exit /b 1" as a line.
    Display ")" as a line.
    Display "pause" as a line.
Note: [BFE] End of batch file content
```

### Makefile Content
Complete Makefiles with proper targets and dependencies:

```pseudocode
Note: [MFB] Main project Makefile
Create a file named Makefile.
Set the contents of Makefile to include these build rules:
    Display "# Makefile for MyProject" as a line.
    Display "CC=gcc" as a line.
    Display "CFLAGS=-Wall -Wextra -std=c99 -Iinclude" as a line.
    Display "SRCDIR=src" as a line.
    Display "OBJDIR=build/obj" as a line.
    Display "BINDIR=build/bin" as a line.
    Display "" as a line.
    Display "SOURCES=$(wildcard $(SRCDIR)/*.c)" as a line.
    Display "OBJECTS=$(SOURCES:$(SRCDIR)/%.c=$(OBJDIR)/%.o)" as a line.
    Display "TARGET=$(BINDIR)/MyProject" as a line.
    Display "" as a line.
    Display ".PHONY: all clean directories" as a line.
    Display "" as a line.
    Display "all: directories $(TARGET)" as a line.
    Display "" as a line.
    Display "directories:" as a line.
    Display "\t@mkdir -p $(OBJDIR) $(BINDIR)" as a line.
    Display "" as a line.
    Display "$(TARGET): $(OBJECTS)" as a line.
    Display "\t@echo \"Linking $(TARGET)...\"" as a line.
    Display "\t$(CC) $(OBJECTS) -o $@" as a line.
    Display "\t@echo \"Build completed: $(TARGET)\"" as a line.
Note: [MFE] End of Makefile content
```

---

## 📚 Complete Project Examples

### Control Statement Examples

#### Selection Statements (CS-SS)
Document conditional logic structures:

```pseudocode
Note: [CS-SS] Multi-way selection for user role
If the userRole equals "admin" then:
    Note: [PROCESS] Admin-specific operations
    Display "Administrator access granted." and a newline.
That's all.
Else, if the userRole equals "user" then:
    Note: [PROCESS] Standard user operations
    Display "User access granted." and a newline.
That's all.
Else, then:
    Note: [OUTPUT] Access denied
    Display "Access denied." and a newline.
That's all.
```

#### Iteration Statements (CS-IS)
Document loop structures:

```pseudocode
Note: [CS-IS] While loop for input validation
While the input is not valid do:
    Note: [INPUT] Request user input
    Display "Enter a number between 1 and 10: " and a newline.
    Set the value of input to call function "ask".
    Note: [DECISION] Validate input range
    If the input is less than 1 or the input is greater than 10 then:
        Note: [OUTPUT] Show error message
        Display "Invalid input. Please try again." and a newline.
    That's all.
That's all.
```

### Full C Project with IDE Integration

```pseudocode
Note: C Project with Full IDE Integration and Build Automation v2.0 - 2025-07-25
Note: Purpose: Demonstrate complete project setup with IDE configs and build scripts

Note: [START] Begin comprehensive project creation

Note: [1-FOLDER] Create complete directory structure
Create a folder named CalculatorProject.
    Note: [FOLDER] Source code organization
    Inside CalculatorProject, create a folder named src.
        Note: [FILE] Main application entry point
        Inside src, create a file named main.c.
        Note: [FILE] Calculator operations
        Inside src, create a file named calculator.c.
    Note: [FOLDER] Header file organization
    Inside CalculatorProject, create a folder named include.
        Note: [FILE] Calculator function declarations
        Inside include, create a file named calculator.h.
    Note: [FOLDER] Build system organization
    Inside CalculatorProject, create a folder named build.
        Inside build, create a folder named obj.
        Inside build, create a folder named bin.
    Note: [FOLDER] IDE configuration organization
    Inside CalculatorProject, create a folder named config.
        Note: [INI] Embarcadero project file
        Inside config, create a file named calculator.cbproj.
        Note: [INI] Geany project file
        Inside config, create a file named calculator.geany.
    Note: [FOLDER] Build automation scripts
    Inside CalculatorProject, create a folder named scripts.
        Note: [BFB] Build automation batch file
        Inside scripts, create a file named build.bat.
        Note: [BFB] Clean automation batch file
        Inside scripts, create a file named clean.bat.

Note: [2-FILE] Generate source code files
Set the contents of src/calculator.h to include these declarations:
    Display "#ifndef CALCULATOR_H" as a line.
    Display "#define CALCULATOR_H" as a line.
    Display "" as a line.
    Display "double add(double a, double b);" as a line.
    Display "double subtract(double a, double b);" as a line.
    Display "double multiply(double a, double b);" as a line.
    Display "double divide(double a, double b);" as a line.
    Display "" as a line.
    Display "#endif // CALCULATOR_H" as a line.

Note: [3-INI] Configure IDE project files
Set the contents of config/calculator.geany to include these settings:
    Display "[project]" as a line.
    Display "name=Calculator Project" as a line.
    Display "base_path=.." as a line.
    Display "description=Simple calculator with build automation" as a line.
    Display "" as a line.
    Display "[build-menu]" as a line.
    Display "FT_00_LB=_Compile Current" as a line.
    Display "FT_00_CM=gcc -c \"%f\" -I../include -o ../build/obj/\"%e.o\"" as a line.
    Display "FT_01_LB=_Build All" as a line.
    Display "FT_01_CM=cd .. && make" as a line.
    Display "FT_02_LB=_Execute" as a line.
    Display "FT_02_CM=cd .. && ./build/bin/calculator" as a line.
    Display "FT_03_LB=_Clean" as a line.
    Display "FT_03_CM=cd .. && make clean" as a line.

Note: [4-MFB] Create comprehensive Makefile
Set the contents of Makefile to include these build rules:
    Display "# Calculator Project Makefile" as a line.
    Display "PROJECT_NAME = calculator" as a line.
    Display "CC = gcc" as a line.
    Display "CFLAGS = -Wall -Wextra -std=c99 -Iinclude -g" as a line.
    Display "LDFLAGS = -lm" as a line.
    Display "" as a line.
    Display "SRCDIR = src" as a line.
    Display "INCDIR
