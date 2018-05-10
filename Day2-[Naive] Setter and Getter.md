# Setter and Getter
### Question:https://www.jiuzhang.com/solution/setter-and-getter/


### My Anwser - Java
*關鍵:記得加上 this*
```Java
public class School {
    private String name;

    public void setName(String type_name){
        this.name = type_name;
    }

    public String getName(){
        return this.name;
    }
}
```

***

### My Answer - Python
*關鍵:記得self位置 & __init__初設*
```Python
class School:
    def __init__(self):
        self.name = None
    
    def setName(self, name):
        self.name = name

    def getName(self):
        return self.name;
```


***

##### Credit to:
* Lintcode: https://www.lintcode.com/problem/setter-and-getter/description
* 九章算法: https://www.jiuzhang.com/solution/setter-and-getter/
