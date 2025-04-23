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

