## The Objective
- Students will be able to run unit tests to develop a better understanding of Comparables, Comparator and sorts

## Project Setup
- In Bash, mkdir `employee-sorts` and run the Gradle script for unit testing.
- Create an `Employee` class to handle id, first name and last name.
- **Implement** the `Comparable` interface on this class as you will be creating a List of Employees.
- Build a Comparator class that sorts by last name and then first name (assuming last names are the same)
- Create the following tests
  - Test if employee id's are identical
  - Sort by id by default (Think about our sort demo before we changed over to Names)
  - Sort by last name and then first name using the Comparator
  
  **Hint** For testing purposes you can initialize an ArrayList with values like this:
  `List<ClassName> foo = new ArrayList<>(asList(foo1, foo2, foo3, etc));
