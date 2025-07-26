# Pseudocode System Specification (AI/Android Edition)

## Table of Contents

- [Overview](#overview)
- [Core Principles](#core-principles)
- [Statement Types](#statement-types)
- [Built-in Functions & Constants](#built-in-functions--constants)
- [Special References](#special-references)
- [Flowchart and Project Notation System](#flowchart-and-project-notation-system)
- [System Error Handling Protocol](#system-error-handling-protocol)
- [Complete Android Project Example](#complete-android-project-example)
- [Usage Guidelines](#usage-guidelines)
- [Benefits](#benefits)

## Overview

This pseudocode system is based on the ~English revised esolang syntax, specifically adapted for an AI agent like Manus operating in a Linux environment. It is designed to create algorithms that read like natural English while generating complete, build-ready Android application projects using languages like Java or Kotlin. The system maintains proper control flow documentation through embedded flowchart notation in comments.

## Core Principles

- **Natural Language**: Code reads like English sentences
- **Loose Syntax**: Flexible sentence structure with multiple keyword synonyms
- **Embedded Flow Documentation**: Flowchart symbols embedded in comments for structure clarity
- **Optional Numbering**: Simple sequential numbering system for complex algorithms

## Statement Types

### 1. Declaration

Creates new variables/objects with specified types.

```pseudocode
Create a variable named appName of type String.
Make another variable called userIntent.
Declare a new object named mainActivity of type Activity.
```

### 2. Display/Output

Shows numbers, strings, or data to a user or writes content to a file.

```pseudocode
Display "Hello world!" and a newline.
Show "Your name is ", the username, "." and a newline.
Set the contents of a file to include "line of text".
```

### 3. Function Calls

Calls built-in, framework, or user-defined functions and methods.

```pseudocode
Set the value of userIntent to call function "new Intent" with mainActivity and "detailsActivity.class".
Vary the value of appName by calling its method "getString" with resource "R.string.app_name".
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

## Built-in Functions & Constants

| Function/Constant | Description |
|-------------------|-------------|
| `ask` | Prompt user for input |
| `get input` | Get user input |
| `to number` | Convert to a numeric type |
| `to string` | Convert to a string type |
| `one`, `zero`, etc. | Numeric words can be used as constants |

## Special References

| Reference | Description |
|-----------|-------------|
| `it` | References the last-used variable |
| `its` | Possessive form for object members |

## Flowchart and Project Notation System

### Basic Symbols

Embedded within `Note` statements to document control flow:

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

Additional notation for programming control structures:

| Symbol | Meaning | Usage Example |
|--------|---------|---------------|
| `[CS-SS]` | Selection Statement | `Note: [CS-SS] If-else condition block` |
| `[CS-IS]` | Iteration Statement | `Note: [CS-IS] While/for loop structure` |
| `[CS-JS]` | Jump Statement | `Note: [CS-JS] Break, continue, or return` |

### File System, Build, and Android Notation

Specialized notation for file operations, build processes, and Android-specific files:

| Symbol | Meaning | Usage Example |
|--------|---------|---------------|
| `[FOLDER]` | Directory/folder operations | `Note: [FOLDER] Create project source structure` |
| `[FILE]` | Generic file operations | `Note: [FILE] Generate source code file` |
| `[BUILD]` | Generic build system configuration. Describes build logic abstractly, allowing the AI to select the optimal tool (e.g., Bazel, Buck2) | `Note: [BUILD] Configure a high-performance build system` |
| `[GRADLE]` | Specific content for a Gradle build file (`build.gradle` or `build.gradle.kts`). This is the default build system for Android | `Note: [GRADLE] Define app dependencies in build.gradle` |
| `[MANIFEST]` | Content for the `AndroidManifest.xml` file. Defines essential app information like permissions and activities | `Note: [MANIFEST] Declare permissions and activities` |
| `[RESOURCE]` | Content for an Android resource file (e.g., XML layouts, string values, styles) | `Note: [RESOURCE] Create the main activity layout XML` |

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

## System Error Handling Protocol

All programs follow a standardized error handling protocol:

1. **On Error**: When any error is detected, immediately halt program execution
2. **Self Diagnosis**: Perform automated system checks to gather context
3. **User Interaction**: Prompt the user for input regarding the error
4. **Report Generation**: Create a comprehensive error report with:
   - Error details
   - User feedback
   - Timestamp
   - Environment info
   - Program state
5. **Repository Logging**: Automatically commit the error report to `error_log.md` in the project's repository

## Complete Android Project Example

```pseudocode
Note: Android Calculator Project for Manus AI v1.0 - 2025-07-26
Note: Purpose: Demonstrate complete Android project setup using the revised specification.

Note: [START] Begin comprehensive project creation

Note: [1-FOLDER] Create a standard Android project directory structure
Create a folder named CalculatorProject.
    Note: [FOLDER] Application module
    Inside CalculatorProject, create a folder named app.
        Note: [FOLDER] Source code directory
        Inside app, create a folder named src.
            Note: [FOLDER] Main source set
            Inside src, create a folder named main.
                Note: [FOLDER] Java source code
                Inside main, create a folder named java.
                    Inside java, create a folder named com.
                        Inside com, create a folder named example.
                            Inside example, create a folder named calculator.
                Note: [FOLDER] Resources
                Inside main, create a folder named res.
                    Inside res, create a folder named layout.
                    Inside res, create a folder named values.

Note: [2-MANIFEST] Create the Android Manifest file
Inside app/src/main, create a file named AndroidManifest.xml.
Set the contents of app/src/main/AndroidManifest.xml to include these elements:
    Display "<manifest xmlns:android=\"http://schemas.android.com/apk/res/android\" package=\"com.example.calculator\">" as a line.
    Display "    <application android:label=\"@string/app_name\" android:theme=\"@style/Theme.AppCompat\">" as a line.
    Display "        <activity android:name=\".MainActivity\" android:exported=\"true\">" as a line.
    Display "            <intent-filter>" as a line.
    Display "                <action android:name=\"android.intent.action.MAIN\" />" as a line.
    Display "                <category android:name=\"android.intent.category.LAUNCHER\" />" as a line.
    Display "            </intent-filter>" as a line.
    Display "        </activity>" as a line.
    Display "    </application>" as a line.
    Display "</manifest>" as a line.

Note: [3-RESOURCE] Create resource files for strings and layout
Inside app/src/main/res/values, create a file named strings.xml.
Set its contents to include:
    Display "<resources>" as a line.
    Display "    <string name=\"app_name\">Calculator</string>" as a line.
    Display "</resources>" as a line.

Inside app/src/main/res/layout, create a file named activity_main.xml.
Set its contents to include a basic layout:
    Display "<LinearLayout xmlns:android=\"http://schemas.android.com/apk/res/android\"" as a line.
    Display "    android:layout_width=\"match_parent\"" as a line.
    Display "    android:layout_height=\"match_parent\">" as a line.
    Display "    <TextView android:text=\"Hello, Calculator!\"" as a line.
    Display "        android:layout_width=\"wrap_content\"" as a line.
    Display "        android:layout_height=\"wrap_content\" />" as a line.
    Display "</LinearLayout>" as a line.

Note: [4-FILE] Generate Java source code for the main activity
Inside app/src/main/java/com/example/calculator, create a file named MainActivity.java.
Set its contents to include:
    Display "package com.example.calculator;" as a line.
    Display "import androidx.appcompat.app.AppCompatActivity;" as a line.
    Display "import android.os.Bundle;" as a line.
    Display "public class MainActivity extends AppCompatActivity {" as a line.
    Display "    @Override" as a line.
    Display "    protected void onCreate(Bundle savedInstanceState) {" as a line.
    Display "        super.onCreate(savedInstanceState);" as a line.
    Display "        setContentView(R.layout.activity_main);" as a line.
    Display "    }" as a line.
    Display "}" as a line.

Note: [5-GRADLE] Create the app-level Gradle build file
Inside app, create a file named build.gradle.
Set its contents to include:
    Display "plugins { id 'com.android.application' }" as a line.
    Display "android {" as a line.
    Display "    namespace 'com.example.calculator'" as a line.
    Display "    compileSdk 34" as a line.
    Display "    defaultConfig { minSdk 24; targetSdk 34; }" as a line.
    Display "}" as a line.
    Display "dependencies {" as a line.
    Display "    implementation 'androidx.appcompat:appcompat:1.6.1'" as a line.
    Display "}" as a line.

Note: [6-GRADLE] Create the project-level Gradle settings file
Inside CalculatorProject, create a file named settings.gradle.
Set its contents to include:
    Display "include ':app'" as a line.

Note: [END] Project creation is complete. The project is ready to be built.
```

## Usage Guidelines

### For Human Reviewers

1. **Review the Plan**: Read through the pseudocode to understand what will be created
2. **Check File Structure**: Verify that the folder and file organization makes sense
3. **Validate Content**: Ensure that file contents are appropriate for the intended purpose
4. **Approve or Modify**: Provide feedback or approval before AI execution

### For AI Implementation

1. **Parse Pseudocode**: Convert natural language statements to executable operations
2. **Create Structure**: Build the folder hierarchy as specified
3. **Generate Files**: Create all specified files with the exact content shown
4. **Execute Build**: Follow the build system configuration to ensure project viability
5. **Error Reporting**: Follow the standardized error handling protocol if issues arise

## Benefits

- **Transparency**: Clear visibility into what the AI will create
- **Control**: Human oversight before any code generation
- **Documentation**: Self-documenting process with embedded flowchart notation
- **Flexibility**: Natural language allows for easy modifications and understanding
- **Standardization**: Consistent format for AI-human collaboration in development projects

---

> **Note**: This specification serves as a human-readable contract between users and AI systems for code generation. It prioritizes transparency and user control over brevity.
