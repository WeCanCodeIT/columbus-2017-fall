## Week 7


### Tues Nov 7

Let's add some queries to the `customers-jpa` project and update our `CustomerController` to see these changes happen in our application

- Remove the commenting from `CustomerPopulator` ... at least so that the database is available during run time
- Run your application to make sure the names are properly showing when navigating to `localhost:8080/customers`
- In `CustomerController` allow for requests to be made to `localhost:8080` that would show all names in the database
- In `CustomerController` display all of the people with the last name of "Bauer" when navigating to `localhost:8080/bauer`
- Update the `CustomerRepository` with the following query: `Collection<Customer> findAll(Sort sort);` 
  - In `CustomerController` allow for requests to be made to `localhost:8080/customers-sorted` to display a sorted list of the database
    - Navigate to `localhost:8080/h2-console` and connect to the default in memory database...add a record and refresh the `customers-sorted` page...notice what happens
