# Accessing data with JPA

## Objectives
- Students will use **Object Relational Mapping (ORM)** to connect entities together 
- Students will become familiar with the tools of the CRUD Repository
- Students will create data to test by @Override of the run method of CommandLineRunner

Today most of the development is carried out in an object oriented manner using languages like java,C++ etc.
When thinking in terms of Java as the programming language,the business logic of an application works with Objects of different class types. 
However when dealing with the data store,it's important to note that the tables of a database are not objects,which becomes an issue. 
This is where the concept of Object Persistence comes in. Object Persistence deals with persistence in object oriented program such as java.
It means determining how objects and their relationships are persisted in a relational database.


## Project Setup
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

## Create the Instructor class
- Our class will use `@Entity` 
- This class will allow for an instance of `instructor` to be built out
- Our `instructor` will have an `id`, `firstName`, and `lastName`
- Attach `@Id` and `@GeneratedValue` to the proper instance variable
- We need to create a `@OneToMany` relationship mapped by `instructor` onto a collection (Set) of `courseTopics` (Why a Set?)
- Let's create a no args constructor, a more defined constructor and some accessor methods so that we can have some display in our Thymeleaf templates

## Create the CourseTopic class
- In similar fashion create this class to hold an instance of `courseTopic`
- What should we use for instance data?
- What is the relationship between `CourseTopic` and `Instructor`?

## Create your interfaces that extend the CrudRepository
- InstructorRepository
- CourseTopicRepository

## Create the CourseTopicPopulator Class
- This will use `@Component`
- Bring in `@Resource` for an `instructorRepo` and a `courseRepo`
- Override the run method to 
  - Create and save 3 instructors
  - Create and save 4 courses

## Create the CourseController Class
- You will need to be able to call methods of the repository interfaces...what should we declare?
- @RequestMapping for all instructors and one instructor....and all courses and one course

## Build out your Thymeleaf templates
- Be able to view a list of courses and navigate into information on each course...including name of course, description and instructor
- Also be able to view a list of instructors and be able to navigate to information on each instructor...including the courses they are teaching

## Stretch Tasks
- Be able to find all courses that contain the word Java

