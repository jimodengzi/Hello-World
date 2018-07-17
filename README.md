# Hello-World
这是我github上的java code (包含24种编程语言)

01. Java

环境: JDK1.7
C:\>java -version   
java version "1.7.0_51"  
Java(TM) SE Runtime Environment (build 1.7.0_51-b13)  
Java HotSpot(TM) Client VM (build 24.51-b03, mixed mode, sharing)

代码: 
#FileName: HelloWorld.java  
public class HelloWorld   #如果有 public 类的话，类名必须和文件同名，注意大小写  
{  
  #Java 入口程序，程序从此入口  
  public static void main(String[] args)  
  {  
  #向控制台打印一条语句  
    System.out.println("Hello,World!");  
  }  
} 

说明：
D:\HelloWorld>javac HelloWorld.java    #用 javac 编译成字节码文件（HelloWorld.class）  
D:\HelloWorld>java HelloWorld          #用 java 解释执行成特定平台的机器码  
Hello,World!  

02. C
 环境: MinGW 或各种 C/C++ 编译器

D:\HelloWorld>gcc -v  
Reading specs from C:/Perl/site/lib/auto/MinGW/bin/../lib/gcc/mingw32/3.4.5/specs  
Configured with: ../gcc-3.4.5-20060117-3/configure --with-gcc --with-gnu-ld --with-gnu-as --host=min  
gw32 --target=mingw32 --prefix=/mingw --enable-threads --disable-nls --enable-languages=c,c++,f77,ad  
a,objc,java --disable-win32-registry --disable-shared --enable-sjlj-exceptions --enable-libgcj --dis  
able-java-awt --without-x --enable-java-gc=boehm --disable-libgcj-debug --enable-interpreter --enabl  
e-hash-synchronization --enable-libstdcxx-debug  
Thread model: win32  
gcc version 3.4.5 (mingw-vista special r3)  

代码: 

#include <stdio.h>  
int main()                #main 入口函数  
{  
  printf("Hello,World!"); #printf 函数打印  
  return 1;               #函数返回值  
}  

说明：

D:\HelloWorld>gcc HelloWorld.c -o output   #文件名 HelloWorld.c，-o 输出文件名 output  
HelloWorld.c:6:2: warning: no newline at end of file  
  
D:\HelloWorld>output                       #直接运行输出文件               
Hello,World!

#如果未安装 GCC，那么必须按照 http://gcc.gnu.org/install/ 上的详细说明安装 GCC。  
#为了在 Windows 上安装 GCC，需要安装 MinGW。
#为了安装 MinGW，请访问 MinGW 的主页 www.mingw.org，进入 MinGW 下载页面，下载最新版本的 MinGW 安装程序，命名格式为 MinGW-<version>.exe。  
#当安装 MinWG 时，至少要安装 gcc-core、gcc-g++、binutils 和 MinGW runtime，但是一般情况下都会安装更多其他的项。    
#添加您安装的 MinGW 的 bin 子目录到您的 PATH 环境变量中，这样您就可以在命令行中通过简单的名称来指定这些工具。    
#当完成安装时，就可以从 Windows 命令行上运行 gcc、g++、ar、ranlib、dlltool 和其他一些 GNU 工具。

03. C++

环境: MinGW 或各种 C++ 编译器

头文件后缀名：.h、.hpp、.hxx
源文件后缀名：.cpp、.c++、.cxx、.cc、.C

代码:

#include <iostream>               //std::cout 要用到的头文件  
#include <stdio.h>                //标准输入输出头文件  
  
int main()  
{  
  printf("Hello,World!--Way 1\n");    //printf 语句打印  
  puts("Hello,World!--Way 2");        //puts 语句  
  puts("Hello," " " "World!--Way 3"); //字符串拼接  
  std::cout << "Hello,World!--Way 4" << std::endl; //C++ 教科书上写法  
  return 1;                                        //作为注释  
} 

说明：

D:\HelloWorld>g++ HelloWorld.c++ -o output   //源文件后缀也可为 .cpp、.C  
  
