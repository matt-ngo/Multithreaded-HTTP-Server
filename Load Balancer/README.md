## Assignment 3: loadbalancer

##### Goal:
To create a load balancer that will distribute connections over a set of servers such as the one that implemented in the previous assignment, while ignoring non-responding servers. 

It will use the health check implemented in that assignment to keep track of the performance of these servers and decide which one will receive the incomingconnection.

##### Usage: 
_Parameters_:  
 - [Port number to receive connections]
 - [Port number for servers (at least 1)]
 - [-N parallel connections serveiced at once (4 default)] 
 - [-R How often (# requests) healthcheck is requested]

_EX:_
```
./loadbalancer 1234 8080 8081 8743
./loadbalancer -N 7 1234 8080 -R 3 8081
./loadbalancer 1234 -N 8 8081
./loadbalancer 1234 9009 -R 12 7890
./loadbalancer 1234 1235 -R 2 1236 -N 11
```
