# Emergency-Dispatch-Vehichle with Re-Routing
The objective of this project is to find and allocate an available emergency vehicle, taking 
source and destination as inputs and providing an optimum path during the course of travel.

# Dijkstra algorithm
Dijkstra algorithm was devised to find the shortest distance between two nodes. This algorithm 
is also called as single source shortest path approach. Dijkstra works affectively on large network
of nodes. It works on relaxation principle and fails to work on negative edges.

> **Relaxation principle:**
>> 
>> if(!visited[i]) :
>>>        if(minDistance + cost[nextNode][i] < distance[i]) :
>>>           distance[i] = minDistance + cost[nextNode][i] 
>>>           where, 
>>>           cost[i][j]=graph[i][j]+traffic_graph[i][j];

> **Algorithm working                                           :**           
>           
During the course of travel since the traffic density isn’t constant, different traffic 
densities are allocated between each of the locations. The densities range from low to 
very high. As the traffic density increases, weight of the path is increased. So the 
distance and traffic densities are deciding factors for weight of that particular path. 
Based on the weight, routing is organized. Shortest weighed path is chosen as optimal path.


# Re-Routing
> **Necessity:**
> Ambulances usually take a lot of time to arrive and there is no guarantee that an ambulance 
> would be allocated to the user. If for any reason the admission is rejected then the users 
> need not waste their time in checkin for a different ambulance rather ro-route in the same 
> ambulance. The grace period offered to opt for re-routing is ten minutes

When the source location is selected, the user is asked to either choose a hospital or a 
nearby hospital would be allocated. If due to any technical reasons like non availability 
of hospital beds, closed admissions, lack of medical equipment in destined hospital or 
need of increase in criticality of case and advanced medical supervision is required, the 
status of admission is recorded and re-routing to a different hospital gets enabled.

