# Bucket Sort

Bucket Sort is a distribution sort algorithm that works by distributing the elements of an array into a number of buckets, and then sorting these buckets individually. Each bucket is then sorted individually, either using a different sorting algorithm, or by recursively applying the bucket sort algorithm. Here are the steps of the Bucket Sort algorithm:

## 1. Create Buckets

First, initialize an array of empty buckets. You can either choose a fixed number of buckets, or calculate the number based on the input data.

## 2. Distribute Input Elements

Next, iterate over the original array, putting each object in its respective bucket. The distribution can be performed using the characteristics of the items, such as their value or some other property.

## 3. Sort Buckets Individually

Then, sort each non-empty bucket. This can be done using any sorting algorithm, even another bucket sort.

## 4. Gather Elements from Buckets

Finally, gather elements from the buckets, placing them back to the original array. This step is done by iterating over the buckets in order and inserting all elements into the original array.

Here's a brief example of how bucket sort works:

**Input**: `[0.9, 0.1, 0.6, 0.7, 0.6, 0.3, 0.1]`

1. **Create Buckets**: Let's say we choose to have 10 buckets, each represented by a decimal point ranging from 0 to 1 (0.1, 0.2, 0.3, etc.). So, we create 10 empty buckets.

2. **Distribute Input Elements**: We distribute the elements in the array to their respective buckets: `0.1` goes to the first bucket, `0.6` goes to the sixth bucket, `0.9` goes to the ninth bucket, and so on.

3. **Sort Buckets Individually**: Sort each bucket. In our case, the contents of each bucket is either empty or has one element, so they are already sorted.

4. **Gather Elements from Buckets**: Now, we gather the elements, leading to a sorted array: `[0.1, 0.1, 0.3, 0.6, 0.6, 0.7, 0.9]`.

Note: Bucket Sort is mainly useful when the input is uniformly distributed over a range. It's also worth mentioning that the performance of Bucket Sort depends on the number of buckets we choose - we can end up with a scenario where all or most elements are placed in a single bucket, causing the complexity to degenerate to that of the sorting algorithm used to sort individual buckets.

For your practice exercise, you could implement Bucket Sort in a language of your choice and run it on a few test cases to ensure it's working correctly. Test cases could be simple arrays of numbers or strings. Ensure you test edge cases such as an already sorted array, a reversely sorted array, and an array with duplicate values.
