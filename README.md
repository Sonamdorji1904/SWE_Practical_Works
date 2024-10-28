### Discussion Questions from Practical Work III
#### 1. What are the advantages and disadvantages of the recursive approach compared to the iterative approach?

| Feature                     | Recursive Approach                                   | Iterative Approach                                   |
|-----------------------------|-----------------------------------------------------|-----------------------------------------------------|
| **Simplicity**              | Easier to understand for naturally recursive problems | Can be more complex for recursive problems          |
| **Code Length**             | Often requires fewer lines of code                  | May require more lines of code                      |
| **Performance**             | Can be slower due to function call overhead         | Generally more efficient                             |
| **Stack Overflow Risk**     | Can lead to stack overflow with deep recursion      | No risk of stack overflow                            |
| **Memory Usage**            | Uses O(n) space for the call stack                  | Typically uses O(1) space (or O(n) with data structures) |

#### 2. How does memoization improve the performance of the recursive function? Are there any drawbacks?
* **Improvement:**

    * `Time Complexity Reduction`: Memoization transforms a naive recursive function with exponential time complexity into one with linear or polynomial time complexity by storing previously computed results. This is particularly beneficial in problems like the Fibonacci sequence or dynamic programming tasks where the same subproblems are solved multiple times.

* **Drawbacks:**

    * `Complexity in Implementation`: Implementing memoization can add complexity to the code, making it harder to read and maintain, especially for those unfamiliar with the concept.

    * `Memory Overhead`: While it saves time, the additional memory required to store results can be a drawback in memory-constrained environments, especially if the number of unique subproblems is large.

#### 3. In what scenarios might you prefer to use a generator function over other implementations?
* `Large Data Sets`: When working with large datasets where you want to iterate through items without loading everything into memory at once (e.g., reading large files line by line).

* `Infinite Sequences`: When generating an infinite sequence of values (e.g., Fibonacci numbers) where you only need one value at a time.

#### 4. How does the space complexity differ between these implementations?
* `Recursive Approach`: Space complexity is O(n) due to the call stack, where n is the recursion depth.

* `Iterative Approach`: Space complexity is O(1) for fixed space usage (e.g., loop counters) or O(n) if additional data structures are used.

* `Memoization`: Increases space complexity to O(n) for cached results, plus O(n) for the call stack in recursion, totaling O(n) in the worst case.

* `Generator Functions`: Space complexity is O(1) as they yield one item at a time without storing the entire output.

