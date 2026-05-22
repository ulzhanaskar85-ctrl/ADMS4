# Assignment 4 + Dijkstra Bonus Task  
#Group: SE-2514  
#Name: Ulzhan Askar  

#Project Overview
This project demonstrates graph traversal algorithms using Java.  
The graph is implemented using an adjacency list representation.

#Implemented Algorithms:
Breadth-First Search (BFS)
Depth-First Search (DFS)
Dijkstra’s Algorithm (Bonus Task)

The project also measures traversal performance using `System.nanoTime()`.

#Graph Concepts
#Vertex
A vertex represents a node in the graph.
Example:
0, 1, 2, 3

#Edge
An edge represents a connection between two vertices.
Example:
0 -> 1  
1 -> 2  

#Adjacency List Representation
The graph is stored using an adjacency list.
Example:
0 -> [1, 2]  
1 -> [0, 3]  
2 -> [0, 4]  
This representation is memory efficient and suitable for sparse graphs.

#Class Descriptions
#Vertex Class
The Vertex class represents a graph node.

#Responsibilities: Store vertex ID  ,Return vertex information  ,Provide string representation  
Screenshot:
<img width="1060" height="635" alt="image" src="https://github.com/user-attachments/assets/5e7ccca6-223a-4554-ac80-f95746d962b5" />

#Edge Class(Updated for weighted graph support)
The Edge class represents a connection between vertices (with weight for Dijkstra).

#Responsibilities: Store source vertex  ,Store destination vertex  ,Store edge weight  

Screenshot:
<img width="1280" height="905" alt="image" src="https://github.com/user-attachments/assets/2ecdd197-ee79-4124-abc1-75d9303454d4" />

#Graph Class(Updated with dijkstra algorithm)
The Graph class stores and manages the graph structure using an adjacency list.

#Responsibilities: Add vertices  ,Add edges  ,Print graph structure  ,Execute BFS traversal  ,Execute DFS traversal  ,Execute Dijkstra algorithm  
Screenshot:
<img width="1305" height="962" alt="image" src="https://github.com/user-attachments/assets/8eec8094-dbcd-449e-80d6-d30e01ce4690" />
<img width="1333" height="955" alt="image" src="https://github.com/user-attachments/assets/d1143170-4777-42ed-8125-5995b0add202" />
<img width="1348" height="959" alt="image" src="https://github.com/user-attachments/assets/9fda8276-5b8c-456a-ad8a-39874e5485ae" />

#Experiment Class
The Experiment class handles traversal execution and performance analysis.

#Responsibilities: Run BFS and DFS  ,Measure execution time  ,Compare results  
Screenshot:
<img width="1324" height="724" alt="image" src="https://github.com/user-attachments/assets/c80cefd7-4d05-45e0-adcb-7ac45370266c" />

#Main Class
The Main class runs the program and creates graphs of different sizes.

#Responsibilities: Create graphs  ,Add vertices and edges  ,Run BFS and DFS  ,Run Dijkstra algorithm  ,Measure execution time  
Screenshot:
<img width="1338" height="850" alt="image" src="https://github.com/user-attachments/assets/78088fb0-eb30-482a-8268-aa438e3d0284" />

#Algorithms

#Breadth-First Search (BFS)
BFS explores neighboring vertices level-by-level.  
It uses a Queue data structure.

###Steps:
1. Start from selected vertex  
2. Mark as visited  
3. Add neighbors to queue  
4. Visit in queue order  
5. Repeat until empty  

###Use Cases: Shortest path in unweighted graphs  ,GPS navigation  ,Social networks  

###Time Complexity:
O(V + E)

##Depth-First Search (DFS)

DFS explores one path deeply before backtracking.  
It uses recursion or a stack.

###Steps:
1. Start from selected vertex  
2. Mark as visited  
3. Visit unvisited neighbor  
4. Go deep until no neighbors  
5. Backtrack  

###Use Cases: Maze solving  ,Cycle detection  ,Path finding  

###Time Complexity:
O(V + E)

##Dijkstra’s Algorithm (Bonus Task)

Dijkstra’s Algorithm finds the shortest path from a starting vertex to all other vertices in a weighted graph.

###Key Idea:
It always selects the vertex with the smallest known distance and updates its neighbors.

###Requirements Implemented: Graph supports weighted edges  ,Distance array used  ,Visited array used  ,Shortest path computed step by step  

###Time Complexity:
O(V²) (without priority queue)

###Use Cases: GPS systems  ,Network routing  ,Shortest path problems  

#Experimental Results
The program was tested on graphs of different sizes.
<img width="1509" height="1016" alt="image" src="https://github.com/user-attachments/assets/39e6e42d-1e65-4eaa-befa-b40b4469dbe7" />
<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/84b5d80a-b3f8-420e-a63a-808264a8458d" />
<img width="1852" height="510" alt="image" src="https://github.com/user-attachments/assets/094e6089-75eb-4db4-9ed3-098889b00634" />

#Observations

- Traversal time increased as graph size increased  
- BFS and DFS show linear growth O(V + E)  
- DFS was slightly faster in some cases  
- BFS visits level-by-level  
- DFS explores deeply before backtracking  
- Dijkstra handles weighted shortest paths  

#Analysis Questions

##How does graph size affect performance?
As the number of vertices and edges increases, traversal time increases because more nodes must be visited.

##Which traversal was faster?
DFS was slightly faster in some experiments, but both are similar in complexity.

##Do results match O(V + E)?
Yes, both BFS and DFS visit every vertex and edge once.

##How does structure affect traversal order?
BFS explores neighbors first, DFS explores deep paths first. Order depends on adjacency list.

##When is BFS preferred?
When shortest path in unweighted graphs is needed.

##Limitations of DFS?
DFS may go too deep and does not guarantee shortest path.

#Reflection

This project helped me understand graph data structures and traversal algorithms. I learned how adjacency lists store graphs efficiently and how BFS, DFS, and Dijkstra behave differently.

I also learned how graph size affects performance and how execution time can be measured using `System.nanoTime()`.

One challenge was implementing Dijkstra’s algorithm and understanding how weighted edges affect shortest path calculations.
sal logic and recursion in DFS, but after testing the program multiple times, the concepts became clearer.
