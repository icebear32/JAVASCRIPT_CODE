[TOC]



# JavaScript



## 1. JavaScript是干什么的？

* HTML是基本的网页（文字 图片 视频）
* CSS通过控制布局和样式让网页更加美观
* JavaScript是给网页添加动画和一些其他的交互事件，让网页变得更加活泼。
* JavaScript跟编程语言差不多，不过它不是编程语言，它是脚本语言，它的运行不需要编译，直接由解释器解释执行。它也有变量、函数。



* JavaScript可以完成的效果
  * 数据校验（输入的密码，年龄，用户名是否符合要求）
  * 图片轮播
  * 广告弹框



## 2. 书写第一个JavaScript代码

* JavaScript的特点：

1. 语法相对来说比较简单（弱类型的变量类型）
2. 跨平台（JavaScript脚本语言不依赖于操作系统,仅需要浏览器的支持）



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			alert("Hello World!");
		</script>
	</head>
	<body>
	</body>
</html>
```

运行结果：

![image-20220311220310966](.\JavaScript学习笔记图片\1.png)



## 3. JavaScript代码书写的三种方式



### 3.1 第一种方式：网页内(可以放在网页的任意位置)

```js
<script type="text/javascript"></script>
```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		
	</head>
	<body>
		<script type="text/javascript">
			alert("Hello World!");
		</script>
	</body>
</html>
```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		
	</head>
	<body>
		
	</body>
</html>
<script type="text/javascript">
			alert("Hello World!");
		</script>
```



### 3.2 第二种方式：行内

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<font onclick="alert('你点击了我')">你好</font>
	</body>
</html>
```

![image-20220311221949374](.\JavaScript学习笔记图片\2.png)



* 多个功能用分号;隔开

```js
<font onclick="alert('你点击了我');alert('你点击了我')">你好</font><!-- 多个功能用分号;隔开 -->
```



### 3.3 第三种方式：外部引入的方式

```js
<script type="text/javascript" src="test.js" ></script>
```

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript" src="test.js"></script>
	</head>
	<body>
		
	</body>
</html>
```



* 创建 test.js 文件

```js
alert("Hello World!");
```



## 4. 函数



### 4.1 什么是函数？

* 一个函数有自己一个固定的功能，调用函数相当于调用这个功能。
* 函数有系统内置的函数，我们也可以定义自己的函数，使用这个函数实现我们想要的功能。
* 在定义函数的时候，我们需要写很多行代码来实现我们想要的功能。
* 函数可以被多次调用，我们只需要通过函数名调用即可调用响应的功能，这样就避免了每次想要调用某个功能的时候，就去书写重复的代码。



### 4.2 函数的作用：

1. 一个函数实现一个固定的功能
2. 避免重复写代码



### 4.3 函数怎么调用？

```js
xxx1(arg1,arg2,arg3);
```

函数名是定义的时候决定的，参数也是定义的时候决定的。我们想要什么功能就必须调用对应名字的函数，并且提供对应的参数。（调用别人的函数的时候，不能自己随便写函数名和参数）



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			alert("Hello World!");
			// Alert("Hello World");//运行不成功，没有定义这个函数
			//函数 function 方法 method
            
            //字符串是js中的一种数据类型
		</script>
	</head>
	<body>
	</body>
</html>
```



## 5. 字符串



### 5.1 什么是字符串？

* 几个字符（中文字符或者英文字符或者某个特殊符号比如逗号）组合在一起，组成一个串，就是字符串。
* 字符串是JavaScript中的一种数据类型。
* JavaScript中的数据是指什么呢？（字符串，数字，图片，某个运算结果等 这些都是数据）
* 每个数据都有自己的数据类型，不同的数据类型在内存中有不同的存储方式。我们只需要告诉解释器某个数据的数据类型是什么，不用管它怎么在内存中存储的。解释器（浏览器）会自动的根据这个数据的类型，把它按照响应的方式存储到内存中。



### 5.2 JavaScript中的字符串的规范

字符串必须使用单引号或者双引号括起来。



### 5.3 什么时候使用单引号，什么时候双引号呢？

（1）只使用字符的字符串（字符串不包括单引号或者双引号），单引号和双引号没有区别
（2）在包括单引号的字符串中可以直接用双引号，在包括双引号的字符串中可以直接用单引号
（3）如果在双引号包括的字符串中用双引号，需要用反斜杠转义，注意是"\"   ;同样在单引号包括的字符串中用单引号，也需要转义
（4）如果要用反斜杠，则输入‘\\’

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
            //字符串是js中的一种数据类型
            
			//alert("Hello World!");//双引号
			//alert('Hello World!');//单引号
			//alert("我的名字是'小明'");//双引号和单引号
			//alert("我的名字是\"小明\"");//转义字符
			alert('我的名字是\'小明\'');//转义字符
		</script>

	</head>
	<body>
	</body>
</html>
```



## 6. JavaScript中的数字类型

数字类型就是可以直接做数学运算（加减乘除）的数据类型。



* JavaScript中的所有数据类型

```
字符串(string)
数字(number)
布尔(boolean)
数组(array)
对象(object)
空(null)
未定义(undefined)
```



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
		   //alert(100);//可以运算
		   //alert("100");//不可以运算
		   
		   alert(typeof("100"));//输出的是string
		   alert(typeof(100));//输出的是number
		   
		</script>
	</head>
	<body>
	</body>
</html>
```



## 7. JavaScript中的变量



### 7.1 js中的变量声明

变量里面存储的是一个数据，使用变量，相当于使用这个变量里面的数据！

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//var str = "Hello World!";//定义变量
			
			//反复调用可以减少书写代码效率
			// var str = "sdhaijsdoajsiodadsakj";
			// alert(str);
			// alert(str);
			// alert(str);
			
			// alert(sdhaijsdoajsiodadsakj);
			// alert(sdhaijsdoajsiodadsakj);
			// alert(sdhaijsdoajsiodadsakj);
			
			// = 赋值运算符 var用来定义变量的 varible
            //在某些情况下，我们需要存储的数据是变化的，比如玩游戏的时候的分数。
			var score = 0;
			score = 30;
			score = 40;
			alert(score);
			
		</script>
	</head>
	<body>
	</body>
</html>
```



### 7.2 注意事项：(JavaScript是弱类型的语言)

* 变量声明的时候不需要指定类型
* 变量的类型是由这个变量里面的值决定的
* 变量可以存储不同类型的数据
* 变量的声明不是必须的

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// var score;
			// alert(score);//变量被声明，但是没有赋值 undefined
			// score = 0;//变量第一次被赋值的时候 成为初始化
			//
			// score = 0;（变量的声明不是必须的）
			// alert(score);
			
			//var a = 100;var b = 50;var c = 20;
			var a = 100, b = 50, c = 20;//两种形式都可以
			alert(a);
			alert(b);
			
		</script>
	</head>
	<body>
	</body>
</html>

```



### 7.3 JavaScript变量命名规则

1. 变量必须以字母开头
2. 变量也能以 $ 和 _ 符号开头（不推荐）
3. 变量名称对大小写敏感（y 和 Y 是不同的变量）
4. 不能使用关键字



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//JavaScript变量命名规则
			//var a = 100;
			
			//运行不成功
			// var 1a = 100;
			// alert(1a);
			
			//合法		a	a1	$a _a	_age	$	good_price	a A		
			//不合法	1	1a  a-
			
			//驼峰命名法：goodPrice dogAge	good_price	dog_age
			
		</script>
	</head>
	<body>
	</body>
</html>

```

打开浏览器使用检查功能查看代码是否错误

![image-20220312170201023](.\JavaScript学习笔记图片\3.png)



## 8. 算术运算符

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			var a = 10;
			var b = 20;

			var res1 = a + b;
			var res2 = a - b;
			var res3 = a * b;
			var res4 = a / b;
			var res5 = a % b; //求余
			
			//console.log	输出到浏览器控制台
			console.log(a + b);
			console.log(res1);
			console.log(res2);
			console.log(res3);
			console.log(res4);
			console.log(res5);
			
		</script>
	</head>
	<body>
	</body>
</html>
```

![image-20220312171929277](.\JavaScript学习笔记图片\4.png)



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			var a = 10;
			var b = 20;

			// var res1 = a + b;
			// var res2 = a - b;
			// var res3 = a * b;
			// var res4 = a / b;
			// var res5 = a % b; //求余

			// //console.log	输出到浏览器控制台
			// console.log(a + b);
			// console.log(res1);
			// console.log(res2);
			// console.log(res3);
			// console.log(res4);
			// console.log(res5);

			//自增
			// a++; //  a = a + 1;
			// b++; //自增
			// console.log(a);//11
			// console.log(b);//21
			// ++a;
			// ++b; 
			// console.log(a);//12
			// console.log(b);//22

			//自减
			// a--; // a = a - 1;
			// b--;
			// console.log(a);//9
			// console.log(b);//19
			// --a; 
			// --b;
			// console.log(a);//8
			// console.log(b);//18

			// +
			// - * / % += -= *= /=	%=
			// a += 2;
			// a = a + 2;
			// console.log(a);
			
			// a -= 2;
			// a = a - 2;
			// console.log(a);
			
			// a *= 2;
			// a = a * 2;
			// console.log(a);
			
			// a /= 2;
			// a = a / 2;
			// console.log(a);
			
			// a %= 2;
			// a = a % 2;
			// console.log(a);

			// var res1 = "Hello" + "World"; // HelloWorld
			// var res2 = "Hello" + 100; //"Hello" "100" Hello100
			// var res3 = 100 + "Hello";
			// var res4 = "100" + 100;
			// var res5 = 100 + "100baidu.com"; // 200baidu.com
			// var res6 = "baidu.com" + 100 + 100; //baidu.com100100
			// console.log(res1);
			// console.log(res2);
			// console.log(res3);
			// console.log(res4); // 100 100
			// console.log(res5);
			// console.log(res6);

			var res7 = "" + a + b; 
			console.log(res7);// 1020
		</script>
	</head>
	<body>
	</body>
