# Library Pair Programming Activity

## Objectives
- Students will use **Object Relational Mapping (ORM)** to connect entities together 
- Students will become familiar with the tools of the CRUD Repository
- Students will create data to test by @Override of the run method of CommandLineRunner
- Students will complete this activity in a pair-programming setting where one is always "driving" and one is "directing"
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
|Fiction|
|Non Fiction| 

