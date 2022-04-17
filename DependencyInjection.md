# Dependency Injection & Repository patterns
## Dependency Injection
ASP.NET Core supports the dependency injection (DI) software design pattern, which is a technique for achieving Inversion of Control (IoC) between classes and their dependencies.

Dependency injection addresses these problems through:
1. The use of an interface or base class to abstract the dependency implementation.
2. Registration of the dependency in a service container. ASP.NET Core provides a built-in service container, IServiceProvider. Services are typically registered in the app's Program.cs file.
3. Injection of the service into the constructor of the class where it's used. The framework takes on the responsibility of creating an instance of the dependency and disposing of it when it's no longer needed.

When designing services for dependency injection:
1. Avoid stateful, static classes and members. Avoid creating global state by designing apps to use singleton services instead.
2. Avoid direct instantiation of dependent classes within services. Direct instantiation couples the code to a particular implementation.
3. Make services small, well-factored, and easily tested.

## Repository patterns
Repositories are classes or components that encapsulate the logic required to access data sources. They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer.

> The repository pattern have two purposes; first it is an abstraction of the data layer and second it is a way of centralising the handling of the domain objects.[ref](https://medium.com/@pererikbergman/repository-design-pattern-e28c0f3e4a30)

The Repository pattern allows you to easily test your application with unit tests. Remember that unit tests only test your code, not infrastructure, so the repository abstractions make it easier to achieve that goal.

## SOLID Principals
The SOLID Principals of software development is the brain child or Robert “Uncle Bob” Martin. In the early 2000 he described five principals that software developers could use to guide them in creating software that was well designed, high quality and easier to maintain than what was being produced at the time. These five ideas are simple, promote good practices in software design and development, and go a long way to help us in our practice of TDD.

1. The Single Responsibility Principal (SRP) is the idea that every method or class in your application should have exactly one reason to change.

2. The Open/Close Principle (OCP) is very closely related to the previously discussed topics of Encapsulation and Inheritance. In fact it’s fair to say the OCP is concept that unifies these two tenants of OOP. OCP states that software, be it a method or a class, should be open for extension, but closed to modification.

3. The Liskov Substitution Principle (LSP) states that an object in your application should be able to be replaced with a type derived from it without breaking the application.

4. The Interface Segregation Principle states that clients should not be forced to rely on interfaces they do not use. Another way to say this is that you should make fine grained interfaces that are specific to the functions and needs of the client.

5. The Dependency Inversion Principle (DIP) is the idea that code should depend on abstractions; not concrete implementations.

After using SOLID principals we could say that, we changed our code so that it only does the one thing that is it supposed to, we removed the concrete implementation, and we injected our dependencies.  The code is still clean and concise, and pretty much the same number of lines that we had before the refactoring.

## Things I want to know more about
- Dependency injection Service lifetimes.
- The Liskov Substitution Principle (LSP).


### Ref: [Dependency Injection](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-6.0),[Repository patterns](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/repository-pattern?view=aspnetcore-2.1) and [SOLID Principals](https://www.telerik.com/blogs/30-days-of-tdd-day-five-make-your-code-solid)