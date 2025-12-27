# Spring Apps
reference: Spring in Action
## chap 0
1. mvnw and mvnw.cmd—These are Maven wrapper scripts. You can use these scripts to build your project, even if you don’t have Maven installed on your machine.
2. Spring Boot starter dependencies are special in that they typically don’t have any library code themselves but instead transi-
tively pull in other libraries. think of your dependencies in terms of what capabilities they
provide, rather than their library names.
3. You’re freed from the burden of worrying about library versions.
## Chap 1
    1. Static contents like images and static static html are kept in resourece/static while dynamic view contents are kept resources/template
    2. In thymeleaf, logical view is returned. It does not have html suffix. The template name is derived form the logical view name by prefixing it with /templates and postfixing it with html. For example if view name is 'home', then template will be templates/home.html
    3. @SpringBootApplication is a composite annotation that combines the following three annotations:
        a. @SpringBootConfiguration—Designates this class as a configuration class.
        b. @EnableAutoConfiguration—Enables Spring Boot automatic configuration.
        c. @ComponentScan—Enables component scanning.
    4. With DevTools as part of your project, you’ll be able to make changes to Java code and properties files in the project and see those changes applied after a brief moment. DevTools monitors for changes, and when it sees something has changed, it automatically restarts the application.
    5. when DevTools is active, the application is loaded into two separate class loaders in the Java virtual machine (JVM). One class loader is loaded with your Java code, property files, and pretty much anything that’s in the src/main/ path of the project. These are items that are likely to change frequently. The other class loader is loaded with dependency libraries, which aren’t likely to change as often.
    5. AUTOMATIC BROWSER REFRESH AND TEMPLATE CACHE DISABLE- Thymeleaf and FreeMarker are configured to cache the results of template parsing so that templates don’t need to be reparsed with every request they serve. good for production. In dev it should be disabled. Dev tools automatically caching them.
    6. The devtool disable caching. But user need to refresh in browser. To Auto refresh browswr. devTools enable LiveReload server. Use it with LievReload browser plugin. It autmatically refreshes your browser whenever  a change occurs in application. A change could be when changes are made to templates, images, stylesheets, JavaScript.
    7. BUILT-IN H2 CONSOLE if your applcaitons uses h2 db. DevTools enables h2 console in browser
    8. 1.4.2 Spring Boot also offers following features:
        a. The Actuator provides runtime insight into the inner workings of an application, including metrics, thread dump information, application health, and environment properties available to the application.
        b. Flexible specification of environment properties.
        c. Additional testing support on top of the testing assistance found in the core framework.
    9. 1.4.3 Spring data:
        a. the ability to define your application’s data repositories as simple Java interfaces, using a naming convention when definingmethods to drive how data is stored and retrieved.
        b. wroks with rdbcs ie jdbc jpa, document(mongoDb), graph (Neo4J) etc
    10. 1.4.4 Spring Security
    11. 1.4.5 Spring Integration and Spring Batch
    12. Spring Cloud -- microservices etc
    13. Spring Native like GraalVM

## Chap 2
    0. highlights: Presenting model data in the browser, Processing and validating form input, Choosing a view template library
    1. Controller fetch an dproecess data. View render that into html that will be displayed in the browser
    2. An application’s domain is the subject area that it addresses—the ideas and concepts that influence the understanding of the application.
       . In our taco design. case, objects are taco design, ingredients, customers, taco orders
    3. @Slf4j, is a Lombok-provided annotation that, at compilation time, will automatically generate an SLF4J Logger static property in the class.
    4. The @RequestMapping annotation, when applied at the class level, specifies the kind of requests that this controller handles.
    5. @SessionAttributes: TacoOrder object that is put into the model a little later in the class should be maintained in session.
    Spring MVC request-mapping annotations
    6. @ModelAttribute has two uses in Spring MVC:
        a. Method-level (with name, creates model attribute)
        b. Method-level (without name )(populates model before handler methods). ie Executes before any request handler (@GetMapping, @PostMapping, etc.). It Adds common data needed by multiple views. In my case, adds ingredients filtered by type to the model
    7. Spring MVC request-mapping annotations:
        @RequestMapping -> General-purpose request handling
        @GetMapping  -> Handles HTTP GET requests
        @PostMapping  -> Handles HTTP POST requests
        @PutMapping  -> Handles HTTP PUT requests
        @DeleteMapping  -> Handles HTTP DELETE requests
        @PatchMapping  -> Handles HTTP PATCH requests
    8.Model is an object that ferries data between a controller and whatever view is charged with rendering that data.Ultimately, data that’s placed in Model attributes is copied into the servlet request attributes, where the view can find them and use them to render a page in the user’s browser.
    9. thymeleaf templates html plus additional tags which guide a template in rendering reequest data. example:
        a. <p th:text="${message}">placeholder message</p>. When the template is rendered into HTML, the body of the <p> element will be replaced with the value of the servlet request attribute whose key is "message".
        b. th:each, that iterates over a collection of elements, rendering the HTML once for each item in the collection.
    10. "redirect:/orders/current" means browser should be directed to the relative patj /orders/current
    





