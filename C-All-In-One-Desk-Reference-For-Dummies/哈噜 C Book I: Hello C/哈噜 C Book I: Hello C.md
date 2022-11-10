### **1** Basic C Program //基础 C 程序
####  Describing the History of C //C 的历史 
##### - C++
##### - Perl
##### - Java
##### - Python
##### learn new thing, baby step 4 editing, compiling, and running a program.
##### save source code files on hard drive(`prog/c/basic`)

####  the basic, simple C program //基本、简易的C 程序
##### command for most C compilers:
##### `gcc dumb.c -o dumb`
##### all C language program is in `main()` function  //所有 C语言存在 `main()` 函数中

####  the `main()` function  //`main()` 函数
##### when the OS runs a program, OS needs to know _where_ inside the program the control needs to be passed. In the case of a C language program,  //操作系统通过寻找 `main()` 函数 在程序中传递控制指令
####  `main() {}`

#### inside the `main()` function //在main() 函数中
##### main()  //`main()` is called by the operating system when the program runs  `main()` 被操作系统called 
##### main()  //`()` contain any information typed after the program name at the command prompt 包含在命令提示符下在程序名称之后键入的任何信息
##### {}: //contain any arguments 包含任何arguments
##### the braces are used for organization // 🤔{}的作用在于组织，他们包含属于函数的programming instructions，所以本质上他们是指示
##### DUMB.C source code源代码创建了C lords称呼的 _dummy function_

#### in C, unlike other programming languages, there is no needs for END and EXIT.
#### in `main(){}`, the last `}` is the sign that program is done, after which control returns to the OS  // `}` 之后便回传到OS
#### various ways to end a program before the last brace is encountered. 诸多结束应用程式的方式：1.使用 `return` 关键词 + `abort()` 与 `exit()` 函数；
#### `return` 是 `main()` 函数的核心部分



####  Time to Program!  //
####  - the basic simple c program  //基本简单的 c 程序
####  - the `main()` function // `main()` 函数
####  - inside the `main()` function //`main()`函数内
####  - "Am I Done?"  
####  - declaring `main()` as an `int`  //`main()` 作为 `int`
##### 
##### - `void:` 一个什么都不回传的函数 a function that doesn't return anything.
##### - `int:` 一个回传一整个数字或者整数值的类型 a function that returns a whole number or _integer_ value.
##### - `char` 回传文字 a function that returns text
##### - `float` 非整数或者带小数的值的函数 A function that returns a non-whole number or value with a fractional part
##### - `double` more precise than `float` 


##### return a arctangent of an angle would be a `float` or `double` value  //回传 角的反正切值 

##### in the most of the case where main() function return to the OS is a value, therefore the proper way to define the `main()` function: //因为 `main()`函数回传的是一个 值

##### `int main() {}` is begins with `int`
##### `return()` is responsible for sending a value back from a function:
##### `return(0);`
##### direct the computer to display text on the screen: `puts()` function
##### `puts("Greetings, human!");`

####  - making `main()` do something  //让 `main()` 函数做点什么 
####  The C Skeleton  // 骨架

--------------------------------------------------

### **2** How It All Works//如何运行
####  C language  //c语言
####  - Keywords  //关键词
####  - Functions //函数
####  - Operator  //操作符
####  - Variables and values  //变量与值
####  - Other C language goodies //其他c 语言的优势
####  Put it Together in Editor //编辑环境
####  - Compiler  //编译器
####  - The object code file  //对象代码文件📃
####  - The linker  //连接器

--------------------------------------------------

### **3** More Basics,Comments, and Errors//基础、注释、&错误
####  Simple "Hello" Programs //
####  The STOP program
####  Reediting your source code  //重新编辑源码
####  Printing text with `printf()` //使用 `printf()` 打印文字
####  Introducing the newline, \n // 使用 `\n` 换行
####  Adding Comments, Remarks, and Suggestions //注释、马克、建议
####  - /* C language comments */
####  - Using comments to disable code
####  - Watch out for nested comments!  //注意⚠️注释
####  - Fixing a double-quote problem //双引号""问题
####  Debugging
####  - Prepare to fail //准备失败
####  - Dealing with linker errors  //链接🔗错误❌
####  - Run-time errors and bugs  //运行时错误❌与bugs
####  - Error messages subtle and gross //关于错误信息的细节