D:\HelloWorld>output  
Hello,World!--Way 1  
Hello,World!--Way 2  
Hello,World!--Way 3  
Hello,World!--Way 4

04. Python

环境: Python 2.x 或 Python 3.x

D:\HelloWorld>python  
Python 2.7.4 (default, Apr  6 2013, 19:55:15) [MSC v.1500 64 bit (AMD64)] on win32  
Type "help", "copyright", "credits" or "license" for more information.  

代码：

>>>> print "Hello,World!"   #Python 2.x  
Hello,World!  
>>> print("Hello,World!")  #Python 3.x    
Hello,World!  

说明:

1. 在 Python 3.x 中，print 语句是函数，所以为 print()。
2. 也可以写在 .py 文件中，同样执行。
3. python2.6 及以上版本和 python3.x 基本相同，也同样可以使用 print() 来打印。
05. C#

环境：Windows

d:\HelloWorld>csc -v  
Microsoft (R) Visual C# 2005 Compiler version 8.00.50727.4927  
for Microsoft (R) Windows (R) 2005 Framework version 2.0.50727  
Copyright (C) Microsoft Corporation 2001-2005. All rights reserved.  

代码：

//FileName: HelloWorld.cs  
using System;  
class TestApp  
{  
  public static void Main()  
  {  
    Console.WriteLine("Hello,World!");  
    Console.ReadKey();  
  }  
}  
//执行如下:  
d:\HelloWorld>csc HelloWorld.cs  
Microsoft (R) Visual C# 2005 Compiler version 8.00.50727.4927  
for Microsoft (R) Windows (R) 2005 Framework version 2.0.50727  
Copyright (C) Microsoft Corporation 2001-2005. All rights reserved.  
  
d:\HelloWorld>HelloWorld.exe  
Hello,World!  

说明：

C# 其实和 Java 非常相像，刚才用的是命令行方式，需要设置环境变量，可以参考：http://www.jb51.net/article/67171.htm。
如果是直接下载 Microsoft Visual Studio 的话，就可以在 IDE 中用快捷键编译、运行。
06. PHP

环境: XAMPP 1.8.3，环境搭建指南：http://www.cnblogs.com/wangkangluo1/archive/2011/07/19/2110943.html

代码：

<!DOCTYPE html>  
<body>  
<?php  
echo "Hello,World!";            //打印语句  
echo "The first php program!";  //打印语句  
echo phpinfo();                 //phpinfo()系统函数,输出环境信息  
?>  
</body>  
</html>  

 说明：

#PHP（Hypertext Preprocessor）。  
#PHP 是一种 HTML 内嵌式的语言，PHP 与微软的 ASP 颇有几分相似，都是一种在服务器端执行的嵌入 HTML 文档的脚本语言。  
#PHP 语言的风格类似于 C 语言，现在被很多的网站编程人员广泛地运用。  
#PHP 独特的语法混合了 C、Java、Perl 以及 PHP 自创新的语法。它可以比 CGI 或者 Perl 更快速地执行动态网页。  
#与其他的编程语言相比，PHP 是将程序嵌入到 HTML 文档中去执行，执行效率比完全生成 HTML 标记的 CGI 要高许多。  
#与同样是嵌入 HTML 文档的脚本语言 JavaScript 相比，PHP 在服务器端执行，充分利用了服务器的性能。  
#PHP 执行引擎还会将用户经常访问的 PHP 程序驻留在内存中，其他用户再一次访问这个程序时就不需要重新编译程序了，只要直接执行内存中的代码就可以了，这也是 PHP 高效率的体现之一。  
#PHP 具有非常强大的功能，所有的 CGI 或者 JavaScript 的功能，PHP 都能实现，而且几乎支持所有流行的数据库以及操作系统。   

07. JavaScript

环境: node.js 或 jaxer

node下载链接: http://nodejs.org/download/  按提示，下载自己想要的文件即可。

D:\>node -v      
v0.10.33  

