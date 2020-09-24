## Review High-level HTTP
- HTTP Request Lifecycle
  - Step 1: Local Processing

  `<protocol>://<host><:optional port>/<path/to/resource><?query>`. An example is `|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|`

  - Step 2: Resolve an IP
   
   If an address for a given domain cannot be resolved the server responds with a failure and your browser returns an error.
   - Step 3: Establish a TCP Commection

   Client must open a TCP connection

   1. client initiates the active open by sending STN control packet to server. sets sequence number.
   2. server responds with SYN-ACK message which containg an acknowledgement number
   3. ensures the that the data is being delivered reliably

   now have an established connection where both client and server have acknowldgement of the connection.

   - Step 4: Send an HTTP Request
   - Step 5: Tearing Down and CLeaning Up

## Java HTTP Request example
  - HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that are needed are contained in the java.net package
  - HttpUrlConnection instance is created by using the openConnection() method of the URL class. This only creates a connection object

  Let's create a connection to a given url using GET method:

URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");

- Adding Request Parameters, have to set doOutput property to true then write a String of the form param1=value¶m2=value to the OutputStream of the HttpUrlConnection
- Adding headers to a request using setRequestProperty() method.
- Handling Cookies, read the cookies from a response, add the sookies to the cookie store, add the cookies to the request.
- Handling Redirects, enable or disable automatically following redirects for a specific connection
- Reading the Response, parsing the InputStream of the HttpUrlConnection instance. To execute the request use getResponseCode(), connect(), getInputStream() or getOutputStream() methods.
- Reading the Response on Failed Requests: consume the steam provided by HttpConnection.getErrorStream()
- Building the Full Response: using some of the methoss the HttpUrlConnection instance offers. Fisrt add the response status information. Next get the headers using getHeaderFields(), Finally read the response content