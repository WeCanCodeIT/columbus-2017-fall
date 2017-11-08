# Library Pair Programming/ Mobbing Activity

## Objectives
- Students will use **Object Relational Mapping (ORM)** to connect entities together 
- Students will become familiar with the tools of the CRUD Repository
- Students will create data to test by @Override of the run method of CommandLineRunner
- Students will complete this activity in a pair-programming setting or mobbing where one is always "driving" and one is "directing"
- Students will create the following relationships:
  -`@OneToMany`
  -`@ManyToOne`
  -`@ManyToMany`


## Setup
- Use the Spring Initilizr to create `library-jpa`
- Bring over the following dependencies
  - Thymeleaf
  - Devtools
  - H2
  - JPA
  - Web

## The Project Explanation
Libraries categorize books by `Genre`. A `Book` can only belong to one `Genre` in our Library. Some of our authors are busy and they have written multiple books. An `Author` can also share duties, so multiple authors can write a single book. 

### The `Genre` Table
|genre|
|----|
|Fiction|
|Non Fiction|

### The `Author` Table
|firstName|lastName|
|----|--------|
|Kathy|Sierra|
|Bert|Bates|
|Elisabeth|Freeman|
|Clifford|Stoll|

### The `Book` Table
|genre|title|authors|
|----|--------|---|
|Non Fiction|Head First Design Patterns|Kathy Sierra, Bert Bates|
|Non Fiction|Head First Java|Kathy Sierra, Elisabeth Freeman|
|Fiction|The Cukoo's Egg|Clifford Stoll|

### Determine your relationships
- One of our tables has a `@OneToMany` relationship
- One of our tables has a `@ManyToMany` relationship
- One of our tables has both a `@ManyToOne` and a `@ManyToMany` relationship

## Build out the necessary files
- An Entity class for each table
- A Repository for each table
- A Controller that handles requests to `genres.html`, `authors.html` and `books.html`
- A Populator to build the database 

### Hints
- Your `Book` constructor must handle the multiple authors last in the params... it will look like this:
  ```bash
  public Book (Foo foo, Bar bar, FooBar ... fooBar){
      this.foo = foo;
      this.bar = bar;
      this.fooBar = new HashSet(Arrays.asList(fooBar));
      }
   ```
 - Use concatenation in Thymeleaf to display attributes in the same way you would in Java...with the + sign...only difference is you will use 'single quotes' to enclose Strings or empty space
   ```bash
   <p th:text="${'Name: ' + item.firstName + ' ' + item.lastName}"></p>
   ```
   
