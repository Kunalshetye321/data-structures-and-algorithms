# Second Largest Element 
[GFG](https://www.geeksforgeeks.org/problems/second-largest3735/1)

## Brute Force Approach
> 1. In brute-force here, biggest problem here is the presence of duplicate numbers. There can be n no. of duplicates.

![Brute Force Approach](/Array/Day1/P2_FindSecondLargestElement/brute-force.jpg)

## Optimized Approach
![Optimized Approach](/Array/Day1/P2_FindSecondLargestElement/optimized-approach-part1.jpg)

![Optimized Approach](/Array/Day1/P2_FindSecondLargestElement/optimized-approach-part2.jpg)

> Pseudo Code
```java
class Solution {
    public int getSecondLargest(int[] arr) {
        // code here
        int l = arr[0];//largest
        int l2 =  -1;//second largest
        
        for(int i = 1; i < arr.length; i++) {
            
            // Edge case_ Case: [10,5,10]
            if(arr[i] == l || arr[i] == l2) {
                continue;
            }
            if(arr[i] > l) {
                
                //Shift
                l2 = l;
                l = arr[i];
            } else if(arr[i] > l2) {
                l2 = arr[i];
            }
        }
        
        return l2;
    }
}
```

## Problem solved.
![Problem Solved](/Array/Day1/P2_FindSecondLargestElement/problem-solution.png)
