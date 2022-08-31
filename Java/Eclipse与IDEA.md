# `Eclipse`

## 常用快捷键

> **可以在`Window->Preference->General->Keys`下设置,修改快捷键**

- `Alt + /`
  - 显示当前可行的**所有代码补全方案**
  - 当然我们可以通过设置`Window->Perference->Java->Editor->Content Assist->Auto activation triggers for java`为`abcdefghijklmnopqrstuvwsyz.`即**可实现像`IDEA`一样的智能提示**
- `Ctrl + 1`
  - 对我们的当前行**代码报错**进行**最可行的自动修复**
- `Ctrl + Shift + o`
  - 当我们**使用了未导入的包中的类时**,可以通过该快捷键让编辑器**自动**为我们**导入其对应的包**
  - 当**出现同名类或接口问题**时会**弹窗**让**我们选择导入哪个包**

- `Ctrl + /`
  - 单行注释
- `Ctrl + Shift + /`
  - 多行注释
- `Ctrl + Shift + \`
  - 取消多行注释
- `Ctrl + Alt + ↑`
  - 将选中的代码复制并粘贴到上一行,当不选中时表示当前行
- `Ctrl + Alt + ↓`
  - 将当前行代码复制并粘贴到下一行,当不选中时表示当前行
- `Ctrl + d`
  - 删除光标选中的代码,当不选中时表示当前行
- `Alt + ↑`
  - 将选中的代码向上移动一行,当不选中时表示当前行
- `Alt + ↓`
  - 将选中的代码向下移动一行,当不选中时表示当前行
- `Shift + Enter`
  - 将当前光标所在行变为空行,原本的代码下移
- `Ctrl + Shift + Enter`
  - 将当前光标所在行变为空行,原本的代码上移
- `Ctrl + 鼠标点击结构`
  - 查看指定结构的源代码
- `Ctrl + Shift + T`
  - 搜索名查看指定结构的源代码
- `Alt + ←`
  - 退回到上一个编辑的页面
- `Alt + →`
  - 返回下一个页面
- `Ctrl + t`
  - 查看光标选中类的继承树
- 综合
  - `Ctrl + s`:保存
  - `Ctrl + z`:撤销
  - `Ctrl + y`:反撤销
  - `Ctrl + c`:复制
  - `Ctrl + v`:粘贴
  - `Ctrl + a`:全选
  - `Ctrl + x`:剪切

- `Ctrl + Shift + f`
  - 快速格式化代码,即美化代码文件结构
- `Ctrl + o`
  - 显示当前类的类结构,并支持搜索该类的指定方法或属性
- `Alt + Shift + r`
  - 对变量名等进行批量修改(同`Matlab`的`Shift + Enter`)
- `Ctrl + Shift + x`
  - 将选中的内容全部变成大写
- `Ctrl + Shift + y`
  - 将选中的内容全部变成小写
- `Alt + Shift + s`
  - 调出构造器等的快速生成功能
- `Alt + Enter`
  - 显示当前文件的各种信息,如`存储路径,创建时间`等
- `Ctrl + k`
  - 快速查找
- `Ctrl + w`
  - 关闭当前窗口
- `Ctrl + Shift + w`
  - 关闭所有窗口
- `Ctrl + Alt + g`
  - 
- `Ctrl + f`
  - 查找与替换
- `Ctrl + m`
  - 最大化当前窗口
- `Home`
  - 将光标移动到当前行的首部
- `End`
  - 将光标移动到当前行的尾部
- `PgUp`
  - 将光标移动到当前文件的首部
- `PgDn`
  - 将光标移动到当前行的尾部

# `IDEA`

## `IDEA`软件的组成

- **工作目录**
  - **`bin`目录**
    - `idea.exe`:`IDEA`的`32bit`启动器
    - `idea64.exe`:`IDEA`的`64bit`启动器
    - `idea.exe.vmoptions`:`32bit` 的`IDEA`的配置文件
    - `idea64.exe.vmoptions`:`64bit` 的`IDEA`的配置文件
  - **`help`目录**
  - **`jre64`目录**:`64bit`的`Java`运行环境
  - **`lib`目录**:`IDEA`的依赖类库
  - **`license`目录**:各个插件的许可证
  - **`plugin`目录**:插件的存储目录
- **`C盘`下的用户目录中的`.IntelliJIdea`文件夹**
  - `config`:`IDEA`的基础配置文件的存储目录
  - `system`:`IDEA`运行所必须的一些文件

## 配置文件组成

- **`-Xms`**:程序的初始内存数
- **`-Xmx`**:程序能够占据的最大内存空间]
- **`-XX:ReservedCodeCacheSize`**:保存代码的内存缓冲区大小

## `JavaEE`项目创建

### 项目基本文件介绍

- **`.idea`**:`IDEA`项目的**运行基本文件**存储目录
- **`.iml`**:`IDEA`项目的**配置文件**

### 包与类的创建

## `IDEA`常用配置

- **鼠标悬浮提示**
  - <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-2" alt="image-20220819210530818" style="zoom: 45%;" />
- **自动包导入**
  - <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-3%E3%80%81" alt="image-20220819210947829" style="zoom:60%;" />
- **不区分大小写的代码补全**
  - <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-4" alt="image-20220819211045717" style="zoom:60%;" />
- **修改默认文件注释作者信息**
  - <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-5" alt="image-20220819211805630" style="zoom:60%;" />
- **编辑器编码集设置**
  - <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-6" alt="image-20220819212029140" style="zoom:60%;" />
- **设置自动编译**
  - <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-7" alt="image-20220819212224020" style="zoom:60%;" />

## `IDEA`快捷补全

- `sout`:可以通过补`tab`进行`System.out.println()`的快速补全

## `IDEA`项目(`Project`)与模块(`Module`)

> **与`Eclipse`的区别**
>
> - 在`Eclipse`中我们可以在一个`Eclipse`窗口中创建多个项目`Project`,而在`IDEA`中一个窗口只能对应一个项目`Project`,如果要同时查看多个项目`Project`则需要打开多个`IDEA`窗口
>
> <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-1" alt="image-20220819205321382" style="zoom:67%;" />

### 基本介绍

- 在`IDEA`中`Project`项目是**最顶级的结构**
- 一个`Project`项目中可以创建**多个模块`Module`**

- 一个`IDEA`窗口**能且仅能**操控一个项目`Project`

## `IDEA`常用快捷键

> **可以通过设置键盘映射为`Eclipse`来让我们的快捷键与`Eclipse`快捷键基本相同**
>
> <img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-8" alt="image-20220819213128055" style="zoom:60%;" />

## == `IDEA`实时代码模板==

> **作用**
>
> - **让我们可以通过如`sout+tab`的方式快速写出`System.out.println()`等语句**

<img src="https://raw.githubusercontent.com/tangling0112/MyPictures/master/img/Eclipse%E5%92%8CIDEA-9" alt="image-20220819213358407" style="zoom: 60%;" />