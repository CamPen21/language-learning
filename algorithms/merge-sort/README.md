# Merge Sort

Merge Sort is a divide-and-conquer algorithm that follows these steps:

## 1. Divide

If the list is of length 0 or 1, then it is already sorted. Otherwise, divide the unsorted list into two sublists of about half the size.

## 2. Conquer (Sort)

Recursively sort each sublist. This is where the divide-and-conquer strategy comes in. Each sublist is further divided into smaller sublists until there is only one element left in the sublist (a list with one element is considered sorted).

## 3. Combine (Merge)

Merge the two sublists back into one sorted list. This is done by repeatedly taking the smallest remaining item among the sorted sublists and adding it to a new list, until all items have been readded. This new list will be sorted.

Here is a quick example of how merge sort works:

**Input**: `[38, 27, 43, 3, 9, 82, 10]`

1. **Divide**: Split the list into two: `[38, 27, 43]` and `[3, 9, 82, 10]`
2. Recursively apply merge sort on these smaller lists:
   - `[38, 27, 43]` gets split into `[38]` and `[27, 43]`, which gets split further into `[27]` and `[43]`.
   - `[3, 9, 82, 10]` gets split into `[3, 9]` and `[82, 10]`, which get split further into `[3]`, `[9]`, `[82]` and `[10]`.
3. **Merge**: The sublists are then merged back together in sorted order:
   - `[27]` and `[43]` merge to form `[27, 43]`.
   - `[38]` and `[27, 43]` merge to form `[27, 38, 43]`.
   - `[3]` and `[9]` merge to form `[3, 9]`.
   - `[82]` and `[10]` merge to form `[10, 82]`.
   - `[3, 9]` and `[10, 82]` merge to form `[3, 9, 10, 82]`.
   - Finally, `[27, 38, 43]` and `[3, 9, 10, 82]` merge to form `[3, 9, 10, 27, 38, 43, 82]`, which is the sorted version of the original list.
