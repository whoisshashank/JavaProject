Campus Course & Records Manager (CCRM)
A Java SE console-based application to manage students, courses, enrollments, grades, transcripts, file operations, and backups, demonstrating modern Java features and OOP principles.

Project Overview
CCRM allows an institute to:

Manage Students: Add, list, update, deactivate, enroll/unenroll in courses, print profile and transcript

Manage Courses: Add, list, update, deactivate, assign instructors

Enrollment & Grades: Enroll/unenroll students with rules, record marks, compute GPA, generate transcripts

File Operations: Import/export data as CSV-like text, perform timestamped backups with recursion

Command-Line Interface: Menu-driven workflow, robust error handling

How to Run
Prerequisites:

JDK 17 or above (tested on JDK 21)

Windows OS

Eclipse IDE (recommended for setup and running)

Quick Start (Console):

bash
javac -d bin src/edu/ccrm/Main.java
java -cp bin edu.ccrm.Main
For Eclipse: Import the project and run Main.java

Directory Structure
text
edu.ccrm/
├─ cli/             // CLI menu, input loop
├─ domain/          // Person (abstract), Student, Instructor, Course, Enrollment, enums
├─ service/         // StudentService, CourseService, EnrollmentService, TranscriptService
├─ io/              // ImportExportService, BackupService, CSV parsing
├─ util/            // Validators, Comparators (lambdas), recursion utilities
└─ config/          // AppConfig (Singleton), builders
screenshots/        // Setup, run, output screenshots
sample-data/        // Example CSV files for import
README.md           // This file
USAGE.md            // Sample usage/commands
Evolution of Java (Key Milestones)
1995: Java 1.0 released (Sun Microsystems)

2004: Java 5 (Generics, Enums, Metadata)

2011: Java 7 (NIO.2, Try-with-resources)

2014: Java 8 (Lambdas, Streams, Date/Time API)

2017: Java 9 (Modules)

2021 onward: Java 17+ (Pattern Matching, Enhanced Switch, Records, etc.)

Java ME vs SE vs EE
Category	Description	Use Case/Scope
Java ME	Micro Edition	Embedded/mobile devices
Java SE	Standard Edition	Desktop/server apps
Java EE	Enterprise Edition	Enterprise/web backend
Java Architecture: JDK vs JRE vs JVM
JDK (Java Development Kit): Toolset for development and building (compiler, docs, etc.)

JRE (Java Runtime Environment): Libraries and JVM for running Java applications

JVM (Java Virtual Machine): Interprets and executes Java bytecode across platforms

Install & Configure Java on Windows
Download JDK from oracle.com

Run installer and set JAVA_HOME environment variable

Add Java bin folder to PATH

Verify installation:

bash
java -version
See screenshots/jdk-install.png

Eclipse IDE: Create and Run Project
Launch Eclipse, go to File > New > Java Project

Add source folders (src/edu/ccrm/…)

Right-click Main.java > Run As > Java Application
See screenshots/eclipse-project.png and screenshots/eclipse-run.png

Mapping Table: Syllabus Topic to Code Location
Topic	File/Class/Method
Encapsulation/Getters/Setters	domain/Student, domain/Instructor
Inheritance/Abstraction/Polymorphism	domain/Person (abstract), subtypes
Interfaces, Diamond Problem	util/Searchable, io/Persistable
Functional Interfaces and Lambdas	util/Comparators, service/CourseService
Anonymous Inner Class	cli/MainMenu (callback)
Enums	domain/Semester, domain/Grade
Singleton Pattern	config/AppConfig
Builder Pattern	domain/Course.Builder, Transcript.Builder
Exception Handling	util/exceptions, service/EnrollmentService
File I/O (NIO.2, Streams)	io/ImportExportService, BackupService
Date/Time API	domain/Enrollment, io/BackupService
Arrays/Sorting/Searching	util/Comparators, Arrays.sort/search
CLI Menu, Switch/Loop constructs	cli/MainMenu, cli/InputHandler
Recursion (Backup Size)	util/RecursionUtil, io/BackupService
toString/Overriding/Overloading	domain/, service/
Upcast/Downcast, instanceof	service/TranscriptService
Assertions	Various classes (see comments)
Notes on Assertions
To enable assertions when running:

bash
java -ea -cp bin edu.ccrm.Main
See README and code comments for invariants.

Usage
Sample commands and CSV file formats are given in USAGE.md.

