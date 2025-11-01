# 🌟 1. Algorithms — Step-by-step problem solving

An algorithm is just a list of steps that tells a computer (or you) how to solve a problem.
Example: Searching a name in a phone book
Imagine you’re looking for someone’s name in a phone book.
* Way 1 – Start from the beginning:
You check one page at a time until you find the name.
✅ It will work.
🕒 But it’s slow if the book is big.
* Way 2 – Skip two pages at a time:
❌ Might skip the page where the name is.
* Way 3 – Open the middle:
Check if the name is before or after the middle.
Then go to that half and repeat.
✅ Much faster because you keep cutting the search in half.
This is how we compare algorithms — by how efficient (fast and memory-saving) they are.
Each of these approaches could be called algorithms. The speed of each of these algorithms can be pictured as follows in what is called **big-o**

![algoritham]("C:\Users\gadak\OneDrive\Documents\GitHub\CS50-Problem-Sets\Notes\Notes\assets\Screenshot_1-11-2025_125218_cs50.harvard.edu.jpeg")

Notice that the first algorithm, highlighted in red, has a big-O of n because if there are 100 names in the phone book, it could take up to 100 tries to find the correct name. The second algorithm, where two pages were searched at a time, has a big-O of n/2 because we searched twice as fast through the pages. The final algorithm has a big-O of log2n, as doubling the problem would only result in one more step to solve the problem.

* Programmers translate text-based, human instructions into code.


# ⚙️ 2. Big O Notation — Measuring algorithm speed

Big O notation is a way to describe how fast an algorithm grows as the input (like number of pages or items) increases.
It doesn’t tell you the exact time, just how the time changes when input grows.
### For example:
The first way (page-by-page) takes time that grows linearly → O(n)
The middle-search way (dividing in half each time) grows much slower → O(log n)
Think of Big O as:
“How bad can it get?” (worst-case scenario)
“How much does the time increase when I add more data?”

# ⏱ 2.1 Time & Space Complexity

We measure efficiency using two things:
* Time Complexity:
How much time an algorithm takes (depends on the size of input, not real seconds).
* Space Complexity:
How much memory it uses.
We ignore hardware differences (CPU, OS) and just focus on the relationship between input size and performance.

# ⚡ 2.1.1 Common Time Complexities
| Type	      | Big O	            |  Meaning                        |	Example |
|-------------|---------------------|---------------------------------|----------|
|Constant	  | O(1)	      |Always takes same time|         Accessing an array element
|Logarithmic	| O(log n) |	Cuts problem in half repeatedly |	Binary search |
|Linear	    | O(n)	|    Grows directly with input	|        Loop through a list once |
|Quadratic  |	O(n²)|   Two nested loops  |                 Comparing all pairs in a list|
|Exponential |	O(2ⁿ)	|    Doubles each time |	                  Recursive Fibonacci|
Factorial	|O(n!)	  | Extremely slow	        |           Trying every possible combination|



Speed ranking (Best → Worst)
✅ O(1) → O(log n) → O(n) → O(n log n) → O(n²) → O(2ⁿ) → O(n!)

# 🔍 How to Guess Time Complexity
O(1): Steps don’t depend on input size.
O(log n): Input gets halved each time (like binary search).
O(n): One loop through input.
O(n²): Nested loops.
O(2ⁿ): Work doubles every time.
O(n!): Every possible combination checked.

# 💡 2.2 Big Omega (Ω) — The Best Case
Big O (O) = Worst case (maximum time).
Big Omega (Ω) = Best case (minimum time).
### Examples of best-case times:
Ω(1), Ω(log n), Ω(n), Ω(n log n), Ω(n²)

# ⚖️ 2.3 Big Theta (Θ) — The Average or Tight Bound
If both the best and worst cases are similar, we use Theta (Θ) notation.
It means — on average, the algorithm behaves the same way most of the time.

### Examples:
Θ(1), Θ(log n), Θ(n), Θ(n log n), Θ(n²)

🧠 Summary:
|Notation |	    Meaning       |                         |Used for |
|----------|-------------------|------------------------|---------------------------|
|O	      |      Worst case	  |                         Upper limit of performance |
|Ω	      |      Best case	  |                         Lower limit of performance |
|Θ	      |      Average case  |	                       Tight bound (both same) |