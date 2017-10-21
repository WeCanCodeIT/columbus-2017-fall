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

Not an annotation:
- **`Model model`**: Java-5-specific interface that defines a holder for model attributes. Primarily designed for adding attributes to the model. Allows for accessing the overall model as a java.util.Map.

