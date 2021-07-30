---
title: 1. Loops
type: labs
---

# Loops Lab
In this lab, we will learn how to make the computer do the same instruction over and over. 
To get started, let's talk about how the code we've written works in your computer.

When you want to run the same code multiple times, we use loops.
How does a loop work in python? Let's see.

{{< code-action >}} Clone the directory for this lab into your `mims_bootcamp`
directory:

```shell
git clone TODO
```

## A. Calculations
Let's start by performing some calculations for many numbers.

 {{< code-action >}} **Type** this starter code at `YOUR CODE HERE (B)`.

```python
# B. Calculations
for i in range(10):
    print(i)
```

### A.0 *Listing numbers*
{{< code-action >}} Run your program and see what gets output.

This loop runs 10 times, repeating everything indented to the right of the `for i in range(10):` line.
`i` is a variable that gets incremented by one every time the loop runs.

### A.1 *Listing more numbers*
{{< code-action >}} Edit the code to make the loop run a different number of times, maybe 5 or 14.
Can you figure out how to do it?

Notice that the count inside `i` starts at 0 and goes up to the number inside `range()` but
doesn't include that number.

### A.2 *Squaring numbers*
{{< code-action >}} Finally, edit the code to make the loop print out the square of every number
from 0 to 12. When you run your program, the output should look like this:

```shell
$ python lab_02.py
0
1
4
9
16
25
36
49
64
81
100
121
```

{{< aside >}}
If you don't want code to be executed when you run a program, you can comment it
out by placing `#` at the beginning of the line.

If you don't wan't to run the code you wrote in the first part of the lab, just
comment it out.
{{< /aside >}}

## B. Geometric sequences
Loops are particularly useful when we need to do things over time. To see this,
let's use a loop to list out the first 10 terms in a geometric sequence.

{{< aside >}}
Sequences are ordered collections of numbers that have a pattern to determine
which numbers appear in the sequence. For example, `2, 4, 6, 8, 10,...` is a
sequence where each number 2 more than the previous number.

Geometric sequences are sequences where there is a common ratio between each
number in the sequence. For example, `3, 9, 27, 81,...` is a geometric sequence
where each number is 3 times the number before it (making the common ratio 3).
{{< /aside >}}

{{< code-action >}} **Type** this code  at `YOUR CODE HERE (C)`.

```python
# B. Geometric sequences
ratio = float(input("What should the ratio of the sequence be? "))
curr = 1
print(curr)
```

### B.0 *Pseudocode*
{{< write-action >}} To get started, think through the *pseudo-code*
of what we want this program to do. *Pseudocode* is an outline of the program
we'll ultimately write where we don't worry about using Python syntax.

Here are some things to consider:
- You will use a loop to calculate each term in the sequence. What is the formula
you will use at each step in the loop to calculate the term?
- You will need to know the previous term to calculate the current term. How will
you keep track of this?

### B.1 *Code*
After you are confident your pseduocode has the correct logic, translate it into
python code. Type this code below the existing code in the `C. Sequences` section.

## C. Fibonacci
Let's explore another sequence, the Fibonacci sequence. This sequence has all kinds
of interesting properties.

{{< look-action >}} Watch this video about how the Fibonacci sequence appears in
nature:
{{< youtube id="ahXIMUkSXX0" >}}

We're going to write an algorithm to print out numbers in the Fibonnaci sequence.
{{< code-action >}} **Type** this code  at `YOUR CODE HERE (D)`.

```python
# C. Fibonacci
num_terms = int(input("How many terms of the fibonacci sequence should I display? "))
```

### C.0 *Pseudocode*
{{< write-action >}} Just like you did with the geometric series algorithm, think
through the pseudo-code of what we want the Fibonacci sequence algorithm to do.

Here are some things to consider:
- Your algorithm should print out the number of terms inputed by the user and
stored in `num_terms`.
- Just like before, you will need a way to track the previous terms of the sequence,
but this time you need two past terms instead of just one.

### C.1 *Code*
{{< code-action >}} After you are confident your pseduocode has the correct logic, translate it into
python code. Type this code below the existing code in the `D. Fibonacci` section.

{{< checkpoint >}}
Answer the following check-in questions on your group's Google doc before moving on:

0. What is a loop?
0. How do you put code into a loop?
0. What changes over each iteration of a loop? What stays the same?
{{< /checkpoint >}}

## D. Loopy drawings
Loops are not just useful for numbers and sequences, they can also be helpful in
making drawings. Any time your code does the same thing multiple times, you can
use a loop to make it simplier and more powerful.

Take a look at the code we've been using to draw a square:

```python
forward(100)
right(90)
forward(100)
right(90)
forward(100)
right(90)
forward(100)
right(90)
```

Pretty repetitive, right?

{{< code-action >}} Edit this code to use a loop to avoid repeating the same code over and over
again.  **Type** this code  at `YOUR CODE HERE (E)`.

## E. Variable drawings
Loops are even more powerful drawing tools when paired with variables. This allows us to draw
things differently over time or based on user input.

{{< code-action >}} **Type** this code  at `YOUR CODE HERE (F)`.

```python
# E. Variable drawings
num_sides = int(input("How many sides? "))
```

{{< code-action >}} Write a loop that draws a polygon with the number of sides
stored in `num_sides`. Type this code below the existing code in the
`E. Variable Drawing` section.

## F. Drawing Fibonacci
Finally, let's use the code you wrote to calculate Fibonacci sequences to make pattern
drawings inspired by flowers and pinecones.

{{< figure src="images/courses/cs9/unit00/00_variables_pinecone.png" title="Fibonacci drawing" >}}

### F.0 One spiral
First, use your Fibonacci code to draw a single spiral. You can do this by drawing a
line for each number in the Fibonacci sequence and connecting the lines at a standard angle.

{{< code-action >}} Write this code at `YOUR CODE HERE (G)`.

The Turtle should draw something like this:

{{< figure src="images/courses/cs9/unit00/00_variables_spiral.png" title="Fibonacci spiral" >}}

### F.1 Multiple spirals
{{< code-action >}} Now, loop your code in `G. Drawing Fibonacci` to draw multiple spirals originating from the
center.

Now, the Turtle should draw something like this:

{{< figure src="images/courses/cs9/unit00/00_variables_vortex.png" title="Many spirals" >}}

{{< aside >}}
You can return your turtle to the center of the window using `goto(0, 0)`. If you want,
you can use `penup()` and `pendown()` to keep the turtle from drawing as it returns to the
center.
{{< /aside >}}

### F.2 Clockwise and counterclockwise
To get a pinecone or flower effect like the video above described, you'll need to spiral clockwise
and countercloackwise.

{{< code-action >}} Repeat your spiral code, changing it to make your spirals turn in the other direction.

## Deliverables
- Once you've reached the end of the lab (or class time is over), please submit the `lab_02.py` file you have been creating
- Each member of your group should submit their own file.
- You will get credit even if you don't finish parts A-F.