</html>
```



## 9. 流程控制

控制程序执行的流程，没有流程控制的话，程序默认从上到下执行！
有了流程控制，可以让程序执行某些满足条件的语句，或者重复执行某些语句！



### 9.1. if 语句

流程控制语句 if

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			hp = 100;

			//流程控制语句 if
			if (hp <= 0) {
				console.log("GameOver!");
			}
			console.log("继续");
            
            if (布尔值) {
				语句块
			}
		</script>
	</head>
	<body>
	</body>
</html>
```



条件判断语句 **if 语句**的三种方式 

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
		<script type="text/javascript">
         	var hp = 50;

			//第一种方式
			if (hp > 0) {
				console.log("继续玩游戏");
			}

			//第二种方式
			if (hp <= 0) {
				console.log("GameOver！");
			} else {
				console.log("继续玩游戏");
			}

			//第三种方式
			int season = 1;
			if (season == 1) {
				console.log("春季");
			} else if (season == 2) {
				console.log("夏季");
			} else if (season == 3) {
				console.log("秋季");
			} else {
				console.log("冬季");
			}
		</script>
	</head>
	<body>
		
	</body>
</html>
```



### 9.2 布尔类型

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			if (true) {
				console.log(true);//运行结果 - true
			}
			if (false) {
				console.log(false);//运行结果 - 判断为false，不执行
			}

			var a = true; //对 是 有 1
			var b = false; //错  不是 没有 0
		</script>
	</head>
	<body>
	</body>
</html>

```



### 9.3 比较运算符

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
        <script type="text/javascript">
            //==	===	 !=	>	<	>=	<=
            
            var n1 = 100,
				n2 = 90;

			var res1 = n1 == n2;
			var res2 = n1 != n2;
			var res3 = n1 > n2; //true
			var res4 = n1 < n2; //false
			var res5 = n1 >= n2; //true
			var res6 = n1 <= n2; //false
			console.log(res1);
			console.log(res2);
			console.log(res3);
			console.log(res4);
			console.log(res5);
			console.log(res6);

			console.log(n1 == n2); //false
			console.log(n1 === n2); //false

			console.log(100 == "100");
			console.log(100 === "100"); // 首先判断类型是否一致，再判断值是否一致
        </script>
	</head>
	<body>
		
	</body>
</html>
```



### 9.4 逻辑运算符

&&   和（and）	表示同时满足两个条件
||	或者（or）	表示满足其中一个条件

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
		<script type="text/javascript">
			var month = 2; // 1 - 12
			//2 - 5
			if (month >= 2) {
				if (month <= 5) {
					console.log("当前是春季");
				}
			}
			//如何简化代码 - 逻辑运算符

			// && 和 ||
			// && - 两边为真才是真，其中一个为假则判断不成立
			var a = 10,
				b = 20;
			var res1 = true && true;
			console.log(res1);

			// || - 其中一个为真则判断成立
			var res1 = a >= 25 || b >= 25;
			console.log(res1);

			if(month>=2 && month<=5 ){
				console.log("春季");
			}
		</script>
	</head>
	<body>
		
	</body>
</html>
```



### 9.5 switch 语句

可以有多个case

当前面的case都不满足的时候才会执行，default语句

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// var season = 3;
			// switch (season) {
			// 	case 1:
			// 		console.log("春季");
			// 		break;
			// 	case 2:
			// 		console.log("夏季")
			// 		break;
			// 	case 3:
			// 		console.log("秋季")
			// 		break;
			// 	default:
			// 		console.log("冬季")
			// 		break;
			// }
			
			// if (season == 1) {
			// 	console.log("春季");
			// } else if (season == 2) {
			// 	console.log("夏季");
			// } else if (season == 3) {
			// 	console.log("秋季");
			// } else {
			// 	console.log("冬季");
			// }

			//switch 和 if 的区别：少的流程使用switch更好，但是流程多且判断条件多则使用 if 语句
			var month = 6;

			if (month >= 2 && month <= 4) {
				console.log("春季");
			} else if (month >= 5 && month <= 7) {
				console.log("夏季");
			} else if (month >= 8 && month <= 10) {
				console.log("秋季");
			} else {
				console.log("冬季");
			}

			//代码变得冗余了
			switch (month) {
				case 2:
				case 3:
				case 4:
					console.log("春季");
					break;
				case 5:
				case 6:
				case 7:
					console.log("夏季");
					break;
				case 8:
				case 9:
				case 10:
					console.log("秋季");
					break;
				default:
					console.log("冬季");
					break;
			}

			var score = 80;
			//优秀 80-100 良好70-80 一般60-70 差小于60 - 使用 if 语句
		</script>
	</head>
	<body>
	</body>
</html>

```



### 9.6 循环语句 - for 循环

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// for (var i = 2; i <= 100; i += 2) {
			// 	// i =1  2  3 4 5 6 7 8 9 10 11
			// 	console.log(i);
			// }

			// for (初始化; 条件判断; 每次循环体执行完会执行这里) {

			// }
			for (var i = 0; i < 10; i++) {
				console.log(i);
			}
		</script>
	</head>
	<body>
	</body>
</html>
```



### 9.7 循环语句 - while 循环

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			
			//死循环
			// while (true) {
			// 	console.log("while循环体");
			// }
			
			//避免死循环，要设定判断的停止循环条件
			var i = 2;
			while (i < 101) {
				console.log(i);

				i += 2;
			}
		</script>
	</head>
	<body>
	</body>
</html>
```



### 9.8 break 和 continue

break 语句和 continue语句
目标都是距离最近的循环

* break	跳出循环
* continue	中断本次循环，继续执行下次循环

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			for (var i = 1; i <= 10; i++) {
				console.log(i);
				if (i == 5) {
					break; //终止循环
				}
			}
			console.log("遇到 break 循环结束");
			
			for (var i = 1; i <= 10; i++) {
				if (i == 5) {
					continue; //中断本次循环，继续执行下次循环
				}
				console.log(i);
			}
			console.log("循环结束");
		</script>
	</head>
	<body>
	</body>
</html>
```



### 9.9 循环嵌套

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// for (var i = 1; i <= 5; i++) {
			// 	for (var j = 1; j <= 4; j++) {
			// 		console.log("i:" + i + " j:" + j);
			// 	}
			// }

			//*     
			//**     
			//***    
			//****   
			//*****  
			for (var i = 1; i <= 5; i++) {
				var s = "";
				for (var j = 1; j <= i; j++) {
					s += "*";
				}
				console.log(s);
			}
		</script>
	</head>
	<body>
	</body>
</html>
```



## 10. 函数



### 10.1 怎么定义自己的函数？

```
function name(arg1,arg2){
}
name：名字 
arg1...：参数 
{}：函数体，也叫做语句块
```



* 用函数解决问题
  1. 创建一个函数，可以打印箭头的符号到控制台
  2. 做一个简化版的日志输出函数
  3. 实现加法（return 语句的作用）
  4. 一个函数相当于一个机器，比如抓娃娃，你投进去的是币（参数），有可能不出来任何东西，有可能出来东西。



* 函数的声明会被前置

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// console.log("数据校验第一步");
			// console.log("数据校验第二步");
			// console.log("数据校验第三步改变");
			// console.log("数据校验第四步");
			//多次使用这四条语句，会冗余，可以使用函数来解决

			//定义函数
			// function myname() {
			// 	console.log("我是函数体");
			// }
			// myname();
			
			//函数的声明会被前置，所以可以把函数调用放在前面
			datacheck();
			datacheck();
			datacheck();

			// 创建一个新的函数（ 声明函数 或者 定义函数）
			function datacheck() {
				console.log("数据校验第一步");
				console.log("数据校验第二步改变");
				console.log("数据校验第三步改变");
				console.log("数据校验第四步");
			}
			
			// datacheck();
			// datacheck();
			// datacheck();
			
		</script>
	</head>
	<body>
	</body>
</html>
```



### 10.2 函数的参数值和返回值



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">			
			function add() {
				var a = 100;
				var b = 200;
				var res = a + b;
			}
			//定义的函数要自定义变量，可以使用传入参数，实现不用自定义变量

			//名字 参数 返回值
			function add(arg1, arg2) {
				var res = arg1 + arg2;
				
				return res;//设置返回值
			}

			var res1 = add(100, 200);
			var res2 = add(80, 90);
			console.log(res1);
			console.log(res2);
		</script>
	</head>
	<body>
	</body>
</html>
```



### 10.3 匿名函数

```
function (){} 
```

因为它没有名字，所以不能调用。



* 匿名函数怎么使用呢？
  * 第一种方式：使用一个变量接收（可以认为这个变量是一个函数类型，用来指向引用一个函数）
  * 第二种方式：作为一个参数传递过去（回调函数）



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//不能直接使用匿名函数
			// function() {
			// 	console.log("我是匿名函数");
			// }

			//将匿名函数当作一个变量来使用
			// var a = function() {
			// 	console.log("我是匿名函数");
			// }
			// a();

			function attack(attackmode) {
				//console.log("我使用刀进行攻击");//写死了，使用匿名函数调用其他函数更灵活
				attackmode();
				console.log("掉血");
			}
			attack(function() {
				console.log("我使用刀进行攻击");
			});

			attack(function() {
				console.log("我使用枪进行攻击");
			});
            
             // window.alert("你好");
			// console.log();//日志打印 - 输出到控制台，日志打印，用于错误调试
			// document.write("你好");// 网页写入
		</script>
	</head>
	<body>
	</body>
</html>
```



