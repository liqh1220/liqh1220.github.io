# 准备

[toc]

## 相关的内容

### 代码风格

主要是设计变量命名格式,缩进,函数等等 coding style. cstyle, 有谷歌的风格,也有linux 风格,或者 gnu 风格.主要是看你的智能格式化等等.

## 资源

* 课件
* 软件 编辑器; 编译器; 调试器;
* 源码
* 书籍
* 视频

## 风格

* 列宽长度

一般长80个字符. stty size: columns x lines 24*80

* 评论

单行和多行评论, 解释变量的设置或者 函数的功能,作者,参数,时间等.

* 库头文件

按字母顺序列出

* 条件

缩进4空格, 大括号单独一行,

* 有限条件

大括号单独一行,每次缩进4空格.

* 函数

声明 main 函数,  

```c
int main(int argc, char *argv[]);
int main(int argc, string argv[]);
int main(int argc, char **argv[]);
// 任选一种写法
```



* 缩进

  一次缩进4空格

* 循环

循环变量一般使用 ijk 三个变量, 如果循环层次太深,考虑重新设计. 

```c
while (condition)
{
 // do something
}

do
{
	// do something
}
while (condition);


```



* 指针

```c

int *p;
// 指针符号紧跟变量名
```



* 变量

变量尽量不适用全局变量,在实际需要情况下使用. 变量命名格式 ``is_ready``

* 结构体

```c

typedef struct
{
	string name;
    string dorm;
} student;
```

* 文件

将程序合理分割成多个文件, 根据算法分割成多个函数. 尽量每个函数大小简洁.

## 软件准备

集成开发环境, 具备自动格式化,自动补全,语法高亮等特性.

* clang/gcc/msvc
* visual studio community 2022
* clion
* codeblocks等

## 语言标准

多个版本,

* c89
* c99
* c11
* c17
* c2x

具体使用 gcc 编译器,命令行参数执行, clang 一般兼容.

```powershell
gcc -g -Wall -std=c17 path/to/source/ -o path/to/execute -lmath
```

源代码 -> 预处理 -> 汇编 -> 编译 -> 链接 -> 执行

