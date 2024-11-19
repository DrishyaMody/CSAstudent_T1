---
layout: post
title: MCQ Review
courses: {'csa': {'week': 13}}
comments: True
type: collab
---

## Question 4
I got this question wrong because I misunderstood how the `if` condition and integer division work in Java. Since `y = 3`, the condition `(y < 0)` is false, so the `else` block executes. I also incorrectly thought `x / y` would include decimals, but Java performs integer division, which truncates decimals, resulting in `2`.

This concept is essential in AP CSA for writing `if-else` statements, using arithmetic correctly, and debugging logic in algorithms.

## Question 13
I got this question wrong because I didn’t properly analyze how the `if` condition within the loop compares consecutive elements in the array. The code prints the index `k` and value `arr[k]` only when `arr[k] > arr[k + 1]`. I mistakenly included the last element in my output, but the loop only goes up to `arr.length - 1` since the comparison requires a `k + 1` index.

This concept is important in AP CSA for iterating over arrays, comparing elements, and debugging logical errors in array manipulations.

## Question 19

I made a mistake in this question because I didn't correctly simplify the logic using De Morgan's Laws. De Morgan's Laws state that:

1. `!(A && B)` is the same as `!A || !B`.
2. `!(A || B)` is the same as `!A && !B`.

In this case, I didn’t apply these rules properly, which caused me to choose the wrong answer. I forgot that negating a condition also flips the operators (`&&` becomes `||` and vice versa). This reminds me to take my time and carefully break down logical expressions step by step.

## Question 25
The mistake lies in not recognizing that Interface II directly provides the necessary comparison methods (smallerHeight, smallerWidth, smallerDepth) to determine if one box can fit inside another. Interfaces I and III require additional logic or provide irrelevant data (e.g., volume, surface area).

In Java-based back-end, such interfaces ensure clean, reusable logic for object relationships. In front-end or AP CSA, they reinforce abstraction and clear design, essential for managing objects or components efficiently.
## Question 29
The mistake here is misunderstanding how the loop increment and modulus conditions interact. Answer E is correct because it starts at 4 and increments by 4, which matches the output of the original code (k % 4 == 0).

In Answer B, starting at 1 and incrementing by 4 skips the multiples of 4 entirely, leading to incorrect output.

**Concept in Java:**
This concept is foundational for understanding loops, conditions, and modular arithmetic. In back-end or front-end Java, such logic ensures correct iterations, like generating sequences or filtering data. For AP CSA, mastering this improves algorithmic thinking, crucial for problem-solving and efficient code design.

## Question 30
The mistake lies in misunderstanding how the substring method works. The correct answer is B ("pilercom") because:

word.substring(howFar + 1, word.length()) extracts the portion from index 4 ("piler").
word.substring(0, howFar) extracts the portion from index 0 to 3 ("com").
Concatenating these results gives "pilercom".
Concept in Java:
Understanding string manipulation methods like substring is essential for text processing in Java. In back-end or front-end tasks, such operations are commonly used for parsing, formatting, or rearranging data. In AP CSA, mastering this concept aids in solving string-related problems effectively.

## Question 40
The mistake lies in not understanding the recursive call's flow. The correct answer is E because:

The method prints after returning from recursion.
It successively shortens the string by one character and goes deeper into recursion until the base case (string length <= 1).
On unwinding, it prints each shortened string in reverse order of the recursion call.
Concept in Java:
Recursive methods often process data in a last-in, first-out manner. In back-end, recursion is used for tasks like traversing trees or generating combinations. For AP CSA, mastering recursion is key to understanding algorithmic problem-solving and stack behavior.


