#  Getting started with algorithms 
Getting started with algorithms can feel daunting, but it's a rewarding journey. Here's a structured approach to help you begin:

**1. Understand the Fundamentals:**

* **What is an algorithm?**  An algorithm is a step-by-step procedure or formula for solving a problem or accomplishing a specific task.  Think of it as a recipe for a computer.  It takes input, performs operations, and produces output.
* **Data Structures:** Algorithms often work with data structures.  These are ways of organizing and storing data to make it efficient to access and manipulate.  Start with basic ones:
    * **Arrays:** Ordered collections of elements.
    * **Linked Lists:** Collections of elements where each element points to the next.
    * **Stacks:** Last-In, First-Out (LIFO) data structure (like a stack of plates).
    * **Queues:** First-In, First-Out (FIFO) data structure (like a queue at a store).
    * **Trees:** Hierarchical data structures.
    * **Graphs:** Collections of nodes and edges, representing relationships.
* **Big O Notation:** This is crucial for understanding algorithm efficiency.  It describes how the runtime or memory usage of an algorithm scales with the input size.  Learn about common notations like O(1), O(log n), O(n), O(n log n), O(n²), and O(2ⁿ).  Understanding Big O helps you compare the performance of different algorithms.

**2. Choose a Programming Language:**

Pick a language you're comfortable with or want to learn. Python is often recommended for beginners due to its readability and extensive libraries.  Java, C++, and JavaScript are also popular choices.

**3. Start with Simple Algorithms:**

Don't jump into complex algorithms immediately. Begin with fundamental ones:

* **Searching:**
    * **Linear Search:**  Checking each element sequentially.
    * **Binary Search:**  Efficiently searching a sorted array.
* **Sorting:**
    * **Bubble Sort:**  Simple but inefficient for large datasets.
    * **Insertion Sort:**  Efficient for small datasets or nearly sorted data.
    * **Merge Sort:**  Efficient and uses a divide-and-conquer approach.
    * **Quick Sort:**  Generally very efficient, but can be slow in worst-case scenarios.
