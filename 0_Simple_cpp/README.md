## Table of Content
### A. C++ Basics
#### 2.Basic of C++
🔭🔭🔭 C++ program can be seen as a set of objects where they can interact C++ 程序能被看作互相交互的一系列对象
- Object: Object is of status and action and object is the instance of a class 对象是 ‘状态’ ‘动作’，对象是类的实例
- Class: A template of any instances 任意实例的模版
- Method: also known as a function 方法也是一种函数
- Instant Variable: determining the status of an object 决定了对象的状态

#### 📌The structure of a C++ program C++ 程序的结构
```C++
#include <iostream>
using namespace std; //“std” is an abbreviation for standard
// main() is the Main entry of a C++ program C++ 程序主要入口

int main()
{
  count << "Hello World"; //output Hello World
  return 0;
}
```
- header #include <iostream>, the decoration at the beginning of the `.cpp` file. it is either a library or a header file `.h`.
- namespace `using namespace std` tell the compiler which namespace to use.
- main function `int main()`, the main function is a `int` type function.
- return value `return 0`, it means this program run successfully.

#### 📌Identifier 
##### The name you assign in C++

#### 📌Trigraph 三位一体

what is the purpose of trigraph?
>##### convert some symbols to other symbols.(for some keyboard missing some symbols)

what is trigraph anyway?
>##### trigraph always starts with `??` which implies this is trigraph, and it takes the **3** symbols into **1** symbols
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
#### ⚠️trigraph is deprecated function of C++. If you compile in VS IDE, the warning will be prompted.
#### 📌📌Space in C++
##### Not like shell scripting, the space in C++ will be ignored.

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
                   
##### the output will be
```C++
1: yes
2: yes
3: yes
```


#### 3.Data Type 数据类型
##### 📌📌Fundamental Primitive Data Type
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
it literally define a type with custom name. The syntax is
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

##### 📌📌Type decorator
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
return how many bytes will be taken of e.g.
```C++
cout << "boolean type takes：" << sizeof(bool) << " bytes";
```  
The answer is 1 Byte.

##### 📌📌Enumeration枚举
it is a set of enumerated constants.
The patterns declaring `enum` is
```C++
enum enum_name{identifier1, identifier2, identifier3} var_name;
```
Therefore, you can declare an `enum` like this:
```C++
enum color {red, green, blue} c;
c = blue;   
```

the default constant for the elements start from 0,1,2,...n. But you can also overwrite this default values.
```C++
enum color { red, green=5, blue };
```
##### 📌📌Difference between `typedef` and `#define`
> 1.Different in execute time
`typedef` executes in compiling therefore `type-check` will be associated.
`#define` is a marco, It executes in linking. It literally replace A to B.
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
  
#### 4.Variable Type 变量类型
#### 5.Scope of Variable 变量的域
#### 6.Constant/Literals 
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