## 11. 字符串常见操作



### 11. 1 长度、索引、大小写转换

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			var str = "heLLO world"; //子串
			str = str + "234234"; //heLLO world234234

			//1,取得长度
			console.log(str.length); //17

			//2,利用索引访问单个字符
			console.log(str[0]); //h
			console.log(str[1]); //e
			console.log(str[2]); //L
			//str[5]="-";//可以获取对应的字符，但是不能修改
			console.log(str); //heLLO world234234

			//for 循环遍历字符串每个字符
			// 0 1 2 3 4 5   str.length-1
			for (var i = 0; i < str.length; i++) {
				console.log(str[i]); //h e L L O 空格 w o r l d 2 3 4 2 3 4
			}

			//toUpperCase - 小写字母变大写字母
			var str2 = str.toUpperCase(); //对原有字符串没有影响，新字符串返回
			console.log(str); // heLLO world234234 - 原有字符串没有发生变化
			console.log(str2); // HELLO WORLD234234

			//toLowerCase - 大写字母变小写字母
			var str3 = str.toLowerCase();
			console.log(str); //heLLO world234234
			console.log(str3); //hello world234234
		</script>
	</head>
	<body>
	</body>
</html>

```



### 11.2 查找、拼接、截取

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			var str = "heLLO world"; //子串
			str = str + "234234"; //heLLO world234234

            //查找
			// var index1 = str.indexOf("world"); //如果子串存在，返回子串首字母索引，如果子串不存在 返回-1
			// console.log(index1);//6
			// var index2 = str.indexOf("worlD"); 
			// console.log(index2);//-1
			// var index3 = str.indexOf("");//空字符串
			// console.log(index3);//0
			// var index4 = str.indexOf("world",4);//4 - 代表从第四个字符开始寻找
			// console.log(index4);//6

            //拼接
			// var str2 = str + "baidu.com";
			// console.log(str2);//heLLO world234234baiedu.com

			// var str3 = str.concat("baidu.com", "!");
			// console.log(str3);//heLLO world234234baiedu.com!

            //截取
			var str = "heLLO,world,javascript,js"; //子串
			var str2 = str.slice(2, 5);//LLO - 第二个开始，最后一个不包括
			var str3 = str.slice(2);//第二个一个到最后的字符
			var str4 = str.slice(5, 3);//没有反着来的
			var str5 = str.slice(2, 40);//可以截取的范围超出字符串长度
			var str6 = str.slice(-4, -2);//可以传递负数，从后面开始数
			console.log(str2);//LLO
			console.log(str3);//LLO,world,javascript,js
			console.log(str4); //""
			console.log(str5);//LLO,world,javascript,js
			console.log(str6);//t,
		</script>
	</head>
	<body>
	</body>
</html>
```



### 11.3 第二、三种截取、去除空格

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// //第二种截取
			// var str = "heLLO,world,javascript,js"; //子串

			// var str2 = str.substring(2, 5);
			// var str3 = str.substring(2);
			// var str4 = str.substring(5, 2);
			// var str5 = str.substring(-4, -2); //str.substring(0,0)
			// console.log(str2); //LLO
			// console.log(str3); //LLO,world,javascript,js
			// console.log(str4); //LLO
			// console.log(str5); //""

			// //第三种截取
			// var str2 = str.substr(2, 3); //第二个开始,截取三个
			// var str3 = str.substr(2); //第二个开始,截取后面全部
			// console.log(str2); //LLO
			// console.log(str3); //LLO,world,javascript,js

			//分割
			var str1 = "heLLO,world,javascript,js"; //子串
			var arr11 = str1.split(",");//按照逗号进行拆分
			console.log(arr11);//['heLLO', 'world', 'javascript', 'js']
			
			var str2 = "heLLO--world--javascript--js"; //子串
			var arr22 = str2.split("--");//按照 -- 进行拆分
			console.log(arr22);//['heLLO', 'world', 'javascript', 'js']
			
			var str3 = "heLLO,world,javascript,js"; //子串
			var arr33 = str3.split(",",3);//按照逗号进行拆分,并且只截取拆分后的前三个字符串
			console.log(arr33);//['heLLO', 'world', 'javascript']

//
			var username = "  baidu com ";//前后空格去掉,中间不去掉
			var newStr = username.trim();
			console.log(username);//  baidu com 
			console.log(newStr);//baidu com
		</script>
	</head>
	<body>
	</body>
</html>
```



## 12. 正则表达式

* 正则表达式描述了一个字符串的书写规则
  * 正则表达式是一个字符串，这个字符串按照正则表达式的语法来进行书写
  * 全部是字母的字符串
  * 全部是数字的字符串
  * 以数字开头，长度为4的字符串
  * 第一字母是a第二个字母是b，没有其他字符的字符串

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			var p1 = /xxxx/;
			//规则1 	全部是字母的字符串	abc	ab12 ab_ 123_ 43ew2 sdfer
			//规则2	全部是数字的字符串	213 sdfkl 23434c adf_ 234
			//规则3 	以数字开头，长度为4的字符串 
			//规则4	第一字母是a第二个字母是b，没有其他字符的字符串	ab
		</script>
	</head>
	<body>
	</body>
</html>

```



### 12.1 正则表达式的操作方式

* 搜索
* 替换
* 判断

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//搜索 替换 判断
			// /正则表达式主体/修饰符
			// i忽略大小写 g全局匹配 m
			// var p1 = /ab/i; //  ab Ab aB AB
			// var str = "hello Abwolrd sikiedu.com ab";

             //搜索
			// //search 为一个字符串对象执行一次正则表达式搜索
			// var index = str.search(p1);//6 - 传入一个正则表达式
			// console.log(index);

			// //传入一个字符串
			// var index = str.search("ab"); //26 - 跟 indexof 函数差不多
			// console.log(index);

			var p1 = /ab/i;
			var str = "hello Abwolrd sikiedu.com ab";
			var str2 = str.replace(p1, "----"); //替换 - 将 p1正则表达式 找到匹配的，进行替换，换成----
			console.log(str2); //hello ----wolrd sikiedu.com ab

			//但是只替换一个，用修饰符 g 表示要全局匹配
			var p2 = /ab/ig;
			var str = "hello Abwolrd sikiedu.com ab";
			var str3 = str.replace(p2, "----"); 
			console.log(str3); //hello ----wolrd sikiedu.com ----

			// var res = p1.test(str);
			// console.log(res);
		</script>
	</head>
	<body>
	</body>
</html>

```



判断

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//判断
			var p1 = /ab/i;
			var str = "hello Abwolrd sikiedu.com ab";
			var res = p1.test(str);
			console.log(res);//true
		</script>
	</head>
	<body>
	</body>
</html>
```



### 12.2 正则表达式的量词、元字符、中括号

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// var p1 = /^a/;//以 a 开头的字符串
			// console.log(p1.test("abc"));//true
			// console.log(p1.test("bc"));//false
			// console.log(p1.test("bac"));//false

			// var p2 = /a$/;//以 a 结尾的字符串
			// console.log(p2.test("abca"));//true
			// console.log(p2.test("abc"));//false

			var p3 = /^a$/;
			console.log(p3.test("a"));//true
			console.log(p3.test("aaa"));//false - 因为它是判断为一个字符 a，需要加限制才可以
		</script>
	</head>
	<body>
	</body>
</html>

```



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// //中括号
			// var p4 = /[1234]/;
			// console.log(p4.test("1"));//true
			// console.log(p4.test("2"));//true
			// console.log(p4.test("3"));//true
			// console.log(p4.test("4"));//true
			// console.log(p4.test("5"));//false - 没有5
			// console.log(p4.test("11"));//true
			// console.log(p4.test("51"));//true - 有1判断为真

			// var p4 = /^[1234]$/;//认定以括号里的一个字符为首为尾
			// console.log(p4.test("1"));//true
			// console.log(p4.test("11"));//false - 不能有两个字符

			// //想要两个字符首尾
			// var p4 = /^[1234][1234]$/;
			// console.log(p4.test("11"));//true
			// console.log(p4.test("111"));//false

			// //中括号另一种方式
			// var p4 = /[1-4]/;
			// console.log(p4.test("a"));//false
			// console.log(p4.test("b"));//false
			// console.log(p4.test("3"));//true
			// console.log(p4.test("4"));//true
			// console.log(p4.test("5"));//false

			// var p4 = /[a-z]/;
			// console.log(p4.test("a"));//true
			// console.log(p4.test("b"));//true
			// console.log(p4.test("3"));//false
			// console.log(p4.test("4"));//false
			// console.log(p4.test("5"));//false

			// var p5 = /\d/;// \d 相当于[0-9]
			// console.log(p5.test("1"));//true
			// console.log(p5.test("3"));//true
			// console.log(p5.test("0"));//true
			// console.log(p5.test("a"));//false

			// //正整数
			// // 1-9 0-9
			// var p6 = /^[1-9]\d*$/; //首位是 1-9，尾位是 0-9，且 * 号表示首位后面可以有多位数字
			// console.log(p6.test("0")); //false
			// console.log(p6.test("5")); //true
			// console.log(p6.test("21")); //true
			// console.log(p6.test("430")); //true
			// console.log(p6.test("-430")); //false

			// * +量词
			// * 号表示前面的字符有零个或多个
			// var p7 = /^a*/;
			// console.log(p7.test("a"));//true
			// console.log(p7.test(""));//true
			// console.log(p7.test("aa"));//true
			// console.log(p7.test("aaa"));//true
			// console.log(p7.test("b"));//true
			
			// + 号表示前面的字符至少要有一个
			// var p7 = /^a+/;
			// console.log(p7.test("a"));//true
			// console.log(p7.test(""));//false
			// console.log(p7.test("aa"));//true
			// console.log(p7.test("aaa"));//true
			// console.log(p7.test("b"));//false

			// var p8 = /^[1-9][0-9]+$/;
			// console.log(p8.test("10"));
			// console.log(p8.test("804632564"));
			// console.log(p8.test("0"));
			// console.log(p8.test("089"));
			// console.log(p8.test("100"));
		</script>
	</head>
	<body>
	</body>
</html>
```



