## Table of Content
### A. C++ Basics
#### 2.Basic of C++
🔭🔭🔭 C++ program can be seen as a set of objects where they can interact C++ 程序能被看作互相交互的一系列对象
- Object: Object is of status and action and object is the instance of a class 对象是 ‘状态’ ‘动作’，对象是类的实例
- Class: A template of any instances 任意实例的一个模版
- Method: also known as a function 方法也是一种函数
- Instant Variable: determining the status of an object 决定了一个对象的状态

#### 📌The structure of a C++ program C++ 程序的结构
```C++
#include <iostream>
using namespace std; //“std” is an abbreviation for standard “std” 是 standard 的缩写
// main() is the Main entry of a C++ program C++ 程序主要入口

int main()
{
  count << "Hello World"; //output Hello World
  return 0;
}
```
- header #include <iostream>, the decoration at the beginning of the `.cpp` file. it is either a library or a header file `.h`. 是一个库或者是一个头文件
- namespace `using namespace std` tell the compiler which namespace to use. 告诉编译器使用哪个命名空间
- main function `int main()`, the main function is a `int` type function. 主函数 `int main()` 是 `int` 类型的主函数
- return value `return 0`, it means this program runs successfully. 回传值 `return 0` 意味着这个程序成功运行

#### 📌Identifier 标识符  
##### The name you assign in C++ assign 分配的名称

#### 📌Trigraph 三位一体

what is the purpose of trigraph? trigraph 的目的是什么？
>##### convert some symbols to other symbols.(for some keyboard missing some symbols) 转换一些符号到其他的符号，（一些键盘上缺失的符号）

what is trigraph anyway? 
>##### trigraph always starts with `??` which implies this is trigraph, and it takes the **3** symbols into **1** symbols 以 `??` 开始，暗示这是一个trigraph
|S.No.|Trigraph|Equivalent|
|-----|--------|----------|
|1.   |??=     |#         | 
|2.   |??/     |\         |
|3.   |??’     |^         |
|4.   |??(     |[         |
|5.   |??)     |]         |
|6.   |??!     ||         |
|7.   |??<     |{         |
|8.   |??>     |}         |
|9.   |??-     |~         |
#### ⚠️trigraph is deprecated function of C++. If you compile in VS IDE, the warning will be prompted. trigraph 是被弃用的函数，如果在VS 编译，会出现warning
#### 📌📌Space in C++
##### Not like shell scripting, the space in C++ will be ignored. C++ 中的 space 会被 ignored

#### 📌📌Comments
##### single line comments
```C++
//Single line comment 
```

#### 📌📌Block of comments
```C++
/*
 * This
 * is 
 * a block of comments
 */
```
#### 📌📌Conditional inclusion 条件包含
##### it uses `#ifdef`
```C++
#ifdef 
#include <iostream>

int main()
{
  //check something is defined?
  #ifdef ABCD
      std::cout << "1: yes\n";
   #else
      std::cout << "1: no\n";
  #endif
  
  //check something is NOT defined?
  #ifdef ABCD
      std::cout << "2: no1\n";
  #elif ABCD == 2
      std::cout << "2: yes\n";
  #else
      std::cout << "2: no2\n";
  #endif
  
  //check logic AND
  #if !defined(DCBA) && (ABCD < 2*4-3)
      std::cout << "3: yes\n";
  #endif
}  
```
                   
##### the output will be 输出为
```C++
1: yes
2: yes
3: yes
```


#### 3.Data Type 数据类型
##### 📌📌Fundamental Primitive Data Type 基础元数据类型
|Type|Keywords|
|--------|----------|
|Boolean      |`bool`      | 
|Character    |`char`      |
|Integer      |`int`       |
|Floating type  |`float`     |
|Double-precision type  |`double`    |
|Void     |`void`      |
|Wide character     |     |
                   
##### 📌📌What is `typedef`
it literally define a type with custom name. The syntax is 实际定义了具有自定义名称的类型，它的语法是
```C++
typedef <type> <new_name>;
```
e.g. `wchar_t` is combined with `short` and `int`.
```C++
typedef short int wchar_t;
```
  
e.g. you can rename `int`. Now `feet` and `int` are the same.
```C++
typedef int feet;
feet age;
```

