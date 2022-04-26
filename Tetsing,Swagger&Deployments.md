# Tetsing, Swagger & Deployments
## Swagger
Swagger (OpenAPI) is a language-agnostic specification for describing REST APIs. It allows both computers and humans to understand the capabilities of a REST API without direct access to the source code.<br>
Its main goals are to:
1. Minimize the amount of work needed to connect decoupled services.
2. Reduce the amount of time needed to accurately document a service.

>The two main OpenAPI implementations for .NET are **Swashbuckle** and **NSwag**.

### OpenAPI
 The OpenAPI specification is a document that describes the capabilities of your API. The document is based on the XML and attribute annotations within the controllers and models. 

### Swagger UI
 Swagger UI offers a web-based UI that provides information about the service, using the generated OpenAPI specification. Both **Swashbuckle** and **NSwag** include an embedded version of Swagger UI, so that it can be hosted in your ASP.NET Core app using a middleware registration call.

## Testing
Three different types of unit tests for the controllers in ASP.NET MVC applications:
1. Test the view returned by a controller action.
2. Test the View Data returned by a controller action.
3. Test whether or not one controller action redirects you to a second controller action.

### Unit tests of controller logic
 Unit tests involve testing a part of an app in isolation from its infrastructure and dependencies. When unit testing controller logic, only the contents of a single action are tested, not the behavior of its dependencies or of the framework itself.

 A controller unit test avoids scenarios such as filters, routing, and model binding. Tests that cover the interactions among components that collectively respond to a request are handled by *integration tests*.

### Test ActionResult<T>
ActionResult<T> (ActionResult<TValue>) enables you to return a type deriving from ActionResult or return a specific type.

#### Ref: [Swagger](https://docs.microsoft.com/en-us/aspnet/core/tutorials/web-api-help-pages-using-swagger?tabs=visual-studio&view=aspnetcore-2.1) and [Testing](https://docs.microsoft.com/en-us/aspnet/core/mvc/controllers/testing?view=aspnetcore-2.1).

## Things I want to know more about
1. integration tests.
2. Test ActionResult.