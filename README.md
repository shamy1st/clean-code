# Clean Code
**Clean Code** is a code that any developer can read and change easily.

**Martin Fowler** "Any fool can write code that a computer can understand. Good programmers write code that humans can understand."

### Why?
* **Maintainable Codebase**: clean code can help develop software that is easy to change and maintain.
* **Easier Troubleshooting**: clean code is easier to troubleshoot for problems.
* **Faster Onboarding**: a quicker onboarding for newcomers to keep productivity high.

### Characteristics
* **Simple**: design and implementation must be as simple as possible.
* **Focused**: code should be written to solve a specific problem.
* **Testable**: easy to test the codebase, preferably in an automated manner.

### In Java

1. **Project Structure**:
   * [Maven Standard Directory Layout](https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html)

   Dir | Description    
   --- | -----------
   src/main/java | Application/Library sources
   src/main/resources | Application/Library resources
   src/main/filters | Resource filter files
   src/main/webapp | Web application sources
   src/test/java | Test sources
   src/test/resources | Test resources
   src/test/filters | Test resource filter files
   src/it | Integration Tests (primarily for plugins)
   src/assembly | Assembly descriptors
   src/site | Site
   LICENSE.txt | Project's license
   NOTICE.txt | Notices and attributions required by libraries that the project depends on
   README.txt | Project's readme

2. **Naming Convetion**:
   * [Oracle Naming Convention](https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html)
   
   Identifier | Description | Example
   ---------- | ----------- | -------
   Package | lowercase, separated by dots | com.sun.project
   Class | nouns, first letter of each word capitalized, avoid abbreviations | InputStreamReader
   Interface | like class names | Runnable, Iterable
   Method | verbs, first letter lowercase, first letter of each internal word capitalized | runInBackground()
   Variable | first letter lowercase, first letter of each internal word capitalized | int streamReader;
   Constant | all uppercase, words separated by underscores ("_") | static final int MIN_WIDTH = 5;

3. **Source File Structure**:
   * [Spring Source File Structure](https://github.com/spring-projects/spring-framework/wiki/Code-Style#source-file-structure)
 
  1. **License**: each source file must specify the following license at the very top of the file

         /*
         * Copyright 2002-2019 the original author or authors.
         *
         * Licensed under the Apache License, Version 2.0 (the "License");
         * you may not use this file except in compliance with the License.
         * You may obtain a copy of the License at
         *
         *      https://www.apache.org/licenses/LICENSE-2.0
         *
         * Unless required by applicable law or agreed to in writing, software
         * distributed under the License is distributed on an "AS IS" BASIS,
         * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
         * See the License for the specific language governing permissions and
         * limitations under the License.
         */

   2. **Package Statement**

   3. **Import Statements**: 

           import java.*
           //blank line
           import javax.*
           //blank line
           import all other imports
           //blank line
           import org.springframework.*
           //blank line
           import static all other imports

   4. **Java Source File Organization**:
       * static fields
       * normal fields
       * constructors
       * (private) methods called from constructors
       * static factory methods
       * JavaBean properties (i.e., getters and setters)
       * method implementations coming from interfaces
       * private or protected templates that get called from method implementations coming from interfaces
       * other methods
       * equals, hashCode, and toString

4. **Whitespaces**:
     * Two blank lines before starting static blocks, fields, constructors and inner classes
     * One blank line after a method signature that is multiline
     * A single space separating reserved keywords like if, for, catch from an open parentheses
     * A single space separating reserved keywords like else, catch from a closing parentheses

5. **Identation**: No single convention
     * 4 spaces or tab
     * Line capacity 80 char.
     * Breaking statement:
       * Break method calls after comma.
       * Break expressions before an operator.
       * Two spaces for next lines.

6. **Method Parameters**:

7. **Hardcoding**:

8. **Code Comments**:

9. **Logging**:

### SOLID Principles

### DRY & KISS
DRY: Don't Repeat Yourself
KISS: Keep It Simple, Stupid.

### TDD
Test Driven Development

### Tools

### Ref
* https://www.baeldung.com/java-clean-code