##### 📌📌Type decorator 类型装饰器
This can be conceived as the **adjective**形容词 of type
- signed
- unsigned
- short
- long

##### 📌📌Frequently Used Data Type
|Type             |Length   |Range                            |
|-----------------|---------|---------------------------------|
|`char`           |1 Byte   |-128 to 127 or 0 to 255          |
|`unsigned char`  |1 Byte   |0 to 255                         |
|`signed char`    |1 Byte 	|-128 to 127                      |
|`int`            |4 Byte 	|-2147483648 to 2147483647        |
|`unsigned int`   |4 Byte 	|0 to 4294967295                  |
|`signed int`     |4 Byte   |-2147483648 to 2147483647        |
|`signed int`     |4 Byte   |-2147483648 to 2147483647        |
|`short int`      |2 Byte 	|-32768 to 32767                  |
|`unsigned short int` |2 Byte|0 to 65,535                     |
|`signed short int`   |2 Byte|-32768 to 32767                 |
|`long int`           |8 Byte|-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|
|`signed long int`    |8 Byte|-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|
|`unsigned long int`  |8 Byte|0 to 18,446,744,073,709,551,615 |
|`float`              |4 Byte|4 Byte（32-bits），+/- 3.4e +/- 38 (~7 characters long number)|
|`double`             |8 Byte|8 Byte（6-bits），+/- 1.7e +/- 308 (~15 characters long number)|
|`long double`        |16 Byte 	|16 Byte（128-bits），18-19 characters long number|
|wchar_t          |2 or 4 Byte 	|1 wide character             |
  
##### 📌📌`sizeof()`
return how many bytes will be taken of e.g. 回传占据多少位
```C++
cout << "boolean type takes：" << sizeof(bool) << " bytes";
```  
The answer is 1 Byte.

##### 📌📌Enumeration枚举
it is a set of enumerated constants. 一系列可枚举的常量
The patterns declaring `enum` is 模式声明 
```C++
enum enum_name{identifier1, identifier2, identifier3} var_name;
```
Therefore, you can declare an `enum` like this: 因此，你能声明 一个 `enum`
```C++
enum color {red, green, blue} c;
c = blue;   
```

the default constant for the elements start from 0,1,2,...n. But you can also overwrite this default values. 默认元素的常量 从 0,1,2,...n. 但你可以重写这些默认常量
```C++
enum color { red, green=5, blue };
```
##### 📌📌Difference between `typedef` and `#define` 差别
> 1.Different in execute time 执行时间上的

`typedef` executes in compiling therefore `type-check` will be associated.

`#define` is a marco,一个宏 It executes in linking.执行链接 It literally replace A to B. 由 A 替代为 B

```C++
typedef unsigned int UINT;
 
void func()
{
    UINT value = "abc"; // error C2440: 'initializing' : cannot convert from 'const char [4]' to 'UINT'
    cout << value << endl;
}
```

```C++
// #define example
#define f(x) x*x
int main()
{
  int a=6, b=2, c;
  c= f(a) / f(b);
  printf("%d/n", c);
  return 0;
}  
```

> 2.Different in their function

`typedef` define the **alias** of something, its definition is not relevant to the data type. 定义某事, 其定义与数据类型不相关

`#define` not only can giving an **alias** but also can define **constant**, **variable**, **option of compile**.

> 3.Different in their scope

`typedef` has its own scope.

`#define` does not have a scope.

``` C++
// typedef only affect its scope
void method1()
{
    typedef unsigned int UINT;
}

void method2()
{
    UINT uValue = 5;//error C2065: 'UINT' : undeclared identifier
}
}
```


``` C++
// #define can apply out of its scope
void method1()
{
    #define HW "HelloWorld";
}
void method2()
{
    string str = HW;
    cout << str << endl;
}
```
> 4. Different in pointers