代码：

var sys = require("sys");    #导入需要的 sys 模块  
sys.puts("Hello,World!");    #调用里面的 puts 函数来打印字符串  

说明：

D:\>node HelloWorld.js       #node + *.js，执行  
Hello,World!  
#JavaScript 是 Web 的编程语言。  
#所有现代的 HTML 页面都使用 JavaScript。  
#JavaScript 非常容易学。  

08. Ruby

环境: ruby 1.9.3

D:\HelloWorld>ruby -v  
ruby 1.9.3p429 (2013-05-15) [i386-mingw32]

代码：

#可用 print 语句打印  
print "Hello,World!\n"   
#可用 puts 语句打印  
puts  "Hello,World!\n"   
#可以先声明一个变量，然后再用 puts 语句  
a = "Hello,World!\n"     
puts a  
#可以先写个函数再调用  
def say(name)  
   "Hello,#{name}"  
end  
puts say("World!")

说明：

D:\HelloWorld>ruby HelloWorld.rb     #运行方式类似 Python、Perl  
Hello,World!  
Hello,World!  
Hello,World!  
Hello,World!  

09. R

环境：R-3.1.2-win（适用于32、64位），分别有相应的 GUI

C:\>R                  #安装好了之后，输入 R 后显示  
  
R version 3.1.2 (2014-10-31) -- "Pumpkin Helmet"  
Copyright (C) 2014 The R Foundation for Statistical Computing  
Platform: i386-w64-mingw32/i386 (32-bit)  
  
R  
  
'license()''licence()'  
  
R.  
'contributors()'  
'citation()'RR  
  
'demo()''help()'  
'help.start()'HTML  
'q()'R.  

 代码：

print("Hello,World!")

 说明：

R 语言，一种自由软件编程语言与操作环境，主要用于统计分析、绘图、数据挖掘。

下面是安装下载比较详细的步骤参见：

http://www.jb51.net/os/RedHat/335436.html
10. SQL

环境： ORACLE SQL/PLUS

代码：

SQL> select 'Hello,World!' from dual;  
  
'HELLO,WORLD  
------------  
Hello,World!  

说明：

还可以建一个表，插入，再查询，最后删除该表。

SQL> CREATE TABLE MESSAGE (TEXT CHAR(15));            #创建表  
INSERT INTO MESSAGE (TEXT) VALUES ('Hello, world!');  #插入表  
SELECT TEXT FROM MESSAGE;                             #查询表  
DROP TABLE MESSAGE;                                   #删除表               
Table created.  
  
SQL>  
1 row created.  
  
SQL>  
TEXT  
---------------  
Hello, world!  

11. Perl

环境：Perl 5.16 或 MinGW

下载 URL：http://www.activestate.com/activeperl/downloads

D:\HelloWorld>perl -v  
  
This is perl 5, version 16, subversion 3 (v5.16.3) built for MSWin32-x86-multi-thread  
(with 1 registered patch, see perl -V for more detail)  
  
Copyright 1987-2012, Larry Wall  
  
Binary build 1603 [296746] provided by ActiveState http://www.ActiveState.com  
Built Mar 13 2013 11:29:21  
  
Perl may be copied only under the terms of either the Artistic License or the  
GNU General Public License, which may be found in the Perl 5 source kit.  
  
Complete documentation for Perl, including FAQ lists, should be found on  
this system using "man perl" or "perldoc perl".  If you have access to the  
Internet, point your browser at http://www.perl.org/, the Perl Home Page. 

代码：

#!C:\Perl\bin                    #Windows 平台下  
#!/usr/bin/env perl              #Linux 环境下  
print "Hello,World!\n";          #print("Hello,World") 也可   

输出结果：

D:\HelloWorld>perl HelloWorld.pl #类似于 python file.py  
Hello,World!  

说明：

#Perl 5.10 及以上的版本可以用  
use 5.010;  
say "Hello,World!";  

12. HTML

环境：HTML 或 HTML 5.0

代码：

