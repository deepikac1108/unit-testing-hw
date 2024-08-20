# unit-testing-hw
**Middleware Functions in Express.js and How They Work**

Middleware functions in Express.js are functions that execute during the lifecycle of a request and response. They have access to the request object, response object, and the next middleware function in the cycle. Middleware functions are typically executed before the request reaches its intended route. For example, if you have routes like '/home' and '/todo' and a middleware function that logs "hello" to the console, applying this middleware to all routes will result in "hello" being printed every time a user makes a request to any of those routes.

**What is JWT, and How Does It Work?**

JSON Web Token (JWT) is a method for securely transmitting information between a client and server, commonly used for authentication and authorization purposes. A JWT is composed of three parts: 
- The header, which specifies the type of token and the algorithm used.
- The payload, which contains the data or claims, such as a user's ID.
- The signature, which is created by encoding the header and payload with a secret key to ensure the token's integrity.

When a user logs in, the server generates a JWT and sends it to the client, where it can be stored, often in local storage. For subsequent requests, the client includes this token, and the server verifies its signature to authenticate the user.

**How Do You Securely Store JWT on the Client-Side?**

JWT can be securely stored on the client side using local storage or cookies.

**How Does Token Expiration Work in JWT?**

In JWT, token expiration is handled by including an expiration time in the token's payload. This expiration claim specifies the exact date and time when the token will no longer be valid. When the server receives a JWT, it checks this expiration value. If the current time exceeds the specified expiration time, the token is considered expired, and the server will reject it, typically requiring the user to log in again.
