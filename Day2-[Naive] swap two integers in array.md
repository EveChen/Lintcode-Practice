# Swap Two Integers in Array
### Question:
https://www.jiuzhang.com/solution/swap-two-integers-in-array/

### My Anwser - Java
關鍵:temp 應用
```Java
public class Solution {
    public void swapIntegers(int[] A, int index1, int index2) {
        // write your code here
        int temp = A[index1];
        A[index1] = A[index2];
        A[index2] = temp;
    }
}
```

***

### My Answer - Python
關鍵: temp 應用
```Python
class Solution:
    def swapIntegers(self, A, index1, index2):
        temp = A[index1]
        A[index1] = A[index2]
        A[index2] = temp


```


***

##### Credit to:
* Lintcode: https://www.lintcode.com/problem/swap-two-integers-in-array/description
* 九章算法: https://www.jiuzhang.com/solution/swap-two-integers-in-array/
