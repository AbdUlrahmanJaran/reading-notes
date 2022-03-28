## Linked Lists
### Linear Complexity Growth:
The Complexity increases at the same rate as Our Input Size (n). If an algorithm has Linear Complexity, the size of our inputs ‘n’ will directly determine the amount of Memory Space used and Running Time length. and this will lead us to O(n) complexity growth.

### What is a Linked List?
- A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each ``Node`` references the next ``Node`` in the link.

- Nodes are the individual items/links that live in a linked list. Each ``Node`` contains the data for each link.
Each ``Node`` contains a property called Next. This property contains the reference to the next ``Node``.
- The Head is a reference of type ``Node`` to the first ``Node`` in a linked list.
- The Current is a reference of type ``Node`` to the ``Node`` that is currently being looked at.
= The best way to approach a traversal is ``while()`` loop. This allows us to continually check that the Next ``Node`` in the list is not null.
<br>
- When traversing through a linked list, the Current variable will tell us where exactly in the linked list we are and will allow us to move forward until we hit the end.

here is a pseudo code for what should we do when we want to add a ``Node``.

```newNode <-- NEW Node```

```new``Node``.Value <-- newValue```

```new``Node``.Next <-- Head```

```Head <-- newNode```


- To print linked list values we use ``while()`` loop to move through the linked list and print each
value until we hit the end.

- A circular linked list doesn’t end with a ``Node`` pointing to a null value. Instead, it has a ``Node`` that acts as the tail of the list, and the ``Node`` after the tail ``Node`` is the beginning of the list.

### Array vs Linked list
- Linked list is better for inserting and deleting.
- Array is better for Searching.
- Linked list size is Dynamic, Array size is Static.