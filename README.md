# Merge-Sort
The merge() function is used for merging two halves. The merge(arr, l, m, r) is a key process that assumes that arr[l..m] and arr[m+1..r] are sorted and merges the two sorted sub-arrays into one. See the following C implementation for details.


## Algorithm
Conceptually, a merge sort works as follows:

Divide the unsorted list into n sublists, each containing one element (a list of one element is considered sorted).
Repeatedly merge sublists to produce new sorted sublists until there is only one sublist remaining. This will be the sorted list.
Top-down implementation
Example C-like code using indices for top-down merge sort algorithm that recursively splits the list (called runs in this example) into sublists until sublist size is 1, then merges those sublists to produce a sorted list. The copy back step is avoided with alternating the direction of the merge with each level of recursion (except for an initial one-time copy). To help understand this, consider an array with two elements. The elements are copied to B[], then merged back to A[]. If there are four elements, when the bottom of the recursion level is reached, single element runs from A[] are merged to B[], and then at the next higher level of recursion, those two-element runs are merged to A[]. This pattern continues with each level of recursion.
