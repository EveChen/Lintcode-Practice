# 521. Remove Duplicate Numbers in Array
### Question: 在一個未排序的 Array 中做兩件事
* 把重複的數字往後丟到 Array 最後
* 數有多少個 unique value
* e.g. Given nums = [1,3,1,4,4,2], you should:
  - Move duplicate integers to the tail of nums => nums = [1,3,4,2,?,?].
  - Return the number of unique integers in nums => 4.
 
### My Answer
```Java
public class Solution {
    /*
     * @param nums: an array of integers
     * @return: the number of unique integers
     */
    public int deduplication(int[] nums) {
        if (nums.length <= 0 ){
            return 0;
        }
        
        //比較兩個位置的數，如果兩數不相同，就把數字移到前面
        Arrays.sort(nums);
        int len = 0;
        for (int i = 0; i < nums.length; i++){
            if(nums[i] != nums[len]){
                nums[++len] = nums[i]; //這步就是在移數字位置
            }
        }
        return len + 1;
    }
}
```

***
###### Credit to: Lintcode
https://www.lintcode.com/problem/remove-duplicate-numbers-in-array/description
