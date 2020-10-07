# JAVA学习笔记

## 1.CS 61B 学习总结

### 1.project0

#### 1.JAVA相关

1. 关于Math.sqrt（double a）：该函数返回a的平方数

   特殊情况：

   - ​	如果参数是NaN或小于零，那么返回结果是NaN

   - ​    如果参数是无穷大，那么返回结果是无穷大

   - ​	如果参数是正零或负零，那么结果是一样的参数

​	

[^关于NaN]: 在实际的运算过程中，可能会出现一些非法操作，导致产生了非法的数值，比如除零，通过NaN来表示这个非数值，NaN与任何浮点数的比较结果都为假，这是NaN独有的特征，所以可以使用与自己相比确定当前数值是不是一个正常的数。

2. equals（）：可以比较两个对象是否相同，不仅限于String

3. 对于类中定义的静态方法，调用时直接用类名调用，这也一定程度说明了静态方法一般的使用场景。

4. 调用其他类中方法

   - 所调用的类在同一个包中

     只需要在最顶：package + 包名

   - 所调用的类不在同一个包中

     只需要在最顶：import + 包名.类名（加点）

5. 创建自定义类的数组

   e.g.  

   ```java
   Body[] body = new Body[5];	//创建了5个Body对象，但是并没有分配空间
   for(int i = 0;i<5;i++){		//为每一个对象分配空间
   	body[i] = new Body();   //初始化每个对象，括号里的内容由Body类的构造函数决定
   }
   ```

6. String与其他数据类型之间的转换

   - 其他数据类型向String转换

     1. ```java
        X.toString()
        ```

     2. ```java
        X+""
        ```

     3. ```java
        String.valueOf(X)
        ```

   - String向其他数据类型转换

     ```java
     byte b = Byte.parseByte(X);
     short t = Short.parseShort(X);
     int i = Integer.parseInt(X);
     long l = Long.parseLong(X);
     Float f = Float.parseFloat(X);
     Double d = Double.parseDouble(X);
     ```

7. ArrayList

   ```java
   import java.util.ArrayList;
   ArrayList<E> al = new ArrayList<E>(); //E为引用数据类型
   al.add(item);
   al.get(index);
   al.set(index,item);
   al.remove(index);//删除指定位置
   al.size();//计算大小
   ```

   | 基本类型 | 引用类型  |
   | :------- | :-------- |
   | boolean  | Boolean   |
   | byte     | Byte      |
   | short    | Short     |
   | int      | Integer   |
   | long     | Long      |
   | float    | Float     |
   | double   | Double    |
   | char     | Character |

#### 2.git 相关

1. 创建版本库（Repository）

   ```
   git init //空仓库
   ```

2. 添加文件到版本库

   ```
   git add xxx.txt
   git commit -m "修改原因"
   ```

3. 回退版本

   ```
   git reset --hard HEAD^ //HEAD表示当前版本，HEAD^表示上一个版本，HEAD^^表示上上个版本 
   ```

4. 其他的

   [1]: https://www.liaoxuefeng.com/wiki/896043488029600/898732792973664

   *******************

   