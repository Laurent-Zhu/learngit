# **第一周任务**

## 一、安装Linux

​	直接借基地的系统盘来安装了，挺顺利，没有遇到什么困难。哈哈哈

## 二、开发工具

### 1. Terminal

学习了`cd`、`ls`、`apt install`等等命令

<img src="/home/laurent/.config/Typora/typora-user-images/image-20240923230448774.png" alt="image-20240923230448774" style="zoom:50%;" />

<img src="/home/laurent/.config/Typora/typora-user-images/image-20240923230532710.png" alt="image-20240923230532710" style="zoom:50%;" />

### 2. Vim

- 三种模式

  <img src="https://i-blog.csdnimg.cn/blog_migrate/93519d09968c6d719e2a34bf89b17e37.png" alt="在这里插入图片描述" style="zoom:50%;" />

  - 普通模式

    在终端中输入vim加文件名后回车即进入普通模式，可以进行删除、复制、粘贴

    常用命令：

    - `h` `j` `k` `l`：分别表示光标左、下、上、右移动
    - `gg` 或`H`：光标移动到页头
    - `G`或`L`：光标移动到页尾
    - `数字G`：光标移动到指定行
    - `w`：移动到下一个词词头
    - `b`：移动到山一个词词头

    - `yy`：复制光标所在的当前行
    - `y数字y`：复制从光标所在行往下数的`数字`行
    - `yw`：复制一个词
    - `p`：从光标所在行开始粘贴
    - `u`：撤销
    - `dd`：删除光标所在行
    - `d数字d`：删除从光标所在行往下数的`数字`行
    - `dw`：删除一个词

    <img src="/home/laurent/.config/Typora/typora-user-images/image-20240925102827975.png" alt="image-20240925102827975" style="zoom: 67%;" />

    <img src="/home/laurent/.config/Typora/typora-user-images/image-20240925102859179.png" alt="image-20240925102859179" style="zoom:50%;" />

  - 编辑模式

    在普通模式下，按`i`键可以进入编辑模式，编辑模式下和普通记事本一样可以直接输入字符，编辑模式中左下角会有“插入”的字样。编辑模式下按ESC键即可退出回到普通模式。

    <img src="/home/laurent/.config/Typora/typora-user-images/image-20240925110714611.png" alt="image-20240925110714611" style="zoom:50%;" />

  - 命令模式

    在普通模式下按下`:`或`/`即可进入命令模式，进入后左下角有`:`或`/`的标识。命令模式下按ESC键可以退回到普通模式。

    <img src="/home/laurent/.config/Typora/typora-user-images/image-20240925111655620.png" alt="image-20240925111655620" style="zoom:40%;" /><img src="/home/laurent/.config/Typora/typora-user-images/image-20240925111728528.png" alt="image-20240925111728528" style="zoom:40%;" />

    常见命令

    - `:w`：保存
    - `:q`：退出
    - `:wq`：保存并退出
    - `:q!`：不保存并强制退出
    - `/要查找的词`：查找内容

    <img src="/home/laurent/.config/Typora/typora-user-images/image-20240925113030385.png" alt="image-20240925113030385" style="zoom:50%;" />

    <img src="/home/laurent/.config/Typora/typora-user-images/image-20240925113111073.png" alt="image-20240925113111073" style="zoom:50%;" />

    <img src="/home/laurent/.config/Typora/typora-user-images/image-20240925113129450.png" alt="image-20240925113129450" style="zoom:50%;" />

    

### 3. g++

- 基本语法格式：

  ```
  g++ [选项] 准备编译的文件 [选项] [目标文件]
  ```

- 单文件：

  <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924205626895.png" alt="image-20240924205626895" style="zoom:50%;" />

  <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924204853278.png" alt="image-20240924204853278" style="zoom:50%;" />

- 多文件：

  <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924205700493.png" alt="image-20240924205700493" style="zoom:50%;" />

  <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924205726630.png" alt="image-20240924205726630" style="zoom:50%;" />

  <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924225313911.png" alt="image-20240924225313911" style="zoom:50%;" />

  <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924225241588.png" alt="image-20240924225241588" style="zoom:50%;" />

- 链接了opencv库

  <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924223548577.png" alt="image-20240924223548577" style="zoom:50%;" />

  

#### 常用选项

1. **编译选项**：
   - `-c`：编译源文件为对象文件，但不链接。
   - `-o <file>`：指定生成的可执行文件的名称。

2. **包含目录**：
   - `-I <directory>`：指定头文件搜索路径。
   - <img src="/home/laurent/.config/Typora/typora-user-images/image-20240924223826525.png" alt="image-20240924223826525" style="zoom:50%;" />
   
3. **库链接**：
   - `-L <directory>`：指定库文件搜索路径。
   - `-l <library>`：链接指定的库文件，例如 `-lm` 链接数学库。

4. **预处理选项**：
   - `-D <macro>`：定义一个宏，例如 `-DDEBUG`。
   - `-U <macro>`：取消定义一个宏。

5. **优化选项**：
   - `-O0`：不优化（默认）。
   - `-O1`、`-O2`、`-O3`：不同级别的优化，级别越高，优化越多。
   - `-Os`：优化以减小可执行文件的大小。

6. **调试选项**：
   - `-g`：生成调试信息，便于使用调试工具（如 `gdb`）。

7. **标准选项**：
   - `-std=c++11`、`-std=c++14`、`-std=c++17`、`-std=c++20`：指定使用的 C++ 标准版本。

8. **警告选项**：
   - `-Wall`：开启所有警告。
   - `-Werror`：将警告视为错误。
   - `-Wextra`：开启额外的警告。

9. **链接选项**：
   - `-static`：生成静态链接的可执行文件。
   - `-shared`：生成共享库（动态库）。

#### 示例

1. **编译并生成可执行文件**：
   ```bash
   g++ -o my_program main.cpp
   ```

2. **编译多个源文件并链接**：
   ```bash
   g++ -o my_program main.cpp utils.cpp
   ```

3. **编译为对象文件**：
   ```bash
   g++ -c main.cpp
   ```

4. **使用头文件和库**：
   ```bash
   g++ -I include -L lib -o my_program main.cpp -lmylib
   ```

5. **开启调试信息并使用特定标准**：
   ```bash
   g++ -g -std=c++17 -o my_program main.cpp
   ```

### 4. CMake

- 在vscode里创建CMakeLists.txt
- 基本语句：
  - `cmake_minimun_required(VERSION 3.0)`：指定cmake最低版本
  - `project(项目名称)`
  - `set(CMAKE_CXX_STANDARD 17)`：指定c++标准
  - `file(GLOB SRC_LIST 源文件路径)`：其中，SRC_LIST是一个变量，名字随意，将所有源文件路径收集到一个列表里，方便后面使用
  - `include_directories(头文件所在的目录)`：告诉编译器需要查找头文件时去该目录下寻找
  - `add_executable(生成可执行文件的名字 源文件列表)`：用于生成可执行文件

![image-20240924153752034](/home/laurent/.config/Typora/typora-user-images/image-20240924153752034.png)

![image-20240924153724068](/home/laurent/.config/Typora/typora-user-images/image-20240924153724068.png)

<img src="/home/laurent/.config/Typora/typora-user-images/image-20240924153705124.png" alt="image-20240924153705124" style="zoom:50%;" />
