## Table of Content
### A. C++ Basics
#### 2.Basic of C++
🔭🔭🔭 C++ program can be seen as a set of objects where they can interact with

#### 📌The structure of a C++ program
```C++
#include <iostream>
using namespace std; //“std” is an abbreviation for standard
// main() is the Main entry of a C++ program

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
|
  
  
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