<!DOCTYPE html>  
<html>  
<body>  
<h1>This is the first program!</h1>  
<p>Hello,World!</p>  
</body>  
</html>

说明：

大多数主流浏览器都支持 HTML4.0，有些浏览器只支持 HTML5.0 的部分功能。
13. VB

环境：

VBC version 8.0.5
D:\Learn\C>vbc -v  
Microsoft (R) Visual Basic Compiler version 8.0.50727.5483  
for Microsoft (R) .NET Framework version 2.0.50727.5485  
Copyright (c) Microsoft Corporation.  All rights reserved.  
  
vbc : Command line warning BC2007 : unrecognized option 'v'; ignored  
vbc : Command line error BC2008 : no input sources specified  

代码：

'FileName: HelloWorld.rb  rb 作为 VB 源文件的后缀  
Module Hello    
  Sub Main()               '程序人口函数  
    MsgBox("Hello,World!") '计算机屏幕上显示信息  
  End Sub                  'End 作为程序块结尾  
End Module                 '单引号作为注释  

说明：

D:\>vbc HelloWorld.vb      #vbs 来编译，生成 HelloWorld.exe 可执行文件  
Microsoft (R) Visual Basic Compiler version 8.0.50727.5483  
for Microsoft (R) .NET Framework version 2.0.50727.5485  
Copyright (c) Microsoft Corporation.  All rights reserved.  
D:\>HelloWorld 

14. Scala

环境：scala-2.11.4.msi 编译器

d:\>scala  
Welcome to Scala version 2.11.4 (Java HotSpot(TM) Client VM, Java 1.7.0_51).  
Type in expressions to have them evaluated.  
Type :help for more information.  
  
scala> println("Hello,World!");   #可在交互式界面执行 println 语句，很像 java  
Hello,World!  

代码：

object HelloWorld  
{  
  def main(args:Array[String])   
  {  
     println("Hello,World!");  
  }  
}  
//编译  
d:\HelloWorld>scala HelloWorld.scala  
Hello,World!  

说明：

Scala 是一门把面向对象和函数式编程思想加入静态类型中的编程语言，志在以简练、优雅及类型安全的方式来表达常用编程模式。它平滑地集成了面向对象和函数语言的特性，使 Java 和其他语言的程序员使用 Scala 时更富有成效。
15. Shell

环境：Linux/Unix 平台，或安装了 MinGW 和 MSYS 的 Windows 平台

代码：

#安装了MinGW和MSYS的Windows平台  
D:\HelloWorld>echo "Hello,World!"  
"Hello,World!"  
#Linux平台下  
#echo "Hello,World!"   或 printf "Hello,World!"  
#如果是写在文件中:  
chmod +x  HelloWorld.sh  
./HelloWorld.sh

说明：

#Shell 诞生于 Unix，是与 Linux/Unix 交互的工具，单独地学习 Shell 是没有意义的，必须先学习 Linux/Unix。  
#Shell 虽然是 Unix 的第一个脚本语言，但它是相当优秀的。它结合了延展性与效率，持续保有独具的特色，并不断的被改良，功能更加强大。  
#缺点：Shell 需要依赖其他程序才能完成大部分的工作，优点：简洁的脚本语言标记方式，比 C 语言编写的程序执行更快、更有效率。

16. Delphi

环境：Delphi 7

代码:

[File|New|Application]-->拖一个Button、一个Label-->双击Button，编码如下：

procedure TForm1.Button1Click(Sender: TObject);  
begin  
  label1.Caption := 'Hello,World!';  
end;  
  
procedure TForm1.FormCreate(Sender: TObject);  
begin  
  
end;  
  
end.  

说明：

Delphi，是 Windows 平台下著名的快速应用程序开发工具（Rapid Application Development，简称 RAD）。
似乎很多人都觉得 Delphi 已经没落了、过时了（我身边有好多同事都没听过 Delphi）。
但我不这么认为，"真正的程序员用 C，聪明的程序员用 Delphi"，经典无需多言，尤其是开发GUI程序，拖一下就 OK 了！！！
17. Fortran

