# Claims and JWT Tokens
Authentication is the process of determining who you are, while Authorisation revolves around what you are allowed to do.

a user may belong to one or more roles, and different sections of your app may require a user to have a particular role in order to access it. In ASP.NET Core this kind of role-based authorisation can still be used, but that is primarily for backward compatibility reasons. The route they really want you to take is claims-based authentication.

## Claims-based authorization in ASP.NET Core
When an identity is created it may be assigned one or more claims issued by a trusted party. A claim is a name value pair that represents what the subject is, not what the subject can do.

Claims based authorization, at its simplest, checks the value of a claim and allows access to a resource based upon that value.

An identity can contain multiple claims with multiple values and can contain multiple claims of the same type.

### Claims checks
Claim based authorization checks:
- Are declarative.
- Are applied to Razor Pages, controllers, or actions within a controller.
- Can not be applied at the Razor Page handler level, they must be applied to the Page.

> Build and register the policy and call ``UseAuthorization``. Registering the policy takes place as part of the Authorization service configuration, typically in the ``Program.cs`` file.

If the claim value isn't a single value or a transformation is required, use ``RequireAssertion`` which is a generic claim check.

If you apply multiple policies to a controller or action, then all policies must pass before access is granted.

## JWT Tokens
JSON Web Token (JWT) is a means of representing claims to be transferred between two parties. The claims in a JWT are encoded as a JSON object that is digitally signed using JSON Web Signature (JWS) and/or encrypted using JSON Web Encryption (JWE).

In simple terms, it is just another way of encoding JSON object and use that encoded object as access tokens for authentication from the server.

There are generally three parts in JWTs
1. 1st part is ``HEADER``
2. 2nd part is ``PAYLOAD``
3. 3rd part is ``SIGNATURE``

### Following are some standard claims:
1. Issuer (iss) - identifies principal that issued the JWT;
2. Subject (sub) - identifies the subject of the JWT;
3. Issued at (iat) - The "iat" (issued at) claim identifies the time at which the JWT was issued.
4. JWT ID (jti) - case sensitive unique identifier of the token even among different issuers.

### Producer and Consumer concept of API’s
- Producer is the one who gives a service. It will be the provider(Server) of the API(s) which are JWT protected.

- Consumer is the one who uses it. It will be the customer(Server/Mobile App/ Web App/ Client) who will be providing the valid JWT token to consume the API(s) being provided by the Producer.

In server to server authentication both the parties need to share the custom contract for specific API based or for all the API(s).This contract can consist of any custom clause that you want to introduce.

## Things I want to know more about
1. Generic claim checks.
2. Multiple authentication.

### Ref: [Claims](https://andrewlock.net/introduction-to-authentication-with-asp-net-core/) and [JWT Tokens](https://codeburst.io/jwt-to-authenticate-servers-apis-c6e179aa8c4e).