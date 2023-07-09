# Quick Sort

Quick Sort is a divide-and-conquer algorithm that works by selecting a 'pivot' element from the array and partitioning the other elements into two sub-arrays, according to whether they are less than or greater than the pivot. The sub-arrays are then recursively sorted. Here are the basic steps:

## 1. Pick a Pivot

First, we choose a "pivot" item in our array. This pivot will be used to split the array into two parts. The pivot selection can be done in various ways: it could be the first element, the last element, or a random element. Sometimes, the median value becomes a pivot.

## 2. Partition

Next, we partition the remaining elements into two subarrays. Elements less than the pivot go to the left subarray and elements greater than the pivot go to the right subarray.

This step involves moving around elements in place. We start two indices - one from the start of the array and one from the end of the array. We move the indices inward until the values at the indices need to be swapped (i.e., the value at the left index is greater than the pivot and the value at the right index is less than the pivot). Then, we swap these values and continue moving the indices inward. This continues until the indices cross. At that point, we move the pivot value to its final location - to the right of the left subarray and to the left of the right subarray.

## 3. Recur

Finally, we recursively apply the same strategy to the subarrays. Each subarray excludes the pivot element because we know the pivot is already in its final sorted position.

Here's a brief example of how quick sort works:

**Input**: `[9, 7, 5, 11, 12, 2, 14, 3, 10, 6]`

1. **Pick a pivot**: Let's say we pick 10 as the pivot.

2. **Partition**: The partition step will look like this:

   `[9, 7, 5, 6, 2, 3]` `10` `[11, 12, 14]`

   All elements to the left of 10 are less than 10 and all elements to the right are greater than 10.

3. **Recur**: Recursively apply quick sort on the two sub-arrays:

   `[5, 6, 2, 3, 7, 9]` `10` `[11, 12, 14]`

   The final sorted array is: `[2, 3, 5, 6, 7, 9, 10, 11, 12, 14]`