环境：Linux 或者安装了 MinGW 的 Windows 平台

D:\HelloWorld>gfortran -v  
Using built-in specs.  
COLLECT_GCC=gfortran  
COLLECT_LTO_WRAPPER=c:/mingw/bin/../libexec/gcc/mingw32/4.8.1/lto-wrapper.exe  
Target: mingw32  
Configured with: ../gcc-4.8.1/configure --prefix=/mingw --host=mingw32 --build=mingw32 --without-pic  
 --enable-shared --enable-static --with-gnu-ld --enable-lto --enable-libssp --disable-multilib --ena  
ble-languages=c,c++,fortran,objc,obj-c++,ada --disable-sjlj-exceptions --with-dwarf2 --disable-win32  
-registry --enable-libstdcxx-debug --enable-version-specific-runtime-libs --with-gmp=/usr/src/pkg/gm  
p-5.1.2-1-mingw32-src/bld --with-mpc=/usr/src/pkg/mpc-1.0.1-1-mingw32-src/bld --with-mpfr= --with-sy  
stem-zlib --with-gnu-as --enable-decimal-float=yes --enable-libgomp --enable-threads --with-libiconv  
-prefix=/mingw32 --with-libintl-prefix=/mingw --disable-bootstrap LDFLAGS=-s CFLAGS=-D_USE_32BIT_TIM  
E_T  
Thread model: win32  
gcc version 4.8.1 (GCC)  

代码：

program hello  
print *,"Hello World!"  
end program hello  

说明：

Fortran 是最早出现的计算机语言，主要用于科学及工程计算领域，这一点和 Python 相同。

D:\HelloWorld>gfortran -ffree-form HelloWorld.f -o out.exe  #-ffree-form 自由格式 -o 后面是输出文件  
#后缀名可以为.f, .F, .f90, .fpp. 如果是 .f90 结尾的文件，可以不用 -ffree-form，因为该后缀结尾的文件默认是自由格式  
D:\HelloWorld>out      #如果是 .f 结尾的话，必须要加上，否则报错  
Hello World!  

18. TCL

环境：Linux 或带有 WinGW 的 Windows 平台

代码：

#命令行交互方式  
D:\>tclsh  
% puts "Hello,World!"  
Hello,World!  
% exit  
D:>  
#文件方式运行  
#!/usr/local/bin/tcl  
puts "Hello, world!"  
D:\>tclsh HelloWorld.tcl  
Hello,World!  

说明：

1. 文件名后缀 .tcl 编译器为 tclsh（命令方式显示）或 wish（GUI方式显示）。
2. TCL（Tool Command Language）一种通用的脚本语言，几乎在所有平台都能运行，功能非常强。
19. FoxPro

环境：VFP9.0

代码：

?"Hello,World!"  

 说明：

尽管编译、运行都通过了，GUI 界面仍然不知道如何显示编译后的结果，还是在命令行界面里运行 .FXP 文件才显示的结果。
Visual FoxPro 原名 FoxBase，最初是由美国 Fox Software 公司于 1988 年推出的数据库产品，在 DOS 上运行，与 xBase 系列兼容。FoxPro 是 FoxBase 的加强版，最高版本曾出过 2.6。之后于 1992 年，Fox Software 公司被 Microsoft 收购，加以发展，使其可以在 Windows 上运行，并且更名为 Visual FoxPro。FoxPro 比 FoxBASE 在功能和性能上又有了很大的改进，主要是引入了窗口、按纽、列表框和文本框等控件，进一步提高了系统的开发能力。
20. Ada

环境：ADA95 的 gnat 编译器

d:\HelloWorld>gnat  
GNAT 4.8.1  
Copyright 1996-2013, Free Software Foundation, Inc.  
  
List of available commands  
  
