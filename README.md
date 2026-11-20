# EXPERIMENT 6: AI-Assisted Programming and Debugging


### Name: Antony Aswin Kumar L
### Register no. 212225040024

---

# AIM

Write and implement programs using AI tools to generate, analyse, debug, optimize and test code, and compare the quality of AI-assisted programming with conventional programming.

---

# AI TOOLS REQUIRED

* ChatGPT
* Google Gemini
* GitHub Copilot

---

# EXPLANATION

Experiment with AI tools as programming assistants for developing applications in different programming languages.

The experiment focuses on using AI for:

* Python programming
* C programming
* Java programming

using AI assistance.

Then:

* Identify programming errors
* Debug incorrect programs
* Optimize code
* Analyse time and space complexity
* Generate unit tests
* Compare manual programming with AI-assisted programming
* Evaluate overall code quality

**Deliverable:** Code quality analysis.

---

# AI-ASSISTED PROGRAMMING AND DEBUGGING

## OBJECTIVE

To use multiple AI tools as programming assistants for generating, analysing, debugging, optimizing and testing programs.

The experiment focuses on comparing AI-generated programs based on correctness, efficiency, readability, maintainability and code quality.

---

# TOOLS USED

| **Tool**       | **Purpose**                                |
| -------------- | ------------------------------------------ |
| ChatGPT        | Code generation, debugging and explanation |
| Google Gemini  | Alternative code generation and comparison |
| GitHub Copilot | Code suggestions and optimization          |
| Python         | Programming and automation                 |
| C              | AI-assisted programming                    |
| Java           | AI-assisted programming                    |

---

# EXERCISE DESCRIPTION

The experiment is carried out using multiple AI programming tools.

The following activities are performed:

1. Generate Python code using AI.
2. Generate C code using AI.
3. Generate Java code using AI.
4. Compare generated programs from different AI tools.
5. Identify bugs in AI-generated code.
6. Correct the identified errors.
7. Optimize an existing program.
8. Analyse time and space complexity.
9. Generate unit test cases.
10. Compare manual coding with AI-assisted coding.
11. Analyse overall code quality.

---

# 1. PYTHON PROGRAMMING

## Prompt

> Act as a Python programmer. Generate a Python program that accepts marks of multiple subjects, calculates the total and average, and assigns a grade based on the average. Provide clean and readable code and explain its complexity.

## AI-Generated Code

```python
marks = [85, 78, 92, 74, 88]

total = sum(marks)
average = total / len(marks)

if average >= 90:
    grade = "A+"
elif average >= 80:
    grade = "A"
elif average >= 70:
    grade = "B"
elif average >= 60:
    grade = "C"
else:
    grade = "D"

print("Total Marks:", total)
print("Average:", average)
print("Grade:", grade)
```

## Output

```text
Total Marks: 417
Average: 83.4
Grade: A
```

## Analysis

The Python program stores the marks of different subjects in a list.

The `sum()` function calculates the total marks, while the length of the list is used to calculate the average.

The program then uses conditional statements to assign a grade according to the average score.

## Complexity

* **Time Complexity:** O(n), where n is the number of subjects.
* **Space Complexity:** O(n), because the marks are stored in a list.

---

# 2. C PROGRAMMING

## Prompt

> Act as a C programmer and generate a simple program that accepts an integer and determines whether the number is a palindrome.

## AI-Generated Code

```c
#include <stdio.h>

int main()
{
    int n, original, reversed = 0, remainder;

    printf("Enter a number: ");
    scanf("%d", &n);

    original = n;

    while (n != 0)
    {
        remainder = n % 10;
        reversed = reversed * 10 + remainder;
        n = n / 10;
    }

    if (original == reversed)
        printf("Palindrome number");
    else
        printf("Not a palindrome number");

    return 0;
}
```

## Output

```text
Enter a number: 1221
Palindrome number
```

## Analysis

The AI-generated C program reverses the digits of the input number.

Each digit is obtained using the modulus operator. The reversed number is constructed by repeatedly multiplying the current reversed value by 10 and adding the extracted digit.

Finally, the reversed number is compared with the original number.

## Complexity

* **Time Complexity:** O(d), where d is the number of digits.
* **Space Complexity:** O(1)

---

# 3. JAVA PROGRAMMING

## Prompt

> Act as a Java programmer and generate a program that accepts an array of integers and calculates its minimum, maximum and average values.

## AI-Generated Code

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] numbers = new int[n];

        System.out.println("Enter the elements:");

        for (int i = 0; i < n; i++) {
            numbers[i] = sc.nextInt();
        }

        int min = numbers[0];
        int max = numbers[0];
        int sum = 0;

        for (int number : numbers) {

            if (number < min)
                min = number;

            if (number > max)
                max = number;

            sum += number;
        }

        double average = (double) sum / n;

        System.out.println("Minimum: " + min);
        System.out.println("Maximum: " + max);
        System.out.println("Average: " + average);

        sc.close();
    }
}
```

## Output

```text
Enter number of elements: 5
Enter the elements:
12
25
8
31
19

Minimum: 8
Maximum: 31
Average: 19.0
```

## Analysis

The program accepts an integer array from the user.

It traverses the array once and simultaneously calculates the minimum value, maximum value and total sum.

The average is calculated by dividing the sum by the number of elements.

## Complexity

* **Time Complexity:** O(n), where n is the number of elements.
* **Space Complexity:** O(n), because the array stores n values.

---

# 4. BUG IDENTIFICATION AND DEBUGGING

## Prompt

> Identify the error in the following Python program, explain why the incorrect result occurs and provide a corrected version.

## Buggy Code

```python
marks = [70, 80, 90, 60]

