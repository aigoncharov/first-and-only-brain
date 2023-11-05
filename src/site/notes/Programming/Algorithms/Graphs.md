---
{"dg-publish":true,"permalink":"/programming/algorithms/graphs/","created":"","updated":""}
---

#algorithms 
## DFS
### Undirected
Counting connected components (CC)
```
DFS(G):

CC = 0
for all v in V, visited(v) = false
for all v in V:
	if not visited(v):
		CC++
		Explore(v)


Explore(v):
visited(v) = true
for all (v, w) in E:
	if not visited(w):
		Explore(w)
```
### Directed
```
DFS(G):

clock = 1
for all v in V, visited(v) = false
for all v in V:
	if not visited(v):
		Explore(v)


Explore(v):
pre(v) = clock
clock++
visited(v) = true
for all (v, w) in E:
	if not visited(w):
		Explore(w)
post(v) = clock
```
### Topological sorting
1. Create an array of size 2n
2. Run DFS on DAG (directed acyclic graph) G 
3. Put the postorder numbers of the edges in the array
4. Run through the array in the reverse order
5. Runtime: O(n + m) just like in DFS

### Strongly connected components
1. Every graph is a DAG of its SCCs (strongly connected components).
2. In a generally directed graph (may have cycles), vertex with the highest postorder number lies in a source SCC.

Algorithm (generally directed graph G):
1. Construct $G^R$ (reverse)
2. Run DFS on $G^R$
3. Order V (vertices) by decreasing postorder number (a source SCC of the reverse graph is a sink SCC of the original one)
4. Run undirected connected components algo on G (or run DFS for a vertex with the highest postorder number, crossing out the vertices that you visit, until nothing is left)
5. It returns the components in the reverse topological order

## Max flow
### Ford-Fulkerson
Assumes int capacities.

#### Runtime
O(mC), where C - size of max flow

### Edmonds-Karp
#### Runtime
O(m^2 n)