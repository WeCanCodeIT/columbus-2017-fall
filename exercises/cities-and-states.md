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
|Task|Points|
|----|------|
|*Prompts for and stores:*|--|
|first name (String)|6|
|last name (String)|6|
|age (int)|6|
|birth month (int)|6|
|favorite color (String)|6|
|number of siblings (int)|6|
|Displays ROYGBIV help if the user types "Help"|6|
|Prompts for a favorite color and stores the value after displaying help if the user typed "Help"|6|
|*Calculates and stores:*|--|
|years until retirement based on odd or even age|8|
|vacation home location based on number of siblings|8|
|mode of transportation based on favorite color|8|
|bank balance based on birth month|8|
|Display the fortune in the specified format|10|
|Style/formatting/code quality:|10|
|**Total:**|**100**|

