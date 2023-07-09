# Depth-First Search (DFS) Deep Dive

Depth-First Search (DFS) is an algorithm for traversing or searching tree or graph data structures. It uses a stack (or recursion which internally uses a stack) to visit and store all the vertices of a graph that we can reach from a source vertex. Here are the basic steps:

## 1. Start at a Node

Start at a chosen node (often the root, if defined; otherwise, any node will do).

## 2. Visit an Adjacent Unvisited Node

Select an adjacent node to the current node and visit it. If there are multiple adjacent nodes, you can choose any node that has not yet been visited.

## 3. Push Current Node to Stack

If we have moved to a new node, we should push the previous node to a stack to keep track of the path.

## 4. Backtrack if No Adjacent Node is Found

If there are no adjacent unvisited nodes to the current node, then backtrack to the previous node using the stack.

## 5. Repeat

Repeat steps 2-4 until all nodes have been visited.

Here's a brief example of how DFS works on a graph:

**Input graph**:
