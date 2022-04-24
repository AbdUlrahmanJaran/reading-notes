# Navigation Properties and Routing
## What is Routing?
Routing is responsible for matching incoming HTTP requests and dispatching those requests to the app's executable endpoints. Endpoints are the app's units of executable request-handling code. Endpoints are defined in the app and configured when the app starts. The endpoint matching process can extract values from the request's URL and provide those values for request processing. Using endpoint information from the app, routing is also able to generate URLs that map to endpoints.

- Routing is registered in the middleware pipeline in Startup.Configure.

Routing uses a pair of middleware, registered by ``UseRouting`` and ``UseEndpoints``:
1. ``UseRouting`` adds route matching to the middleware pipeline. This middleware looks at the set of endpoints defined in the app, and selects the best match based on the request.
2. ``UseEndpoints`` adds endpoint execution to the middleware pipeline. It runs the delegate associated with the selected endpoint.

### Endpoint
The ``MapGet`` method is used to define an endpoint. An endpoint is something that can be:
- Selected, by matching the URL and HTTP method.
- Executed, by running the delegate.

An endpoint defines both:
1. A delegate to process requests.
2. A collection of arbitrary metadata. The 'metadata' is used to implement cross-cutting concerns based on policies and configuration attached to each endpoint.

### URL matching
- Is the process by which routing matches an incoming request to an endpoint.
- Is based on data in the URL path and headers.
- Can be extended to consider any data in the request.

## Using the Default Route Table
When you create a new ASP.NET MVC application, the application is already configured to use ASP.NET Routing. ASP.NET Routing is setup in two places.

First, ASP.NET Routing is enabled in your application's Web configuration file (Web.config file).

Second, and more importantly, a route table is created in the application's Global.asax file. The Global.asax file is a special file that contains event handlers for ASP.NET application lifecycle events. The route table is created during the Application Start event.

Ref: [Routing](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/routing?view=aspnetcore-3.1)

## Things I want to know more about
- Endpoint metadata.
- What can be writen in a Route template.