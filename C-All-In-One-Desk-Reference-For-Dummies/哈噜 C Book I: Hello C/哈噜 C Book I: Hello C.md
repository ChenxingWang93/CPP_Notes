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

#### in C, unlike other programming languages, there is no needs for END and EXIT.  //不同于其他编程语言, C不需要END & EXIT
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
##### direct the computer to display text on the screen: `puts()` function  //🖨️显示文字在屏幕🖥上
##### `puts("Greetings, human!");`

> ```C
> /**/
> #include <studio.h>
> ```

##### `#include` isn't a word in the C programming language. Instead, it's an instruction for the compiler to _include_ another file on disk,// 指示编译器包含另一个文件📃到硬盘中

##### in above case, the text is grabbed from the file named _studio.h_ , which is the standard input/output header file for the C language//C语言的I/O
##### the final complete source code for DUMB.C should looks like this: 

> ```C
> #include <studio.h>
> int main()
> {
>     puts("Greetings, human!");
>     return(0);
> }

##### it needs to be done only once to specify header file no matter how many time you use a function in C
##### but for other functions use other head files, such as MATH.H, STDLIB.H


####  - making `main()` do something  //让 `main()` 函数做点什么
##### how `puts()` file into the DUMB.C source code:
> ```C++
> #include <stdio.h>
> int main()
> {
>     puts("Greetings, human!");
>     return(0);
> }
> ```

####  The C Skeleton  // 骨架
##### Most C language source code listings start with a basic skeloton that looks like this://多数c语言代码都以基础的架构呈现
> ```C
> #include <something.h>
> int main()
> {
>     statement;
>     statement;
>     return(0);
> }
> ```

--------------------------------------------------

### **2** How It All Works//如何运行
####  C language Computer Programming Bag of Tools  //c语言
##### - A programming language  //语言
##### - An editor, to create source code files  //  编辑器
##### - A compiler and linker, to create program files  //编译器、链接器、
##### it's the compiler’s job to convert the source code files into a program.  //编译器的任务是将源代码转化为应用程序



####  - Keywords  //关键词
##### 32 keywords, some are specific programming commands directing the computer to do something  //特定计算机指令指引计算机行为
##### some are used in conjunction with other keywords to make up commands, //与其他关键词组合成指令
##### some are used to create things your program uses  //创建一些供程序使用的
##### some are antique, and a couple of them are never used!//一些是从没用过的老古董
|**Table2-1 **|**C Language Keywords C 语言关键词**|-|-|
|-------------|----------------------------------|-|-|
|auto         |double                            |int |struct |
|break        |else                              |long|switch |
|case         |enum                              |register|typedef|
|char         |extern                            |return  |union  |
|const        |float                             |short   |unsigned|
|continue     |for                               |signed  |void    |
|default      |goto                              |sizeof  |volatile|
|do           |if                                |static  |while   |


####  - Functions //函数
##### the C language, has hundreds of functions.Most programs use a common set of about 50 or so.
##### `abort();` function is used to quit program
##### `puts("Hello!");` //展示文字在屏幕上
##### `key = getchar();` //functions return information from the computer, telling u what's going on 从电脑回传的信息，告诉你进程
##### `root = sqrt(27);`  //takes a value and returns that value's square root:

####  - Operator  //操作符
##### `sum = first + second`

####  - Variables and values  //变量与值
##### use various numbers and bits of text called _strings_, they are known collectively as _values_ or _variables_,
##### 

####  - Other C language goodies //其他c 语言的优势
##### C language syntax glue the words, functions, and operators together

####  Put it Together in Editor //编辑环境
> ```C
> #include <stdio.h>
> #define TOTAL 300
> int main()
> {
>     int count;
>     for(count=0;count<TOTAL;count++)
>         printf("I think I am going to be sick!")
> }
> ```

####  - Compiler  //编译器
##### read source code file and convert the source code into _object_ code, //转化源代码为 对象代码
##### but splitting the tasks into two part: compiling &linking //但实际上分为：编译与链接🔗

<img width="495" alt="Screen Shot 2022-11-12 at 18 48 22" src="https://user-images.githubusercontent.com/31954987/201503228-79641d58-3fcd-4dc0-85a1-5dbf43bc1675.png">

### finding header files  //找到头部文件📃
#### _#include_ directive directs the compiler to insert special files into source code
#### _.H_ stands for header //.H 是header 的意思

<img width="750" alt="Screen Shot 2022-11-13 at 00 56 21" src="https://user-images.githubusercontent.com/31954987/201513843-24ca7ec5-c75f-4c92-92b9-32587cf9829c.png">

#### an object file isn't a program file. what the compiler has done is translate, or parse, the c language you typed, converting the instructions into a type of shorthand. //对象文件不是一个程序文件，编译器所做的是translate, 或者parse c语言把提示转化为 
####  gcc -c sick .c
#### type the command and press Enter. 
#### use the _dir_ or _ls_ _-l_ command to view the contents of the directory 

<img width="569" alt="Screen Shot 2022-11-13 at 01 07 28" src="https://user-images.githubusercontent.com/31954987/201514207-344c9a8c-cd70-41e4-b143-bccf4e54930a.png">


#### in Windows, a folder named _include_ branching beneath the main folder where the compiler is installed, such as `\MinGW\include` //在分支 主文件夹📁下，编译器安装
#### in Unix, the folder is `/usr/include`

##### the preprocessor includes a header file.  //预处理器包括一个头部文件
##### how _#include_ directive inserts a header file into source code; it doesn't modify the source code file itself.  //_#include_ 指令插入一个头部📃到源代码中，它并不直接修改源代码📃本身

##### linker's job is to find C language files and link them in with your object code to create the final program file. //连接器的作用：找到C语言的文件库并与对象代码建立联系来创造最终的应用程序文件📃

##### windows: _lib_ directory is found beneath the directory where ur compiler is installed. //在编译器安装的目录下
##### unix: _/usr/lib_ directory
##### for instance, to compile some high-level math function you must specifically link in a math library.  //
##### example, explains that the option you must type is _-lm_ to include the math library: //包括数学库

> ```C
> gcc -lm math_program.c -o
>    math_program
> ```

##### in this command, the _-lm_ switch directs the linker to fetch and include the math library (name _m_). That library includes the instructions necessary for the _sqrt()_ function to work // _-lm_ 切换

##### the size of the library file directly affects the size of the final program you create  //库文件的大小直接影响最后创建程序的大小
##### C language functions lives in the libraries, not in the header files  


##### to use the routines, you must both use the proper header file and link in the appropriate library for your compiler.  //合适头部文件 链接到合适的图库给编译器


####  - The object code file  //对象代码文件📃
####  - The linker  //连接器

--------------------------------------------------

### **3** More Basics,Comments, and Errors//基础、注释、&错误
####  - Putting text up on the screen //把文字打印在屏幕上
####  - Displaying hard-to-type characters  //展示难输入的字符
####  - Adding comments to your code  //添加注释到code中
####  - Avoiding nested comments  //避免 密集的注释
####  - understanding different types of errors //不同类型的错误❌
####  - fixing problems and erroes  //解决问题与错误❌
####  - displaying even more error message  //显示更多错误❌


### simple "hello" programs //简单的"hello"项目
### the STOP program  //名为 “停止🤚” 的程序
> ```C
> #include <stdio.h>
> int main()
> {
>     /*puts()函数用来展示 a string of 文字到🖥上*/
>     
>     puts("Stop: Unable to stop.");
>     return(0);
> }
> ```
// #### program uses _puts()_ function to display a string of text to the screen
#### save source code to disk as STOP.C. Compile and run the program: //

> ```C
> /**/
> Stop: Unable to stop.
> ```


###  reediting your source code //重新编辑源码
####  reedit the source code for STOP.C. Add a second _puts()_ function below the first:

> ``` C
> /*第2⃣️个put()*/
> puts(“Missing fragus found in memory.”);
> ```

### printing text with _printf()_ //使用 `printf()` 打印文字
####  _printf()_ function prints formatted text(print-formatted).This gives you more control over the outputs,


###  Introducing the newline, \n // 使用 `\n` 换行
####  \(backslash)
#### the compiler sees `\n` as one character.


###  Adding Comments, Remarks, and Suggestions //注释、马克、建议
> ``` C
> /*STOP.c source code. By Dan Gookin. February 26, 2009*/
> #include <stdio.h>
> int main()
> {
> /* NOTE: added a beep to the following line
> The \a is the Alert or bell character */
> put("\aStop: Unable to stop.");
> put("Missing fragus found in memory.");
> return(0);
> }
> ```

###  - /* C language comments */
####  - Using comments to disable code
> ``` C
> #include <stdio.h>
> int main()
> {
>     printf("The First Soloist\n\n"); /* Extra blank line */
>     printf("Vocalist Mary McDiva\n");
> /*  printf("Song, “Under the Sea.”\n"); */
> }
> ```

> ``` C
> 
> ```

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
####  


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

|Table 5-1  |C Language Text I/O Functions  | |
|-----------|-------------------------------|-|
|Function 函数 |Format 样式                    |Description 描述  |
|getchar()    |[ch = ]getchar();              |Reads a single character from the keyboard. The character is displayed and, optionally, stored in the _char_ variable _ch_. 从键盘上读取一个单一的字符。存储在_char_ 类型的名为_ch_ 的变量中|
|gets()     |gets(string);                  |read a string of text from the keyboard(terminated by the enter key.)The text is stored in the variable _string_ 文字存储在变量 _string_ 中|
|printf()   |printf("format"[,var[,var...]]);|displays formatted text according to the format string. Optional values or variables, var, can be specified to match placeholders or conversion characters in the format string.(See Appendix G for the full list.)根据格式展示格式文件。可选择的值或者变量, var, 能被声明用来匹配 占位符或者转换字符|
|putchar()  |putchar(ch);                    |displays the character _ch_ on the screen, where _ch_ is a single character in single string of text or the name of a string variable 展示 _ch_ 字符在🖥上，_ch_ 是单一字符或者escape code 
|puts()     |puts(string);                   |在🖥上展示一个text string, _string_ 是一个text在语义上的string(enclosed in double quotes) 或者是一个string 变量的名字，换句话说这个string究竟是一个text作为string还是一个变量
|scanf()    |scanf("format",&var);           |根据转化字符从键盘上读取信息in format string, 信息因此存储在变量 _var_ 中，必须要与各种字符的转化类型相匹配(例如：`int`, `float` or `char`)|
|atof()     |[numvar = ]atof(string);        |


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
