# LINQ
Language-Integrated Query (LINQ) is the name for a set of technologies based on the integration of query capabilities directly into the C# language.

The most visible "language-integrated" part of LINQ is the query expression. Query expressions are written in a declarative query syntax. By using query syntax, you can perform filtering, ordering, and grouping operations on data sources with a minimum of code. You use the same basic query expression patterns to query and transform data in **SQL databases**, XML documents and **.NET collections**.

> At compile time, query expressions are converted to Standard Query Operator method calls according to the rules set forth in the C# specification. Any query that can be expressed by using query syntax can also be expressed by using method syntax. 

> Some query operations, such as Count or Max, have no equivalent query expression clause and must therefore be expressed as a method call. 

## LINQ Queries
A query is an expression that retrieves data from a data source. Queries are usually expressed in a specialized query language.

### All LINQ query operations consist of three distinct actions:
1. Obtain the data source.<br>
When the data source is an array, it implicitly supports the generic IEnumerable<T> interface. This fact means it can be queried with LINQ. Types that support IEnumerable<T> **queryable types**.

2. Create the query.<br>
The query specifies what information to retrieve from the data source or sources. Optionally, a query also specifies how that information should be sorted, grouped, and shaped before it is returned. A query is stored in a query variable and initialized with a query expression.<br>
The query expression contains clauses, most used are: from, where and select.
The from clause specifies the data source, the where clause applies the filter, and the select clause specifies the type of the returned elements.

3. Execute the query.<br>
The query variable itself only stores the query commands. The actual execution of the query is deferred until you iterate over the query variable in a foreach statement. This concept is referred to as deferred execution.<br>

### Basic LINQ Query Operations
1. Filtering<br>
The ``filter`` causes the query to return only those elements for which the expression is true. The result is produced by using the where clause. 

2. Ordering<br>
The ``orderby`` clause will cause the elements in the returned sequence to be sorted according to the default comparer for the type being sorted.

3. Grouping<br>
The ``group`` clause enables you to group your results based on a key that you specify.

4. Joining<br>
``Join`` operations create associations between sequences that are not explicitly modeled in the data sources.

5. Selecting<br>
The ``select`` clause produces the results of the query and specifies the "shape" or type of each returned element.

## Things I want to know more about
1. Query Forcing Immediate Execution.
2. Join clause.

### Ref: [LINQ](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/) , [Queries](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries) and [Query Operations](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/basic-linq-query-operations).