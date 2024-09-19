# core concepts

## tools/frameworks
* Raft

## questions
* why do we need odd number of nodes in a cluster?


## answers

why do we need odd number of nodes in a cluster?
Ans:
  * <b>for election</b> - in a cluster when a node is down, relection takes place to identify the new master node. For this to happen it must have more than half of the nodes. In case of 3 mode clusters, if a node is down it will have remaining 2 modes
    which is greater than then half of 3 (1.5). In case of 4 nodes cluster, if a node goes down it will be equallent to 3 nodes cluster. But if 2 node goes down then the election won't happen since the half of 4 is 2. which fails the greater then half rule
    So the extra node in 4 is useless, since it acts like 3 nodes cluster

  * <b>split brain problem</b> - Consider we have cluster with combined of 2 datacenters, one data center have 5 nodes and another one with 5 nodes in total of 8 nodes cluster. If there is network partition between two datacenters then both clusters will independently pariticipate in election and selects the master node. So the traffic would be routed same time to clusters creating data corruption.
    When the partition is esablished again, there will be master node in both datacenters causing issues in data syncup
    Let redo the cluster with 6 node in one dataceter and 4 in another, in this case the 4 node will not participate in election considring it is less count in nodes when compared to the another datacenter, which will avoid this issue
    

## tools/frameworks

### Raft
https://www.youtube.com/watch?v=P9Ydif5_qvE&t=53s

### Redis
https://www.youtube.com/watch?v=3WOfXRjYnGA

### kafka

https://www.youtube.com/watch?v=6YL0L4lb9iM

### mongodb







