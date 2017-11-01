### Getting Started
## Accessing Data with JPA
  - Purpose: [This guide](https://wecancodeit.github.io/java-resources/spring/getting-started-guides/accessing-data-with-jpa/) will demonstrate how to use Spring and JPA to save objects to a database and fetch them. 
  
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

## Creating Queries
- Popular queries include:
  - saving
  - deleting
  - finding

## Let's observe our application in action
- We can see in our `CustomerPopulator` class a  `CommandLineRunner` what is this doing?
- We can see calls to `findOne`and `findAll` as well as `save` but we haven't coded these methods...where are they coming from?
- Where is `findByLastName` coming from?

## What is Hibernate?
- Wired together by the Spring framework, Hibernate is used to persist Java objects into Relational Databases
- It is not easy to get object oriented code...remember == and .equals()???...identity and equality???? yeahhhhh to mesh well with Relational Databases...and Relational Databases are going to be very popular in the enterprise world ...[READ MORE...](https://www.packtpub.com/books/content/introduction-hibernate-and-spring-part-1)



