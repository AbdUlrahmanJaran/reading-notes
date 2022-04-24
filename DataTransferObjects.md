# Data Transfer Objects
A Data Transfer Object (commonly known as a DTO) is usually an instance of a POCO (plain old CLR object) class used as a container to encapsulate data and pass it from one layer of the application to another. You would typically find DTOs being used in the service layer to return data back to the presentation layer. The biggest advantage of using DTOs is decoupling clients from your internal data structures.

- You can take advantage of DTOs to abstract the domain objects of your application from the user interface or the presentation layer.
- Another reason you would want to use DTOs is data hiding. That is, by using DTOs you can return only the data requested.

## Immutability of DTOs
A DTO is meant to transport data from one layer of an application to another layer. The consumer of a DTO might be built in .NET/C#/Java or even JavaScript/TypeScript. A DTO is often serialized so that it can be independent of the technology used in the receiver.

There are several ways in which you can implement immutable DTOs in C#. You could use a ReadOnlyCollection or the thread-safe immutable collection types present in the System.Collections.Immutable namespace.

## Things I want to know more about
- DTO serialization challenges

### Ref: [DTO](https://www.infoworld.com/article/3562271/how-to-use-data-transfer-objects-in-aspnet-core-31.html)
