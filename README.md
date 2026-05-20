# ADMS4
#Group: SE-2514
#Name: Ulzhan Askar

#Project Overview
This project demonstrates the implementation of graph traversal algorithms using Java.  
The graph is represented using an adjacency list structure.
  The program includes:
Vertex representation
Edge representation
Graph creation using adjacency lists
Breadth-First Search (BFS)
Depth-First Search (DFS)
Performance testing using execution time measurements
  Graphs of different sizes were created:
Small graph (10 vertices)
Medium graph (30 vertices)
Large graph (100 vertices)
  The project also compares traversal performance and analyzes graph behavior.
  
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

#Vertex class
  The Vertex class represents a graph node.
Responsibilities:Store vertex ID, Return vertex information, Provide string representation
<img width="1508" height="1024" alt="image" src="https://github.com/user-attachments/assets/209b692a-0060-4459-8819-e208a0fa42cc" />

#Edge class
  The Edge class represents a connection between vertices.
Responsibilities: Store source vertex, Store destination vertex, Return edge information
<img width="1512" height="1022" alt="image" src="https://github.com/user-attachments/assets/2abca1c2-d52c-46bb-8cca-1dc96481f8d8" />

#Graph class
  The Graph class stores and manages the graph structure using an adjacency list.
Responsibilities: Add vertices, Add edges, Print graph structure, Execute BFS traversal, Execute DFS traversal
<img width="1507" height="1018" alt="image" src="https://github.com/user-attachments/assets/54c9014e-db7e-4a7a-8267-9ff75fabf8ae" />
<img width="1513" height="1021" alt="image" src="https://github.com/user-attachments/assets/44033786-52db-4d16-aa97-a0f2916a0d1a" />

#Experiment class
  The Experiment class handles traversal execution and performance analysis.
Responsibilities: Run BFS and DFS, Measure execution time, Compare results
<img width="1506" height="1021" alt="image" src="https://github.com/user-attachments/assets/61005550-6a34-4ccb-b5b6-2d9cea8eb6ed" />

#Main class
  The Main class runs the program and creates graphs of different sizes.
Responsibilities: Create graphs, Add vertices and edges, Run BFS and DFS, Print results, Measure execution time
<img width="1506" height="1013" alt="image" src="https://github.com/user-attachments/assets/a2d79802-0c25-4c13-8b9e-7cb032ebce2e" />

#Algorithms

#Breadth-First Search (BFS)
  Breadth-First Search explores neighboring vertices level-by-level.
  BFS uses a Queue data structure.
#BFS Steps
1. Start from the selected vertex
2. Mark the vertex as visited
3. Add neighbors to the queue
4. Visit vertices in queue order
5. Repeat until queue becomes empty
#BFS Use Cases
Shortest path in unweighted graphs
GPS navigation
Social network analysis
#BFS Time Complexity
O(V + E)
Where:
V = number of vertices
E = number of edges

#Depth-First Search (DFS)
  Depth-First Search explores one path deeply before backtracking.
  DFS uses recursion or a stack.
#DFS Steps
1. Start from selected vertex
2. Mark vertex as visited
3. Visit unvisited neighbor
4. Continue deeply until no neighbors remain
5. Backtrack and continue traversal
#DFS Use Cases
Maze solving
Cycle detection
Path finding
#DFS Time Complexity
O(V + E)

#Experimental Results
  The program was tested on graphs of different sizes.
<img width="1509" height="1016" alt="image" src="https://github.com/user-attachments/assets/39e6e42d-1e65-4eaa-befa-b40b4469dbe7" />

<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/84b5d80a-b3f8-420e-a63a-808264a8458d" />
<img width="1852" height="510" alt="image" src="https://github.com/user-attachments/assets/094e6089-75eb-4db4-9ed3-098889b00634" />

#Observations
Traversal time increased as graph size increased.
BFS and DFS both showed linear growth relative to graph size.
DFS was slightly faster in some experiments.
BFS visited vertices level-by-level.
DFS explored deeply before backtracking.

The results matched the expected complexity:
O(V + E)

#Analysis Questions

#How does graph size affect BFS and DFS performance?
  As the number of vertices and edges increases, traversal time also increases because more nodes and connections must be visited.

#Which traversal was faster in the experiments?
  The difference was small, but DFS was slightly faster in some tests.
  
#Do results match expected complexity O(V + E)?
  Yes. Both BFS and DFS visited each vertex and edge once.

#How does graph structure affect traversal order?
  Traversal order depends on how vertices are connected. BFS visits nearby vertices first, while DFS explores deeply into one branch.

#When is BFS preferred over DFS?
  BFS is preferred when finding the shortest path in an unweighted graph.

#What are the limitations of DFS?
  DFS may use deep recursion and does not guarantee the shortest path.

#Screenshots
<img width="1512" height="1015" alt="image" src="https://github.com/user-attachments/assets/72682877-0f0f-4f13-9560-f2ebe333e1f3" />

#Reflection
This project helped me understand graph structures and traversal algorithms. I learned how adjacency lists efficiently store graph data and how BFS and DFS explore graphs differently.

I also learned how graph size affects algorithm performance and how execution time can be measured using System.nanoTime(). One challenge during implementation was understanding traversal logic and recursion in DFS, but after testing the program multiple times, the concepts became clearer.
