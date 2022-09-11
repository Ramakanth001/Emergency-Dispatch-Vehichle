# Emergency-Dispatch-Vehichle
The objective of this project is to find and allocate an available emergency vehicle, taking 
source and destination as inputs and providing an optimum path during the course of travel.

# Dijkstra algorithm
Dijkstra algorithm was devised to find the shortest distance between two nodes. This algorithm 
is also called as single source shortest path approach. Dijkstra works affectively on large network
of nodes. It works on relaxation principle and fails to work on negative edges.

> **Relaxation principle:**
>>if(!visited[i]) 
    {
        if(minDistance + cost[nextNode][i] < distance[i]) 
        {
            distance[i] = minDistance + cost[nextNode][i] 
            
        }
    }

# Algorithm working
During the course of travel since the traffic density isn’t constant, different traffic 
densities are allocated between each of the locations. The densities range from low to 
very high. As the traffic density increases, weight of the path is increased. So the 
distance and traffic densities are deciding factors for weight of that particular path. 
Based on the weight, routing is organized. Shortest weighed path is chosen as optimal path.

# 
