# Object Oriented Principles
C# is an object-oriented programming language. The four basic principles of object-oriented programming are:

1. Abstraction: Modeling the relevant attributes and interactions of entities as classes to define an abstract representation of a system.
2. Encapsulation: Hiding the internal state and functionality of an object and only allowing access through a public set of functions.
3. Inheritance: Ability to create new abstractions based on existing abstractions.
4. Polymorphism: Ability to implement inherited properties or methods in different ways across multiple abstractions.

## Inheritance
- Inheritance enables you to create new classes that reuse, extend, and modify the behavior defined in other classes. 
- The class whose members are inherited is called the base class, and the class that inherits those members is called the derived class. 
- A derived class can have only one direct base class.

## Abstract
### Abstract base classes
You can declare a class as abstract if you want to prevent direct instantiation by using the new operator. An abstract class can be used only if a new class is derived from it. An abstract class can contain one or more method signatures that themselves are declared as abstract.

The abstract keyword enables you to create classes and class members that are incomplete and must be implemented in a derived class.

### Abstract method
Abstract classes may also define abstract methods. This is accomplished by adding the keyword abstract before the return type of the method.

Abstract methods have no implementation, so the method definition is followed by a semicolon instead of a normal method block. Derived classes of the abstract class must implement all abstract methods. 

### Interfaces
An interface is a reference type that defines a set of members. All classes and structs that implement that interface must implement that set of members. An interface may define a default implementation for any or all of these members. A class can implement multiple interfaces.

## Polymorphism
Polymorphism is a Greek word that means "many-shaped" and it has two distinct aspects:

- At run time, objects of a derived class may be treated as objects of a base class in places such as method parameters and collections or arrays. When this polymorphism occurs, the object's declared type is no longer identical to its run-time type.
- Base classes may define and implement virtual methods, and derived classes can override them, which means they provide their own definition and implementation. At run-time, when client code calls the method, the CLR looks up the run-time type of the object, and invokes that override of the virtual method. In your source code you can call a method on a base class, and cause a derived class's version of the method to be executed.[ref](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/object-oriented/polymorphism)

## Summary
- You used Abstraction when you defined classes for different types, Those classes described the behavior for each type.
- You used Encapsulation when you kept many details private in each class.
- You used Inheritance when you leveraged the implementation already created in the class to save code.
- You used Polymorphism when you created virtual methods that derived classes could override to create specific behavior for that account type.[ref](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/oop)
