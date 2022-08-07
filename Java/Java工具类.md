## 前置

> **`Java`工具类都保存在`java.utils`包中**

## `Arrays`数组工具类

> - **`import java.utils.Arrays`**
> - `Arrays.方法名(<实参列表>)`

### 使用方法

### 常用方法

| 方法                                          | 作用                                | 示例                       |
| --------------------------------------------- | ----------------------------------- | -------------------------- |
| `boolean equals(数据类型[] a,数据类型[]b) `   | 比较两个数组是不是相等              | `Arrays.equal(a,b)`        |
| `String toString(数据类型[] a)`               | 输出数组信息                        | `Arrays.toString(a)`       |
| `void fill(数据类型[] a,数据类型 val)`        | 用`val`填充数组`a`                  | `Arrays.fill(a,5)`         |
| `void sort(数据类型[] a)`                     | 对数组进行排序(是原地操作)          | `Arrays.sort(a)`           |
| `int binarySearch(数据类型[] a,数据类型 key)` | 使用二分法查找`key`是否出现在数组中 | `Arrays.binarySearch(a,5)` |



- ![image-20220716130506987](F:\A_Java_DataBase_Study_FIle\Java\Java工具类.assets\image-20220716130506987.png)