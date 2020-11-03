# Clean Code
**Clean Code** is a code that any developer can read and change easily.

## Why?
* **Maintainable Codebase**: clean code can help develop software that is easy to change and maintain.
* **Easier Troubleshooting**: clean code is easier to troubleshoot for problems.
* **Faster Onboarding**: a quicker onboarding for newcomers to keep productivity high.

## Characteristics
* **Simple**: design and implementation must be as simple as possible.
* **Focused**: code should be written to solve a specific problem.
* **Testable**: easy to test the codebase, preferably in an automated manner.

## Java

### 1. Project Structure
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

### 2. Naming Convetion
 * [Oracle Naming Convention](https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html)

 Identifier | Description | Example
 ---------- | ----------- | -------
 Package | lowercase, separated by dots | com.sun.project
 Class | nouns, first letter of each word capitalized, avoid abbreviations | InputStreamReader
 Interface | like class names | Runnable, Iterable
 Method | verbs, first letter lowercase, first letter of each internal word capitalized | runInBackground()
 Variable | first letter lowercase, first letter of each internal word capitalized | int streamReader;
 Constant | all uppercase, words separated by underscores ("_") | static final int MIN_WIDTH = 5;

### 3. Source File Structure
* [Spring Source File Structure](https://github.com/spring-projects/spring-framework/wiki/Code-Style#source-file-structure)

  * **License**: each source file must specify the following license at the very top of the file

         /*
         * Copyright 2002-2020 the original author or authors.
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

   * **Package Statement**

   * **Import Statements**: 
      * All static imports
      * All non-static imports

   * **Java Source File Organization**:
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

### 4. Whitespaces
   * Two blank lines before starting static blocks, fields, constructors and inner classes
   * One blank line after a method signature that is multiline
   * A single space separating reserved keywords like if, for, catch from an open parentheses
   * A single space separating reserved keywords like else, catch from a closing parentheses

### 5. Identation
No single convention
   * 4 spaces or tab
   * Line capacity 80 char.
   * Breaking statement:
     * Break method calls after comma.
     * Break expressions before an operator.
     * Two spaces for next lines.

### 6. Method Parameters
  * Max. 3 parameters.
  * Refactor methods having more than recommended parameters.
  * Don't put unrelated parameters together to decrease number of parameters.
  * You mustn't be pedantic about this.

### 7. Hardcoding
  * It can lead to duplication, which makes change more difficult.
  * If possible, replace with values which can be picked from configuration or environment.

        private int storeClosureDay = 7;
        // This can be refactored to use a constant from Java
        private int storeClosureDay = DayOfWeek.SUNDAY.getValue()

### 8. Code Comments
  * Don't include obvious things in the comments.
  * Comments should only complement a code.
  * Use block comments rarely, possibly to describe non-trivial design decisions.
  * Use JavaDoc comments for most of our classes, interfaces, public and protected methods.
  * All comments should be well-formed with a proper indentation for readability.

  * Two Types of Comments:
    * Documentation/JavaDoc Comments
        * The audience here is the users of the codebase
        * The details here are typically implementation free, focusing more on the specification
        * Typically useful independent of the codebase
    * Implementation/Block Comments
        * The audience here is the developers working on the codebase
        * The details here are implementation-specific
        * Typically useful together with the codebase

### 9. Logging
  * Avoid excessive logging.
  * Choose log levels wisely.
  * Be very clear and descriptive in the log message.
  * Use external tools for tracing, aggregation, filtering of log messages for faster analytic.
  * Frameworks in Java for logging, including **SLF4J**, **Logback**.

### 10. Tools
  * **Code Reviews** have always been a great tool to maintain consistency and help the developers grow through constructive feedback.
  * However, we do not necessarily have to validate all these principles and best practices manually during code reviews.
  * **Code Formatters**: Eclipse and IntelliJ.
  * **Static Analysis Tools**: SonarQube, Checkstyle, PMD and SpotBugs.
    * detecting a lot of code smells like violations of naming conventions and resource leakage.

## DRY & KISS
* **DRY**: Don't Repeat Yourself.
* **KISS**: Keep It Simple, Stupid.

## TDD
Test Driven Development
* Start with the design development of automated tests.
* This leads to software that always works as expected.
* As we always start with tests, we incrementally add working code in small chunks.
* Also, we only add code if the new or any of the old tests fail. Which means that it leads to reusability as well.

## SOLID Principles
**Martin**: design principles encourage us to create more maintainable, understandable, and flexible software.

### 1. Single Responsibility
(interface, class, or method) should have only one responsibility, and one reason to change.
* Book, BookPrinter [example](https://www.baeldung.com/solid-principles#s)

### 2. Open/Closed


### 3. Liskov Substitution

### 4. Interface Segregation

### 5. Dependency Inversion

## Ref
* https://www.baeldung.com/java-clean-code
* https://www.baeldung.com/solid-principles

