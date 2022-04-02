# Collections
For many applications, you want to create and manage groups of related objects. There are two ways to group objects: by creating arrays of objects, and by creating collections of objects.

A collection is a class, so you must declare an instance of the class before you can add elements to that collection.

Collections provide a more flexible way to work with groups of objects. Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change. For some collections, you can assign a key to any object that you put into the collection so that you can quickly retrieve the object by using the key.

## Using a Simple Collection
The generic List<T> class enables you to work with a strongly typed list of objects.

```c#
// Create a list of strings.
var salmons = new List<string>();
salmons.Add("chinook");
salmons.Add("coho");
salmons.Add("pink");
salmons.Add("sockeye");

// Iterate through the list.
foreach (var salmon in salmons)
{
    Console.Write(salmon + " ");
}
// Output: chinook coho pink sockeye
```
You can use a for statement instead of a foreach statement to iterate through a collection. You accomplish this by accessing the collection elements by the index position. The index of the elements starts at 0 and ends at the element count minus 1.
```c#
// Create a list of strings by using a
// collection initializer.
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };

for (var index = 0; index < salmons.Count; index++)
{
    Console.Write(salmons[index] + " ");
}
// Output: chinook coho pink sockeye
```
## Kinds of Collections
Many common collections are provided by .NET. Each type of collection is designed for a specific purpose.

Some of them are:

1. System.Collections.Generic classes
You can create a generic collection by using one of the classes in the System.Collections.Generic namespace. A generic collection is useful when every item in the collection has the same data type. A generic collection enforces strong typing by allowing only the desired data type to be added.

2. System.Collections.Concurrent classes
The classes in the System.Collections.Concurrent namespace should be used instead of the corresponding types in the System.Collections.Generic and System.Collections namespaces whenever multiple threads are accessing the collection concurrently.
<br>
Some classes included in the System.Collections.Concurrent namespace are:        
BlockingCollection<T>, ConcurrentDictionary<TKey,TValue>, ConcurrentQueue<T>, and ConcurrentStack<T>.

3. System.Collections classes
The classes in the System.Collections namespace do not store elements as specifically typed objects, but as objects of type Object.
<br>

The Dictionary<TKey,TValue> generic collection enables you to access to elements in a collection by using the key of each element. Each addition to the dictionary consists of a value and its associated key. Retrieving a value by using its key is fast because the Dictionary class is implemented as a hash table.

## Using LINQ to Access a Collection
LINQ (Language-Integrated Query) can be used to access collections. LINQ queries provide filtering, ordering, and grouping capabilities.

here is an Example:
```c#
private static void ShowLINQ()
{
    List<Element> elements = BuildList();

    // LINQ Query.
    var subset = from theElement in elements
                 where theElement.AtomicNumber < 22
                 orderby theElement.Name
                 select theElement;

    foreach (Element theElement in subset)
    {
        Console.WriteLine(theElement.Name + " " + theElement.AtomicNumber);
    }

    // Output:
    //  Calcium 20
    //  Potassium 19
    //  Scandium 21
}

private static List<Element> BuildList()
{
    return new List<Element>
    {
        { new Element() { Symbol="K", Name="Potassium", AtomicNumber=19}},
        { new Element() { Symbol="Ca", Name="Calcium", AtomicNumber=20}},
        { new Element() { Symbol="Sc", Name="Scandium", AtomicNumber=21}},
        { new Element() { Symbol="Ti", Name="Titanium", AtomicNumber=22}}
    };
}

public class Element
{
    public string Symbol { get; set; }
    public string Name { get; set; }
    public int AtomicNumber { get; set; }
}
```
## Defining a Custom Collection
You can define a collection by implementing the IEnumerable<T> or IEnumerable interface.

Although you can define a custom collection, it is usually better to instead use the collections that are included in .NET.

## Iterators
An iterator is used to perform a custom iteration over a collection. An iterator can be a method or a get accessor. An iterator uses a yield return statement to return each element of the collection one at a time.

You call an iterator by using a foreach statement. Each iteration of the foreach loop calls the iterator.

# Enums
- An enumeration type (or enum type) is a value type defined by a set of named constants of the underlying integral numeric type. To define an enumeration type, use the enum keyword and specify the names of enum members.

- The System.Enum type is the abstract base class of all enumeration types. It provides a number of methods to get information about an enumeration type and its values.

- For any enumeration type, there exist explicit conversions between the enumeration type and its underlying integral type. If you cast an enum value to its underlying type, the result is the associated integral value of an enum member.
- Use the Enum.IsDefined method to determine whether an enumeration type contains an enum member with the certain associated value.

## Things I want to know more about
1. Those Classes BlockingCollection<T>, ConcurrentDictionary<TKey,TValue>, ConcurrentQueue<T>, and ConcurrentStack<T>.
2. ``TryGetValue`` method. 
3. Sorting a Collection.
4. Enumeration types as bit flags.


### Ref: [Collections](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/collections) , [Enum](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/enum).