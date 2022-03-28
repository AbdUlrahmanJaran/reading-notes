# Interfaces
An interface contains definitions for a group of related functionalities that a non-abstract class must implement. An interface may define static methods, which must have an implementation.

By using interfaces, you can, for example, include behavior from multiple sources in a class.You define an interface by using the ``interface`` keyword.

- The name of an interface must be a valid C# identifier name. By convention, interface names begin with a capital I.

## But, What problem does the interface solve?
> The basic problem an interface is trying to solve is to separate how we use something from how it is implemented.So we can write code that can work with a variety of different implementations of some set of responsibilities without having to specifically handle each implementation.[ref](https://simpleprogrammer.com/back-to-basics-what-is-an-interface/)

## An interface has the following properties:

1. An interface is like an abstract base class with only abstract members. A class that implements the interface must implement all its members.
2. An interface can't be instantiated directly. Its members are implemented by any class that implements the interface.
3. A class can implement multiple interfaces. A class can inherit a base class and also implement one or more interfaces.[ref](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/types/interfaces)

