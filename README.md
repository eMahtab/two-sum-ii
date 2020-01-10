# Two Sum II
## https://leetcode.com/problems/two-sum-ii-input-array-is-sorted

Given an array of integers that is already sorted in ascending order, find two numbers such that they add up to a specific target number.

The function twoSum should return indices of the two numbers such that they add up to the target, where index1 must be less than index2.

Note:
1. Your returned answers (both index1 and index2) are not zero-based.
2. You may assume that each input would have exactly one solution and you may not use the same element twice.

```
Example:

Input: numbers = [2,7,11,15], target = 9
Output: [1,2]
Explanation: The sum of 2 and 7 is 9. Therefore index1 = 1, index2 = 2.
```
## Implementation :

```java
public static int[] twoSum(int[] numbers, int target) {
        if(numbers == null || numbers.length < 2)
        	return new int[2];
        
        int left = 0;
        int right = numbers.length - 1;
        while(left < right) {
        	if((numbers[left] + numbers[right]) < target) {
        		left++;
        	} else if((numbers[left] + numbers[right]) > target) {
        		right--;
        	} else {
        		return new int[] {left + 1, right + 1};
        	}
        }
        return new int[2];
}
```

Above implementation have runtime complexity of O(n) and space complexity of O(1)

```
Runtime Complexity = O(n)
Space Complexity   = O(1)
```
