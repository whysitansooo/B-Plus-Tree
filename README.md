# 🌳 B+ Tree Implementation in C++

## 📌 Overview
This repository contains a **console-based implementation of a B+ Tree** data structure in C++.  
B+ Trees are balanced tree structures that maintain sorted data and allow for **efficient insertion, deletion, and search operations** with **logarithmic time complexity**.

---

## ✨ Features

- **Tree Initialization**  
  Define the order of the B+ Tree (maximum number of keys per node).

- **Key-Value Operations**
  - **Insert**: Add key-value pairs to the tree.
  - **Delete**: Remove keys from the tree.
  - **Search**: Find values by key or search within a key range.

- **Tree Visualization**  
  Display the current structure of the B+ Tree with detailed node information.

---

## 🔍 How B+ Trees Work

- Stores data in **sorted order**.
- Maintains balance to ensure **O(log n)** performance for insert, delete, and search.
- All **data records are stored at the leaf level**.
- Uses **internal nodes for indexing**.
- Automatically **rebalances** when nodes become overfull or underfull.

---

## 🛠️ Commands

| Command             | Description                                 | Example               |
|---------------------|---------------------------------------------|-----------------------|
| `Initialize(x)`     | Set the order of the B+ Tree                | `Initialize(3)`       |
| `Insert(key,value)` | Add a key-value pair to the tree            | `Insert(10,20.5)`     |
| `Delete(key)`       | Remove a key from the tree                  | `Delete(10)`          |
| `Search(key)`       | Find a value by its key                     | `Search(25)`          |
| `Search(k1,k2)`     | Find values within a key range              | `Search(10,50)`       |
| `Display`           | Visualize the structure of the tree         | `Display`             |
| `Exit`              | Exit the program                            | `Exit`                |

---

## 💡 Usage Example

```bash
> Initialize(3)
> Insert(10,100.5)
> Insert(20,200.75)
> Insert(5,50.25)
> Display

==== B+ TREE STRUCTURE ====

Node(0x55f5e76a8eb0): [10] (Internal) -> Root
  Child[0]: 0x55f5e76a8f20
  Child[1]: 0x55f5e76a9060

=== LEVEL 1 ===
Node(0x55f5e76a8f20): [5] (Leaf) -> Parent(0x55f5e76a8eb0)
Node(0x55f5e76a9060): [10|20] (Leaf) -> Parent(0x55f5e76a8eb0)

=========================

> Search(10)
100.5

> Search(5,20)
50.25 ,100.5 ,200.75 ,

> Delete(10)
> Display
```

## 🧩 Implementation Details

- The tree dynamically adjusts its structure through **node splitting** and **merging**.
- **Leaf nodes** store both keys and values.
- **Internal nodes** store keys and pointers to child nodes.
- Efficient **redistribution** and **merging algorithms** maintain tree balance after deletions.
- The visual tree display shows:
  - Memory addresses of nodes
  - Keys within nodes
  - Parent-child relationships

---

## ⚙️ Building & Running

### 🔧 Prerequisites

- A **C++ compiler** supporting **C++11** or later.

### 🏗️ Build

```bash
g++ -std=c++11 main.cpp -o bplustree
```
## Notes
- The current implementation has a maximum order size of 50 (configurable via MAX constant)
- **If an order greater than 50 is specified, it defaults to 3
- Memory management is handled automatically
## Performance
B+ Trees provide efficient operations with the following average time complexities:

-**Search**: O(log n)
-**Insert**: O(log n)
-**Delete**: O(log n)
Where n is the number of keys in the tree.


