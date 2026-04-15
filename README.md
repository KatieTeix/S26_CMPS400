1.
for (int i = 0; i < 15; i++) {
    sum += i;
}
Time Complexity: O(1)
The loop runs exactly 15 times no matter what. Since it does not depend on input size n, it is constant time.

2.
for (int i = 0; i < n; i++) {
    sum += a[i];
}
Time Complexity: O(n)
The loop runs n times, and each operation takes constant time. So total time grows linearly with n.

3.
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        count++;
    }
}
Time Complexity: O(n²)
There are two nested loops, each running n times. Total operations = n × n = n².

4.
int i = 1;
while (i < n) {
    i *= 2;
}
Time Complexity: O(log n)
The value of i doubles each iteration (1 → 2 → 4 → 8 → ...).
The number of times you can double before reaching n is logarithmic.

5.
int i = 2;
while (i <= n) {
    i = i * i;
}
Time Complexity: O(log log n)
Here, i is being squared each time (2 → 4 → 16 → 256 → ...).
This grows much faster than doubling, so it reaches n in about log log n steps.





1. Why is asymptotic analysis usually more useful than timing two programs on a single computer?
Asymptotic analysis evaluates how an algorithm performs as the input size grows, independent of hardware or environment. Timing two programs on a single computer can be misleading because results depend on factors like processor speed, memory, and system load. Asymptotic analysis provides a general and scalable way to compare algorithms.

2. Why does Binary Search require sorted data?
Binary Search works by repeatedly dividing the dataset in half and determining which half may contain the target. This is only possible if the data is sorted, because the algorithm relies on comparing the target to the middle element to decide whether to search left or right.

3. For a nearly sorted array, which algorithm is usually a better choice: Selection Sort or Insertion Sort? Explain.
Insertion Sort is usually the better choice for a nearly sorted array. This is because it runs in near O(n) time when the data is already mostly ordered, requiring only a few shifts. Selection Sort, on the other hand, always performs O(n²) comparisons regardless of how sorted the data is.

4. If memory writes are expensive, which algorithm is usually more attractive: Selection Sort or Insertion Sort? Explain.
Selection Sort is usually more attractive when memory writes are expensive. This is because it performs fewer swaps, typically at most one swap per iteration. In contrast, Insertion Sort may require many shifts (data moves), which increases the number of memory writes.
