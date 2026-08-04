## Largest and Second Largest
[![Codechef](../../../logo/codechef.jpg)](https://www.codechef.com/practice/course/arrays/ARRAYS/problems/LARGESECOND?tab=statement)

Largest and Second Largest
You are given an array of N integers.
Find the maximum sum of two distinct integers in the array.

Note: It is guaranteed that there exist at least two distinct integers in the array.


## Optimized Approach
 > Pseudo code [ O(n) ]

 ```java
for(int i = 0; i < a.length; i++) {
                if(a[i] == l || a[i] == l2) {
                    continue;
                }
                if(a[i] > l) {
                    l2 = l;
                    l = a[i];
                }
                else if(a[i] > l2) {
                    l2 = a[i];
                }
            }
            System.out.println(l+l2);
 ```

## Problem Solved

![Problem Solved](/Array/Day1/P2_2FindMaxSumOfTwoDistinctIntegers/problem-solved.png)