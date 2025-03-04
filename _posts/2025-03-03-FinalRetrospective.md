---
layout: post
title: Retrospective
comments: True
type: ccc
permalink: /retrospective
---
# CSA Retrospective

### *5 Things Over 12 Weeks*


Throughout the past 12 weeks, I worked on various aspects of our CSA projects, including:

* **2d Array Team Teach**
    - Worked with team to ensure class is effectively introduced to concepts
* **Burn Down Chart for crypto (fullstack)**
    - Connection between frontend and backend, developed several api methods and fetch calls
* **Efficiency in work enviornments**
    - working in branches, Sending PR's, became proficient at resolving merge errors
* **Burndown List**
    - Creating a definitive plan and points to attack and address for further fullstack development
* **API methods in Java trough Controllers** 
    - [First API Method Commit](https://github.com/DrishyaMody/CollegeAppBackend/commit/53bce0881fdaf77fd61afe10682820ee29e8db79#diff-ceaf5d81a61ec0de50f1017d9b7e36e474c5e9a9a6545fb2d960d78f9cbc4f1d)

* **Issue Tracking** 
    - [Project Issues & Tracking](https://github.com/nighthawkcoders/portfolio_2025/issues/622)
## 🔗 Key Links

* [Project Issues & Tracking](https://github.com/nighthawkcoders/portfolio_2025/issues/622)
* [2D Arrays Project](https://nighthawkcoders.github.io/portfolio_2025/csa/p3-2darrays2)
* [Planning Repository Issue](https://github.com/CSA-Coders-2025/Planning-Repository-Issue-House-/issues/201)
* [Spring 2025 Commits](https://github.com/nighthawkcoders/spring_2025/commits?author=DrishyaMody)
* [Portfolio 2025 Commits](https://github.com/nighthawkcoders/portfolio_2025/commits?author=DrishyaMody)

---

## 🌙 N@tM Feedback

Our Night at the Museum (N@tM) event provided valuable feedback and insights. Here are some key moments captured:

<div align="center">
  <img src="/CSAstudent_T1/images/n@tm1.jpeg" alt="DECA N@TM" width="400">
  <img src="/CSAstudent_T1/images/n@tm2.jpeg" alt="DECA N@TM" width="400">
  <img src="/CSAstudent_T1/images/n@tm3.jpeg" alt="DECA N@TM" width="400">
  <img src="/CSAstudent_T1/images/n@tm4.jpeg" alt="DECA N@TM" width="400">
</div>

## 📋 Google Form Feedback

<div align="center">
  <img src="/CSAstudent_T1/images/GoogleForm1.png" alt="Form Responses" width="400">
  <img src="/CSAstudent_T1/images/GoogleForm2.png" alt="Form Responses" width="400">
</div>

---

# 📝 MCQ Reflection

Below are incorrect answers I got on the 2015 MCQ:

<div align="center">
  <img src="/CSAstudent_T1/images/CBexamQ1.png" alt="MC Question 1" width="300">
  <img src="/CSAstudent_T1/images/CBexamQ4.png" alt="MC Question 4" width="300">
  <img src="/CSAstudent_T1/images/CBexamQ16.png" alt="MC Question 16" width="300">
  <img src="/CSAstudent_T1/images/CBexamQ23.png" alt="MC Question 23" width="300">
  <img src="/CSAstudent_T1/images/CBexamQ27.png" alt="MC Question 27" width="300">
  <img src="/CSAstudent_T1/images/CBexamQ34.png" alt="MC Question 34" width="300">
  <img src="/CSAstudent_T1/images/CBexamQ39.png" alt="MC Question 39" width="300">
</div>

---

## 🔍 Question 1

### Problem Understanding  
The given method `numDivisors` is designed to count how many numbers between `1` and `inputVal` are divisors of `inputVal`. This means we need to check which numbers `k` within this range evenly divide `inputVal`.  

### Code Analysis  
The method follows these steps:  

1. Initialize `count = 0` to track the number of divisors.  
2. Iterate `k` from `1` to `inputVal`.  
3. Check if `k` is a divisor using the condition inside the `if` statement.  
4. If the condition is true, increment `count`.  
5. Return `count` at the end.  

### Correct Condition  
To check if `k` is a divisor of `inputVal`, we need to verify that `inputVal` is divisible by `k` without a remainder. This is correctly expressed as:  

```java
if (inputVal % k == 0)

## Question 4

## Question Analysis

The given question presents a Java method `findMax()` designed to return the largest value in a 1D integer array `arr`. The method iterates over the array using an enhanced `for` loop and keeps track of the maximum value encountered.

### **Code Breakdown**
```java
private int[] arr;

/** Precondition: arr.length > 0
  * @return the largest value in array arr
  */
public int findMax() {
    int maxVal = 0;

    for (int val : arr) {
        if (val > maxVal) {
            maxVal = val;
        }
    }

    return maxVal;
}
``` 
## Potential Issues

- Initialization Problem: The method initializes maxVal = 0. This causes issues when:

- All values in arr are negative, as maxVal will never update and always return 0 (which is incorrect).

- The largest value in arr is zero, making it impossible to determine if the function worked correctly or if it was due to the incorrect initialization.

- Correct Approach: The best way to initialize maxVal is to use Integer.MIN_VALUE or set maxVal = arr[0] to ensure correctness.


## Question 16

The given question presents a Java method `calculate()` that iterates over a **2D integer array** and determines a specific value to return.

### **Code Breakdown**
```java
/** Precondition: values has at least one row */
public static int calculate(int[][] values)
{
    int found = values[0][0];
    int result = 0;
    
    for (int[] row : values)  // Iterate through each row
    {
        for (int y = 0; y < row.length; y++)  // Iterate through elements in the row
        {
            if (row[y] > found)  // If current element is larger than `found`
            {
                found = row[y];   // Update `found` to the new largest value
                result = y;       // Store the column index of the largest value
            }
        }
    }
    return result;
}
```
## Key Observations
Tracking Largest Value:

The nested loop scans all elements in the 2D array.

Whenever a larger value is found, found is updated, and result is updated with its column index (y).

Final Value of result:

After scanning the entire 2D array, result will contain the column index of the largest value in the array

(E)	The column index of an element with the largest value in the two-dimensional array.	Correct (Method tracks and returns column index y of the largest element).

# Question 23:

## **Question Analysis**
The provided code segment is an implementation of **insertion sort**, which sorts an array step by step by shifting elements to their correct position.

### **Given Array:**
Initial array: `{5, 4, 3, 2, 1}`

### **How Insertion Sort Works (Step by Step)**
#### **Pass 1 (j = 1)**
- `insertItem = arr[1] = 4`
- Compare `4` with `5`, shift `5` to the right.
- Place `4` in position `0`.
- **Array after Pass 1:** `{4, 5, 3, 2, 1}`

#### **Pass 2 (j = 2)**
- `insertItem = arr[2] = 3`
- Compare `3` with `5` → shift `5` to the right.
- Compare `3` with `4` → shift `4` to the right.
- Place `3` in position `0`.
- **Array after Pass 2:** `{3, 4, 5, 2, 1}`

### **Correct Answer**
✅ **(C) `{3, 4, 5, 2, 1}`**


# Question 27

## **Question Analysis**
The provided code is a **selection sort** algorithm, which finds the smallest element and swaps it with the first unsorted element.

### **Given Array:**
Initial array: `{6, 3, 2, 5, 4, 1}`

### **Selection Sort Step-by-Step**
#### **Pass 1 (j = 0)**
- Find the smallest value (`1` at index `5`).
- Swap `1` with `6`.
- **Array after Pass 1:** `{1, 3, 2, 5, 4, 6}`

#### **Pass 2 (j = 1)**
- Find the smallest value (`2` at index `2`).
- Swap `2` with `3`.
- **Array after Pass 2:** `{1, 2, 3, 5, 4, 6}`

#### **Pass 3 (j = 2)**
- The next smallest value is `3`, already in place.
- **Array remains:** `{1, 2, 3, 5, 4, 6}`

### **Correct Answer**
✅ **(C) `{1, 2, 3, 6, 5, 4}`**


# Question 34

## **Question Analysis**
The method `wordsWithCommas()` generates a string representation of a list, separating words with commas and enclosing them in `{}`.

### **Missing Expressions:**
- `sizeOfList = listOfWords.size()`
- `condition` to decide **when to add a comma**: 
  - It should **not** add a comma after the last element.
  - The correct condition is `k != sizeOfList - 1`.

### **Example Case**
For `listOfWords = ["one", "two", "three"]`, the expected output:
```java
"{one, two, three}"

```

## Question 39

## **Question Analysis**
The given Java code manipulates an `ArrayList<String>` and uses the `set()` method, which:
- Replaces an element at a specific index and returns the **previous value**.

### **Code Breakdown**
```java
List<String> students = new ArrayList<>();
students.add("Alex");
students.add("Bob");
students.add("Carl");

for (int k = 0; k < students.size(); k++) {
    System.out.print(students.set(k, "Alex") + " ");  // Prints previous values
}

System.out.println();

for (String str : students) {
    System.out.print(str + " "); // Prints final list
}
```

## Step-by-Step Execution

First Loop Output (students.set(k, "Alex"))

students.set(0, "Alex") returns "Alex" → prints "Alex" <br>
students.set(1, "Alex") returns "Bob" → prints "Bob"<br>
students.set(2, "Alex") returns "Carl" → prints "Carl" <br>

 First printed line: "Alex Bob Carl"

Second Loop Output

The list is now ["Alex", "Alex", "Alex"]

 Second printed line: "Alex Alex Alex"



### **Key Areas to Improve & Action Plan**  

#### **1️⃣ Sorting Algorithms (Insertion & Selection Sort)**  
- Dry-run each step manually to track element shifts.  
- Implement sorting in code and print the array after each pass.  

#### **2️⃣ 2D Arrays & Indexing**  
- Predict whether a method returns a value, row index, or column index.  
- Debug nested loops by tracking variable updates at each step.  

#### **3️⃣ String Manipulation**  
- Practice `substring()` for first/second halves of words.  
- Handle odd-length words properly when recombining.  

#### **4️⃣ ArrayList Methods (`set()`, `get()`)**  
- Understand `set()` returns the old value and modifies the list.  
- Predict list changes before running code.  

#### **5️⃣ Debugging & Logical Flow**  
- Use print debugging to track variable updates in loops.  
- Write edge cases before coding (empty arrays, single elements, duplicates).  

