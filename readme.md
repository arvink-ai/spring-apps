# Spring Apps
reference: Spring in Action
## chap 0
1. mvnw and mvnw.cmd—These are Maven wrapper scripts. You can use these scripts
to build your project, even if you don’t have Maven installed on your machine.
2. Spring Boot starter dependencies are spe-
cial in that they typically don’t have any library code themselves but instead transi-
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







