# Classes & Memory Management
## What does Reference type mean?
> A type that is defined as a class is a reference type. At run time, when you declare a variable of a reference type, the variable contains the value null until you explicitly create an instance of the class by using the new operator, or assign it an object of a compatible type that may have been created elsewhere.[Classes Microsoft](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/types/classes)

## Declaring Classes
- Classes are declared by using the class keyword followed by a unique identifier
- The name of the class follows the class keyword. The name of the class must be a valid C# identifier name.

## Creating Objects:
- Classes and Objects are different things. A class defines a type of object, but it is not an object itself. An object is a concrete entity based on a class, and is sometimes referred to as an instance of a class.

- Objects can be created by using the new keyword followed by the name of the class that the object will be based on.

## What is Constructor?
- A constructor is a method whose name is the same as the name of its type. Its method signature includes only an optional access modifier, the method name and its parameter list; it does not include a return type.

### Static constructors
- a static constructor, which initializes static members of the type. Static constructors are parameterless.

## Properties overview
> A get property accessor is used to return the property value, and a set property accessor is used to assign a new value.<br>
> The value keyword is used to define the value being assigned by the set accessor.[Properties Microsoft](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)

### Auto-implemented properties
In some cases, property get and set accessors just assign a value to or retrieve a value from a backing field without including any additional logic. By using auto-implemented properties.

- You define an auto-implemented property by using the get and set keywords without providing any implementation.

## Stack vs Heap
With the Heap, there are no constraints as to what can be accessed like in the stack. The Heap is like the heap of clean laundry on our bed that we have not taken the time to put away yet - we can grab what we need quickly.  The Stack is like the stack of shoe boxes in the closet where we have to take off the top one to get to the one underneath it.

### Pointers
 A Pointer is a space in memory that points to another space in memory. Pointer takes up space just like any other thing that we're putting in the Stack and Heap and its value is either a memory address or null. 

## What is garbage collector?
The garbage collector (GC) serves as an automatic memory manager. The garbage collector manages the allocation and release of memory for an application. Automatic memory management can eliminate common problems, such as forgetting to free an object and causing a memory leak or attempting to access memory for an object that's already been freed.

#### The garbage collector provides the following benefits:
1. Frees developers from having to manually release memory.

2. Allocates objects on the managed heap efficiently.

3. Reclaims objects that are no longer being used, clears their memory, and keeps the memory available for future allocations.

4. Provides memory safety.

#### Garbage collection occurs when one of the following conditions is true:
1. The system has low physical memory.

2. The memory that's used by allocated objects on the managed heap surpasses an acceptable threshold.

3. The GC.Collect method is called. The garbage collector runs continuously. but This method is primarily used for unique situations and testing.

#### A garbage collection has the following phases:
- A marking phase that finds and creates a list of all live objects.

- A relocating phase that updates the references to the objects that will be compacted.

- A compacting phase that reclaims the space occupied by the dead objects and compacts the surviving objects.