total = 0

for mark in marks:
    total = mark

average = total / len(marks)

print("Average:", average)
```

## AI-Generated Analysis

The error occurs because the program assigns each mark directly to `total`.

Instead of adding each mark to the previous total, the statement:

```python
total = mark
```

replaces the previous value.

Therefore, after the loop finishes, `total` contains only the last mark.

The correct operation is:

```python
total = total + mark
```

or:

```python
total += mark
```

## Corrected Code

```python
marks = [70, 80, 90, 60]

total = 0

for mark in marks:
    total += mark

average = total / len(marks)

print("Average:", average)
```

## Output

```text
Average: 75.0
```

## Result of Debugging

The logical error was identified and corrected.

The program now adds all marks before calculating the average instead of retaining only the final mark.

---

# 5. CODE OPTIMIZATION

## Original Code

```python
def fibonacci(n):
    if n <= 1:
        return n

    return fibonacci(n - 1) + fibonacci(n - 2)

print(fibonacci(10))
```

## Prompt

> Optimize the following Python Fibonacci program to improve its efficiency while keeping the same output. Use a simple and readable approach and explain the complexity.

## Optimized Code

```python
def fibonacci(n):

    if n <= 1:
        return n

    a = 0
    b = 1

    for _ in range(2, n + 1):
        a, b = b, a + b

    return b

print(fibonacci(10))
```

## Output

```text
55
```

## Analysis

The original recursive implementation repeatedly calculates the same Fibonacci values.

This results in a large number of unnecessary function calls.

The optimized version uses an iterative approach and stores only the two previous values.

Therefore, the optimized implementation is significantly more efficient for larger values of `n`.

* **Original Time Complexity:** O(2^n)
* **Optimized Time Complexity:** O(n)
* **Optimized Space Complexity:** O(1)

---

# 6. UNIT TEST GENERATION

## Prompt

> Generate unit test cases for a Python function that converts a temperature from Celsius to Fahrenheit.

## Function

```python
def celsius_to_fahrenheit(celsius):
    return (celsius * 9 / 5) + 32
```

## Unit Tests

```python
def test_freezing_point():
    assert celsius_to_fahrenheit(0) == 32

def test_boiling_point():
    assert celsius_to_fahrenheit(100) == 212

def test_room_temperature():
    assert celsius_to_fahrenheit(25) == 77

def test_negative_temperature():
    assert celsius_to_fahrenheit(-10) == 14
```

## Test Cases

| **Test Case**        | **Input** | **Expected Output** |
| -------------------- | --------- | ------------------- |
| Freezing point       | `0`       | `32`                |
| Boiling point        | `100`     | `212`               |
| Room temperature     | `25`      | `77`                |
| Negative temperature | `-10`     | `14`                |

## Output

```text
All test cases passed successfully.
```

## Result

Unit tests were successfully generated using AI to verify the temperature conversion function with positive, negative and standard reference values.

---

# 7. MANUAL CODING VS AI-ASSISTED CODING

| **Criteria**         | **Manual Coding**                    | **AI-Assisted Coding**                |
| -------------------- | ------------------------------------ | ------------------------------------- |
| Code Generation      | Written entirely by programmer       | AI generates an initial solution      |
| Development Speed    | Usually slower                       | Generally faster                      |
| Error Identification | Programmer identifies errors         | AI can identify common errors         |
| Debugging            | Requires manual investigation        | AI suggests possible corrections      |
| Optimization         | Programmer develops improvements     | AI can suggest alternative approaches |
| Complexity Analysis  | Calculated by programmer             | AI can explain complexity             |
| Unit Testing         | Test cases written manually          | AI can generate test cases            |
| Code Explanation     | Programmer analyses the code         | AI can explain generated code         |
| Learning             | Requires independent practice        | AI provides additional guidance       |
| Verification         | Programmer checks the implementation | Human verification remains necessary  |

---

# 8. CODE QUALITY ANALYSIS

The generated programs were analysed based on the following factors:

| **Factor**       | **Analysis**                                          |
| ---------------- | ----------------------------------------------------- |
| Correctness      | Programs generally produced the expected results      |
| Readability      | AI-generated code was relatively simple to understand |
| Efficiency       | AI suggested improved approaches for inefficient code |
| Debugging        | Logical errors were identified and corrected          |
| Testing          | AI generated multiple test scenarios                  |
| Maintainability  | Structured programs were easier to modify             |
| Development Time | AI assistance reduced initial implementation time     |
| Explanation      | AI provided explanations of program functionality     |
| Complexity       | Time and space complexity could be analysed using AI  |

The outputs generated by different AI tools can be compared based on correctness, readability, efficiency, completeness and usefulness.

---

# CONCLUSION

The experiment demonstrated the use of AI tools for programming, debugging, optimization and testing.

Python, C and Java programs were generated using AI assistance and analysed for their functionality and complexity.

A logical error in a Python program was identified and corrected using AI. An inefficient recursive Fibonacci implementation was also optimized using an iterative approach.

Unit test cases were generated for a temperature conversion function to verify its behaviour under different inputs.

The comparison between manual coding and AI-assisted coding showed that AI can reduce development time, suggest alternative solutions and help programmers identify common errors.

However, AI-generated code should always be reviewed, tested and verified by the programmer before being used in a real application.

---

# RESULT

The corresponding prompts were successfully executed using AI-assisted programming tools. Programs were generated, analysed, debugged, optimized and tested successfully.
