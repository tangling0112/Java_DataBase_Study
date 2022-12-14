## ``.class`字节码文件解读

## 为什么计算机中整数都是用补码存储

- **正数相加问题**
- **正数与负数相加问题**
- **正数与负数相减问题**

## `Java`程序的内存结构

![image-20220716111055598](F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716111055598.png)

![image-20220716111538719](F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716111538719.png)

## `Java`数组的底层结构

> **数组实际上是通过指针来进行实现的**
>
> 

### 二维数组(``int[][] 数组名 = new int[3][4]``)

#### 建立过程

- :one:首先我们的系统将数组名压栈到我们的`stack`栈区内
- :two:然后系统通过``new``指令获取一个可以存储三个指针的连续空间
- :three:将上一步获得的连续空间的首地址给到我们第一步的`stack`栈区内的数组名保存
- :four:然后通过`new`指令获取到三个可以存储`4`个`int`值的连续空间
- :five:将上一步得到的三个连续空间的首地址给到我们第二步得到的可以存储三个指针的连续空间中存储

#### 索引取值过程

- :one:首先在`stack`栈区查找到数组名对于的内存空间的首地址
- :two:然后根据第一个中括号内的数,在通过首地址索引到的存储三个指针的连续空间中的找到其中一个指针
- :three:根据上一步获得的指针获取到我们的一个可以存储`4`个元素的连续空间
- :four:根据第二个中括号内的数,在我们上一步得到的连续空间中索引得到指定的元素并返回给我们的用户进程

#### 注意

> **数组名存储的实际就是我们栈区中该数组名对于的堆区存储指针的连续空间的首地址**
>
> **我们上面提到的`数组名[]`的地址值在`Java`中不仅仅只是地址值,而是如下的一个值**
>
> - `I@15db9742`	
>   - `I`:指示其为`int`型
>   - `@15db742`表示其指向的行连续空间在堆区的首地址
> - `Ljava.lang.String;@7852e922`

<img src="F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716122656809.png" alt="image-20220716122656809" style="zoom: 50%;" /><img src="F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716122755651.png" alt="image-20220716122755651" style="zoom:50%;" />

<img src="F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716122755651.png" alt="image-20220716122755651" style="zoom:50%;" />

## `Java`类对象的实例化时的流程与内存占用分析

> <img src="F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716140125320.png" alt="image-20220716140125320" style="zoom: 45%;" />

### 只有成员变量无成员函数时

#### 实例化

- :one:首先通过`Person p1`将`p1`这个变量名压入`stack`栈区中
- :two:然后系统根据`new Person()`指令在堆区中申请一个能够存储`Person`类的属性的空间
- :three:根据`Person p1 = new Person()`将申请到的空间的首地址给与栈区内的`p1`变量保存

#### 调用并访问非静态成员变量

- :one:首先根据我们的`p1`找到我们的栈区中存储的类实例的``堆区``空间首地址
- :two:然后根据`.name`找到该``堆区``空间中`name`属性对应的值,并返回给我们的用户

- <img src="F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716140558567.png" alt="image-20220716140558567" style="zoom:40%;" />

### 成员变量与成员函数都有时

#### 实例化的流程

- 

#### 调用非静态成员变量

- 

#### 调用静态成员变量

- 

#### 调用非静态成员函数

- 

#### 调用静态成员函数

- 

## `Java`引用数据类型与我们的自定义类为什么在数组中保存方式不同?

> - **引用数据类型保存在一维数组中是直接保存其本身,即与八大基本数据类型的存储方式相同**
> - ==**自定义类的实例化对象保存在一维数组中保存的是指向该类在堆区中的位置的指针**==

### `Java`自定义类的对象在数组中保存的内存结构

#### 对象实例化并数组化

- :one:首先由`Student[] stus`向我们的程序的栈区压入`stus`变量
- :two:然后由`new Student[5]`在我们程序的堆区开辟一个可以容纳五个指向`Student`实例的指针的连续空间,此时这五个指针都为`null`
- :three:然后根据`Student[] stus = new Student[5]`将我们在堆区开辟的空间的首地址交给我们栈区的`stus`变量存储

#### 对象数组的初始化

- :one:首先我们通过`stus[i]`找到在堆区中存储我们的`Students`实例指针的数组
- :two:然后我们找到第`i`个指针,此时该指针的值为`null`
- :three:我们通过`new Student()`的方式在堆区中开辟一个存储`Student`实例的空间
- :four:然后我们将开辟的空间的首地址交给我们的第二步获取到的指针保存
- :five:至此就完成了一个对象数组元素的初始化,只要重复进行就可以完成我们对象数组的全部初始化

#### 对象数组元素的非静态成员变量的调用

- :one:首先我们根据`stus`对象数组名获取到我们的对象数组指针存储的堆区空间首地址
- :two:然后根据我们的索引值,结合获得的堆区空间首地址做地址偏移,获取到指向我们某一个对象数组元素的指针
- :five:然后我们根据该指针访问我们堆区的某个地址,然后根据我们的`.属性名`索引到我们的对象实例中对应的属性的值
- :six:至此我们就完成了对对象数组中某个元素的指定属性的访问

#### 对象数组元素的静态成员变量的调用

- 

#### 对象数组元素的非静态成员函数的调用

- 

#### 对象数组元素的静态成员函数的调用

- 

<img src="F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716153824547.png" alt="image-20220716153824547" style="zoom:50%;" />

## `Java`程序从编译到运行的流程

<img src="file://F:\A_Java_DataBase_Study_FIle\Java\Java重要工作原理解析.assets\image-20220716140125320.png?lastModify=1657958341" alt="image-20220716140125320" style="zoom:50%;" />

- **`方法区`:**存储**类的加载信息**,**所有的常量**,**所有的静态变量**
- **`堆区`**:存储我们使用**`new`生成的结构**以及**类的属性**
- **`栈`**:存储**局部变量**

## `Java`匿名对象的工作原理

## `Java`包导入的工作原理