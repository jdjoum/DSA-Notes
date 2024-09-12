# DSA-Notes
  This repository contains notes and example code based on what I learned from the Bro Code [Data Structures and Algorithms Course](https://www.youtube.com/watch?v=CBYHwZcbD-s). It covers fundamental DSA concepts, algorithmic strategies, and practical coding examples.

## Table of Contents
  1. [What is a Data Structure?](#what-is-a-data-structure)
  2. [What is an Algorithm?](#what-is-an-algorithm)
  3. [Why Should You Learn Data Structures and Algorithms?](#why-should-you-learn-data-structures-and-algorithms)
  4. [Stacks](#stacks)
  5. [Queues](#queues)
  

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