* 使用正则表达式来判断邮箱

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//使用正则表达式来判断邮箱 xxx@xx.com  xx.org xx.net
			var p9 = /^[\w-]+(\.[\w-]+)*@[\w-]+(\.[\w-]+)+$/;
			console.log(p9.test("xxx@qq.com"));//true
			console.log(p9.test("xxx@qq.net")); //true
			console.log(p9.test("xxx@qq.cn"));//true
			console.log(p9.test("@qq.cn"));//false
			console.log(p9.test("123@baidu.com"));//true
			console.log(p9.test("&123@baidu.xcvxcvds"));//false
		</script>
	</head>
	<body>
	</body>
</html>
```



## 13.js - 对象



### 13.1 创建对象的两种方式

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// //创建对象
			// //key value 键值对
			// user1 = {
			// 	name: "siki",
			// 	age: 80,
			// 	sex: "男"
			// };
			// console.log(user1.name); //siki
			// console.log(user1.age); //80
			// console.log(user1.sex); //男

			//创建对象的另一种方式
			var user1 = new Object();
			user1.name = "sikiedu";
			user1.age = 20;
			user1.sex = "男";
			console.log(user1.name);//sikiedu
			console.log(user1.age);//20
			console.log(user1.sex);//男
		</script>
	</head>
	<body>
	</body>
</html>
```



### 13.2 构造函数

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			////创建多个对象 - 一个一个创建麻烦 - 可以使用构造函数来创建对象
			// user1 = {
			// 	name: "siki",
			// 	age: 80,
			// 	sex: "男"
			// };
			// user2 = {
			// 	name: "蓝猫",
			// 	age: 10,
			// 	sex: "女";
			// };

			//构造函数
			function user(name, age, sex) {
				this.name = name;
				this.age = age;
				this.sex = sex;
			}
			//创建两个对象 - 简洁
			user3 = new user("小红", 20, "女");
			user4 = new user("李白", 40, "男");
			console.log(user3.name);//小红
			console.log(user3.age);//20
			console.log(user3.sex);//女
		</script>
	</head>
	<body>
	</body>
</html>
```



### 13.3 给对象添加普通函数和对象属性的遍历

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//给对象添加普通函数和对象属性的遍历
			function user(name, age, sex) {
				this.name = name;
				this.age = age;
				this.sex = sex;

				// function show() {
				// 	console.log(this.name + ":" + this.age + ":" + this.sex);
				// }
				//报错 - 定义函数而已，并没有赋值给这个对象

				//解决1：
				//this.show = show();//给对象添加一个show的属性
				// function show() {
				// 	console.log(this.name + ":" + this.age + ":" + this.sex);
				// }

				//解决2：this.show 调用匿名函数
				this.show = function() {
					console.log(this.name + ":" + this.age + ":" + this.sex);
				}

				this.setAge = function(age) { //定义更改年龄的函数
					this.age = age;
				}
			}
			user3 = new user("小红", 20, "女");
			user4 = new user("李白", 40, "男");
			// console.log(user3.name);//小红
			// console.log(user3.age);//20
			// console.log(user3.sex);//女
			user3.show(); //小红:20:女
			user4.show(); //李白:40:男
			user4.setAge(18);
			user4.show(); //李白:18:男

			//对象属性的遍历
			//访问user3的name的值（两种方式）
			// console.log(user3.name);
			// console.log(user3["name"]);

			for (key in user3) {
				console.log(key + ":" + user3[key]);
			}
			/* 遍历结果：
				name:小红
				age:20
				sex:女
				show:function() {
									console.log(this.name + ":" + this.age + ":" + this.sex);
								}
				setAge:function(age) { //定义更改年龄的函数
									this.age = age;
								}
			*/
		</script>
	</head>
	<body>
	</body>
</html>
```



## 14. 开发注册表单页面



### 14.1 表单页面

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<form>
			<table border="1" width="500px" height="500px">
				<tr>
					<td colspan="2" align="center">注册</td>
				</tr>
				<tr>
					<td align="right">用户名：</td>
					<td align="left">
						<input type="text" />
					</td>
				</tr>
                 <tr>
					<td align="right">邮箱：</td>
					<td> <input type="text" id="email" /> </td>
				</tr>
				<tr>
					<td align="right">密码：</td>
					<td>
						<input type="password" />
					</td>
				</tr>
				<tr>
					<td align="right">重复密码：</td>
					<td>
						<input type="password" />
					</td>
				</tr>
				<tr>
					<td colspan="2" align="center">
						<input type="submit" value="注册" />
					</td>
				</tr>
		</form>
	</body>
</html>

```

![image-20220315220726735](.\JavaScript学习笔记图片\5.png)



### 14.2 表单提交事件和获取 html 元素

* 怎么通过id获得某个元素

  ```js
  document.getElementById("username")
  ```

* 怎么获得输入框输入的内容

  ```js
  username.value
  ```

  

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			function check() {
				// alert("check");
				
				var username = document.getElementById("username");//得到usernamede的网页的某个元素
				
				console.log(username);
				console.log(username.value);
				
				return false;//暂时不用提交到register.jsp文件
			}
		</script>
	</head>
	<body>
		<!-- onsubmit="check()" 表单提交的时候，触发事件，会调用check函数 -->
		<!-- action="register.jsp" 内容提交到register.jsp 文件 -->
		<form action="register.jsp" onsubmit="check()">
			<table border="1" width="500px" height="500px">
				<tr>
					<td colspan="2" align="center">注册</td>
				</tr>
				<tr>
					<td align="right">用户名：</td>
					<td align="left">
						<input type="text" id="username"/>
					</td>
				</tr>
                 <tr>
					<td align="right">邮箱：</td>
					<td> <input type="text" id="email" /> </td>
				</tr>
				<tr>
					<td align="right">密码：</td>
					<td>
						<input type="password" />
					</td>
				</tr>
				<tr>
					<td align="right">重复密码：</td>
					<td>
						<input type="password" />
					</td>
				</tr>
				<tr>
					<td colspan="2" align="center">
						<input type="submit" value="注册" />
					</td>
				</tr>
		</form>
	</body>
</html>
```

![image-20220317142240235](.\JavaScript学习笔记图片\6.png)



### 14.3 完成用户名和邮箱的校验

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			function check() {
				// alert("check");

				var username = document.getElementById("username"); //得到usernamede的网页的某个元素

				// console.log(username);
				// console.log(username.value);

				// 用户名的检验
				var length = username.value.length;
				// if (length >= 3 && length <= 6) {

				// } else {
				// 	alert("用户名长度必须是3-6位");
				// }
				if (length < 3 || length > 6) {
					alert("用户名长度必须是3-6位");
				}

				// 邮箱的检验
				var email = document.getElementById("email").value;
				var p = /^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;
				// p.test(email);
				if (p.test(email) == false) {
					alert("邮箱格式不正确");
				}

				return false; //暂时不用提交到register.jsp文件
			}
		</script>
	</head>
	<body>
		<!-- onsubmit="check()" 表单提交的时候，触发事件，会调用check函数 -->
		<!-- action="register.jsp" 内容提交到register.jsp 文件 -->
		<form action="register.jsp" onsubmit="check()">
			<table border="1" width="500px" height="500px">
				<tr>
					<td colspan="2" align="center">注册</td>
				</tr>
				<tr>
					<td align="right">用户名：</td>
					<td align="left">
						<input type="text" id="username" />
					</td>
				</tr>
                 <tr>
					<td align="right">邮箱：</td>
					<td> <input type="text" id="email" /> </td>
				</tr>
				<tr>
					<td align="right">密码：</td>
					<td>
						<input type="password" />
					</td>
				</tr>
				<tr>
					<td align="right">重复密码：</td>
					<td>
						<input type="password" />
					</td>
				</tr>
				<tr>
					<td colspan="2" align="center">
						<input type="submit" value="注册" />
					</td>
				</tr>
		</form>
	</body>
