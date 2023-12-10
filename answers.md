# CMPS 2200 Assignment 5
## Answers

**Name:**__Raiya Dhalwala________________

- **1a.**
The maximum depth of a d-ary heap is logdn.

- **1b.**
The work done by delete-min is O(d logd n)
The work doen by insert is O(logd n)

- **1c.**
The new bound of the work for d-ary heap for dijkstras algortihm is O(|V|logd|V| + |E|logd|V|).

O(V) is for initializing and making heap. VlogdV and ElogdV to insert and delete.

- **1d.**
  We want d to get rid of the |V| part. So d= |V| so logd|V|= 1. Then we are left with O(|E|)
The value of d that will yield a runtime of O(|E|) is 
d = |V|

- **2a.**

k= 0 :APSP(0,1,0) = -2/APSP(0,2,0) = 2/APSP(1,2,0) = 0
k=1 :APSP(0,1,1) = -2/APSP(0,2,1) = -1/APSP(1,2,1) = 0
k=2 :APSP(0,1,2) = -2/APSP(0,2,2) = -1/APSP(1,2,2) = 0

- **2b.**
I do see a relationship between APSP(i,j,1) and APSP (i,j,2). In the graphs the values would be the same. So you can write (i,j,2) in term sof (i,j,0) and (i,j,1) only. The graph is only 3 nodes so there aren't many options, so the paths will all be accounted for.

- **2c.**
This optimal substructure property is the min of the fastest route from i to j: APSP(i,j,k−1). OR when it goes from i to k and k to j APSP(i,k,k−1) + APSP(k,j,k−1). 

- **2d.**
n^3 sub-problems will be computed bcause n values for i,j,k. So, O(n^3) will be the resulting work.

- **2e.**
Johnson's algorithm is better. 

- **3a.**
A solution to MST is not guaranteed to be a solution to MMET because the MST tries to lower the total weight of the tree while MMET lowers max weight of tree. Their goals are different so the same solution is not guaranteed.

- **3b.**
The algorithm would iterate through and sort edges with lowest weights to tree. In increasing order. Start from smallest edge and see if the edges make a spanning tree. If edge doesn't then include, and if does then don't use it. Repeat until no more vertices. If resulting tree isn't optimal then repeat with second smallest edge. 

- **3c.**
The work of this alternative algorithm is O(ElogV)