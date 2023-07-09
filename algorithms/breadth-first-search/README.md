# Breadth-First Search (BFS) Deep Dive

Breadth-First Search (BFS) is an algorithm for traversing or searching tree or graph data structures. It starts at the root (or an arbitrary node for a graph) and explores the neighbor nodes at the present depth before moving on to nodes at the next depth level. BFS uses a queue data structure to keep track of nodes to visit. Here are the basic steps:

## 1. Start at a Node

Start at a chosen node (often the root, if defined; otherwise, any node will do). Visit this node and mark it as visited.

## 2. Visit all Neighbors

Visit all the neighboring nodes at the current depth level.

## 3. Add Neighbors to Queue

Add any neighboring nodes that you plan to visit to a queue.

## 4. Move to Next Node

Once all the neighbors of the current node are visited, dequeue the next node from the queue and repeat the process.

## 5. Repeat

Repeat steps 2-4 until the queue is empty, i.e., all nodes reachable from the starting node have been visited.

Here's a brief example of how BFS works on a graph:

**Input graph**:

```python
A - B
| \ |
D - C
```