</html>
```



* 用户名的检验

![image-20220317142340925](.\JavaScript学习笔记图片\7.png)



* 邮箱的检验

![image-20220317142439511](.\JavaScript学习笔记图片\8.png)



### 14.4 完成密码的校验和校验成功的跳转

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			function check() {
				// alert("check");

				var username = document.getElementById("username"); //得到usernamede的网页的某个元素

				// console.log(username);
				// console.log(username.value);

				var isPass = true; //设置一个变量来判断每个校验环节是否全部通过

				// 用户名的检验
				var length = username.value.length;
				// if (length >= 3 && length <= 6) {

				// } else {
				// 	alert("用户名长度必须是3-6位");
				// }
				if (length < 3 || length > 6) {
					alert("用户名长度必须是3-6位");
					isPass = false;
				}

				// 邮箱的检验
				var email = document.getElementById("email").value;
				var p = /^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;
				// p.test(email);
				if (p.test(email) == false) {
					alert("邮箱格式不正确");
					isPass = false;
				}

				// 密码的检验
				var password = document.getElementById("password").value;
				var rePassword = document.getElementById("rePassword").value;
				if (password.length < 6 || password.length > 10) {
					alert("密码必须在6-10位之间");
					isPass = false;
				} else {
					if (password != rePassword) {
						alert("两次输入密码不一致");
						isPass = false;
					}
				}

				// return false; //暂时不用提交到register.jsp文件
				// if (isPass == false) {
				// 	isPass = false;
				// } else {
				// 	isPass = true;
				// }
				//简化代码
				return isPass; //返回判断检验的变量，是否全部通过
			}
		</script>
	</head>
	<body>
		<!-- onsubmit="check()" 表单提交的时候，触发事件，会调用check函数 -->
		<!-- action="register.jsp" 内容提交到register.jsp 文件 -->
		<form action="register.jsp" onsubmit="check()">
			<table border="1" width="500px" height="500px">
				<tr>
					<td colspan="2" align="center">注册</td>
				</tr>
				<tr>
					<td align="right">用户名：</td>
					<td align="left">
						<input type="text" id="username" />
					</td>
				</tr>
				<tr>
					<td align="right">邮箱：</td>
					<td> <input type="text" id="email" /> </td>
				</tr>
				<tr>
					<td align="right">密码：</td>
					<td>
						<input type="password" id="password" />
					</td>
				</tr>
				<tr>
					<td align="right">重复密码：</td>
					<td>
						<input type="password" id="rePassword" />
					</td>
				</tr>
				<tr>
					<td colspan="2" align="center">
						<input type="submit" value="注册" />
					</td>
				</tr>
		</form>
	</body>
</html>
```



![image-20220317142646554](.\JavaScript学习笔记图片\9.png)



### 14.5 表单校验提示信息的显示方式

* 怎么修改元素的内容

  ```js
  usernameMsg.innerText = "用户名长度必须是3-6位";
  ```

* 两种给出用户提示的方式

  * alert方式
  * 网页上显示

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			function check() {
				// alert("check");

				var username = document.getElementById("username"); //得到usernamede的网页的某个元素
				
				var usernameMsg = document.getElementById("usernameMsg");//得到usernameMsg的网页的某个元素
				var emailMsg = document.getElementById("emailMsg");//usernameMsg
				var passwordMsg = document.getElementById("passwordMsg");//usernameMsg

				// console.log(username);
				// console.log(username.value);

				var isPass = true; //设置一个变量来判断每个校验环节是否全部通过

				// 用户名的检验
				var length = username.value.length;
				// if (length >= 3 && length <= 6) {

				// } else {
				// 	alert("用户名长度必须是3-6位");
				// }
				if (length < 3 || length > 6) {
					// alert("用户名长度必须是3-6位");
					usernameMsg.innerText = "用户名长度必须是3-6位"; //通过 innerText 修改 font 标签里的内容
					isPass = false;
				} else {
					usernameMsg.innerText = "";
				}

				// 邮箱的检验
				var email = document.getElementById("email").value;
				var p = /^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;
				// p.test(email);
				if (p.test(email) == false) {
					// alert("邮箱格式不正确");
					emailMsg.innerText = "邮箱格式不正确";
					isPass = false;
				} else {
					emailMsg.innerText = "";
				}

				// 密码的检验
				var password = document.getElementById("password").value;
				var rePassword = document.getElementById("rePassword").value;
				if (password.length < 6 || password.length > 10) {
					// alert("密码必须在6-10位之间");
					passwordMsg.innerText = "密码必须在6-10位之间"
					isPass = false;
				} else {
					if (password != rePassword) {
						// alert("两次输入密码不一致");
						passwordMsg.innerText="两次输入密码不一致";
						isPass = false;
					}else{
						passwordMsg.innerText="";
					}
				}

				// return false; //暂时不用提交到register.jsp文件
				// if (isPass == false) {
				// 	isPass = false;
				// } else {
				// 	isPass = true;
				// }
				//简化代码
				return isPass; //返回判断检验的变量，是否全部通过
			}
		</script>
	</head>
	<body>
		<!-- onsubmit="check()" 表单提交的时候，触发事件，会调用check函数 -->
		<!-- action="register.jsp" 内容提交到register.jsp 文件 -->
		<form action="register.jsp" onsubmit="check()">
			<table border="1" width="500px" height="500px">
				<tr>
					<td colspan="2" align="center">注册</td>
				</tr>
				<tr>
					<td align="right">用户名：</td>
					<td align="left">
						<input type="text" id="username" />
						<font color="red" id="usernameMsg"></font><!-- 用户在输入用户名信息时错误的提示信息 -->
					</td>
				</tr>
				<tr>
					<td align="right">邮箱：</td>
					<td>
						<input type="text" id="email" />
						<font color="red" id="emailMsg"></font>
					</td>
				</tr>
				<tr>
					<td align="right">密码：</td>
					<td>
						<input type="password" id="password" />
						<font color="red" id="passwordMsg"></font>
					</td>
				</tr>
				<tr>
					<td align="right">重复密码：</td>
					<td>
						<input type="password" id="rePassword" />
					</td>
				</tr>
				<tr>
					<td colspan="2" align="center">
						<input type="submit" value="注册" />
					</td>
				</tr>
		</form>
	</body>
</html>
```

![image-20220317142852078](.\JavaScript学习笔记图片\10.png)



### 14.6 修改表单校验的时机

* 校验的时机
  * onsubmit
  * onchange
  * onfocus onblur

* 校验要求

  * 用户名长度必须位于3到6位之间
  * 邮箱格式 xxx@xxx	第二部分是域名结尾.com .org .cn .net等
  * 密码必须是6到10为之间
  * 密码和重复密码必须一样

  

* 将表单校验的时间由原来的提交注册再校验修改为输入一个信息先后就开始校验

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			function check() {
				// alert("check");

				var username = document.getElementById("username"); //得到usernamede的网页的某个元素

				var usernameMsg = document.getElementById("usernameMsg"); //得到usernameMsg的网页的某个元素
				var emailMsg = document.getElementById("emailMsg"); //usernameMsg
				var passwordMsg = document.getElementById("passwordMsg"); //usernameMsg

				// console.log(username);
				// console.log(username.value);

				var isPass = true; //设置一个变量来判断每个校验环节是否全部通过

				// 用户名的检验
				var length = username.value.length;
				// if (length >= 3 && length <= 6) {

				// } else {
				// 	alert("用户名长度必须是3-6位");
				// }
				if (length < 3 || length > 6) {
					// alert("用户名长度必须是3-6位");
					usernameMsg.innerText = "用户名长度必须是3-6位"; //通过 innerText 修改 font 标签里的内容
					isPass = false;
				} else {
					usernameMsg.innerText = "";
				}

				// 邮箱的检验
				var email = document.getElementById("email").value;
				var p = /^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;
				// p.test(email);
				if (p.test(email) == false) {
					// alert("邮箱格式不正确");
					emailMsg.innerText = "邮箱格式不正确";
					isPass = false;
				} else {
					emailMsg.innerText = "";
				}

				// 密码的检验
				var password = document.getElementById("password").value;
				var rePassword = document.getElementById("rePassword").value;
				if (password.length < 6 || password.length > 10) {
					// alert("密码必须在6-10位之间");
					passwordMsg.innerText = "密码必须在6-10位之间"
					isPass = false;
				} else {
					if (password != rePassword) {
						// alert("两次输入密码不一致");
						passwordMsg.innerText = "两次输入密码不一致";
						isPass = false;
					} else {
						passwordMsg.innerText = "";
					}
				}

				// return false; //暂时不用提交到register.jsp文件
				// if (isPass == false) {
				// 	isPass = false;
				// } else {
				// 	isPass = true;
				// }
				//简化代码
				return isPass; //返回判断检验的变量，是否全部通过

			}

			//onblur 失去焦点的时候调用
			// function checkUsername() {
			// 	var username = document.getElementById("username");
			// 	var usernameMsg = document.getElementById("usernameMsg");

			// 	var length = username.value.length;
			// 	if (length < 3 || length > 6) {
			// 		usernameMsg.innerText = "用户名长度必须是3-6位";
			// 	} else {
			// 		usernameMsg.innerText = "";
			// 	}
			// }
			//使用 this 传入的值，就不用 document.getElementById 去获得 用户名 的元素 username
			function checkUsername(username) {
				// var username = document.getElementById("username");
				var usernameMsg = document.getElementById("usernameMsg");

				var length = username.value.length;
				if (length < 3 || length > 6) {
					usernameMsg.innerText = "用户名长度必须是3-6位";
				} else {
					usernameMsg.innerText = "";
				}
			}

			function checkEmail(email) {
				var emailMsg = document.getElementById("emailMsg");
				var p = /^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;
				if (p.test(email.value) == false) {	//email.value是因为传入的是一个对象，要使用对象的值
					emailMsg.innerText = "邮箱格式不正确";
				} else {
					emailMsg.innerText = "";
				}
			}

			function checkPassword() {
				var passwordMsg = document.getElementById("passwordMsg");
				var password = document.getElementById("password");
				var rePassword = document.getElementById("rePassword").value;
				if (password.value.length < 6 || password.value.length > 10) {
					passwordMsg.innerText = "密码必须在6-10位之间"
					isPass = false;
				} else {
					passwordMsg.innerText = ""
					if (password.value != rePassword) {
						passwordMsg.innerText = "两次输入密码不一致";
						isPass = false;
					} else {
						passwordMsg.innerText = "";
					}
				}
			}
		</script>
	</head>
	<body>
		<!-- onsubmit="check()" 表单提交的时候，触发事件，会调用check函数 -->
		<!-- action="register.jsp" 内容提交到register.jsp 文件 -->
		<form action="register.jsp" onsubmit="check()">
			<table border="1" width="500px" height="500px">
				<tr>
					<td colspan="2" align="center">注册</td>
				</tr>
				<tr>
					<td align="right">用户名：</td>
					<td align="left">
						<!-- onblur 失去焦点的时候调用
							onblur 事件：当用户离开input输入框时执行一段Javascript代码：
						 -->
						<!-- <input type="text" id="username" onblur="checkUsername()" /> -->
						<input type="text" id="username" onblur="checkUsername(this)" />
						<!-- this直接就是使用输入的username的值，传入checkUsername函数 -->
						<font color="red" id="usernameMsg"></font><!-- 用户在输入用户名信息时错误的提示信息 -->
					</td>
				</tr>
				<tr>
					<td align="right">邮箱：</td>
					<td>
						<!-- <input type="text" id="email" /> -->
						<input type="text" id="email" onblur="checkEmail(this)" />
						<font color="red" id="emailMsg"></font>
					</td>
				</tr>
				<tr>
					<td align="right">密码：</td>
					<td>
						<!-- <input type="password" id="password" /> -->
						<input type="password" id="password" onblur="checkPassword()" />
						<font color="red" id="passwordMsg"></font>
					</td>
				</tr>
				<tr>
					<td align="right">重复密码：</td>
					<td>
						<!-- <input type="password" id="rePassword" /> -->
						<input type="password" id="rePassword" onblur="checkPassword()" />
					</td>
				</tr>
				<tr>
					<td colspan="2" align="center">
						<input type="submit" value="注册" />
					</td>
				</tr>
		</form>
	</body>
</html>
```

