# ArrayList
### Question:https://www.jiuzhang.com/solution/arraylist/


### My Anwser - Java
*關鍵: 知道 Java methods 的運用，如list.add(k), list.remove(k), list.get(k), list.indexOf(val), list.set(k, val)*
```Java
public class ArrayListManager {
 
    public static ArrayList<Integer> create(int n) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        for (int i = 0; i < n; i++){
            list.add(i);
        }
        return list;
    }
    
    public static ArrayList<Integer> clone(ArrayList<Integer> list) {
        ArrayList<Integer> clonelist = new ArrayList<Integer>();
        for (int j : list){
            clonelist.add(j);
        }
        return clonelist;
    }
    
    public static int get(ArrayList<Integer> list, int k) {
        return list.get(k);
    }
    
    public static void set(ArrayList<Integer> list, int k, int val) {
        list.set(k, val);
    }
    
    public static void remove(ArrayList<Integer> list, int k) {
        list.remove(k);
    }
    
    public static int indexOf(ArrayList<Integer> list, int val) {
        if (list == null)
            return -1;
        return list.indexOf(val);
    }
}
```



***

##### Credit to:
* Lintcode: https://www.lintcode.com/problem/arraylist/description
* 九章算法: https://www.jiuzhang.com/solution/arraylist/
