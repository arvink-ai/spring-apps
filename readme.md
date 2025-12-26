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
    
