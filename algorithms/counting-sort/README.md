# Counting Sort

Counting Sort is a sorting algorithm that sorts elements based on the count of individual elements present in the array. It works by counting the number of objects having distinct key values, and applying arithmetic to calculate the position of each object in the output sequence. Here are the basic steps:

## 1. Count Elements

First, count the occurrence of each element in the input array, and store it in a separate 'count' array. This count array's size should be equal to the range of the input values (max - min + 1).

## 2. Update Count Array

Next, transform the count array such that each element at each index stores the sum of previous counts. Each index of the array now represents the cumulative count of the elements up to that point.

## 3. Place Elements in Output Array

For each element in the input array, go to its corresponding index in the count array, and place it in the output array. Decrease the count by one each time an element is placed in the output.

## 4. Copy Back to Original Array

Finally, copy the sorted elements from the output array back to the original array.

Here's a brief example of how counting sort works:

**Input**: `[1, 4, 1, 2, 7, 5, 2]`

1. **Count Elements**: The count array would look like this: `[0, 2, 2, 0, 1, 1, 0, 1]` (index 0 has count 0, index 1 has count 2, index 2 has count 2, etc.)

2. **Update Count Array**: Update the count array: `[0, 2, 4, 4, 5, 6, 6, 7]`

3. **Place Elements in Output Array**: Each element in the original array is placed in the sorted output array based on the counts in the count array: `[1, 1, 2, 2, 4, 5, 7]`

4. **Copy Back to Original Array**: The original array becomes: `[1, 1, 2, 2, 4, 5, 7]`

Counting Sort is an efficient algorithm for sorting an array of elements that are known to fall within a certain range, and it is extremely efficient when the range of potential items in the input is approximately equal to the number of items in the input.

For your practice exercise, you could implement Counting Sort in a language of your choice and run it on a few test cases to ensure it's working correctly. Test cases could be simple arrays of numbers. Ensure you test edge cases such as an already sorted array, a reversely sorted array, and an array with duplicate values.
