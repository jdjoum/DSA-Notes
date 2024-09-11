# DSA-Notes
  This repository contains notes and example code based on what I learned from the Bro Code [Data Structures and Algorithms Course](https://www.youtube.com/watch?v=CBYHwZcbD-s). It covers fundamental DSA concepts, algorithmic strategies, and practical coding examples.

## Table of Contents
  1. [What is a Data Structure?](#what-is-a-data-structure)
  2. [What is an Algorithm?](#what-is-an-algorithm)

## What is a Data Structure?

  A **data structure** is a way of organizing and storing data so that it can be accessed and modified efficiently. Different types of data structures are designed to suit different kinds of operations and performance requirements, making them fundamental to computer science and software development.

  <ins>Common Types of Data Structures</ins>
    
  1. Array:
  - Description: A collection of elements, typically of the same type, stored in contiguous memory locations.
  - Example: `int[] numbers = {1, 2, 3, 4, 5};`
  - Use case: Good for accessing elements by index, such as in lists of numbers or objects.

  2. Linked List:
  - Description: A sequence of nodes where each node contains data and a reference (or link) to the next node.
  - Example:
    ```
    class Node {
      constructor(data) {
        this.data = data;
        this.next = null;
      }
    }
    ```
  - Use case: Useful for dynamic memory allocation and efficient insertion/deletion operations, like in queues or stacks.

  3. Stack:
  - Description: A collection of elements that follows the Last In, First Out (LIFO) principle.
  - Example: Imagine a stack of plates where the last one added is the first one to be removed.
  - Use case: Useful in recursion, undo operations, or browser history navigation.

  4. Queue:
  - Description: A collection of elements that follows the First In, First Out -(FIFO) principle.
  - Example: A line of people waiting for service where the first person in line is served first.
  - Use case: Task scheduling or handling requests in order.

  5. Hash Map (Hash Table):
  - Description: A collection of key-value pairs, where each key is unique, and a hash function is used to compute an index in an array to store the value.
  - Example: { "name": "John", "age": 30 } in JSON or a dictionary in Python.
  - Use case: Efficient lookups by key, like storing user data by their ID.

  6. Tree:
  - Description: A hierarchical structure with a root node and child nodes, where each node can have multiple children.
  - Example: A file system structure where directories can have subdirectories.
  - Use case: Searching and sorting algorithms, hierarchical data representation.

  7. Graph:
  - Description: A collection of nodes (vertices) and edges connecting them, representing relationships between pairs of objects.
  - Example: Social networks where users are nodes and friendships are edges.
  - Use case: Modeling networks, paths, and connections like web pages and links.

  <ins>Why Data Structures Matter</ins>

  The choice of data structure affects the efficiency of algorithms. For instance, a linked list is more efficient for frequent insertions and deletions compared to an array, while an array is better for random access.

## What is an Algorithm?

  An **algorithm** is a step-by-step procedure or set of rules used to solve a specific problem or perform a task. It is a sequence of instructions that can be executed to produce a desired outcome. Algorithms are widely used in computer programming, mathematics, and everyday problem-solving.

  <ins>Examples of Algorithms:</ins>

  1. Binary Search Algorithm:
  - Problem: Find an element in a sorted array.
  - Algorithm:
    1. Start with the middle element of the array.
    2. If the middle element is the target, return its index.
    3. If the middle element is greater than the target, repeat the process on the left half of the array.
    4. If the middle element is smaller, repeat the process on the right half of the array.
    5. Continue this process until the element is found or the array is exhausted.
  - Use Case: Searching for a name in a sorted list of contacts.

  2. Bubble Sort Algorithm:
  - Problem: Sort an array of numbers in ascending order.
  - Algorithm:
    1. Start from the first element of the array.
    2. Compare the current element with the next element.
    3. If the current element is greater than the next, swap them.
    4. Move to the next pair and repeat.
    5. After each pass through the array, the largest element moves to the end.
    6. Continue until the array is sorted.
  - Use Case: Organizing a list of students' grades from lowest to highest.

  3. Euclidean Algorithm:
  - Problem: Find the greatest common divisor (GCD) of two numbers.
  - Algorithm:
    1. Divide the larger number by the smaller one.
    2. Take the remainder and replace the larger number with it.
    3. Repeat the process until the remainder is zero.
    4. The non-zero divisor at that point is the GCD.
  - Use Case: Simplifying fractions.

  4. Dijkstra’s Algorithm:
  - Problem: Find the shortest path between two nodes in a graph.
  - Algorithm:
    1. Set the starting node’s distance to zero and all other nodes' distances to infinity.
    2. Select the unvisited node with the smallest distance.
    3. Update the distances of its neighboring nodes.
    4. Repeat the process until all nodes have been visited or the shortest path to the target node is found.
  - Use Case: Finding the shortest driving route between two cities on a map.

  These examples illustrate how algorithms are designed to solve specific problems efficiently. Each step in an algorithm is clearly defined to ensure it can be followed systematically. 