gnat bind               gnatbind  
gnat chop               gnatchop  
gnat clean              gnatclean  
gnat compile            gnatmake -f -u -c  
gnat check              gnatcheck  
gnat elim               gnatelim  
gnat find               gnatfind  
gnat krunch             gnatkr  
gnat link               gnatlink  
gnat list               gnatls  
gnat make               gnatmake  
gnat metric             gnatmetric  
gnat name               gnatname  
gnat preprocess         gnatprep  
gnat pretty             gnatpp  
gnat stack              gnatstack  
gnat stub               gnatstub  
gnat test               gnattest  
gnat xref               gnatxref  

代码：

 说明：

Ada 是一种表现能力很强的通用程序设计语言，它是美国国防部为克服软件开发危机而研发的。在经过除去 # 行获得最终处理过的文件后即可交由 GNAT 编译。
21. AWK

环境：Linux/Unix 平台，或安装了 MinGW 和 MSYS 的 Windows 平台

代码：

[root@Linux ~]# echo | awk '{print "Hello,World!"}'  
Hello,World!  
[root@Linux ~]# echo | awk 'BEGIN {print "Hello,World!"}'
Hello,World!  
[root@Linux ~]# awk 'BEGIN {print "Hello,World!"}'  
Hello,World!  
[root@Linux ~]# echo "hello world" | awk '{print}'  
hello world  

说明：

#AWK 是一种优良的文本处理工具。它不仅是 Linux 中也是任何环境中现有的功能最强大的数据处理引擎之一。<br />
#AWK 名称得自于它的创始人，分别是 Alfred Aho、Peter Weinberger 和 Brian Kernighan 姓氏的首个字母。<br />
#AWK 提供了极其强大的功能：可以进行样式装入、流控制、数学运算符、进程控制语句甚至于内置的变量和函数。它具备了一个完整的语言所应具有的几乎所有精美特性。

22. Sed

环境：Linux/Unix

代码：

# sed -ne '1s/.*/Hello, world!/p'  
Hello,World!                     #第一行为输入  
Hello, world!                    #  

说明：

sed 流编辑器，和 awk、正则表达式等一起，是编写 Linux 脚本中非常有用的工具。
23. Pascal

环境：Free Pacal IDE

代码：

Program HelloWorld(output);  
begin  
  writeln('Hello, world!') 

 {程序块的最后一条语句后不需要";" - 如果添加一个";"，会在程序中增加一个“空语句”}  
end.

说明：

Pascal 程序开始于外部文件描述符作为参数的 program 关键字；然后跟着 begin 和 end 关键字封装的主要块。分号分区语句，句点终结整个程序（或单元）。Pascal 源代码是大小写不敏感的。这里是一个非常简单的"Hello world"程序示例的源代码，在实际编程中，通常可以省略第一行的output。从语法整理上来看，很像 Delphi，基本上是一个等级的。另外，FPC 编译器安装后，居然显示是乱码，看来还是要下载（Turbo Pascal）更经典些，不过听说 Turbo Pascal 下载比较难，再说，能不能在 WIN*64 位的平台编译也不知道，就下了个 FPC 用用。
24. Prolog

环境：SWI-PrologPortable 编译器

代码：

write("Hello,World!").    
#注意，句末有点号 
附录:

IEEE Spectrum 根据十多个数据来源，对各大编程语言的使用普及率进行了统计，公布了 2014 年编程语言总排行榜前二十名、Web 开发语言排行榜前十名以及移动应用开发语言排行榜前十名。统计数据结果如下:
总排行榜见图片01（后期更新中）

 Web 开发排行 TOP10：

    Java
    Python
    C#
    PHP
    JavaScript
    Ruby
    Perl
    HTML
    Scala
    Go

移动应用开发语言排行 TOP10：

    Java
    C
    C++
    C#
    JavaScript
    Objective-C
    Scala
    Delphi
    Scheme
    ActionScript

以上统计数据分别来自 Google 搜索结果、Google 趋势分析、推特、GitHub 库、StackOverflow 问答、Reddit 文章、Hacker News、Career Builder、ice job 以及 IEEE 期刊论文等。
 
