# DSA-Notes
  This repository contains notes and example code based on what I learned from the Bro Code [Data Structures and Algorithms Course](https://www.youtube.com/watch?v=CBYHwZcbD-s). It covers fundamental DSA concepts, algorithmic strategies, and practical coding examples.

## Table of Contents
  1. [What is a Data Structure?](#what-is-a-data-structure)
  2. [What is an Algorithm?](#what-is-an-algorithm)
  3. [Why Should You Learn Data Structures and Algorithms?](#why-should-you-learn-data-structures-and-algorithms)
  4. [Stacks](#stacks)
  5. [Queues](#queues)
  6. [Priority Queues (Heaps)](#priority-queues-heaps)
  7. [Linked Lists](#linked-lists)
  8. [Dynamic Arrays](#dynamic-arrays)
  9. [Big O Notation](#big-o-notation)
  10. [Linear Search](#linear-search)
  
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

## Why Should You Learn Data Structures and Algorithms?

  Learning Data Structures and Algorithms (DSA) is crucial for several reasons:

  1. Problem-Solving Skills: DSA teaches how to break down complex problems and solve them efficiently. It enhances logical thinking and helps in developing optimal solutions.
  2. Efficient Coding: Algorithms and data structures provide a foundation for writing code that runs faster and uses fewer resources. This is vital in real-world applications where performance matters.
  3. Technical Interviews: Many software engineering interviews focus on DSA. Mastering these concepts is essential for landing a job in top tech companies, as they evaluate problem-solving skills through DSA-related questions.
  4. Building Scalable Systems: When designing large systems, understanding how different data structures and algorithms behave in terms of time and space complexity helps in making better architectural decisions.
  5. Versatility: DSA knowledge applies across various domains, including web development, mobile applications, artificial intelligence, and game development, making you a more versatile developer.
  6. Foundation for Advanced Topics: Concepts in DSA form the basis for learning more advanced topics like machine learning, cryptography, and database management.

  In short, DSA equips you with the skills to solve complex problems efficiently, crucial for both technical growth and career progression.

## Stacks

  <ins>Comprehensive Overview of the Stack Data Structure</ins>

  A **Stack** is a linear data structure that follows the Last In, First Out (LIFO) principle. This means that the last element added to the stack is the first one to be removed. It's similar to a stack of plates—only the top plate can be removed, and new plates are added to the top.

  <ins>Key Operations</ins>

  1. Push: Add an element to the top of the stack.
  2. Pop: Remove and return the element from the top of the stack.
  3. Peek (or Top): Retrieve the top element without removing it.
  4. IsEmpty: Check whether the stack is empty.
  5. Size: Return the number of elements in the stack.

  Stacks can be implemented using arrays, linked lists, or dynamic data structures like lists in high-level programming languages.

  <ins>Applications of Stacks</ins>

  1. Function Call Management: Programming languages use stacks to manage function calls and local variables in recursive functions. Each call is pushed onto the call stack, and when the function returns, it's popped off the stack.
  2. Expression Evaluation and Syntax Parsing: Stacks are used to evaluate expressions, including converting infix expressions to postfix (Reverse Polish Notation) or prefix. Parsing expressions in compilers also relies on stacks.
  3. Undo Mechanism: In text editors, stacks store previous actions so that undoing them can be done in reverse order of their execution.
  4. Balanced Parentheses Problem: Stacks are commonly used to check whether parentheses in expressions are balanced.
  5. Browser History: The back/forward navigation buttons in browsers use stacks to manage visited web pages.

  <ins>Stack Operations in Python Example</ins>
  
  Consider a stack that holds integers:
  ```
  stack = []
  ```

  1. Push Operation: Adding an element to the top of the stack:
      ```
      stack.append(10)  # Stack: [10]
      stack.append(20)  # Stack: [10, 20]
      ```
  2. Pop Operation: Removing the top element from the stack:
      ```
      top_element = stack.pop()  # Removes 20; Stack: [10]
      ```
  3. Peek Operation: Retrieving the top element without removing it:
      ```
      top_element = stack[-1]  # Retrieves 10 without removing
      ```
  4. IsEmpty Operation: Checking if the stack is empty:
      ```
      is_empty = len(stack) == 0  # False, since the stack is not empty
      ```
  5. Size Operation: Checking the size of the stack:
      ```
      size = len(stack)  # 1, since there is one element (10)
      ```
  
  Python uses lists as dynamic arrays to implement a stack.

  <ins>Advantages of Stacks</ins>

  1. Simple to Implement: Stacks are relatively easy to implement and manage.
  2. Efficient Operations: Push and pop operations run in constant time, O(1).

  <ins>Disadvantages of Stacks</ins>

  1. Limited Access: Elements can only be accessed from the top, making it inefficient for accessing elements deep within the stack.
  2. Fixed Size (in Array Implementation): When implemented using arrays, stacks may run into size limitations unless a dynamic resizing mechanism is used.

  <ins>Stack Implementations</ins>

  1. Array-Based Stack: Easy to implement but requires predefined size or dynamic resizing.
  2. Linked List-Based Stack: More flexible since it can grow dynamically without needing a fixed size.

  <ins>Conclusion</ins>

  Stacks are essential for many computing problems, especially those that require managing data in a LIFO order. Their simplicity, coupled with efficiency in performing basic operations, makes them a fundamental tool in algorithms, system design, and software development.

## Queues

  <ins>Comprehensive Overview of the Queue Data Structure</ins>

  A **Queue** is a linear data structure that follows the First In, First Out (FIFO) principle. This means that the element added first will be removed first, similar to a line of people waiting for service.

  <ins>Key Operations</ins>

  1. Enqueue (Insertion): Adds an element to the rear (or back) of the queue.
  2. Dequeue (Removal): Removes an element from the front of the queue.
  3. Peek (Front): Retrieves the element at the front of the queue without removing it.
  4. IsEmpty: Checks if the queue is empty.
  5. Size: Returns the number of elements in the queue.

  <ins>Characteristics</ins>

  - FIFO: The first element enqueued will be the first one dequeued.
  - Front and Rear: The queue has two ends — the front where elements are removed, and the rear where elements are added.

  <ins>Types of Queues</ins>

  1. Simple Queue: Also known as a linear queue, elements are inserted from the rear and removed from the front. Once full, it cannot reuse space.
  2. Circular Queue: Overcomes the limitation of the simple queue by connecting the rear to the front, forming a circular structure. This allows reuse of space that was freed by dequeuing elements.
  3. Priority Queue: Elements are dequeued based on priority rather than their insertion order. Each element has a priority, and the one with the highest priority is dequeued first.
  4. Double-Ended Queue (Deque): Elements can be added or removed from both the front and rear, making it more flexible than a standard queue.

  <ins>Use Cases</ins>

  1. CPU Scheduling: Queues manage processes in a multitasking system.
  2. I/O Buffers: Queues handle data between slower and faster devices.
  3. Breadth-First Search (BFS): BFS uses a queue to explore nodes level by level.
  4. Task Scheduling: When tasks are handled in the order they arrive, queues manage them efficiently.
  5. Print Spooling: Queues handle print jobs, ensuring documents are printed in the order they were submitted.

  <ins>Queue Implementation</ins>

  Queues can be implemented using various data structures, such as:

  1. Arrays: Easy to implement but can be inefficient in terms of memory due to fixed size.
  2. Linked List: Efficient in terms of memory and dynamic resizing, avoiding the overflow problem of arrays.
  3. Stacks: A queue can also be implemented using two stacks to reverse the LIFO behavior of stacks into FIFO for the queue.

  <ins>Time Complexity</ins>

  - Enqueue: O(1) (amortized O(1) for circular queues or queues implemented using dynamic arrays)
  - Dequeue: O(1)
  - Peek: O(1)
  - IsEmpty/Size: O(1)

  <ins>Real-World Analogy</ins>

  Consider a line at a movie theater. The first person in line is served first, and new people join at the end of the line.

  <ins>Queue Implementation Using Python List</ins>

  Python lists can be used to implement a queue, but appending to the end and removing from the front can be inefficient for large queues due to the shifting of elements.

  ```
  class QueueList:
    def __init__(self):
        self.queue = []

    def enqueue(self, item):
        # Add an item to the rear of the queue
        self.queue.append(item)
        print(f"Enqueued: {item}")

    def dequeue(self):
        if self.is_empty():
            return "Queue is empty"
        # Remove an item from the front of the queue
        return self.queue.pop(0)

    def peek(self):
        if self.is_empty():
            return "Queue is empty"
        # Return the front element without removing it
        return self.queue[0]

    def is_empty(self):
        # Check if the queue is empty
        return len(self.queue) == 0

    def size(self):
        # Return the number of items in the queue
        return len(self.queue)

  # Example usage
  q = QueueList()
  q.enqueue(10)
  q.enqueue(20)
  q.enqueue(30)
  print(f"Front item: {q.peek()}")
  print(f"Dequeued: {q.dequeue()}")
  print(f"Queue size: {q.size()}")
  ```

  Output:

  ```
  Enqueued: 10
  Enqueued: 20
  Enqueued: 30
  Front item: 10
  Dequeued: 10
  Queue size: 2
  ```

  <ins>Queue Implementation Using Python `collections.deque`</ins>

  For a more efficient queue, the collections.deque can be used, which provides O(1) time complexity for both append and pop operations from either end.

  ```
  from collections import deque

  class QueueDeque:
      def __init__(self):
          self.queue = deque()

      def enqueue(self, item):
          # Add an item to the rear of the queue
          self.queue.append(item)
          print(f"Enqueued: {item}")

      def dequeue(self):
          if self.is_empty():
              return "Queue is empty"
          # Remove an item from the front of the queue
          return self.queue.popleft()

      def peek(self):
          if self.is_empty():
              return "Queue is empty"
          # Return the front element without removing it
          return self.queue[0]

      def is_empty(self):
          # Check if the queue is empty
          return len(self.queue) == 0

      def size(self):
          # Return the number of items in the queue
          return len(self.queue)

  # Example usage
  q = QueueDeque()
  q.enqueue(10)
  q.enqueue(20)
  q.enqueue(30)
  print(f"Front item: {q.peek()}")
  print(f"Dequeued: {q.dequeue()}")
  print(f"Queue size: {q.size()}")
  ```

  Output:

  ```
  Enqueued: 10
  Enqueued: 20
  Enqueued: 30
  Front item: 10
  Dequeued: 10
  Queue size: 2
  ```

  <ins>Differences Between List and `deque`:</ins>

  - Efficiency: deque is more efficient for queue operations because it allows O(1) operations for both enqueue and dequeue.
  - List: When using a list, dequeuing requires O(n) because removing the first element requires shifting all the other elements forward.

## Priority Queues (Heaps)

  <ins>Comprehensive Overview of the Priority Queue (Heap) Data Structure</ins>

  A **Priority Queue** (often implemented as a Heap) is a data structure that stores elements such that the element with the highest priority is always accessible at the front of the queue. It supports efficient retrieval of the highest (or lowest) priority element.

  <ins>Key Concepts</ins>

  1. Priority: Each element has an associated priority. The priority queue serves elements based on their priority rather than their order of insertion.
  2. Min-Heap vs Max-Heap:
  - In a Min-Heap, the smallest (or highest priority) element is at the top.
  - In a Max-Heap, the largest (or highest priority) element is at the top.
  3. Heap Property: Heaps maintain a complete binary tree structure where:
  - Min-Heap: Every parent node has a value less than or equal to its children.
  - Max-Heap: Every parent node has a value greater than or equal to its children.

  <ins>Key Operations</ins>

  1. Insert (Push):
  - Adds an element to the priority queue.
  - Complexity: O(log n), since the heap property must be maintained (involves "bubbling up" the newly inserted element).
  2. Extract Max/Min (Pop):
  - Removes and returns the highest (or lowest) priority element.
  - Complexity: O(log n), as the heap needs to be restructured after removal (involves "bubbling down" the last element to maintain the heap property).
  3. Peek (Top):
  - Retrieves the element with the highest (or lowest) priority without removing it.
  - Complexity: O(1), as the top element is always at the root of the heap.
  4. Decrease/Increase Key:
  - Changes the priority of an element.
  - Complexity: O(log n), since the heap property must be restored (either by bubbling up or down).
  5. Heapify:
  - Converts an arbitrary array into a heap.
  - Complexity: O(n).

  <ins>Conclusion</ins>

  Priority queues (heaps) are efficient for scenarios requiring frequent access to the highest or lowest priority element. They are widely used in algorithms and applications like graph traversal, scheduling, and event-driven simulations. The binary heap provides a good balance between simplicity and performance, while specialized heaps like the Fibonacci heap offer performance boosts for more complex operations.

## Linked Lists

  A **Linked List** is a linear data structure where elements, called nodes, are not stored in contiguous memory locations. Each node consists of two parts:
  
  1. Data: The value stored in the node.
  2. Pointer (or Reference): A reference to the next node in the sequence.

  <ins>Types of Linked Lists:</ins>
  
  1. Singly Linked List:
  - Each node contains data and a single pointer to the next node.
  - Last node points to `null` (or `None` in Python) to indicate the end of the list.

  Structure:
  ```
  [Data | Next] -> [Data | Next] -> [Data | Next] -> null
  ```

  2. Doubly Linked List:
  - Each node contains data, a pointer to the next node, and a pointer to the previous node.
  - Enables traversal in both directions (forward and backward).

  Structure:
  ```
  null <- [Prev | Data | Next] <-> [Prev | Data | Next] <-> [Prev | Data | Next] -> null
  ```

  3. Circular Linked List:
  - The last node points back to the first node, forming a circular chain.
  - Can be either singly or doubly linked.

  Structure:
  ```
  [Data | Next] -> [Data | Next] -> [Data | Next] --\
     ^                                            |
     \--------------------------------------------/
  ```

  <ins>Operations on Linked Lists:</ins>

  1. Insertion:
  - Can be done at the head, tail, or any specific position.
  - Time complexity:
    - O(1) for insertion at the head.
    - O(n) for insertion at a specific position or tail (due to traversal).

  2. Deletion:
  - Can remove nodes from the head, tail, or any specific position.
  - Time complexity:
    - O(1) for deletion at the head.
    - O(n) for deletion at a specific position or tail.

  3. Traversal:
  - To access or print all nodes in the list, you traverse from the head node to the last node.
  - Time complexity: O(n).

  4. Searching:
  - Searching for a node involves traversing through the list.
  - Time complexity: O(n).

  <ins>Advantages of Linked Lists:</ins>
  - Dynamic Size: Unlike arrays, linked lists do not need a predefined size. Memory is allocated dynamically as nodes are added.
  - Efficient Insertions/Deletions: Inserting or deleting a node at the beginning is O(1), whereas in an array, it may involve shifting elements.

  <ins>Disadvantages of Linked Lists:</ins>
  - Memory Overhead: Each node requires additional memory for storing the pointer(s).
  - Sequential Access: Linked lists do not provide random access like arrays. To access a particular node, traversal from the head is necessary.
  - Cache Unfriendliness: Due to non-contiguous memory allocation, linked lists do not benefit as much from modern CPU caches compared to arrays.

  <ins>Common Use Cases:</ins>
  - Dynamic data structures: Suitable for situations where the size of the structure is unknown in advance.
  - Undo functionality: In applications like text editors, where you may want to revert to the previous state (can be implemented using doubly linked lists).
  - Circular buffers: For tasks like memory management or scheduling.
  - To implement stacks or queues.
  - For GPS navigation.
  - For a music playlist.

  <ins>Example of a Singly Linked List in Python:</ins>
  ```
  class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

  class LinkedList:
      def __init__(self):
          self.head = None

      # Insertion at the head
      def insert_at_head(self, data):
          new_node = Node(data)
          new_node.next = self.head
          self.head = new_node

      # Traversal
      def print_list(self):
          current = self.head
          while current:
              print(current.data, end=" -> ")
              current = current.next
          print("None")

  # Usage
  ll = LinkedList()
  ll.insert_at_head(3)
  ll.insert_at_head(2)
  ll.insert_at_head(1)
  ll.print_list()  # Output: 1 -> 2 -> 3 -> None
  ```

  This example demonstrates a simple singly linked list with insertion at the head and traversal.

## Dynamic Arrays

  A **dynamic array** is a data structure that provides a resizable array-like interface. Unlike static arrays, which have a fixed size, dynamic arrays can grow and shrink in response to insertions and deletions of elements. Here’s a detailed overview of its characteristics, operations, and underlying mechanics:

  1. Basic Structure
  
  - A dynamic array starts with a fixed initial size. As elements are added, the array might eventually reach its capacity. When this happens, the dynamic array allocates a new, larger array (usually with a size double the original), copies over the elements, and continues inserting. The old array is then deallocated.

  2. Key Properties

  - Capacity: The total size of the allocated memory block (often larger than the actual number of elements stored).
  - Size: The current number of elements stored in the array.
  - Resizing: When the size exceeds the capacity, the array is resized to accommodate more elements.

  3. Common Operations

  - Accessing elements: O(1) time complexity. Accessing any element by index is instantaneous since dynamic arrays use contiguous memory, just like static arrays.
  - Appending an element: Typically O(1) amortized. When the array has space, appending is O(1). However, when resizing is required, the operation takes O(n) because every element needs to be copied to the new array.
  - Inserting elements: O(n) in the worst case. Inserting into the middle or the front of the array requires shifting elements, which takes O(n).
  - Deleting elements: O(n). Similar to insertion, elements need to be shifted to fill the gap left by the deleted element.
  - Resizing: When the array is full, a new array (usually double the size) is allocated, and all elements are copied over, resulting in an O(n) time complexity for that operation.

  4. Amortized Time Complexity

  - While appending elements might trigger a resize, which is O(n), the overall cost of appending multiple elements averages out. This is because doubling the capacity happens infrequently (after every n inserts). This leads to an amortized time complexity of O(1) for appending elements.

  5. Shrinkage

  - Some dynamic arrays may shrink when elements are removed to avoid wasting memory. This might happen when the array’s size falls below a certain threshold, such as one-fourth of the capacity. The shrinking process also involves allocating a new, smaller array and copying elements, similar to how it grows.

  6. Memory Allocation

  - Dynamic arrays rely on **heap memory** for their dynamic nature, allowing them to grow as needed. However, resizing can lead to a performance hit due to the overhead of memory allocation and copying elements.

  7. Advantages

  - Flexibility: Dynamic arrays can grow and shrink as needed, unlike static arrays.
  - Random Access: Constant-time access to any element by index.
  - Ease of Use: Especially in higher-level languages, dynamic arrays abstract away the complexity of memory management.

  8. Disadvantages

  - Resizing Cost: Occasionally, resizing can be expensive in terms of time.
  - Wasted Space: Dynamic arrays typically allocate more space than needed to prepare for future growth, leading to potential memory wastage.
  - Shifting Cost: Inserting or deleting elements from anywhere other than the end of the array is inefficient because of the need to shift elements.

  9. Dynamic Array in Programming Languages

  - C++: `std::vector` is a dynamic array that handles resizing automatically.
  - Java: `ArrayList` is a resizable array implementation.
  - Python: Lists in Python are dynamic arrays under the hood.

  10. Applications

  Dynamic arrays are widely used in scenarios requiring frequent insertion, deletion, and resizing of elements, such as:
  - Implementing stacks, queues, and other dynamic data structures.
  - Storing collections of items that may change in size over time (e.g., dynamic list of items in a UI, dynamic buffers).

  In summary, dynamic arrays provide a balance between the memory efficiency of static arrays and the flexibility of linked lists, making them a versatile choice for many algorithms and applications.

## Big O Notation

  **Big O Notation** is a mathematical concept used in computer science to describe the efficiency of algorithms, particularly in terms of their time complexity and space complexity. It provides a high-level understanding of how an algorithm's performance scales as the size of the input increases. Here's a breakdown:

  1. Purpose of Big O Notation
  - Big O measures the upper bound (worst-case scenario) of an algorithm’s performance. It doesn't provide an exact number of operations but rather a classification of the growth rate of the function based on the size of the input (denoted as `n`).

  2. Types of Complexity
  - Time Complexity: Measures the time an algorithm takes to complete as a function of the input size.
  - Space Complexity: Measures the amount of memory an algorithm uses as a function of the input size.

  3. Common Big O Notations
  
  | Big O Notation | Name | Description |
  | ---------------|------|-------------|
  | O(1) | Constant Time | The algorithm's performance is independent of the input size. |
  | O(log(n)) | Logarithmic Time | Performance increases logarithmically as the input size grows (e.g., binary search). |
  | O(n) | Linear Time | Performance grows linearly with the input size (e.g., iterating over an array). |
  | O(nlog(n)) | Log-Linear Time | Common in efficient sorting algorithms like mergesort or heapsort. |
  | O(n^2) | Quadratic Time | Performance is proportional to the square of the input size (e.g., bubble sort). |
  | O(2^n) | Exponential Time | Performance doubles with each addition to the input size (e.g., recursive algorithms). |
  | O(n!) | Factorial Time | Performance increases factorially, often seen in brute force solutions for permutation problems. |

  4. How to Analyze Big O

  - Key factors to consider:
    - Loops: A single loop over n elements is O(n). Nested loops typically increase the time complexity (e.g., a loop within a loop is O(n²)).
    - Recursive Algorithms: Analyze recursive calls to determine the overall complexity. Exponential growth often arises from recursive algorithms that make multiple calls per level.
    - Ignoring Constants: Big O ignores constant factors because they don’t significantly affect growth as the input size becomes large. For example, O(2n) simplifies to O(n).

  - Example Analysis:
    - Linear Search: Iterates through each element once, so the time complexity is O(n).
    - Binary Search: Divides the problem size by half each step, leading to O(log n) time complexity.
    - Bubble Sort: Compares each pair of elements repeatedly, leading to O(n²) complexity.

  5. Best, Worst, and Average Case
  - Best Case: The ideal scenario for the algorithm.
  - Worst Case: The worst performance scenario, typically what Big O focuses on.
  - Average Case: The expected scenario under typical conditions.

  6. Comparing Algorithms

  - Big O Notation allows us to compare the relative performance of different algorithms. For example:
    - A binary search with O(log n) is much more efficient than a linear search with O(n) for large datasets.
    - A quicksort algorithm has a best-case time complexity of O(n log n), which is generally faster than bubble sort, which is O(n²).

  7. Limitations of Big O
  - Practical considerations: Big O does not account for constant factors, hardware differences, or specific input cases.
  - Asymptotic behavior: It focuses only on large input sizes, which might not be relevant for small or practical inputs.

  Big O is an essential tool in understanding and comparing algorithms, offering insight into how well an algorithm scales as the input size increases.

## Linear Search 

  **Linear search**, also known as sequential search, is a simple searching algorithm that scans each element in a list or array sequentially until the desired element is found or the end of the list is reached. It works by comparing each element of the list with the target value until a match is found or all elements have been checked.

  How It Works:
  
  1. Start at the first element of the list or array.
  2. Compare the target value with the current element.
  3. If they match, return the index of the current element.
  4. If they do not match, move to the next element.
  5. Repeat steps 2-4 until the target value is found or the end of the list is reached.
  6. If the target value is not found after checking all elements, return a "not found" indicator (such as -1).

  Example:

  Given an array: `[5, 8, 3, 1, 9, 6]`

  To search for the value `9`:

  - Compare `5` (first element) with `9`: no match.
  - Compare `8` (second element) with `9`: no match.
  - Continue until reaching `9` (fifth element): match found at index 4.

  Algorithm:

  ```
  def linear_search(arr, target):
    for index in range(len(arr)):
        if arr[index] == target:
            return index  # Target found, return the index
    return -1  # Target not found
  ```

  Time Complexity:

  - Best case: O(1) - The target value is at the first position.
  - Worst case: O(n) – The target value is at the last position or not present in the list.
  - Average case: O(n) – On average, about half of the elements are checked.

  Space/Memory Complexity:

  - O(1) – No extra space or memory is required except for a few variables.

  When to Use:

  - Small data sets: Since the time complexity is O(n), linear search is most efficient with small lists or arrays.
  - Unsorted data: If the data is unsorted or there's no extra information about the data structure, linear search is a good starting point.
  - Simplicity: It's simple to implement and understand.

  Advantages:

  - Simple to implement.
  - Works on any list, whether sorted or unsorted.
  - No additional space is needed.
  - Useful for data structures that don't have random access like Linked Lists.

  Disadvantages: 

  - Inefficient for large datasets because it requires checking each element individually.
  - Slower than more advanced algorithms like binary search for sorted data.

  In summary, linear search is useful for smaller datasets or when dealing with unsorted data where simplicity is a priority. However, for larger datasets or when performance is critical, more advanced search algorithms like binary search (for sorted data) are preferred.