--------------------------------------------------

### **4** Introducing Numbers and Variables //数& 变量
####  Going Numb with Numbers
####  - The joys of integers  //整数
####  - Flying high with floating-point numbers //浮点数
####  Introduction to Variables //变量
####  - Creating variables  //创建
####  - Assigning values to variables //赋值
####  - Using an int variable //整数变量
####  - Changing a variable’s contents  //改变变量内容
####  - Using a float variable  //浮点数变量
####  - Using multiple variables  //多重变量
####  - Immediately declaring a variable’s value  //声明变量值
####  - Basic Math Operators  //基本数学运算

--------------------------------------------------

### **5** More Variables and Basic I/O //更多变量与基础I/O
####  The Good Ol’ char Variable
####  - Presenting the single character //展示单一
####  - Single quotes'' are holy too
####  - Here a char, there a char, everywhere a char char //这里一个 `char`， 那里一个 `char`， 到处都是 `char` `char` `char`
####  - Displaying characters one at a time with putchar()  //使用 `putchar()` 展示characters
####  - Using char as a tiny integer value  // char 作为 整数integer 值
####  Getting Input from the Keyboard //从键盘⌨️接收 输入
####  - Reading the keyboard one key at a time  //一次读一个 按键
####  - The problem with getchar()  // `getchar()` 的问题
####  - Clearing the input stream //输入流的 清晰
####  - Reading a chunk of text with gets() // `gets()` 读取大块 文字
####  - How to input numeric values //如何输入 数值
####  - Directly reading values with scanf()  // 用 `scanf()` 直接读取 值
####  Summary of Basic Text I/O Functions //基本 文字 I/O 函数


--------------------------------------------------

### **6** Decision Time //决定时间
####  Making Decisions with `if`  //做决定
####  - Are they equal? //是否相等
####  - The old less-than, greater-than puzzle  //
####  - Even more comparisons!  //更多对比
####  `else`, the `Anti-if` Statement 
####  Or Else!
####  Making Multiple Decisions //做多个决定
####  - `else if` to the rescue!
####  - get the order right

--------------------------------------------------

### **7** Looping //♻循环
####  Presenting the `for` Loop // `for` 循环
####  - Dissecting the `for` loop // 剖析 `for` 循环
####  - Counting to 10  //数到10
####  - Counting by twos  //两个 两个数
####  Endless Loops //♾️ 循环
####  - Your first endless loop //☝️ 个 ♾️ 循环
####  - A forever loop on purpose //有目的的 ♾️ 循环
####  - Breaking out with `break` // 打破 loop
####  Nesting Loops //
####  The 17,576 Names of God // 
####  Multiple `for` Conditions // `for` 条件

--------------------------------------------------

### **8** Constants //
####  Are Constants Necessary?  //Constants是否必要？
####  - A program example to drive home the point
####  - But then, something changes!  //
####  - Chickening out and using variables instead  //
####  Constants: The Anti-Variable! //反-变量
####  - Declaring a constant  //声明一个constant
####  - Using constants in your code  //在code里使用 constants
####  Other Things You Can #define

--------------------------------------------------

### **9** Math  //数学
####  Math Review //数学复盘
####  The Sacred Order of Precedence  //
####  - My Dear Aunt Sally
####  - What about multiple multiplications?  //多个 乘法
####  - Fooling old Sally with parentheses
####  Say It Out Loud: Unary Operators! //
####  - Going negative  //负数
####  - Getting silly
####  Incrementing and Decrementing and Loving It //增值、减值
####  - Just add one to it  //添加一个
####  - Just take one away from it
####  - Pre-incrementing and post-incrementing  
####  Other Cryptic Math Shortcuts  //其他隐秘的数学捷径
####  - Incrementing by more than one //step大于于1的 Increment
####  - Multiplying a variable by itself  //

--------------------------------------------------

### **10** Only Logical //只有逻辑
####  Comparisons from Hell
####  - YORN.C, attempt number 1  
####  - YORN.C, attempt number 2
####  - YORN.C, attempt number 3
####  Here Are Your Logical Operators, Mr. Spock! //逻辑运算
####  - Introducing Mr. Logical OR
####  - Say hello to Mr. Logical AND
####  - YORN.C, attempt number 4
####  Multiple Madness with Logical Operators 


--------------------------------------------------
