/**
 * LeetCode #26: Remove Duplicates from Sorted Array
 * 
 * Given a sorted array nums, remove duplicates in-place such that each element 
 * appears only once. Return the number of unique elements.
 * 
 * Requirements:
 * - Modify nums in-place so first k elements contain unique values
 * - Maintain relative order of elements
 * - Return count of unique elements (k)
 * 
 * Example 1: nums = [1,1,2] → k = 2, nums = [1,2,_]
 * Example 2: nums = [0,0,1,1,1,2,2,3,3,4] → k = 5, nums = [0,1,2,3,4,_,_,_,_,_]
 * 
 * Constraints:
 * - 1 <= nums.length <= 3 * 10^4
 * - -100 <= nums[i] <= 100
 * - nums is sorted in non-decreasing order
 * 
 * Time: O(n) | Space: O(1)
 */

class Solution {
    public int removeDuplicates(int[] nums) {
        if(nums.length == 0)
            return 0; 
        int writeIndex = 1;

        for (int readIndex = 1; readIndex < nums.length; readIndex++){
            if(nums[readIndex] != nums[writeIndex - 1]){
                nums[writeIndex] = nums[readIndex] ;
                writeIndex++;
            }
        }
        return writeIndex ; 
    }
}
