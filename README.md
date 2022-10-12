# Codility_PermMissingElem
Find the missing element in a given permutation.

# Task description
An array A consisting of N different integers is given. The array contains integers in the range [1..(N + 1)], which means that exactly one element is missing.

Your goal is to find that missing element.

# Link Details
[trainingJYH9S7-2PU](https://app.codility.com/demo/results/trainingJYH9S7-2PU/)

# Programming Language
Java SE 11

# Solution Code

```

import java.util.*;

class Solution {
    public int solution(int[] A) {
        // write your code in Java SE 11
       int N = A.length;
        Set<Integer> set = new HashSet<>();
        for (int a : A) {
            if (a > 0) {
                set.add(a);
            }
        }
        for (int i = 1; i <= N + 1; i++) {
            if (!set.contains(i)) {
                return i;
            }
        }

        
        return 0;
    }
}

```


