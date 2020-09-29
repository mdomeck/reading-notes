## Spring Request Mapping
- `@RequestMapping` is used to map web requests to Spring Controller methods
- can optionally define the parameters
- binding parts of the URI with `@PathVariable`

## Accessing Data with JPA
- `@SpringBootApplication` will add...
- `@Configuration` Tags the class as a source of bean definitions for the application context.
- `@EnableAutoConfiguration` Tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings. For example, if spring-webmvc is on the classpath, this annotation flags the application as a web application and activates key behaviors, such as setting up a DispatcherServlet.
- `@ComponentScan` Tells Spring to look for other components, configurations, and services in the com/example package, letting it find the controllers.

## Comparing repositories

Notice the typical CRUD functionality:

- save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch
- findOne(…) – get a single entity based on passed primary key value
- findAll() – get an Iterable of all available entities in database
- count() – return the count of total entities in a table
- delete(…) – delete an entity based on the passed object
- exists(…) – verify if an entity exists based on the passed primary key value

JpaRepository interface

- findAll() – get a List of all available entities in database
- findAll(…) – get a List of all available entities and sort them using the provided condition
- save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch
- flush() – flush all pending task to the database
- saveAndFlush(…) – save the entity and flush changes immediately
- deleteInBatch(…) – delete an Iterable of entities. Here, we can pass multiple objects to delete them in a batch
