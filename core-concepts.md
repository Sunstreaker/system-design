# core concepts

## questions
* why do we need odd number of nodes in a cluster?


## answers

why do we need odd number of nodes in a cluster?
Ans:
  * <b>for election</b> - in a cluster when a node is down, relection takes place to identify the new master node. For this to happen it must have more than half of the nodes. In case of 3 mode clusters, if a node is down it will have remaining 2 modes
    which is greater than then half of 3 (1.5). In case of 4 nodes cluster, if a node goes down it will be equallent to 3 nodes cluster. But if 2 node goes down then the election won't happen since the half of 4 is 2. which fails the greater then half rule
    So the extra node in 4 is useless, since it acts like 3 nodes cluster
    

## concepts
