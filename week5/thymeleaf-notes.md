## Using Thymeleaf templates

### What is Thymeleaf?
- a modern server-side Java Template engine for both web and standalone environments, capable of processing HTML, XML, JavaScript, CSS and even plain text
- assists in your front-end HTML designs

### Iterating in Thymeleaf
-th: each 
  - for each item in a collection of items
  - similar to a for each loop traversing a List
  - will iterate over a list of products, array, map or other collection
  
  ### Examples
  ```
  <tbody>
    <tr th:each="student: ${students}">
        <td th:text="${student.id}" />
        <td th:text="${student.name}" />
    </tr>
</tbody
  
  
  <td>
    <span th:if="${student.gender} == 'M'" th:text="Male" /> 
    <span th:unless="${student.gender} == 'F'" th:text="Female" />
</td>

```


  
