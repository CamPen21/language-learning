# Heap Sort

Heap Sort is a comparison-based sorting algorithm that leverages a data structure called a heap. A heap is a complete binary tree where each parent node is less than or equal to its child node (min-heap) or where each parent node is greater than or equal to its child node (max-heap). Here are the steps of the Heap Sort algorithm:

## 1. Build a Heap

First, transform the input array into a heap. A heap is a binary tree where each parent node is greater (max heap) or less (min heap) than its children nodes. In the context of Heap Sort, we typically use a max heap to sort in ascending order.

## 2. Delete the Root

Next, continually remove the root node (which is the maximum element in a max heap), and place it in the sorted section of the array. This removal must be done while maintaining the heap property.

## 3. Heapify

After removing the root node, you must "heapify" the tree, which means rearranging it to maintain the heap property (i.e., ensuring the parent node is always greater than its child nodes in a max heap).

## 4. Repeat

The process of removing the root and heapifying is repeated until the heap is empty. The resulting array will be sorted in ascending order.

Here's a brief example of how heap sort works:

**Input**: `[12, 11, 13, 5, 6, 7]`

1. **Build a Heap**: Convert the original array into a max heap. The array representation will look like this: `[13, 11, 12, 5, 6, 7]`.

2. **Delete the Root and Heapify**: The root (which is `13`, the maximum element) is moved to the end of the array, and the rest of the array is heapified. The array looks like this: `[12, 11, 7, 5, 6]` and `[13]`.

3. **Repeat**: Repeat the process. The root (`12`) is moved to the end of the array, and the rest of the array is heapified: `[11, 6, 7, 5]` and `[12, 13]`. This process continues until the array is fully sorted: `[5, 6, 7, 11, 12, 13]`.

Your task for the practice exercise would be to implement Heap Sort and run it on several test cases to ensure it's working correctly. Ensure you test edge cases such as an already sorted array, a reversely sorted array, and an array with duplicate values.
