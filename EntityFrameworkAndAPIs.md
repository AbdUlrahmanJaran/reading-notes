# Entity Framework and APIs
## Entity Framework
Entity Framework (EF) Core is a lightweight, extensible, open source and cross-platform version of the popular Entity Framework data access technology.

EF Core can serve as an object-relational mapper (O/RM), which:
1. Enables .NET developers to work with a database using .NET objects.
2. Eliminates the need for most of the data-access code that typically needs to be written.

### The model
With EF Core, data access is performed using a model. A model is made up of entity classes and a context object that represents a session with the database. the context object allows querying and saving data.
- Querying: instances of your entity classes are retrieved from the database using Language Integrated Query (LINQ).
- Saving data: data is created, deleted, and modified in the database using instances of your entity classes.
- Data seeding: the process of populating a database with an initial set of data.

Seeding data can be associated with an entity type as part of the model configuration. Then EF Core migrations can automatically compute what insert, update or delete operations need to be applied when upgrading the database to a new version of the model.[Ref](https://docs.microsoft.com/en-us/ef/core/)

## Razor Pages
Razor Pages is a newer, simplified web application programming model. It removes much of the ceremony of ASP.NET MVC by adopting a file-based routing approach. Each Razor Pages file found under the Pages directory equates to an endpoint.

- Razor Pages is enabled in Program.cs
- ``AddRazorPages`` adds services for Razor Pages to the app.
- ``MapRazorPages`` adds endpoints for Razor Pages to the IEndpointRouteBuilder.

## User Secrets
User secrets is a secure way of storing private user information such as API keys, client secrets, and connection strings. Essentially anything that you don’t want others to know about when using your code base.

>The user secrets is not uploaded to any source control. This ensures your keys do in fact stay “secret” to your local machine.

To know how to add a user secret step by step go to [codefellows-user-secrets](https://codefellows.github.io/code-401-dotnet-guide/resources/user-secrets.html).

## APIs
To create a simple Web API using ASP.NET MVC, C#, and Visual Studio. you have to:
1. Create ASP.NET Web Application in Visual Studio.
2. Select Web API Template.
3. Review Project Files.
4. Add a Controller. 
5. Add Controller Method.
6. build your project.
[Ref](https://www.c-sharpcorner.com/article/create-simple-web-api-in-asp-net-mvc/)

## Things I want to know more about
1. Asynchronous code.
2. Custom initialization logic instead of Model seeding data.