![image-20220317214858530](.\JavaScript学习笔记图片\11.png)

![image-20220317215133876](.\JavaScript学习笔记图片\12.png)



## 15. DOM



### 15.1 DOM文件对象模型

当网页被加载时，浏览器会创建页面的文档对象模型（*D*ocument *O*bject *M*odel）

*HTML DOM* 模型被结构化为**对象树**



* 对象的 HTML DOM 树

![image-20220317220818958](.\JavaScript学习笔记图片\13.png)

简述：网页就是有标签组成的，标签是层层包裹的（父标签和子标签），最内存的标签包裹着内容。（文本或者图片）



### 15.2 什么是 HTML DOM？

HTML DOM 是 HTML 的标准*对象*模型和*编程接口*。它定义了：

- 作为*对象*的 HTML 元素
- 所有 HTML 元素的*属性*
- 访问所有 HTML 元素的*方法*
- 所有 HTML 元素的*事件*

**换言之：HTML DOM 是关于如何获取、更改、添加或删除 HTML 元素的标准**



### 15.3 第一种获取 html 元素的方法（根据id）



* 问题：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div>
			<span id="one">
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div>
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div>
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p>
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	var div = document.getElementById("one"); //通过 document 获取文档的元素
	console.log(div); //null
	//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
	//id="one" 的元素没有获取到，所以得到的是 null
</script>
```

![image-20220318195439509](.\JavaScript学习笔记图片\14.png)



* 第一种获取 html 元素的方法（根据id）

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	// 第一种
	var div = document.getElementById("one"); //通过 document 获取文档的元素
	console.log(div);
</script>
```

![image-20220319012549189](.\JavaScript学习笔记图片\15.png)



### 15.4 第二、三、四种获取 html 元素

* 第二种 - 通过 tagname 标签名

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	// //getElementsByName() 方法可返回带有指定名称的对象的集合。
	// var div = document.getElementsByName("div");
	// console.log(div);
	// //第二种 - 通过 tagname 标签名
	var div = document.getElementById("one");
	var arr1 = div.getElementsByTagName("span");
	console.log(arr1);
</script>
```

![image-20220319013120110](.\JavaScript学习笔记图片\16.png)



* 第三种 - 通过类名

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	//第三种 - 通过类名
	var arr1 = document.getElementsByClassName("two");
	console.log(arr1);
</script>

```

![image-20220319013350183](.\JavaScript学习笔记图片\17.png)



* 第四种 - 通过标签的 name 值来查找

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two" name="last">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two" name="last">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	//第四种 - 通过标签的 name 值来查找
	var arr1 = document.getElementsByName("last");
	console.log(arr1);
</script>

```

![image-20220319013819204](.\JavaScript学习笔记图片\18.png)



### 15.5 对元素的三种操作



* 设置内容

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two" name="last">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two" name="last">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	var myfont = document.getElementById("myfont");
	myfont.setAttribute("color","green");
</script>
```

![image-20220319190909278](.\JavaScript学习笔记图片\19.png)



* 设置属性

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two" name="last">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two" name="last" id="three">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	//设置 html 属性
	var myfont = document.getElementById("myfont");
	// // myfont.setAttribute("color","green");
	var size = myfont.getAttribute("size");//返回的都是字符串类型
	console.log(typeof(size));//string
	console.log(size);//6
</script>
```

![image-20220319210030910](.\JavaScript学习笔记图片\20.png)



* 设置 css 样式

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two" name="last">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two" name="last" id="three">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6" style="font-family: 仿宋;">父标签和子标签</font>），最内存的标签包裹着内容。（文本或者图片）
		</p>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">	
	//设置 css 样式
	// style="font-family: 仿宋;"
	var myfont = document.getElementById("myfont");
	myfont.setAttribute("style","font-family: 仿宋;");
</script>

```

![image-20220319210548301](.\JavaScript学习笔记图片\21.png)



### 15.6 修改超链接、图像、复选框和 css 样式的单独函数

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 问题 -->
		<!-- <script type="text/javascript">
			var div = document.getElementById("one");//通过 document 获取文档的元素
			console.log(div);//null
			//文档是先加载 head 再加载 body ，head 代码先执行，这样 body 的标签还没生成
			//id="one" 的元素没有获取到，所以得到的是 null
		</script> -->
	</head>
	<body>
		<div id="one">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<div class="two" name="last">
			<span>
				DOM：文档对象模型（Document Object Model）
				简述：网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。我们可以获取这个对象，来操作对应的标签的一些属性。
				总结：获取要操作的标签元素对应的对象，通过这个对象来操作这个元素。
			</span>
		</div>
		<p class="two" name="last" id="three">
			DOM树（图片）：
			简述：网页就是有标签组成的，标签是层层包裹的（<font id="myfont" size="6" style="font-family: 仿宋;">父标签和子标签</font>
			），最内存的标签包裹着内容。（文本或者图片）
		</p>

		<a href="#" id="mya">进入百度</a>
		<img src="img/p6-pic1.jpg" id="myimg" />
		<input type="checkbox" id="mycheckbox" />

		<div id="mydiv">
			网页被加载的时候，浏览器会给网页上的每个标签创建这个标签对应的对象。
		</div>
	</body>
</html>

<!-- 解决 -->
<script type="text/javascript">
	var mya = document.getElementById("mya");
	var myimg = document.getElementById("myimg");
	var mycheckbox = document.getElementById("mycheckbox");

	// //修改超链接
	// // mya.setAttribute("href", "https://www.baidu.com");
	// //直接修改
	// mya.href = "https://www.baidu.com";

	// //修改图片
	// // myimg.setAttribute("src", "img/p6-pic2.jpg");
	// //直接修改
	// myimg.src = "img/p6-pic2.jpg";

	// //修改复选框
	// // mycheckbox.setAttribute("checked", "true");
	// //直接修改
	// mycheckbox.checked=true;

	//css 修改样式的需要
	mydiv = document.getElementById("mydiv");
	mydiv.style.fontSize = "20px";
	mydiv.style.color = "blueviolet";
</script>
```



###  15.7 给元素添加DOM事件的三种方式

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<!--第一种 通过onclick属性添加事件-->
		<div onclick="console.log('我被点击了');">DOM事件div</div><!-- 点击去输出 -->
		<div onclick="divClick()">DOM事件div</div><!-- 点击触发去调用函数 -->

		<span id="myspan">DOM事件span</span>

		<p>DOM事件p</p>

		<font size="" color="">DOM事件font</font>

		<a href="">DOM事件a</a>
	</body>
</html>
<script type="text/javascript">
	//通过JavaScript代码添加点击事件（第二种方式）
	function divClick() {
		console.log('我被点击了');
	}
	var myspan = document.getElementById("myspan");
	myspan.onclick = function() {
		console.log("span被点击了");
	}

	//通过JavaScript代码添加点击事件（第三种方式）
	// var myspan = document.getElementById("myspan");
	// myspan.addEventListener("click", spanClick);

	// function spanClick() {
	// 	console.log("span被点击了");
	// }

	//也使用匿名函数
	var myspan = document.getElementById("myspan");
	myspan.addEventListener("click", function() {
		console.log("span被点击了");
	});
</script>
```



### 15.8 DOM节点操作

* 创建新元素（DOM树中的新节点）

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<div id="mydiv">
			<span>第一个span</span>
			<span>第二个span</span>
			<span>第三个span</span>
			<span>第四个span</span>
			<p id="myp">我是p标签</p>

		</div>
	</body>
