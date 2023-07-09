# Binary Search Deep Dive

Binary Search is an efficient search algorithm that finds the position of a target value within a sorted array. It compares the target value to the middle element of the array; if they are unequal, the half in which the target cannot lie is eliminated, and the search continues on the remaining half until it is successful or the remaining half is empty. Here are the basic steps:

## 1. Find the Middle Element

Find the middle element of the array. If the array has an even number of elements, the middle element will be the higher of the two, i.e., `array.length / 2`.

## 2. Compare Middle Element and Target

Compare the middle element with the target value. There are three cases:

- If the middle element equals the target, then the search is done; return the index of the middle element.

- If the middle element is greater than the target, then the target must lie in the first half of the array.

- If the middle element is less than the target, then the target must lie in the second half of the array.

## 3. Repeat on the Subarray

Repeat the process on the new half-array. The new array should be from the start of the array to the middle element if the middle element is greater than the target, and from the middle element to the end of the array if the middle element is less than the target.

Here's a brief example of how binary search works:

**Input**: `[1, 3, 4, 6, 8, 9, 11, 13, 14, 15]`, Target: `11`

1. **Find the Middle Element**: The middle element is `8`.

2. **Compare Middle Element and Target**: The target `11` is greater than `8`, so we now consider the second half of the array: `[9, 11, 13, 14, 15]`.

3. **Repeat on the Subarray**: Again find the middle element (`13`), compare it to the target, and consider the first half of the new subarray: `[9, 11]`. Repeat this process until you find the target `11`.

Binary Search is efficient with a time complexity of `O(log n)`, but it requires the input to be sorted beforehand.

For your practice exercise, implement Binary Search in a language of your choice and run it on a few test cases to ensure it's working correctly. Test cases could be simple sorted arrays of numbers. Ensure you test edge cases such as an array with one element, an empty array, and an array with duplicate values.
