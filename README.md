B+ Tree Implementation
Overview
This repository contains a console-based implementation of a B+ Tree data structure in C++. B+ Trees are balanced tree data structures that maintain sorted data and allow for efficient insertion, deletion, and search operations with logarithmic time complexity.

Features
Tree Initialization: Define the order of the B+ tree (maximum number of keys per node)
Key-Value Operations:
Insert: Add key-value pairs to the tree
Delete: Remove keys from the tree
Search: Find values by key or search within a key range
Tree Visualization: Display the current structure of the B+ tree with detailed node information
How B+ Trees Work
B+ Trees are a type of self-balancing tree data structure that:

Stores data in sorted order
Maintains balance to ensure O(log n) performance for insert, delete and search operations
Has all data records stored at the leaf level
Uses internal nodes for indexing
Automatically rebalances when nodes become overfull or underfull
Commands
Command	Description	Example
Initialize(x)	Set the order of the B+ tree (maximum keys per node)	Initialize(3)
Insert(key,value)	Add a key-value pair to the tree	Insert(10,20.5)
Delete(key)	Remove a key from the tree	Delete(10)
Search(key)	Find a value by its key	Search(25)
Search(key1,key2)	Find values within a range of keys	Search(10,50)
Display	Visualize the structure of the tree	Display
Exit	Exit the program	Exit
Usage Example
Implementation Details
The tree dynamically adjusts its structure through node splitting and merging
Leaf nodes store both keys and values
Internal nodes store keys and pointers to child nodes
Efficient redistribution and merging algorithms maintain tree balance after deletions
Visual tree display shows the memory addresses of nodes, keys, and parent-child relationships
Building & Running
Prerequisites
C++ compiler supporting C++11 or later
Build
Run
Notes
The current implementation has a maximum order size of 50 (configurable via MAX constant)
If an order greater than 50 is specified, it defaults to 3
Memory management is handled automatically
Performance
B+ Trees provide efficient operations with the following average time complexities:

Search: O(log n)
Insert: O(log n)
Delete: O(log n)
Where n is the number of keys in the tree.
