# graphs-presentation

# Graph

A graph is a collection of nodes, which store data, and edges, which represent relationships or connections between nodes.
Uses

Social network, Google Maps, Instagram, PayPal




Relationships are general, not hierarchical, like trees.

**Undirected** - mutual connection between nodes
**Directed** - pointing from one node to another

### Undirected

Edges do not point from one node to another


Example: friending someone on Facebook.

### Directed Graph

Edges have a direction, they point from one node to another.



Example: Liking someone’s post on Facebook.

## Representing Graphs

There are also two ways to represent a graph in code: 
- an adjacency list and 
- an adjacency matrix. 

At a high level:
An **adjacency list** uses a collection of arrays for each node.
An **adjacency matrix** is represented by a two-dimensional array.

### The Adjacency List Representation
- More common
- a graph is represented with a collection of arrays for each node

```js
let graph = {
  'A': ['B', 'E'],
  'B': ['A', 'C', 'D', 'E'],
  'C': ['B', 'D'],
  'D': ['B', 'C', 'E'],
  'E': ['A', 'B', 'D'],
}
```
Does this adjacency list represent an undirected or directed graph?

The Adjacency Matrix Representation
In an adjacency matrix, a graph is represented by a two-dimensional array (an array of arrays). Each subarray is a node, and the values in the node represent edges to other nodes. 
```js
let graph = [
  [0, 1, 0, 0, 1, 1],
  [1, 0, 0, 0, 1, 0],
  [0, 1, 1, 1, 0, 0],
  [0, 0, 1, 0, 1, 0],
  [1, 1, 1, 0, 0, 0],
]```
1 represents an edge and a 0 represents a lack of an edge:



### Common graph methods

**.addNode(N)**: Add a node, N, to the graph.
**.addEdge(src, dest)** : Add an edge between Nodes src and dest.

```js
// Instantiate a new instance of a graph:
const g = new Graph()

// Add three nodes, 'A', 'B', and 'C':
g.addNode('A')
g.addNode('B')
g.addNode('C')

// Create edges between our nodes:
g.addEdge('A', 'B');
g.addEdge('A', 'C');
g.addEdge('B', 'C');
g.addEdge('C', 'A');

// Each node now has at least one edge:
// A -> B, C
// B -> C
// C -> A
```

### Traversing a Graph

Navigating from one node to the next through the edges between them in order to search, count, or add nodes.

#### There are two common ways of traversing graphs: 

**Breadth First Search (BFS for short)**
**Depth First Search (DFS)**

Great animation for those here: [Graphs](https://stackabuse.com/graph-data-structure-interview-questions)




