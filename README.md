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
