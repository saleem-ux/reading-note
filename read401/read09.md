#  Authorization/Authentication

### 1. What header(s) are used in authentication and authorization
  1. Basic Auth 

It is a simple authentication scheme built into the HTTP protocol. The client sends HTTP requests with the Authorization header that contains the word Basic, followed by a space and a base64-encoded(non-encrypted) string username: password. For example, to authorize as username / Pa$$w0rd the client would send.

  2. Bearer Token:

Commonly known as token authentication. It is an HTTP authentication scheme that involves security tokens called bearer tokens. As the name depicts “Bearer Authentication” gives access to the bearer of this token.

The bearer token is a cryptic string, usually generated by the server in response to a login request.

### 2. What is safe to put into a JWT
WTs are by-value tokens. This means that they contain data. Even if you can’t read that data with your own eyes, it’s still there, and is quite easily available. Whether it’s a problem or not depends on the intended audience of the token. An ID Token is intended for the client’s developers. You expect it to be decoded and its data used by the client. An Access Token, on the other hand, is intended for the API developers. The API should decode and validate the token. But if you issue JWTs to your clients to be used as Access Tokens you have to remember that client developers will be able to access the data inside of that token.

### 3. How are JWTs validated 
Check signature. The last segment of a JWT is the signature, which is used to verify that the token was signed by the sender and not altered in any way. The Signature is created using the Header and Payload segments, a signing algorithm, and a secret or public key (depending on the chosen signing algorithm).

----------------------------


### Terms:

**RBAC:** Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.



**User Roles:** User Roles are permission sets that control access to areas and features within the Professional Archive Platform. Each User account requires a Role assignment.

**JWT Token:** JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.