</html>
<script type="text/javascript">
	//通过 innerHTML 给标签添加子标签
	myp = document.getElementById("myp");
	myp.innerHTML = "<span>第五个span</span>";
	
	//缺点：把已有的标签给覆盖掉
	mydiv = document.getElementById("mydiv");
	mydiv.removeChild(myp);
	mydiv.innerHTML = "<span>第六个span</span>";
</script>
```

![image-20220320131624266](.\JavaScript学习笔记图片\22.png)



* 创建新元素（不影响其他标签）

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<div id="mydiv">
			<span>第一个span</span>
			<span>第二个span</span>
			<span>第三个span</span>
			<span>第四个span</span>
			<p id="myp">我是p标签</p>

		</div>
	</body>
</html>
<script type="text/javascript">
	//不影响其他标签
	var newSpan = document.createElement("span"); // <span></span> - 只是创建出来，本没有放入文本里面，而且span标签里面没有内容
	mydiv.appendChild(newSpan);
</script>
```

![image-20220320132503444](.\JavaScript学习笔记图片\23.png)



* 创建新元素（创建文本节点）

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<div id="mydiv">
			<span>第一个span</span>
			<span>第二个span</span>
			<span>第三个span</span>
			<span>第四个span</span>
			<p id="myp">我是p标签</p>

		</div>
	</body>
</html>
<script type="text/javascript">
	//不影响其他标签
	var newSpan = document.createElement("span"); // <span></span> - 只是创建出来，本没有放入文本里面，而且span标签里面没有内容
	// mydiv.appendChild(newSpan);
	newSpan.innerText = "我是第五个span"; //添加内容
	mydiv.appendChild(newSpan); //一定要的，把span标签放到文本里面

	//另一种方式 - 创建一个文本节点
	var newSpan = document.createElement("span");
	var textNode = document.createTextNode("我是第六个span");
	newSpan.appendChild(textNode);
	mydiv.appendChild(newSpan);
</script>
```

![image-20220320132955924](.\JavaScript学习笔记图片\24.png)



## 16. 图片轮播



### 16.1 设置图片更换

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			div {
				width: 900px;
				height: 400px;
				margin: 0 auto;
			}

			div img {
				width: 900px;
				height: 400px;
			}
		</style>
		<script type="text/javascript">
			window.setTimeout(changeImg, 2000); //两秒后开始调用，以此来调整图片轮换速度

			function changeImg() {
				myimg = document.getElementById("myimg");
				myimg.src = "img/p6-pic2.jpg"
			}
		</script>
	</head>
	<body>
		<div>
			<img src="img/p6-pic1.jpg" id="myimg" />
		</div>
	</body>
</html>
```

**注意：只是图片更换而已，图片还不会轮播**



### 16.2 设置图片循环更换

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			div {
				width: 900px;
				height: 400px;
				margin: 0 auto;
			}

			div img {
				width: 900px;
				height: 400px;
			}
		</style>
		<script type="text/javascript">
			//防止文本还没加载完就直接调用函数，可能导致需要的文本参数没加载导致错误
			function init() {
				//缺点:只待用一次
				// window.setTimeout(changeImg, 2000); //两秒后开始调用，以此来调整图片轮换速度
				window.setInterval(changeImg,2000);//每两秒调用一次函数
			}

			// //写死了，不会轮换
			// function changeImg() {
			// 	myimg = document.getElementById("myimg");
			// 	myimg.src = "img/2.jpg" //更换图片
			// }
			
			var index = 1;
			function changeImg() {
				myimg = document.getElementById("myimg");
				index++;
				if (index > 2) {
					index = 1;
				}
				myimg.src = "img/" + index + ".jpg"; //更换图片
			}
		</script>
	</head>
	<body onload="init()">
		<div>
			<img src="img/1.jpg" id="myimg" />
		</div>
	</body>
</html>
```



### 16.3 添加上一张和下一张的按钮

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			div {
				width: 900px;
				height: 400px;
				margin: 0 auto;
			}

			div img {
				width: 900px;
				height: 400px;
			}
		</style>
		<script type="text/javascript">
			//防止文本还没加载完就直接调用函数，可能导致需要的文本参数没加载导致错误
			function init() {
				//缺点:只待用一次
				// window.setTimeout(changeImg, 2000); //两秒后开始调用，以此来调整图片轮换速度
				window.setInterval(changeImg, 2000); //每两秒调用一次函数
			}

			// //写死了，不会轮换
			// function changeImg() {
			// 	myimg = document.getElementById("myimg");
			// 	myimg.src = "img/2.jpg" //更换图片
			// }

			var index = 1;

			// function changeImg() {
			// 	myimg = document.getElementById("myimg");
			// 	index++;
			// 	if (index > 2) {
			// 		index = 1;
			// 	}
			// 	myimg.src = "img/" + index + ".jpg"; //更换图片
			// }

			function changeImg() {
				nextImg();
			}

			function preImg() {
				myimg = document.getElementById("myimg");
				index--;
				if (index < 1) {
					index = 2;
				}
				myimg.src = "img/" + index + ".jpg";
			}

			function nextImg() {
				myimg = document.getElementById("myimg");
				index++;
				if (index > 2) {
					index = 1;
				}
				myimg.src = "img/" + index + ".jpg";
			}
		</script>
	</head>
	<body onload="init()">
		<p align="center">
			<button onclick="preImg()">上一张</button>
			<button onclick="nextImg()">下一张</button>
		</p>
		<div>
			<img src="img/1.jpg" id="myimg" />
		</div>
	</body>
</html>
```

![image-20220320164527982](.\JavaScript学习笔记图片\25.png)



### 16.4 数组

* 数组的创建、访问和遍历

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			// var score1 = 100;
			// var score2 = 30;
			// var score3 = 20;
			// //定义很多数据很麻烦 - 可以使用数组，用来存储数据

			// 数组可以存储一组数据
			var arr1 = new Array();
			arr1[0] = 100;
			arr1[1] = 30;
			arr1[2] = 60;
			arr1[3] = "baidu.com";
			arr1[4] = 80;
			arr1[5] = 90;
			console.log(arr1[3]); //baidu.com
			console.log(arr1.length); //6

			//遍历
			for (var i = 0; i < arr1.length; i++) {
				console.log(arr1[i]);
			}
		</script>
	</head>
	<body>
	</body>
</html>
```

![image-20220320192516085](.\JavaScript学习笔记图片\26.png)



* 数组的其他用法

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			// var arr2 = new Array(10);
			// for (var i = 0; i < arr2.length; i++) {
			// 	console.log(arr2[i]);
			// }
			// //undefined - 因为没有数据在里面

			// //数组存放number
			// var arr3 = new Array(90, 80, 50, 40);
			// for (var i = 0; i < arr3.length; i++) {
			// 	console.log(arr3[i]);
			// }
			// //数组存放字符串
			// var arr3 = new Array("李白", "孙尚香", "夏侯惇");
			// for (var i = 0; i < arr3.length; i++) {
			// 	console.log(arr3[i]);
			// }

			//数组存放对象
			function user(name, age, sex) {
				this.name = name;
				this.age = age;
				this.sex = sex;
			}
			user1 = new user("李白", 90, "男");
			user2 = new user("孙尚香", 30, "女");
			user3 = new user("夏侯惇", 20, "男");

			var arr = new Array(user1, user2, user3);//对象数组
			for (var i = 0; i < arr.length; i++) {//遍历 - 访问对象的 age 元素
				console.log(arr[i].age);
			}
		</script>
	</head>
	<body>
	</body>
</html>
```



### 16.5 图片轮播的优化

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			div {
				width: 900px;
				height: 400px;
				margin: 0 auto;
			}

			div img {
				width: 900px;
				height: 400px;
			}
		</style>
		<script type="text/javascript">
			function init() {
				window.setInterval(changeImg, 2000); //每两秒调用一次函数
			}

			var pathArr = new Array(
				"img/1.jpg",
				"img/2.jpg",
				"img/3.jpg",
				"img/4.jpg"
			);
			var index = 1;

			function changeImg() {
				nextImg();
			}

			// function preImg() {
			// 	myimg = document.getElementById("myimg");
			// 	index--;
			// 	if (index < 1) {
			// 		index = 2;
			// 	}
			// 	myimg.src = "img/" + index + ".jpg";
			// }
			function preImg() {
				myimg = document.getElementById("myimg");
				index--;
				if (index < 0) {
					index = pathArr.length - 1;
				}
				myimg.src = pathArr[index];
			}

			// function nextImg() {
			// 	myimg = document.getElementById("myimg");
			// 	index++;
			// 	if (index > 2) {
			// 		index = 1;
			// 	}
			// 	myimg.src = "img/" + index + ".jpg";
			// }
			function nextImg() {
				myimg = document.getElementById("myimg");
				index++;
				if (index >= pathArr.length) {
					index = 0;
				}
				myimg.src = pathArr[index];
			}
		</script>
	</head>
	<body onload="init()">
		<p align="center">
			<button onclick="preImg()">上一张</button>
			<button onclick="nextImg()">下一张</button>
		</p>
		<div>
			<img src="img/1.jpg" id="myimg" />
		</div>
	</body>