``` C++
typedef int * pint;
#define PINT int *

int i1 = 1, i2 = 2;

const pin p1 = &i1;    //change of p[x], what p points to [√], equivalent to int * const p;
const pin p2 = &i2;    //change of p[√], what p points to [x], equivalent to const int *p; or int const *p;

pint s1, s2;           //s1 and s2 are of pointer
PINST s3, s4;          //equivalent to int * s3, s4; there is only 1 pointer

void TestPointer()
{
    cout << "p1:" << p1 << "  *p1:" << *p1 << endl;
    //p1 = &i2; //error C3892: 'p1' : you cannot assign to a variable that is const
    *p1 = 5;
    cout << "p1:" << p1 << "  *p1:" << *p1 << endl;

    cout << "p2:" << p2 << "  *p2:" << *p2 << endl;
    //*p2 = 10; //error C3892: 'p2' : you cannot assign to a variable that is const
    p2 = &i1;
    cout << "p2:" << p2 << "  *p2:" << *p2 << endl;
}
```

#### 4.Variable Type 变量类型
a variable is really nothing more than the name of a storage area. 一个变量无非就是一个存储区域的名称

Each variable in C++ has a specified type, and the type determines the size and location of the variable's storage. 每个变量在 C++ 中都有一个特定的类型，类型决定了变量存储的 大小 和 位置

|Type|Description|
|--------|-----------|
|`bool`||
|`char`||
|`int`||
|`float`||
|`double`||
|`void`||
|`wchar_t`||

#### 5.Scope of Variable 变量的域
🔭🔭🔭 Big picture: A trick to find out the scope of a variable - The variable only affects inside its nearest curly bracket `{}` 找到变量的域 - 变量只会影响最近 `{}` 的内部
> #### Local
```C++
#include <iostream>
using namespace std;

int main ()
{
  // declare/define local variable 声明/定义局部变量
  int a, b;
  int c;

  // init
  a = 10;
  b = 20;
  c = a + b;

  cout << c;

  return 0; 
}
```
> #### Global
```C++
#include <iostream>
using namespace std;

// declare global variable
int g;

int main()
{
  // declare local
  int a, b;

  // int
  a = 10;
  b = 20;
  g = a + b;

  cout << g;

  return 0;
}
```

> #### :warning: Unlike C#, you can declare one variable twice in global and local scope. BUT! The local will overwrite global one.

📌Initial value
|Data Type|Initial Value|
|---------|-------------|
|`int`    |0            |
|`char`   |'\0'         |
|`float`  |0            |
|`double` |0            |
|`pointer`|             |

#### 6.Constant/Literals
There are some general knowledge listing here. In computers, there are 3 different types of integer.
此处列出了一些常识，在计算机中，3种类型的整数

> #### Prefix 字首
` ` nothing before a number, **decimal** - 10 进制

`0` before a number, octal - 8 进制

`0x` or `0X` before a number, hexadecimal - 16 进制

> #### Suffix 后缀
`U` or `u` behind a number, **unsigned** value 

`L` or `l` behind a number, **long** value

📌Integer Literals 整数文字

```C++
85        // decimal
0213      // octal
0x4b      // hexadecimal

30        // integer
30u       // unsigned integer
30l       // long integer
30ul      // unsigned long integer
```

📌 Floating Literals 浮点数文字
a floating-point constant consists of an **integer part** 整数部分

**a decimal separator** 小数点

**a decimal** 小数部分, 

& an **exponential part** 指数部分

You can use either the ***decimal form*** or the ***exponential form*** to represent floating-point constants 能使用 ***小数点 形式*** 或 ***指数 形式***

📌

#### 7.Modifier
#### 8.Storage Class
#### 9.Operators
#### 10.Loop Types
#### 11.Decision Making
#### 12.Functions
#### 13.Numbers
#### 14.Arrays
#### 15.Arrays Advanced
#### 16.Strings
#### 17.Pointers
#### 18.Advanced Pointers
#### 19.References 
#### 20.Date& Time 📅& ⌚️
#### 21.Basic Input/Output 基本输入/输出
#### 22.Data Structure 数据结构

### B. C++ Object Oriented
#### 1.Classes& Objects 类& 对象
#### 2.Advanced Classes 高级类
#### 3.Inheritance 继承
#### 4.Overloading 
#### 5.Advanced Overloading
#### 6.Polymorphism 多态
#### 7.Abstraction 抽象化
#### 8.Data Encapsulation 数据封装📦

### C. C++ Advanced

### D. Disk Drive C
####
