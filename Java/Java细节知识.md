# 基于`Java`与`C/C++`对比的细节汇总

## 共有特性

- **`Java`与`C++/C`都严格区分大小写**
- **`Java`与`C/C++`一样默认以`main`函数为程序运行入口**
- **`Java`的程序格式与`C/C++`相同,都是必须加分号,加大括号**
- **`System.out.print()`与`System.out.prinln()`**
  - 前者不自带换行
  - 后者自带换行
- **封装,继承,多态**
  - 封装:即将一系列的函数与变量
  - 继承:
  - 多态:
- **`Java`的变量的使用与`C/C++`基本完全相同,都需要实现声明**

****

- **`Java`的变量也有作用域的概念,其内涵与`C/C++`相同**

****

- **`Java`中也有转义字符`\`**

****

- **`Java`与`C/C++`相同,对不同数据类型的值之间直接进行赋值时会进行自动类型转换(甚至于将`double`型赋值给`int`型会直接对小数部分直接截断不要**

****

- **`Java`中如果计算时发生了数值范围溢出问题,与`C/C++`具有相同的特性**

****

- **`String`类型的常量必须使用`""`包括**

****

- **二进制存储的``原码``,``反码``与``补码``**
  - **计算机中正数与负数按照`补码`存储**
    - **值得注意的是,正数的原码,反码,补码都相同**
  - ``反码``是``原码``除符号位外各个位置取反
  - ``补码``是``反码``+1

****

- **三元运算符的表达式1与表达式2必须最终有相同数据类型**

****

- **用`if-else`可以实现的就不一定可以用`switch`实现,用`switch`可以实现一定可以用`if-else`实现**
  - **能用`switch case`尽量用**

****

- **`Java`中无论是几维的数组,实际上都是数组嵌套生成的,即用数组里面存储数组的方式实现**
  - **二维数组是在一维数组中存一维数组**
  - **三维数组是在一维数组中存二维数组**
  - 因此,二维数组的`.length`属性的值为其保存的**一维数组的个数**,三维数组的`.length`属性的值为其保存的**二维数组的个数**
  - 并且值得注意的是,在二维数组下`.length`的值等于**二维数组的行数**,三维数组下`length`的值等于**三维数组的高度**
- **值得注意的是,当二维数组没有给内存数组分配存储空间时那么我们的外层数组的元素的值不再是指针,而是`null`**

****

- **算法的五大特性**
  - **输入**
  - **输出**
  - **有穷性**
  - **确定性**
  - **可行性**

****

# `Java`独有特性

- **`Java`中也有`break`与`continue`与`C/C++`中效果相同,并且新加了跳出指定循环结构的新特性**
  - 默认情况下效果与`C/C++`效果相同
  - **带标签的为`break 标签名`,`continue 标签名`,此时我们的循环体需要添加`标签名:`的结构**
  - <img src="F:\A_Java_DataBase_Study_FIle\Java\Java细节知识.assets\image-20220715201700624.png" alt="image-20220715201700624" style="zoom: 80%;" />

****

- **`switch case`的`default`用在`switch case`语句最后,表示当前面的都未匹配时执行该语句,若匹配到了则不执行,并且`switch case`的运行机制与`C/C++`相同都是不遇到``break``就会继续进行**
  - **`case`之后只能是常量**
  - **`default`可以有也可以不要**
  - **`default`位置可以随意设置,但是`default`内不加`break`就会导致和`case`里不加`break`一样的后果,虽然位置可以随意设置,但是其位置的不同且不加`break`的话会导致不同的结果**

****

- **`Java`中常量整数默认为`int`,常量浮点数默认为`double`**

****

- **`Java`的`char`字符类型不同于`C/C++`的单字节`ASCII`码,`Java`使用双字节的`Unicode`编码来存储字符.因此`Java`中字符类型可以存储中文**
- **`Java`中`char`只能存储一个字符**
  - 在`Unicode`编码下,无论是英文单词还是中文汉字都是使用两个字节进行存储,因此`'A'`与`'中'`占据的空间相同

****

- **`System.out.print()`与`System.out.prinln()`**
  - 前者不自带换行
  - 后者自带换行

****

- **`Java`是严格的``面向对象语言``**
  - 因此在`Java`中没有单独的函数,而是只有类,所有函数都需要作为某个类的成员函数.同理`Java`也没有`C/C++`类似的全局变量,``Java``中的类的成员变量的含义等价于`C/C++`的全局函数.

****

- **一个简单的`Java`程序的运行流程**
  - `java.exe`调用`.class`字节码文件
  - 获取`.class`字节码文件中的类
  - 通过调用类内成员的方法对类中的`main()`函数进行调用

****

- **`Java`中的注释分为`单行注释`,`多行注释`,`文档注释`三种**
  - `单行注释`:**`//注释内容`**
  - `多行注释`:**`/*注释内容*/`**
  - **`文档注释`:`/**注释内容*/`**
  - ==**注意**==:当我们使用`javadoc.exe`对我们的`.java`程序进行读取时,其会将我们程序中所有的文档注释提取出来生成网页形式的程序说明文档

****

- **`Java`标识符命名规则**
  - <img src="F:\A_Java_DataBase_Study_FIle\Java\Java细节知识.assets\image-20220714223647568.png" alt="image-20220714223647568" style="zoom:80%;" />
- **`Java`标识符命名规范**
  - <img src="F:\A_Java_DataBase_Study_FIle\Java\Java细节知识.assets\image-20220714223812917.png" alt="image-20220714223812917"  />

****

- **`Java`数据类型定义时的要求**
  - `long`数据类型如果需要在定义的同时进行初始化,那么用于初始化的常量**必须后缀`l/L`**
  - `float`数据类型如果需要在定义的同时进行初始化,那么用于初始化的常量**必须后缀`f/F`**

****

- **`Java`中物理地址的存储不只是简单的存储地址,还会带上指向的地址存储的数据的类型**
  - `I@15db9742`	
    - `I`:指示其为`int`型
    - `@15db742`表示其指向的行连续空间在堆区的首地址
  - `Ljava.lang.String;@7852e922`

****

- **`Java`中我们必须时刻注意数组的数组名存储的是地址`数组1=数组2`实际上就是把``数组2``的地址赋值给了`数组1`**
- **`Java`中要对地址进行赋值必须保证地址指向的空间存储的数据的数据类型相同**

****

- **`Java`中所有引用数据类型的不初始化时的默认值为`null`**
- **`Java`中局部变量(即类方法或构造器的形式参数,内部变量等)是没有默认值的,因此调用之前一定要被显式地赋值,否则会报错**

****

- **`Java`类在`C++`类的基础上的特性**

  > **`Java`与`C++`的类在基本特性上是相同的**

  - **相同点**
    - **`public`,`private`,`protected`用于成员变量或成员函数的权限指定**
    - **当不指定权限时,`Java`与`C++`默认都是`private`**
    - **使用`static`定义静态方法与属性**

  > **但是有些特性又有所区别**

  - **不同点**
    - **类内方法与属性的权限不再与`C/C++`一样直接`public:`指定,而是每一个方法与属性都应该声明权限**

****

- **`Java`中如果声明方法为`void`类型,那么我们方法内不要再使用``return``或直接`return;`,如果没有声明为`void`类型那么就必须保证程序在任何情况下都会有返回值**

****

- **`Java`中类的方法可以直接调用该类的其他方法,而无需借助类实例**

****

- **`Java`中不能在成员函数中定义类,方法,属性.成员函数中只能定义局部变量.**

****

- **`Java`引用数据类型的名称与实例化对象的名称只能取`null`或`地址值`**