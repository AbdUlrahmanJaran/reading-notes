# Graphs
A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

Here is some common terminology used when working with Graphs:
- `Vertex` - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
- `Edge` - An edge is a connection between two nodes.
- `Neighbor` - The neighbors of a node are its adjacent nodes, i.e., are connected via an `edge`.
- `Degree` - The degree of a `vertex` is the number of edges connected to that `vertex`.

### Undirected Graphs
An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

### Directed Graphs (Digraph)
A Directed Graph also called a Digraph is a graph where every edge is directed.<br>
 Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

### Complete vs Connected vs Disconnected
Depending on how connected the graphs are to other node/vertices, there is three different types:
#### 1. Complete Graphs
A complete graph is when all nodes are connected to all other nodes.<br>
 each vertex is connected to every other node on the graph.

#### 2. Connected Graphs
A connected graph is graph that has all of vertices/nodes have at least one edge.<br>
 each node is connected to at least one other node or vertices. A ``Tree`` is a form of a connected graph.

#### 3. Disconnected Graphs
A disconnected graph is a graph where some vertices may not have edges.<br>
 some nodes may not be connected to other nodes or vertices of the graph. It is complelty possible to have standalone nodes or edges (also known as ``islands``) in a graph data structure.

## Graph Representation
We represent graphs through:

### 1. Adjacency Matrix
An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix.<br>
Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.

### 2. Adjacency List
An adjacency list is the most common way to represent graphs.<br>
An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.<br>
Adjacency lists make it easy to view if one vertices connects to another.

### Weighted Graphs
A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.<br>
When representing a weighted graph in a matrix, you set the element in the 2D array to represent the actual weight between the two paths. If there is not a connection between the two vertices, you can put a 0, although it is known for some people to put the infinity sign instead.

## Traversals
### 1. Breadth First
In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. Traversing a graph that has cycles will result in an infinite loop….this is bad. To prevent such behavior, we need to have some way to keep track of whether a vertex has been “visited” before. Upon each visit, we’ll add the previously-unvisited vertex to a visited set, so we know not to visit it again as traversal continues.

Breadth first traversal algorithm:
- ``Enqueue`` the declared start node into the `Queue`.
- Create a loop that will run while the node still has nodes present.
- ``Dequeue`` the first node from the `queue`
- if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the `queue`.

### 2. Depth First
In a depth first traversal, our approach is a bit different than the approach used for breadth first. While the breadth first traversal uses a Queue to visit all children at a given level, the depth first traversal uses a Stack to visit all children of a given subtree. (This differs from our approach to tree traversal, where we visit nodes via recursive calls. Recursive calls use a call stack internally.)

Depth first traversal algorithm:
- ``Push`` the root node into the `Stack` and mark as visited.
- Start a while loop that runs as long as the `stack` is not empty.
- ``Pop`` the top node off of the `stack` and check its neighbors.
- If a neighbor hasn’t been visited, push it onto the `stack` and mark as visited.
- Repeat until the `stack` is empty.

## Real World Uses of Graphs
Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:
1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic
5. Netflix uses graphs for suggestions of products

### Ref: [Graph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html).
