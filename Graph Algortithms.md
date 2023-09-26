# Graph Algorithms

- Euler’s Path - Path including every edge exactly once
- Fleury’s → to find euler’s path (start at odd vertex if exists, always choose non-bridge)
- Heirholzer → find euler’s path by combining two paths
- Kruskal’s → find MST (sort edges by wt and add if no cycle)
- Prim’s → find MST
- Boruvka’s → find MST (combine small components to bigger components)
- Reverse Deletion → find MST
- Greedy Algorithm for Chromatic # → color, go to next node, color with lowest possible color
- Welsh Powell → Chromatic #, Same but sort nodes in decreasing order of degree and move down list and color all not connected nodes
- Dijkstra’s → Single source shortest path, no -ve wts
- Bellman Ford → Single source shortest path, -ve and positive wts
- Johnson’s → Shortest path for every pair
- Chinese Postman → add edges to odd degree nodes for euler path
- Tarjan’s algorithm → find articulation point
- Ford Fulkerson → network flow
- Push Relabel → flow