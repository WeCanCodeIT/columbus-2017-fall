### Getting Started
## Accessing Data with JPA
  - Purpose: [This guide](https://wecancodeit.github.io/java-resources/spring/getting-started-guides/accessing-data-with-jpa/) will demonstrate how to use Spring and JPA to save objects to a database and fetch them. 
  - By the end of this guide, students will be able to 
    - Create an in memory database using Command Line Runner in a Populator class
    - Create an in memory database using H2
    - Create a persistent database using H2
    - Write SQL commands to develop and manipulate a database
    - Write queries using the CRUD repository and add own implementations to a Repository class
  
## Customer Class
- `Customer` objects are stored as a JPA Entity
  - Contains 3 attributes
    - id
    - firstName
    - lastName
   - Default Constructor
    - exists for the sake of JPA
    - but don't all classes already contain a default constructor? Why do I need to specify this?
      - all classes do...until you implement a constructor of your own with arguments
      - so make sure to specify the default no args constructor
      
     - can be protected or public
     - JPA & Hibernate will use reflection to create an instance of an object at runtime...being dynamic, this constructor will be needed
- `@Entity`: maps class to a table called `Customer`
  - attributes of `id`, `firstName` and `lastName` can be thought of as the columns
  - each created object can be thought of as the rows in the table
  
  - Object Relational Mapping: **[ORM](http://hibernate.org/orm/what-is-an-orm/)**

## Creating Queries
- Spring Data JPA focuses on using JPA to store data in a relational database
- One of its most compelling features is its ability to create repository implementations from the CRUD repository
- Popular queries include:
  - saving
  - deleting
  - finding
- The [CRUD Repository](https://docs.spring.io/autorepo/docs/spring-data-commons/1.5.1.RELEASE/api/org/springframework/data/repository/CrudRepository.html)

## Let's observe our application in action
- We can see in our `CustomerPopulator` class a  `CommandLineRunner` what is this doing?
- We can see calls to `findOne`and `findAll` as well as `save` but we haven't coded these methods...where are they coming from?
- Where is `findByLastName` coming from?
- Add the ability to `findByFirstName` and test this Query
- Change `findByLastName` to `lookForLastName` and observe what happens....[Here's Why: Working with Spring Data Repositories](https://docs.spring.io/spring-data/data-commons/docs/1.6.1.RELEASE/reference/html/repositories.html)
- Change queries to `readByLastName` or `getByLastName` and notice what happens

## What is Hibernate?
- Wired together by the Spring framework, Hibernate is used to persist Java objects into Relational Databases
- It is not easy to get object oriented code...remember == and .equals()???...identity and equality???? yeahhhhh to mesh well with Relational Databases...and Relational Databases are going to be very popular in the enterprise world ...[READ MORE...](https://www.packtpub.com/books/content/introduction-hibernate-and-spring-part-1)

## Connecting to an H2 Database
`jdbc`: protocol
`h2`: database (vendor)
`mem`: H2-specific, means use a temporary in-memory database
`testdb`: arbitrary database identifier/name, the default used by Spring Boot

- Add a record through the H2 Database, refresh the MVC application to see the results
- Remove the added record from the H2 Database, refresh the MVC application to see the results
- Remove all last names of Bauer, using the H2 Database, refresh the MVC application to see the results

## In memory database
So far, we’ve been using a temporary embedded in-memory database that disappears once our app shuts down. We can still run H2 as embedded (as opposed to installing a standalone server) but use a persistent datastore. To do so, we need to specify a JDBC URL.

## Persistent database
[Configuring H2 to use a Persistent Database](https://wecancodeit.github.io/java-resources/data-access/h2/persistent-storage/)

## Extra Practice
- Use this same project to create another persistent database. Practice adding a few items, deleting items and ordering items. Use the SQL commands from W3 Schools for guidance. 
- Create a java class called `CustomerOrder` that creates an entity to handle customer orders. It can become a table to handle order number, customer and item. Build a database (in memory or persistent) your choice. Create a simple MVC application to show the orders.
