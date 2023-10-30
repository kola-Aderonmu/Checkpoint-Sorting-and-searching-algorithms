# Checkpoint-Sorting-and-searching-algorithms

## Insertion Sort Algorithm Readme file

#### Overview:

Insertion Sort is a simple sorting algorithm that builds the final sorted array one item at a time. It is much less efficient on large lists than more advanced algorithms.

#### Procedure: insertionSort(arr: array)

1. **Input:** Takes an array `arr` as input.
2. **Initialization:** Get the length of the array, `n = length(arr)`.
3. **Sorting Loop:** Iterate over the array starting from index 1 to n - 1.
   - **Call:** For each iteration, call the `insertElement` procedure.

#### Procedure: insertElement(arr: array, currentIndex: integer)

1. **Input:** Takes the array `arr` and the current index `currentIndex`.
2. **Key Element:** Set `key` as the element at the current index (`arr[currentIndex]`).
3. **Comparison and Shifting Loop:**
   - Initialize `j` as `currentIndex - 1`.
   - While `j` is greater than or equal to 0 and `key` is less than the element at index `j`:
     - Shift the element at index `j` to the next position (`arr[j + 1] = arr[j]`).
     - Decrement `j`.
   - Insert the `key` at the correct position (`arr[j + 1] = key`).

#### Example:

Consider the array `arr = [5, 2, 9, 1, 5]`.

1. In the first iteration, `insertElement` is called with `key = 2` (at index 1).
2. It finds the correct position for `2` in the sorted sequence `[5]` and updates the array to `[2, 5, 9, 1, 5]`.
3. The process repeats for each element, resulting in the sorted array `[1, 2, 5, 5, 9]`.















#### Complexity:

- **Time Complexity:** O(n^2) - Quadratic time complexity.
- **Space Complexity:** O(1) - Constant space complexity.

#### Note:

This algorithm efficiently builds the sorted sequence by iteratively inserting each element into its correct position, making it suitable for small datasets. However, its efficiency decreases for larger datasets compared to more advanced sorting algorithms.