* **Basic Math Operations:**  Implement algorithms for addition, subtraction, multiplication, and division (you'll likely already know these, but coding them reinforces the algorithmic thinking process).

**4. Practice, Practice, Practice:**

* **Work through examples:**  Find algorithm examples online (many websites offer this) and try implementing them yourself.
* **Solve problems:**  Websites like LeetCode, HackerRank, Codewars, and others offer coding challenges of varying difficulty.  Start with the easier ones and gradually increase the difficulty.
* **Implement data structures:**  Don't just use built-in data structures; try implementing your own to understand how they work internally.
* **Debug:**  Learning to debug your code is essential.  Use a debugger or print statements to track the execution of your algorithms and identify errors.

**5. Learn from Resources:**

* **Online Courses:**  Platforms like Coursera, edX, Udacity, and Udemy offer excellent courses on algorithms and data structures.
* **Books:**  "Introduction to Algorithms" (CLRS) is a classic but challenging textbook.  There are many other more beginner-friendly books available.
* **YouTube Channels:**  Many channels provide tutorials and explanations of algorithms and data structures.

**6.  Focus on Understanding, Not Just Memorization:**

Don't try to memorize algorithms. Focus on understanding the underlying principles and how they work.  This will allow you to adapt and modify them as needed.


**Example (Python - Linear Search):**

```python
def linear_search(arr, target):
  """Searches for a target value in an array."""
  for i in range(len(arr)):
    if arr[i] == target:
      return i  # Return the index if found
  return -1  # Return -1 if not found

my_array = [10, 20, 30, 40, 50]
target_value = 30
index = linear_search(my_array, target_value)

if index != -1:
  print(f"Target found at index: {index}")
else:
  print("Target not found")
```

This is a starting point.  Consistent effort and a focus on understanding the fundamentals will pave the way for your success in learning algorithms. Remember to start small, build a solid foundation, and gradually increase the complexity of the problems you tackle.

#  A sample algorithmic problem 
Here are a few algorithmic problems of varying difficulty, categorized for clarity:

**Easy:**

* **Two Sum:** Given an array of integers `nums` and an integer `target`, return *indices of the two numbers such that they add up to `target`*.  You may assume that each input would have **exactly one solution**, and you may not use the *same* element twice.

   * **Example:**
     `nums = [2,7,11,15], target = 9`
     *Output:* `[0,1]` (because `nums[0] + nums[1] == 9`)


* **Reverse a String:** Write a function that reverses a string.

   * **Example:**
     *Input:* `"hello"`
     *Output:* `"olleh"`


**Medium:**

* **Palindrome Check:**  Write a function to determine if a given string is a palindrome (reads the same forwards and backward), ignoring case and non-alphanumeric characters.

   * **Example:**
     *Input:* `"A man, a plan, a canal: Panama"`
     *Output:* `true`


* **Merge Intervals:** Given an array of intervals where intervals[i] = [starti, endi], merge all overlapping intervals, and return an array of the non-overlapping intervals that cover all the intervals in the input.

   * **Example:**
     *Input:* `[[1,3],[2,6],[8,10],[15,18]]`
     *Output:* `[[1,6],[8,10],[15,18]]`


**Hard:**

* **Longest Palindromic Substring:** Given a string `s`, find the longest palindromic substring in `s`.

   * **Example:**
     *Input:* `"babad"`
     *Output:* `"bab"` or `"aba"` (both are valid answers)


* **Graph Traversal (e.g., Dijkstra's Algorithm):**  Find the shortest path between two nodes in a weighted graph.  Dijkstra's algorithm is a common approach.


These problems illustrate different algorithmic concepts:

* **Easy** problems focus on basic data structures and simple loops.
* **Medium** problems require more sophisticated logic and potentially more advanced data structures (like hash maps for Two Sum or sorting for Merge Intervals).
* **Hard** problems often involve more complex algorithms and may require optimization for efficiency (e.g., dynamic programming for Longest Palindromic Substring).


Remember to consider:

* **Time complexity:** How does the runtime scale with the input size?
* **Space complexity:** How much extra memory does your solution use?

These are crucial aspects of algorithm design and analysis.  Choose a problem that matches your current skill level and work through it, focusing on both correctness and efficiency.  There are many resources online (like LeetCode, HackerRank, etc.) with solutions and discussions for these types of problems.

#  Getting Started with Simple Fizz Buzz Algorithm in Swift 
The FizzBuzz algorithm is a classic programming challenge.  Here's how to implement it in Swift, starting with a simple, straightforward approach and then progressing to more advanced techniques:

**Method 1: Basic Approach (Most Readable)**

This approach uses a simple `for` loop and `if/else if/else` statements. It's easy to understand and a great starting point.

```swift
func fizzBuzz(n: Int) {
    for i in 1...n {
        if i % 15 == 0 {
            print("FizzBuzz")
        } else if i % 3 == 0 {
            print("Fizz")
        } else if i % 5 == 0 {
            print("Buzz")
        } else {
            print(i)
        }
    }
}

fizzBuzz(n: 15) // Call the function
```

**Method 2: Slightly More Concise (Using Ternary Operator)**

This version uses the ternary operator (`condition ? value1 : value2`) to make the code a bit more compact, but it might be slightly less readable for beginners.

```swift
func fizzBuzzConcise(n: Int) {
    for i in 1...n {
        let output = (i % 15 == 0) ? "FizzBuzz" : (i % 3 == 0) ? "Fizz" : (i % 5 == 0) ? "Buzz" : String(i)
        print(output)
    }
}

fizzBuzzConcise(n: 15) // Call the function
```


**Method 3:  Functional Approach (Using `map` and a closure)**

This method uses a functional programming style with the `map` function. It's more advanced but demonstrates a different way of thinking about the problem.

```swift
func fizzBuzzFunctional(n: Int) {
    (1...n).map { i in
        let output = (i % 15 == 0) ? "FizzBuzz" : (i % 3 == 0) ? "Fizz" : (i % 5 == 0) ? "Buzz" : String(i)
        print(output)
    }
}

fizzBuzzFunctional(n: 15) // Call the function
```

**Explanation of the Code:**

* **`%` (Modulo Operator):** This operator returns the remainder of a division.  For example, `10 % 3` is 1 because 10 divided by 3 is 3 with a remainder of 1.
* **`if/else if/else`:**  This is a conditional statement that executes different blocks of code based on different conditions.
* **Ternary Operator (`condition ? value1 : value2`):**  This is a shorthand way to write a simple `if/else` statement.  If the `condition` is true, it returns `value1`; otherwise, it returns `value2`.
* **`map`:** This higher-order function applies a given closure to each element of a sequence (in this case, the numbers 1 through `n`) and returns a new array containing the results.  We use it here to process each number individually and print the output.


Remember to choose the method that best suits your understanding and the context of your project. The first method is the most beginner-friendly, while the others showcase more advanced Swift techniques.  They all achieve the same result: printing the FizzBuzz sequence.

#  Algorithm Complexity 
Algorithm complexity refers to the amount of resources an algorithm consumes.  The resources most commonly considered are:

* **Time complexity:** How long the algorithm takes to run as a function of the input size.
* **Space complexity:** How much memory the algorithm uses as a function of the input size.

We typically analyze complexity using **Big O notation**, which describes the growth rate of the resource consumption as the input size grows very large.  It focuses on the dominant factors and ignores constant factors.

Here's a breakdown:

**1. Time Complexity:**

Time complexity is often expressed as a function of the input size, `n`. Common time complexities (from best to worst) include:

* **O(1) - Constant Time:** The algorithm's execution time remains the same regardless of the input size.  Example: Accessing an element in an array by index.
* **O(log n) - Logarithmic Time:** The execution time increases logarithmically with the input size.  Example: Binary search in a sorted array.
* **O(n) - Linear Time:** The execution time increases linearly with the input size. Example: Searching for an element in an unsorted array.
* **O(n log n) - Linearithmic Time:**  A combination of linear and logarithmic time.  Example: Merge sort, heap sort.
* **O(n²) - Quadratic Time:** The execution time increases quadratically with the input size. Example: Nested loops iterating over the input.
* **O(2ⁿ) - Exponential Time:** The execution time doubles with each addition to the input size. Example: Finding all subsets of a set.
* **O(n!) - Factorial Time:** The execution time grows factorially with the input size.  Example:  Traveling Salesperson Problem (brute force approach).


**2. Space Complexity:**

Space complexity measures the amount of memory an algorithm uses.  It's also expressed using Big O notation.  Similar classifications apply:

* **O(1) - Constant Space:** The algorithm uses a fixed amount of memory regardless of the input size.
* **O(n) - Linear Space:** The memory usage increases linearly with the input size.
* **O(log n) - Logarithmic Space:** The memory usage increases logarithmically with the input size.
* **O(n²) - Quadratic Space:** The memory usage increases quadratically with the input size.
* and so on...


**Analyzing Complexity:**

To analyze the complexity of an algorithm, you typically:

1. **Identify the basic operations:**  Determine the operations that contribute most significantly to the running time (e.g., comparisons, assignments, arithmetic operations).
2. **Count the number of operations:**  Express the number of operations as a function of the input size `n`.
3. **Identify the dominant term:**  As `n` gets very large, certain terms in the function will dominate.  Keep only the dominant term, ignoring constant factors and lower-order terms.
4. **Express using Big O notation:**  Use Big O notation to represent the growth rate of the dominant term.


**Example:**

Consider a simple function that sums all elements of an array:

```python
def sum_array(arr):
  total = 0
  for num in arr:
    total += num
  return total
```

This function iterates through the array once.  The number of additions is directly proportional to the size of the array (`n`).  Therefore, its time complexity is O(n) and its space complexity is O(1) (it uses a constant amount of extra space).


**Best, Worst, and Average Case:**

Complexity analysis can also consider best-case, worst-case, and average-case scenarios.

* **Best Case:** The most favorable input scenario.
* **Worst Case:** The least favorable input scenario.
* **Average Case:** The expected performance over many different inputs.

Often, the worst-case complexity is the most important to consider, as it provides an upper bound on the algorithm's performance.


Understanding algorithm complexity is crucial for choosing the right algorithm for a given task, especially when dealing with large datasets.  An algorithm with a lower time and space complexity will generally perform better.

#  Big-Theta notation 
Big-Theta (Θ) notation is a mathematical notation used in computer science to describe the asymptotic behavior of functions.  Specifically, it describes the tight bound of a function's growth rate.  This means it provides both an upper and lower bound, indicating that the function grows at the *same rate* as another function, within constant factors.

Here's a breakdown:

**Formal Definition:**

We say that *f(n) = Θ(g(n))* if and only if there exist positive constants *c₁*, *c₂*, and *n₀* such that for all *n ≥ n₀*,

```
c₁g(n) ≤ f(n) ≤ c₂g(n)
```

**What this means:**

* **`f(n)`:**  The function whose growth rate we're analyzing (e.g., the runtime of an algorithm).
* **`g(n)`:** A simpler function that represents the growth rate of `f(n)` (e.g., n, n², log n).  This is often called the *complexity* of the algorithm.
* **`c₁` and `c₂`:** Positive constants.  These constants account for variations in different implementations or hardware.  They essentially say that the growth rate is the same, even if the exact time differs by a constant factor.
* **`n₀`:** A threshold value.  The inequality only needs to hold for values of `n` greater than or equal to `n₀`.  This accounts for the fact that the growth rate might not be consistent for small inputs.

**In simpler terms:**

`f(n) = Θ(g(n))` means that `f(n)` grows proportionally to `g(n)`.  As `n` gets very large, the ratio between `f(n)` and `g(n)` stays within a constant range.  It's neither significantly faster nor significantly slower.

**Examples:**

* **`7n² + 3n + 10 = Θ(n²) `:**  The dominant term is n².  We can find constants that satisfy the definition. For example, for sufficiently large n,  `n² ≤ 7n² + 3n + 10 ≤ 8n²`.  Therefore, c₁ = 1, c₂ = 8.
* **`log₂(n) = Θ(log₁₀(n))`:**  Different logarithmic bases only differ by a constant factor.
* **`n³ = Θ(n³) `:** Trivially true.
* **`2ⁿ = Θ(2ⁿ)`:**  Exponential functions are in the same theta class.
* **`n² ≠ Θ(n)`:**  A quadratic function does not grow at the same rate as a linear function.

**Contrast with Big O and Big Omega:**

* **Big O (O):** Provides an *upper bound*.  `f(n) = O(g(n))` means `f(n)` grows *no faster* than `g(n)`.
* **Big Omega (Ω):** Provides a *lower bound*.  `f(n) = Ω(g(n))` means `f(n)` grows *at least as fast* as `g(n)`.
* **Big Theta (Θ):** Provides both an upper and lower bound, signifying that the growth rate is *tightly bound*.  It combines the information from Big O and Big Omega.  `f(n) = Θ(g(n))` if and only if `f(n) = O(g(n))` and `f(n) = Ω(g(n))`.


Big-Theta notation is crucial for analyzing algorithm efficiency and comparing the performance of different algorithms, as it allows for a precise description of their asymptotic behavior.  It focuses on the dominant terms in the function, ignoring constant factors and lower-order terms that become insignificant as the input size grows.

#  Comparison of the asymptotic notations 
Asymptotic notations describe the behavior of functions as their input approaches infinity.  They're crucial in computer science for analyzing algorithm efficiency.  Here's a comparison of the most common notations:

**1. Big O Notation (O):**

* **Meaning:**  Provides an *upper bound* on the growth rate of a function.  It describes the *worst-case* scenario.  We say f(n) = O(g(n)) if there exist positive constants c and n₀ such that 0 ≤ f(n) ≤ c * g(n) for all n ≥ n₀.
* **Example:** If an algorithm has a time complexity of O(n²), it means the runtime grows no faster than the square of the input size.  The actual runtime might be smaller, but it won't exceed a constant multiple of n² for sufficiently large n.
* **Focus:** Worst-case scenario.  Doesn't give information about the best or average case.

**2. Big Omega Notation (Ω):**

* **Meaning:** Provides a *lower bound* on the growth rate of a function. It describes the *best-case* scenario (though not necessarily the best-case runtime of a specific algorithm). We say f(n) = Ω(g(n)) if there exist positive constants c and n₀ such that 0 ≤ c * g(n) ≤ f(n) for all n ≥ n₀.
* **Example:** If an algorithm has a time complexity of Ω(n), it means the runtime grows at least as fast as the input size.  The actual runtime might be larger, but it won't be smaller than a constant multiple of n for sufficiently large n.
* **Focus:** Best-case scenario. Doesn't provide information about the worst or average case.

**3. Big Theta Notation (Θ):**

* **Meaning:** Provides a *tight bound* on the growth rate of a function. It means the function grows at the *same rate* as another function, both from above and below.  We say f(n) = Θ(g(n)) if there exist positive constants c₁, c₂, and n₀ such that 0 ≤ c₁ * g(n) ≤ f(n) ≤ c₂ * g(n) for all n ≥ n₀.  This means f(n) is both O(g(n)) and Ω(g(n)).
* **Example:** If an algorithm has a time complexity of Θ(n log n), it means the runtime grows proportionally to n log n.
* **Focus:** Precise description of growth rate.  Provides both upper and lower bounds.


**4. Little o Notation (o):**

* **Meaning:**  Indicates that a function grows *strictly slower* than another function.  f(n) = o(g(n)) means that for any positive constant c, there exists a positive constant n₀ such that 0 ≤ f(n) < c * g(n) for all n ≥ n₀.
* **Example:**  n = o(n²)  (n grows strictly slower than n²)

**5. Little omega Notation (ω):**

* **Meaning:** Indicates that a function grows *strictly faster* than another function. f(n) = ω(g(n)) means that for any positive constant c, there exists a positive constant n₀ such that 0 ≤ c * g(n) < f(n) for all n ≥ n₀.
* **Example:** n² = ω(n) (n² grows strictly faster than n)


**Summary Table:**

| Notation | Meaning                               | Upper/Lower Bound | Tight Bound? | Strict? |
|----------|---------------------------------------|--------------------|---------------|---------|
| O(g(n))  | Upper bound                           | Upper             | No            | No       |
| Ω(g(n))  | Lower bound                           | Lower             | No            | No       |
| Θ(g(n))  | Tight bound (both upper and lower)    | Both              | Yes           | No       |
| o(g(n))  | Strictly slower growth                | Upper             | No            | Yes      |
| ω(g(n))  | Strictly faster growth                | Lower             | No            | Yes      |


**Relationship between notations:**

* If f(n) = Θ(g(n)), then f(n) = O(g(n)) and f(n) = Ω(g(n)).
* If f(n) = o(g(n)), then f(n) = O(g(n)) but f(n) ≠ Θ(g(n)).
* If f(n) = ω(g(n)), then f(n) = Ω(g(n)) but f(n) ≠ Θ(g(n)).


Understanding these notations is fundamental to analyzing algorithms and comparing their efficiency.  They allow us to abstract away from constant factors and lower-order terms, focusing on the dominant behavior as the input size grows large.

#  Big-Omega Notation 
Big-Omega notation (Ω) is used in computer science to describe the lower bound of an algorithm's runtime or space complexity.  It provides a way to express the best-case (or a lower bound on the) performance of an algorithm.  In simpler terms, it tells us that the algorithm will *at least* perform this well.

Here's a breakdown of Big-Omega notation:

**Formal Definition:**

A function *f(n)* is said to be Big-Omega of *g(n)*, written as *f(n) = Ω(g(n))*, if there exist positive constants *c* and *n₀* such that:

`0 ≤ c * g(n) ≤ f(n)` for all `n ≥ n₀`

What this means:

* **`f(n)`:**  Represents the actual runtime (or space complexity) of the algorithm.
* **`g(n)`:** Represents a simpler function (e.g., n, n², log n) that describes the growth rate of the algorithm's lower bound.
* **`c`:** A positive constant that scales `g(n)`.  It allows for a constant factor difference between `f(n)` and `g(n)`.
* **`n₀`:** A threshold value.  The inequality only needs to hold for input sizes greater than or equal to `n₀`.  This is important because for small inputs, the behavior of an algorithm might be unpredictable.


**In simpler terms:**

Imagine you're measuring the time an algorithm takes to run for different input sizes (n).  *f(n)* represents the actual measured time.  *Ω(g(n))* says that no matter what, the time will always be *at least* proportional to *g(n)* for sufficiently large inputs (n ≥ n₀).  The constant *c* accounts for variations in hardware, implementation details, etc.  We're only interested in the general growth rate.

**Examples:**

* **Linear Search:**  A linear search in an unsorted array has a best-case time complexity of Ω(1). This is because if the target element is the first element, the algorithm finds it immediately (constant time).  Its worst-case and average-case are O(n).

* **Binary Search:** A binary search on a sorted array has a best-case time complexity of Ω(1) (if the element is found at the root). Its worst-case and average-case are O(log n).

* **Merge Sort:** Merge sort has a time complexity of Ω(n log n). This means its runtime will *always* be at least proportional to n log n, no matter how the data is arranged.


**Relationship to Big-O and Big-Theta:**

* **Big-O (O):** Describes the upper bound (worst-case) complexity.
* **Big-Omega (Ω):** Describes the lower bound (best-case or a lower bound on the runtime) complexity.
* **Big-Theta (Θ):** Describes both the upper and lower bounds (tight bound) complexity.  If f(n) = Θ(g(n)), then f(n) = O(g(n)) and f(n) = Ω(g(n)).


**Key takeaway:**  Big-Omega notation provides a valuable perspective on the best-case (or a lower bound of) performance an algorithm can achieve. While Big-O is often the focus when analyzing algorithms, understanding Ω gives a more complete picture of its complexity characteristics.

#  Big-O Notation 
Big O notation is a mathematical notation used to describe the limiting behavior of a function when the argument tends towards a particular value or infinity.  In computer science, it's used to classify algorithms according to how their runtime or space requirements grow as the input size grows.  It focuses on the dominant factors affecting performance, ignoring constant factors and lower-order terms.  This allows us to compare the efficiency of different algorithms in a general way, regardless of specific hardware or implementation details.

Here's a breakdown of key aspects:

**What Big O Describes:**

* **Worst-Case Scenario:** Big O notation typically describes the *worst-case* time or space complexity of an algorithm. This means it represents the upper bound on the resources the algorithm will use.

* **Growth Rate:** It's concerned with how the resource usage (time or space) scales with the input size (n).  The exact execution time is not the focus; rather, the *rate of growth* as n becomes large is what matters.

* **Asymptotic Analysis:** Big O describes the behavior of an algorithm as the input size approaches infinity.  Small inputs might have different performance characteristics, but Big O is about the long-term trend.

**Common Big O Notations and Their Growth Rates:**

* **O(1) - Constant Time:** The algorithm's runtime remains constant regardless of the input size.  Example: Accessing an element in an array by its index.

* **O(log n) - Logarithmic Time:** The runtime increases logarithmically with the input size.  Example: Binary search in a sorted array.

* **O(n) - Linear Time:** The runtime increases linearly with the input size.  Example: Searching an unsorted array for a specific element.

* **O(n log n) - Linearithmic Time:** The runtime is a combination of linear and logarithmic growth.  Example: Merge sort, heap sort.

* **O(n²) - Quadratic Time:** The runtime increases proportionally to the square of the input size.  Example: Nested loops iterating through the input data.

* **O(2ⁿ) - Exponential Time:** The runtime doubles with each addition to the input size.  Example: Finding all subsets of a set.

* **O(n!) - Factorial Time:** The runtime grows factorially with the input size.  Example: Traveling salesman problem (brute-force approach).


**Example:**

Let's say we have two algorithms to search for a number in a list:

* **Algorithm 1 (Linear Search):** Iterates through the list one by one.  Its runtime is proportional to the size of the list (n).  Therefore, its Big O notation is O(n).

* **Algorithm 2 (Binary Search):**  Works only on sorted lists.  It repeatedly divides the search interval in half.  Its runtime is proportional to the logarithm of the list size (log₂n).  Therefore, its Big O notation is O(log n).

Binary search (O(log n)) is significantly more efficient than linear search (O(n)) for large lists because logarithmic growth is much slower than linear growth.


**Important Considerations:**

* **Space Complexity:** Big O notation can also describe the space complexity of an algorithm, which refers to the amount of memory it uses as a function of the input size.

* **Best-Case and Average-Case:** While Big O often focuses on the worst-case, sometimes best-case (Ω notation) and average-case (Θ notation) complexities are also considered.

* **Dominant Terms:** When expressing Big O, only the dominant term (the term that grows fastest) is kept.  For example, O(n³ + 2n² + 100n) simplifies to O(n³).

* **Constants are Ignored:** Constant factors are ignored because they are less significant compared to the growth rate as n becomes large.


Understanding Big O notation is crucial for choosing efficient algorithms and writing performant code, especially when dealing with large datasets.  It provides a standardized way to compare the scalability of different approaches.

#  A Simple Loop 
A simple loop repeatedly executes a block of code until a certain condition is met.  The specific implementation depends on the programming language, but the general structure is the same.  Here are examples in a few popular languages:

**1. While Loop:**

This loop continues as long as a given condition is true.

* **Python:**

```python
count = 0
while count < 5:
  print(count)
  count += 1
```

* **JavaScript:**

```javascript
let count = 0;
while (count < 5) {
  console.log(count);
  count++;
}
```

* **C++:**

```c++
#include <iostream>

int main() {
  int count = 0;
  while (count < 5) {
    std::cout << count << std::endl;
    count++;
  }
  return 0;
}
```

**2. For Loop:**

This loop iterates a specific number of times or over a sequence (like an array or list).

* **Python:**

```python
for i in range(5):
  print(i)
```

* **JavaScript:**

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

* **C++:**

```c++
#include <iostream>

int main() {
  for (int i = 0; i < 5; i++) {
    std::cout << i << std::endl;
  }
  return 0;
}
```

**3. Do-While Loop (less common, but available in some languages):**

This loop executes the code block at least once, and then continues as long as the condition is true.

* **C++:**

```c++
#include <iostream>

int main() {
  int count = 0;
  do {
    std::cout << count << std::endl;
    count++;
  } while (count < 5);
  return 0;
}
```

These examples all print the numbers 0 through 4.  The choice of which loop to use depends on the specific task.  `while` loops are best when the number of iterations isn't known beforehand, while `for` loops are better for iterating a known number of times or over a collection.  `do-while` is used less frequently, generally only when you need to guarantee at least one execution.

