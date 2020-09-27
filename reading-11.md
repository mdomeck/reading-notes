## Spring App Basics
- Start with Spring Initializr. Offers a fast way to pull in all the dependencies you need for an application and does a lot of the setup for you. 
- `@Controller` handles HTTP requests
- `GreetingController` handles GET requests
- `View` is responsible for rendering the HTML content.
- `@GetMapping` annotation ensures that HTTP GET requests to `/greeting` are mapped to the `greeting()` method.
- `@RequestParam` binds the value of the query string parameter `name` int othe `name` parameter of the `greeting()` method. THe query string parameter is not `required`
- implementation of the method body relies on a view technology to perform server-side rendering of the HTML.
- common feature is coding a change, restarting your application and refreshing the browser to view the change.
- Spring Initializr created an application class for you. 

## Spring MVC and Thymeleaf

- how to access data from templates
1. Spring model attributes
  Spring MVC calles the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is content variables.
1. Request parameters
  can be easily accesed in the Thymeleaf views. Request parameters are passed from the clent to server 
1. Session attributes
1. ServletContext attributes
  shared between requests and sessions.
1. Spring beans
  

