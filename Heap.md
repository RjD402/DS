A heap is a tree-based data structure in which all the nodes of the tree are in a specific order

The maximum number of children of a node in a heap depends on the type of heap. However, in the more commonly-used heap type, there are at most  children of a node and it's known as a Binary heap.

In binary heap, if the heap is a complete binary tree with N  nodes, then it has smallest possible height which is logN (base2) .

**Max Heap**: In this type of heap, the value of parent node will always be greater than or equal to the value of child node across the tree and the node with highest value will be the root node of the tree.

### Time complexity
*O(N)* max_heapify function has complexity logN and the build_maxheap functions runs only N/2 times, but the amortized complexity for this function is actually linear.

*O(LogK)* is the time complexity to insert or delete an element from a heap having size K 

Thus the time complexity to build a heap of N elements is O(N)

Heaps are implemented using STL - priority_queue


### Uses of heap

1. Heap Sort
2. Priority Queue