</html>
```

![image-20220320194229711](.\JavaScript学习笔记图片\27.png)



## 17. 广告弹窗

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			#ad {
				width: 300px;
				height: 300px;
				background-color: antiquewhite;
				position: fixed;
				bottom: 0px;
				right: 0px;
				display: none;//none 使得弹窗没有显示
			}
		</style>
		<script type="text/javascript">
			function init() {
				// setTimeout(showAd, 5000); //设置初始化网页后五秒调用弹窗函数
				setInterval(showAd, 5000);//设置初始化网页后每隔五秒调用一次弹窗函数
			}

			function showAd() {
				var ad = document.getElementById("ad");
				ad.style.display = "block";//block 使得弹窗显示
			}

			function closeAd() {
				var ad = document.getElementById("ad");
				ad.style.display = "none";
			}
		</script>
	</head>
	<body onload="init()">
		<!-- 换行为了查看滑动是否影响弹窗的位置 -->
		<br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
		<div id="ad">
			<button onclick="closeAd()">关闭</button><!-- 弹窗的关闭按钮 -->
		</div>
	</body>
</html>
```

![image-20220320230631233](.\JavaScript学习笔记图片\28.png)



## 18. window对象



### 18.1 什么是 window 对象

* window对象是一个浏览器对象，代表浏览器窗口。
* 我们定义的变量、函数会自动放在window对象里面。
* document也是window里面的。window.document
* window中的变量或者对象一般可以直接写，不加 window.前缀



```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			//window浏览器窗口
			// var name = "baidu";
			// console.log(window.name); //baidu

			// window.document.getElementById()
			// document.getElementById()//简写

			// window	窗口
			// document	网页

			// 之前的调用
			// window.alert();//弹出框
			// window.setInterval	//设置时间间隔调用函数
			// window.setTimeout	//设置多长时间调用函数

			var res = window.confirm("你确定要点击我吗？");//确定框
			console.log(res);//确定得到 true ；取消得到 false

			var res = window.prompt("请输入你的性别：");
			console.log(res);
		</script>
	</head>
	<body>
	</body>
</html>

```

![image-20220320235016800](.\JavaScript学习笔记图片\29.png)

![image-20220320235250200](.\JavaScript学习笔记图片\30.png)



### 18.2 通过window创建新的窗口

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			function myopen() {
				// open() 方法用于打开一个新的浏览器窗口或查找一个已命名的窗口。
				//参数	URL	声明了要在新窗口中显示的文档的 URL
				//name	该字符声明了新窗口的名称
				//features	声明了新窗口要显示的标准浏览器的特征
				//replace	true - URL 替换浏览历史中的当前条目。	false - URL 在浏览历史中创建新的条目。
				var w = window.open("https://www.baidu.com", "new_window", "width=500,height=500");
				
				//设置窗口的大小、位置
				w.resizeTo(400, 400);//修改大小
				w.moveTo(500, 500);//移动位置
				
				//w.close();//关闭网页窗口
				
				w.focus();//获取焦点
			}
		</script>
	</head>
	<body>
		<button onclick="myopen()">打开</button>
	</body>
</html>
```

![image-20220321001117984](.\JavaScript学习笔记图片\31.png)



### 18.3 screen 和 location 对象

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			// // screen( window.screen ) 获取屏幕分辨率
			// console.log(screen.availWidth);//可用的屏幕宽度
			// console.log(screen.availHeight);//可用的屏幕高度
			
			console.log(location.protocol);//返回所使用的 web 协议（http:// 或 https://）
			console.log(location.hostname);//返回 web 主机的域名
			console.log(location.port);//返回 web 主机的端口 （80 或 443）
			console.log(location.pathname);//返回当前页面的路径和文件名
			console.log(location);//对象用于获得当前页面的地址 (URL)，并把浏览器重定向到新的页面。

            // window.location.assign("https://www.baidu.com");  //相当于一个超链接的功能
			location.assign("604 - 广告弹窗.html");//从当前网址跳转到另一个网址
		</script>
	</head>
	<body>
		<button onclick="myopen()">打开</button>
	</body>
</html>
```



### 18.4 history对象控制网页前进和后退

* a页面代码

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// window.history	//对象包含浏览器的历史
		</script>
	</head>
	<body>
		<a href="701 - window对象b.html">下一个页面</a>
		<button onclick="history.back()">后退</button>
		<button onclick="history.forward()">前进</button>
	</body>
</html>
```



* b页面代码

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// window.history	//对象包含浏览器的历史
		</script>
	</head>
	<body>
		<a href="701 - window对象c.html">下一个页面</a>
		<button onclick="history.back()">后退</button>
		<button onclick="history.forward()">前进</button>
	</body>
</html>
```



* c页面代码

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			// window.history	//对象包含浏览器的历史
		</script>
	</head>
	<body>
		<a href="#">下一个页面</a>
		<button onclick="history.back()">后退</button>
		<button onclick="history.forward()">前进</button>
	</body>
</html>
```

![image-20220321005649963](.\JavaScript学习笔记图片\32.png)



## 19. 案例开发 - 全选功能

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			function selectAll(choiceBtn){
//				document.getElementsByTagName()	//不合适
				var arr = document.getElementsByName("choice");
				for(var i = 0;i<arr.length;i++){
					arr[i].checked=choiceBtn.checked;//取得复选框的状态改为 true
				}
			}
		</script>
	</head>
	<body>
		
		<table border="1" width="800px" height="800px">
			<tr>
				<td> <input type="checkbox" onclick="selectAll(this)" /> 全选</td><td>用户名</td><td>邮箱</td><td>电话号码</td><td>性别</td><td>操作</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
			<tr>
				<td> <input type="checkbox" name="choice" /> </td><td>张三</td><td>123456789@qq.com</td><td>123456789</td><td>男</td><td>发邮件 封号 编辑</td>
			</tr>
		</table>
	</body>
</html>
```

![image-20220321120553635](.\JavaScript学习笔记图片\33.png)



## 20. 案例开发 - 省市联动

* 省市二级显示效果

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			
			var provinceArr = new Array(5);
			provinceArr[0]=new Array("北京市");
			provinceArr[1]=new Array("郑州市","洛阳市","濮阳市","驻马店市");
			provinceArr[2]=new Array("石家庄市","唐山","秦皇岛","邯郸");
			provinceArr[3]=new Array("西安市","宝鸡市","延安");
			provinceArr[4]=new Array("菏泽市","济南市","青岛");
			
			function provinceChange(province){
				console.log(provinceArr[province.value]);//查看省的城市
			}
			
		</script>
	</head>
	<body>
		<select onchange="provinceChange(this)">
			<option value="0">北京市</option>
			<option value="1">河南省</option>
			<option value="2">河北省</option>
			<option value="3">陕西省</option>
			<option value="4">山东省</option>
		</select>
	</body>
</html>
```

![image-20220326171300510](.\JavaScript学习笔记图片\34.png)



* 省市二级下拉效果

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			var provinceArr = new Array(5);
			provinceArr[0] = new Array("北京市");
			provinceArr[1] = new Array("郑州市", "洛阳市", "濮阳市", "驻马店市");
			provinceArr[2] = new Array("石家庄市", "唐山", "秦皇岛", "邯郸");
			provinceArr[3] = new Array("西安市", "宝鸡市", "延安");
			provinceArr[4] = new Array("菏泽市", "济南市", "青岛");

			function provinceChange(province) {
				var city = document.getElementById("city");
				// console.log(provinceArr[province.value]); //查看省的城市
				var cityArr = provinceArr[province.value];
				for (var i = 0; i < cityArr.length; i++) {
					var cityOption = document.createElement("option");
					cityOption.innerText = cityArr[i];
					city.appendChild(cityOption);
				}
			}
		</script>
	</head>
	<body>
		<select onchange="provinceChange(this)">
			<option value="0">北京市</option>
			<option value="1">河南省</option>
			<option value="2">河北省</option>
			<option value="3">陕西省</option>
			<option value="4">山东省</option>
		</select>
		<select id="city">
			<option>-请选择-</option>
		</select>
	</body>
</html>
```

![image-20220326172144993](.\JavaScript学习笔记图片\35.png)



解决问题：

![image-20220326173209051](.\JavaScript学习笔记图片\36.png)





```javascript
<option value="-1">-请选择-</option>
```

![image-20220326173741105](.\JavaScript学习笔记图片\37.png)



* 变回原来**请选择**状态

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<script type="text/javascript">
			var provinceArr = new Array(5);
			provinceArr[0] = new Array("北京市");
			provinceArr[1] = new Array("郑州市", "洛阳市", "濮阳市", "驻马店市");
			provinceArr[2] = new Array("石家庄市", "唐山", "秦皇岛", "邯郸");
			provinceArr[3] = new Array("西安市", "宝鸡市", "延安");
			provinceArr[4] = new Array("菏泽市", "济南市", "青岛");

			function provinceChange(province) {
				var city = document.getElementById("city");
				if (province.value == "-1") {
					city.innerHTML="<option value='-1'>-请选择-</option>";
					return;
				}
				// console.log(provinceArr[province.value]); //查看省的城市
				var cityArr = provinceArr[province.value]; //得到城市的某一数组
				city.options.length = 0; //表示把上一次选择的内容清除
				for (var i = 0; i < cityArr.length; i++) {
					var cityOption = document.createElement("option");
					cityOption.innerText = cityArr[i];
					city.appendChild(cityOption);
				}
			}
		</script>
	</head>
	<body>
		<select onchange="provinceChange(this)">
			<option value="-1">-请选择-</option>
			<option value="0">北京市</option>
			<option value="1">河南省</option>
			<option value="2">河北省</option>
			<option value="3">陕西省</option>
			<option value="4">山东省</option>
		</select>
		<select id="city">
			<option value="-1">-请选择-</option>
		</select>
	</body>
</html>
```

![image-20220326174537954](.\JavaScript学习笔记图片\38.png)



代码文件地址：

[GitHub](https://github.com/icebear32/JAVASCRIPT_CODE.git)

[Gitee](https://gitee.com/ygh_ich/JAVASCRIPT_CODE.git)
