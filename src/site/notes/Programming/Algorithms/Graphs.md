---
{"dg-publish":true,"permalink":"/programming/algorithms/graphs/","created":"","updated":""}
---

#algorithms 

## Shortest path

### Dijkstra (single source)
O((n+m) log n)

### Bellman-Ford (single source)
```
for all z in V, D(0, z) = inf
D(0, s) = 0
for i = 1 -> n-1:
	for all z in V:
		D(i, z) = D(i-1, z)
		for all edges from y to z:
			if D(i, z) > D(i-1, y) + w(y,z):
				D(i,z) = D(i-1, y) + w(y,z)
return (D(n-1, ...))
```
**Runtime**: O(nm)

To find **negative weight cycles** run it to n instead of n-1 and see if for some z in D(n,z), D(n,z) != D(n-1, z).
Key idea - if there is no negative weight cycle, the algo stops updating rows at n-1.

### Floyd-Warshall (all vertices)
Somehow enumerate vertices from 1 to n.
```
for s = 1 -> n:
	for t = 1 -> n:
		if edge st exists:
			D(0, s, t) = w(s,t)
		else:
			D(0, s, t) = inf
for i = 1 -> n:
	for s = 1 -> n:
		for t = 1 -> n:
			D(i,s,t) = min{D(i-1, s, t), D(i-1, s, i) + D(i-1, i, t )}
return (D(n, ..., ...))
```
To find **negative weight cycles** we check if for every y in V there is y such that D(n, y, y) < 0.
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