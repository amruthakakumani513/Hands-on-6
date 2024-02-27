Let T(n) = average case time complexity to sort an array of length n using non-randomized Quicksort

Steps in Quicksort:

Select a pivot element (constant time)
Partition the array into two sub-arrays based on pivot (linear time O(n))
Recursively sort the two sub-arrays
Let m and n-m-1 be the sizes of the two sub-arrays after partitioning, where m is a random variable between 0 to n-1.

The recurrence relation for average time complexity is:

T(n) = T(m) + T(n-m-1) + O(n)

Taking expectation over m: E[T(n)] = E[T(m)] + E[T(n-m-1)] + O(n)

Since m is randomly uniformly distributed: E[m] = (n-1)/2

Therefore,

E[T(n)] = 2 E[T(n/2)] + O(n)

Solving the recurrence using Master method (with a = 2, b = 2, c = 1): E[T(n)] = Θ(n log n)

Therefore, the average case time complexity of non-randomized Quicksort is Θ(n log n).
