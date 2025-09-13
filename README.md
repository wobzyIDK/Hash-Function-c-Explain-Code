# Top N Numbers Finder

A simple C++ program that reads a list of integers and finds the top `m` largest numbers using a **presence array** (similar to counting sort). This approach is fast for small or moderate ranges of integers and demonstrates a memory-efficient method for sorting and selecting numbers without using standard sorting algorithms.

---

## Features

- Reads `n` integers from input.
- Finds the top `m` largest numbers.
- Uses a presence array for fast lookup and selection.
- Handles negative and positive numbers.
- Simple, easy-to-understand code.

---

## How It Works

1. The program initializes a large array to record the presence of numbers.
2. Each input number is mapped to the array using an offset to handle negative numbers.
3. The program then scans the array from the largest index to the smallest, printing numbers until `m` numbers are found.

This is effectively a **specialized counting sort** for selecting the largest numbers.

---

## Example Usage

### Input
5 3
1 7 -2 4 7


- `5` → number of integers (`n`)  
- `3` → number of largest numbers to output (`m`)  
- `1 7 -2 4 7` → list of integers  

### Output


7 4 1


---

### Another Example

#### Input


6 2
-1 0 5 3 2 -1


#### Output


5 3


---

## How to Run

1. Save the program as `top_n_numbers.cpp` (or `crack.cpp`) on your computer.
2. Compile using a C++ compiler:
```bash
g++ -std=c++17 top_n_numbers.cpp -o top_n_numbers


Run the program:

./top_n_numbers


Enter your input in the terminal as shown in the examples above.

Notes

Make sure the array size (MAXN) and offset are set appropriately to cover the full range of your input numbers.

For extremely large or sparse ranges of numbers, a hash map or standard sorting algorithm may be more memory-efficient.
