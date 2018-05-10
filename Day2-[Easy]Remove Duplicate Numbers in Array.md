# 521. Remove Duplicate Numbers in Array
### Question: 在一個未排序的 Array 中做兩件事
* 把重複的數字往後丟到 Array 最後
* 數有多少個 unique value
* https://www.jiuzhang.com/solution/remove-duplicate-numbers-in-array/
 
### My Answer - Java
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

### My Answer - Python


***
###### Credit to: 
* Lintcode: https://www.lintcode.com/problem/remove-duplicate-numbers-in-array/description
* 九章算法: https://www.jiuzhang.com/solution/remove-duplicate-numbers-in-array/
