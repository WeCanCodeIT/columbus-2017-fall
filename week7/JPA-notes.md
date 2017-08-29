## Spring Data JPA

### There are standard methods in a typical resource in a REST API in Spring MVC

- Get all resources
- Get an individual resource 
- Create or add new resource
- Update/change a resource
- Delete a resource

### What is JPA

- Java Persistence API
  - Allows for **Object-Relational Mapping (ORM)**
- Most databases that you are accessing are SQL
- **SQL** is a Relational Database
- A **Relational Database** contains tables and keys 
- ORM lets you map entity classes to SQL tables

### The Entity Class

- The class that needs mapped to the database
- Think of the member variables (instance data) as the columns
- Think of the objects (class instances) as the rows 

Example:

 ```
  @Entity
  public class Topic {
  
  @Id
  private String id;
  private String name;
  private String description;

```
- with the **@Entity** annotation JPA knows to create a table called Topic with 3 columns: id, name and description
- **@Id** tells the database where the primary key is
- The annotaions affect what is directly underneath, therefore attaching @Id to the String id member

### The Process

- Step 1: Entity Mapping
- Step 2: Find the class to connect to the database and run commands to access, save and retrieve data
  - No matter what your entity is, the structor will remain very similar (Standard operations)

### The CrudRepository

- Contains the logic for an entity class
- CrudRepository Generic Type
- CrudRepository<What is the Entity Class?, What is the id this Entity class has?>
  - **public interface TopicRepository extends CrudRepository<Topic,String>**
- You will now have access to all methods that come out of the box with CrudRepository
  - These methods will update
    - Get all resources
    - Get an individual resource 
    - Create or add new resource
    - Update/change a resource
     - Delete a resource 

### One to Many

- **@OneToMany** 
- Topics can contain multiple courses, for example,  but each course will belong to one topic 
- A course is then tied to a particular topic 


  
