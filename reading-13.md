## Related data in Spring
- Relationship annotations

- One-to-One Relationship, must be careful to have different names for each association resource
- to expose entities as resources create 2 repository interfaces for each by extending the interface
- Before creating an association sending a GET request to endpoint will return an empty object
- establish relationship with PUT or remove with DELETE

- One-to-Many Relationship, create an instance
-POST request then associate sending a PUT request, verify with GET method

- Many-to-Many relationship, must first create the resources. POST to add to database. 
- GET request to view association URL


## Spring Integration Testing

- Get the right dependecies for testing
- perform() method will call a get request method which returns the ResultActions. Using this result we can have assertion expectations on response like content, HTTP status, header, etc
- andDo(print()) will print the request and response. This is helpful to get a detailed view in case of error
- andExpect() will expect the provided argument. In our case we are expecting “index” to be returned via MockMvcResultMatchers.view()
-andExpect(MockMvcResultMatchers.status().isOk()) will verify that response HTTP status is Ok i.e. 200. This ensures that the request was successfully executed
- andExpect(MockMvcResultMatchers.jsonPath(“$.message”).value(“Hello World!!!”)) will verify that response content matches with the argument “Hello World!!!“. Here we used jsonPath which extracts response content and provide the requested value
- andReturn() will return the MvcResult object which is used when we have to verify something which is not achievable by the library. You can see we have added assertEquals to match the content type of response that is extracted from the MvcResult object