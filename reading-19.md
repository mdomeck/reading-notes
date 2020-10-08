## Spring and Sockets
### Real time messaging with websockets
- Add needed dependencies
- Create a Resource Representation Class
  - This will accept messages that contain a name in STOMP message whose body is a JSON object.
  - Java Object with `name` property and a corresponding `getName()` method.
  - receiving the message and extracting the name will process it by creating a greeting and publishing that on a separate queue to which the client is subscribed.
  `content` property and cooresponding `getContent()` method.
- Create a Message-handling Controller
  - `@MessageMapping` annotation ensures that if a message is sent to the `/hello` destination the `greeting()` method is called.
  - `greeting()` method created a `Greeting` object and returns it.
  - `@Configuration` to indicate that it is a Spring configuration class.
  - `@EnableWebSocketMessageBroker` enables WebSocket message handling
- Create a Browser Client
  - `index.html` 
  - `connect()` function uses SockJS and stomp,js to open a connection
  - `sendName()` function retrieves the name entered by the user and suser the STOMP client to sent it to the `/app/hellp` destination 
- Make the Application Executable
- Build an executable JAR