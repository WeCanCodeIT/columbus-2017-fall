#Accessing data with JPA

##Objectives
- Students will use **Object Relational Mapping (ORM)** to connect entities together 
- Students will become familiar with the tools of the CRUD Repository
- Students will create data to test by @Override of the run method of CommandLineRunner

Today most of the development is carried out in an object oriented manner using languages like java,C++ etc.
When thinking in terms of Java as the programming language,the business logic of an application works with Objects of different class types. 
However when dealing with the data store,it's important to note that the tables of a database are not objects,which becomes an issue. 
This is where the concept of Object Persistence comes in. Object Persistence deals with persistence in object oriented program such as java.
It means determining how objects and their relationships are persisted in a relational database.


##Project Setup
- Using the [Spring Initializr](https://start.spring.io/) build out a new Gradle Project
  - name the package `com`
  - use kebab case to name the Artifact `courses-with-instructors`
  - bring in the following dependencies
      - Thymeleaf
      - H2
      - Web
      - Devtools
      - Jpa
- Extract all into your `code` directory
- Through Bash, access `courses-with-instructors` and run **gradle eclipse**
- Import your project through Eclipse

##
