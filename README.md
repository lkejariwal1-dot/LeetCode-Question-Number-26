# LeetCode-Question-Number-26

Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once. The relative order of the elements should be kept the same.

Consider the number of unique elements in nums to be k​​​​​​​​​​​​​​. After removing duplicates, return the number of unique elements k.

The first k elements of nums should contain the unique numbers in sorted order. The remaining elements beyond index k - 1 can be ignored.

Custom Judge:

The judge will test your solution with the following code:

int[] nums = [...]; // Input array
int[] expectedNums = [...]; // The expected answer with correct length

int k = removeDuplicates(nums); // Calls your implementation

assert k == expectedNums.length;
for (int i = 0; i < k; i++) {
    assert nums[i] == expectedNums[i];
}
If all assertions pass, then your solution will be accepted.


# This is the result of the Solution

<img width="1917" height="912" alt="image" src="https://github.com/user-attachments/assets/c1114929-3848-41a5-a2a2-ce81b6fe13a2" />


# Work Flow

1. Initialize `k = 1` to represent the position of the next unique element, since the first element is always unique.

2. Iterate through the array starting from index `1`, using `i` to examine each element.

3. Compare the current element `nums[i]` with the last unique element `nums[k-1]`.

4. If both elements are equal, skip the current element because it is a duplicate.

5. If they are different, copy `nums[i]` to `nums[k]` and increment `k` to update the position for the next unique element.

6. Continue this process until all elements in the array have been checked, keeping the unique elements in their original sorted order.

7. Return `k`, which represents the total number of unique elements in the modified array.


