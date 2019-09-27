# Lab 3: Basic Sorting Algorithms

## Introduction

To become more familiar with basic sorting algorithms and input types, this week you will be testing some algorithms you write yourselves.
More specifically, you will be implementing the Insertion and Bubble Sort algorithms you learned about in class, and benchmarking them against the standard Python library's sorting algorithm.

**Be sure to read this lab's instructions extra carefully**, as you may be unfamiliar with some of the concepts.

Other things to note about this lab:

1. The content of the lists passed into each of your algorithms should be exactly the same (not just the same length).
2. If your sorting algorithms work **in-place**, you must be sure to avoid *accidentally* passing in an already sorted list.
3. (**Important**) You **may not** use the slides or any online resources to guide your implementation, instead you should come up with the algorithms based on your understanding of how the insertion and bubble sort algorithms work.

## Inputs

The performance of an algorithm can depend greatly on the type of input it receives.
In fact, most professional sorting algorithms are *hybrid* algorithms, which use different routines depending on the size of the input.
As you've seen, even algorithms that grow in complexity faster than others can be more effective on small input sizes.
Along with input size, as a programmer, you should also consider what state the input will be in on arrival; i.e. is there a chance it is already sorted? Partially sorted?

Generally, these different scenarios will be referred to as **best case**, **average case**, and **worst case**.
To explore this topic further, today you will examine what happens to the runtime of your sorting algorithms given a variety of inputs:

- Random Unsorted List
- Already Sorted List
- Reverse Sorted List
- Partially Sorted List

Each of the above list types is exactly what you would expect (Reverse Sorted List are lists in reverse order, for example) except, perhaps, for partially sorted lists.
A partially sorted list has a definition which is a bit more complicated, but for the purpose of this lab a partially sorted list is one which requires **at most** n swaps to sort, where n is the length of the list.
In other words, the number of *inversions* in the list is at most n.

## Starter Code

If you take a look into the starter code for the lab, you will find a lot of the code has already been written!
To make this a bit less intimidating, here is a rough breakdown of the code:

### Sorting Functions

The functions used for sorting in this lab are as follows:

`def int_sort(arr: list) -> list` Performs insertion sort on the given list, returning a sorted list.

`def bub_sort(arr: list) -> list` Performs bubble sort on the given list, returning a sorted list.

`void python_sort(arr: list) -> list` Uses the standard Python sorting algorithm (Timsort), returning a sorted list.

### Input Generating Functions

The functions for creating lists of different types are as follows:

`def gen_list_unsorted(size: int) -> list` Creates and returns a random, unsorted list.

`def gen_list_sorted(size: int) -> list` Creates and and returns a random, sorted list.

`def gen_list_reversed(size: int) -> list` Creates and returns a list in sorted, reversed order.

`def gen_list_partial_sorted(size: int) -> list` Creates and returns a partially sorted list.

Here, `size` is the length of the list to be generated, but it also specifies the bounds for the random values in the list (`[-size, size]`).

> All of the functions in this section are already completed, and ready to be used.

### Unit Testing

Also within the starter code, is a testing class (`class Tests`), which you can use to test your code.

> Adding unit tests is not mandatory, but it is highly encouraged.

### `main()`

Inside of main we have provided you with a list of algorithm names, a list of input types, the input size you should use, and a dictionary that allows you to call the list generating functions a bit more concisely.

## Instructions

For each sorting algorithm, do the following:

1. Consider the problem.
2. Work through the algorithm on paper.
3. Write pseudocode.
4. [Recommended] Implement unit tests.
5. Implement the algorithm to pass the unit tests.

Once you've written all three of the sorting functions, you can begin working on the `main` function.

1. Consider the table you are required to make.
2. Write pseudocode to solve the problem.
3. Check, does your pseudocode use the **exact** same input list for each algorithm? (remember: [1, 3, 2, 4] != [1, 2, 3, 4]; Do not accidentally use an already sorted array if the desired input type is not sorted!)
4. Implement your pseudocode.
5. Test your implementation, revise your code as necessary.

## Questions

Once all of your code is complete, answer the following questions.

### Question 1

On which type(s) of input did insertion sort perform best? On which type(s) did it perform worst?

### Question 2

What was the overall difference between insertion sort's best input and its worst input? (no need for numbers on this question, just describe the difference the two input types made).

### Question 3

On which type(s) of input did bubble sort perform best? On which type(s) did it perform worst?

### Question 4

What was the overall difference between bubble sort's best input and its worst input?

### Question 5

How do the insertion sort and bubble sort compare with the Python's built-in sorting function?

## Submission

You will submit 2 text files named lab.py and lab.txt on Gradescope by the end of your lab session.

Please ensure your files contain the following:

1. lab.py should contain your entire source code
2. lab.txt should contain the table (running times) generated by your program, and the answers to the above questions.
