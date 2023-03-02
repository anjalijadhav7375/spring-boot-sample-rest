# spring-boot-sample-rest-app

### A sample spring boot rest application and demo rest methods

REST (Representational State Transfer) is an architectural style used in web development for building scalable, performant, and maintainable web services. RESTful API (Application Programming Interface) is an implementation of the REST architecture.

RESTful API is a type of web API that is designed to work with HTTP (Hypertext Transfer Protocol) requests such as GET, POST, PUT, DELETE, etc., to retrieve, create, update or delete resources on the web. RESTful APIs use HTTP methods to define the actions to be performed on resources, and use URLs (Uniform Resource Locators) to identify resources.

RESTful APIs typically return data in JSON (JavaScript Object Notation) or XML (Extensible Markup Language) format, which are both lightweight and easy to parse. They also use hypermedia links to navigate between resources and represent the state of the system.

RESTful APIs are widely used in modern web development for creating web services that are easy to consume, scalable, and platform-agnostic. They are used by many popular web applications and services, such as Twitter, Facebook, and Google Maps.


> Example of URL :- `http://localhost:8080/greeting?name=Vikram`

* http -> protocol
* localhost -> domain name
* 8080 -> http port
* /greeting -> path or endpoint
* name -> request parameter key
* Vikram -> request parameter value

### Spring Boot Annotations:
1. `SpringBootApplication` : `@SpringBootApplication` is a convenience annotation that adds all of the following:
   `@Configuration`: Tags the class as a source of bean definitions for the application context.
   `@EnableAutoConfiguration`: Tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings. For example, if spring-webmvc is on the classpath, this annotation flags the application as a web application and activates key behaviors, such as setting up a DispatcherServlet.
   `@ComponentScan`: Tells Spring to look for other components, configurations, and services in the com/example package, letting it find the controllers.
2. `SpringBootTest`
3. `RestController` : The Spring boot `@RestController` annotation, which marks the class
   as a controller where every method returns a domain object instead of a view.
   It is shorthand for including both `@Controller` and `@ResponseBody`.
4. `GetMapping` : The @GetMapping annotation ensures that HTTP GET requests to /greeting are mapped to the greeting() method.
5. `PostMapping` : Create resource
6. `PutMapping` : Update resource
7. `PatchMapping` : Partial update of resource
8. `DeleteMapping` : Delete existing resource
9. `RequestParam` : @RequestParam binds the value of the query string parameter name into the name parameter of the greeting() method. If the name parameter is absent in the request, the defaultValue of World is used.

The main() method uses Spring Boot’s SpringApplication.run() method to launch an application. Did you notice that there was not a single line of XML? There is no web.xml file, either. This web application is 100% pure Java and you did not have to deal with configuring any plumbing or infrastructure.

Note:
There are companion annotations for other HTTP verbs (e.g. @PostMapping for POST). There is also a @RequestMapping annotation that they all derive from, and can serve as a synonym (e.g. @RequestMapping(method=GET)).
### Reference [Tutorial](https://spring.io/guides/gs/rest-service/)