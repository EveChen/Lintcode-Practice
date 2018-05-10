# Rectangle Area 
### Question: 
* 做constructor
* 做method去算長方形面積
* e.g. 
Java:
    Rectangle rec = new Rectangle(3, 4);
    rec.getArea(); // should get 12

Python:
    rec = Rectangle(3, 4)
    rec.getArea()
    
***
### My Answer - Java:
```Java
public class Rectangle {
    int width, height;

    public Rectangle(int input_width, int input_height){
        width = input_width;
        height = input_height;
    }

    public int getArea(){
        return width * height;
    }
}

```


***
### My Answer - Python:
```Python
class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def getArea(self):
        return self.width * self.height
```

***

##### Credit to:
* Lintcode: https://www.lintcode.com/problem/rectangle-area/description
* 九章算法: https://www.jiuzhang.com/solution/rectangle-area/
* 其他: https://blog.csdn.net/gamesluo/article/details/76721560
