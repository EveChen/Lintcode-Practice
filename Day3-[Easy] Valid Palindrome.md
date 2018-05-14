# Valid Palindrome
### Question: 判斷字詞是否回文
https://www.jiuzhang.com/solution/valid-palindrome/


### My Anwser - Java
*關鍵: 用雙指針，先定義出指針範圍，然後各自移動、與移動後的數相比*
```Java
public class Solution {
    public boolean isPalindrome(String s) {
        if (s == null || s.length() == 0) {
            return true;
        }

        int front = 0;
        int end = s.length() - 1;
        while (front < end) {
        // nead to check range of a/b
        //要s.charAt(front)并非字母或数字时才移动front, 因为不需要比较其他字符, 当遇到其他字符时，忽略他们
        //判断是否是回文串，是否应该是a和d比较，b和c比较, 如果写成isvalid，那么front会一直移动到末尾，不会停在a的位置, 就不会和end比较了
            while (front < s.length() && !isvalid(s.charAt(front))){ 
                front++;
            }
        
            if (front == s.length()) { // for empty string “.,,,”     
                return true; 
            }           

            while (end >= 0 && ! isvalid(s.charAt(end))) { // same here, need to check border of a,b
                end--;
            }

            if (Character.toLowerCase(s.charAt(front)) != Character.toLowerCase(s.charAt(end))) {
                break;
            } else {
                front++;
                end--;
            }
        }
//回文串的定义是不是就是对称，那么end<=start或者的时候就是在对称轴上或者越过了对称轴, 那么就说明是一个回文串
        return end <= front; 
    }

    private boolean isvalid (char c) {
        return Character.isLetter(c) || Character.isDigit(c);
    }
}
```

***


##### Credit to:
* Lintcode: https://www.lintcode.com/problem/valid-palindrome/description
* 九章算法: https://www.jiuzhang.com/solution/valid-palindrome/
