# Longest-continuous-increasing-subsequence
Given an unsorted array of integers, find the length of longest continuous increasing subsequence (subarray).
class Solution {
    public int findLengthOfLCIS(int[] nums) {
        if(nums == null || nums.length ==0){
            return 0;
        }
        int count=1;//for length of subsequence
        int result=1;
        for(int i=1;i<nums.length;i++){
            if(nums[i-1]<nums[i]){
                count++;
            }
            else{
                count=1;
            }
            result =  Math.max(result,count);
        }
        return result;
    }
}
