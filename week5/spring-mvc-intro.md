# Using Spring to build an MVC Application

### Objectives
- Students will be introduced to the Spring Framework by creating a sample MVC application
- Stidents will `Model` a `CourseTopic` and setup a `CourseController` to handle GET requests to display many and one courses in a `View`

### Annotations used in this tutorial
- **`@Repository`**: Indicates that an annotated class is a "Repository", originally defined by Domain-Driven Design (Evans, 2003) as "a mechanism for encapsulating storage, retrieval, and search behavior which emulates a collection of objects".
- **`@Controller`**: Handles HTTP Requests
- **`@Resource`**: The Resource annotation marks a resource that is needed by the application. This annotation may be applied to an application component class, or to fields or methods of the component class. When the annotation is applied to a field or method, the container will inject an instance of the requested resource into the application component when the component is initialized.
- **`@RequestMapping`**: Annotation for mapping web requests onto specific handler classes and/or handler methods.
- **`@RequestParam`**: Annotation which indicates that a method parameter should be bound to a web request parameter. If the method parameter type is Map and a request parameter name is specified, then the request parameter value is converted to a Map assuming an appropriate conversion strategy is available. 

Not an annotation but important to define:
- **`Model model`**: Java-5-specific interface that defines a holder for model attributes. Primarily designed for adding attributes to the model. Allows for accessing the overall model as a java.util.Map.

### Project Set-up (will be demonstrated in the video tutorial)
- Use the Spring Initializr to create the java-courses project
  - We will add the devtools dependency. This will allow us to make changes during run time without having to restart our server.
- Unzip to your default-package or code folder 
- Access through `Bash` and do a `gradle eclipse`
- `import` through your Eclipse package explorer

### Classes to build
- `CourseTopic`: The Model Class
  - contains object properties for `id`, `name`, and `description`
  - contains appropriate constructor, getters and setters
- `CourseRepository`: The Maintenance Class for the map
 - contains the ability to access the entire map or one item in a map
- `CourseController`: The Controller class to handle HTTP requests
- An Application class that will already be build out using the Spring Initializr

### Resources to build

The following html resources are needed to `View` the application during run time. We will begin to go into deeper detail about these files on Wednesday and Thursday once we get into Front End Design with Intro to HTML and Thymeleaf. For now, copy these into your project so that you are able to see this application in action.

In **templates** create **`courses.html`** and paste the following code snippet
```bash
<!DOCTYPE HTML>

<html xmlns:th="http://www.thymeleaf.org">

<head>
<title>A list of courses</title>
</head>

<body>
	<header>
		<h1>A List of Courses</h1>
	</header>
	
	<div th:each="course: ${courses}">
		<h2>
			<a th:href="@{/course(id=${course.getId()})}" th:text="${course.getName()}"></a>
		</h2>
	</div>


</body>
</html>
```

In the templates package, create **`course.html`** and paste the following code snippet
```bash
<!DOCTYPE HTML>

<html xmlns:th="http://www.thymeleaf.org">

<head>
<title>A course</title>
</head>

<body>

	<header>
		<h1> A Course </h1>
	</header>

	<div th:each="course: ${courses}">
		<h2 th:text="${course.getName()}"></h2>
		<h2 th:text="${course.getDescription()}"></h2>
		<a href="http://localhost:8080/courses">Back to home</a>
	</div>

</body>
</html>
```

