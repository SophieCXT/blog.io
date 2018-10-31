---
layout: post
title: SSD1-Review of the Knowledge Points(3)
date: 2016-1-12
categories: blog
tags: Software Systems Development1(SSD1)
description: SSD1-Review of the Knowledge Points. From Chapter_01 to Chapter_09.
---

# 流程控制

- Java中的流控制语句
分支语句：if…else, switch, break, return
循环语句：while, do…while, for, continue
异常处理语句：try…catch…finally, throw


## if语句

布尔表达式是任意一个返回布尔型数据的表达式
每个单一的语句后面必须有分号
语句statement1和statement2可以为复合语句，也可以是一条语句
```$xslt
    if(i>1)
	System.out.println("i>1");
    else
	System.out.println("i<=1");

    if(i>1){
      i=0;
	System.out.println("i>1");
    }
    else
	System.out.println("i<=1");
```
- 嵌套if语句
条件表达式从上而下被求值，一旦找到为真的条件，则执行与它关联的语句，而其他的部分被忽略了。
如果所有的条件都不为真，则执行最后的else语句。
```$xslt
 if(条件)
 		statement1;
 else if(条件)	statement2;
 ……
 else 	statement2;
```
```$xslt
class IfElse {
     public static void main(String args[]) {
           int month = 4; // April
          String season;
          if(month == 12 || month == 1 || month == 2)
                    season = "Winter";
          else if(month == 3 || month == 4 || month == 5)
                     season = "Spring";
          else if(month == 6 || month == 7 || month == 8)
                    season = "Summer";
          else if(month == 9 || month == 10 || month == 11)
                    season = "Autumn";
          else
                    season = "Bogus Month";
          System.out.println("April is in the " + season + ".");
       }
}
```
## while语句
- 条件可以是任何布尔表达式。只要条件表达式为真，循环体就被执行。当条件为假时，程序控制就传递到循环后面紧跟的语句行。
- 如果只有单个语句需要重复，则不需要大括号，否则需要大括号。

 >while(条件)
 		statement;

```$xslt
class While {
    public static void main(String args[]) {
         int n = 10; 
         while(n > 0) {
               System.out.println(“Numer" + n);
               n--;
          }
         n = 10;
         while(n-- > 0);   //while体可以为空语句
     }
}
```
## for语句
> for( initialization; condition; iteration[计算机]循环) {
     // body
 }
```$xslt
int n;
for(n=10; n>0; n--)
            System.out.println(“number " + n);

//在for循环中声明循环控制变量
for(int n=10; n>0; n--)
     System.out.println("tick " + n);

//使用逗号
for(a=1, b=4; a<b; a++, b--) {
     System.out.println("a = " + a);
     System.out.println("b = " + b);
}
```
- for语句的嵌套循环

```$xslt
// Loops may be nested.
class Nested {
    public static void main(String args[]) {
         int i, j;
         for(i=0; i<10; i++) {
            for(j=i; j<10; j++)
                 System.out.print(".");
            System.out.println();
         }
     }
}
```

## switch语句
switch语句是java的多路分支语句
它提供一种基于一个表达式的值来使程序执行不同部分的简单方法
它提供了一个比一系列if-else-if语句更好的选择

```$xslt
 switch(expression){
	   case value1:
		  //statement1
   	  break;
		……
	   case valueN:
		 //statementN
	     break;   default:
		 //default statement
}

class SampleSwitch {
    public static void main(String args[]) {
         for(int i=0; i<6; i++)
             switch(i){
                 case 0:
                    System.out.println(“i is zero”);
		   break;
	        case 1:
		     System.out.println(“i is one”);
		   break;
	        case 2:
		   System.out.println(“i is two”);
		   break;
  	       default:
		     System.out.println(“i is greater 
                        than two”);
		   break;}
}
```

## 跳转语句
- Java 支持三种跳转语句
※ break
※ continue
※ return
这些语句把控制转移到程序的其他部分
- Java还支持另一种能改变程序执行流程的方法:通过异常处理。异常处理提供了一种结构化的方法，通过该方法可以使你的程序捕获并处理运行时刻错误。它由五个关键字来控制：try，catch，throw，throws，和 finally。

## 使用break语句
- 使用break语句可以强行退出循环，忽略循环体中的任何其他语句和循环的条件测试。在循环中遇到break语句时，循环被终止，程序控制在循环后面的语句重新开始。
- break语句能用于任何 Java循环中，包括人们有意设置的无限循环。
```$xslt
class BreakLoop {
      public static void main(String args[]) {
            for(int i=0; i<100; i++) {
                 if(i == 10) break; 			         
                 System.out.println("i: " + i);
             }
            System.out.println("Loop complete.");
       }
}
//在一系列嵌套循环中使用break语句时，它将仅仅终止最里面//的循环。
class BreakLoop {
   public static void main(String args[]) {
      for(int i=0; i<3; i++) {
          System.out.print("Pass " + i + ": ");
          for(int j=0; j<100; j++) {
                if(j == 10) break; 
                System.out.print(j + " ");
          }
          System.out.println();
      }
      System.out.println("Loops complete.");
}
}
```
- 注意
首先，一个循环中可以有一个以上的break语句。但要小心，太多的break语句会破坏代码结构。
其次，switch语句中的break仅仅影响该switch语句，而不会影响其中的任何循环。
break不是被设计来提供一种正常的循环终止的方法。循环的条件语句是专门用来终止循环的。只有在某类特殊的情况下，才用break语句来取消一个循环。

## continue语句
```$xslt
class Continue {
     public static void main(String args[]) {
         for(int i=0; i<10; i++) {
             System.out.print(i + " ");
             if (i%2 == 0) continue;
             System.out.println("");
		    }
     }
}
```
- continue强迫一个循环提早反复，也即，继续运行循环，但是要忽略这次重复剩余的循环体的语句。
- continue语句是break语句的补充
※ 在while循环中，continue语句使控制直接转移给控制循环的条件表达式，然后继续循环过程。
※ 在for循环中，循环的反复表达式被求值，然后执行条件表达式，循环继续执行。

## return语句
- return语句用来明确地从一个方法返回，也就是，return语句使程序控制返回到调用它的方法。
- 在一个方法的任何时间，return语句可被用来使正在执行的分支程序返回到调用它的方法。
```$xslt
class ReturnStatement {
      public static void main(String args[]) {
          boolean t = true;
          System.out.println("Before the  
                    return.");
          if(t) return; // return to caller
          System.out.println("This won't       
                    execute.");
    }
}
```



















