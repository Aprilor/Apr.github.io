## 前端学习笔记之 JavaScript

### 计算 2 的 n 次幂，n 可输入，n 为自然数
```
	// 计算 2 的 n 次幂，n 可输入，n 为自然数
	var n = parseInt(window.prompt('input'));
	if(n >= 0) {
		var value = 1;
		for(var i = 0; i < n; i ++) {
			value *= 2;
		}
		document.write(value);
	}
	else {
		document.write("Error!");
	}
```
<!-- more -->
### 计算 n 的阶乘，n 可输入
```
	// 计算 n 的阶乘，n 可输入
	var n = parseInt(window.prompt('input'));
	// 阶乘亦可以递归方式定义：0!=1，n!=(n-1)!×n
	if(n >= 0) {
		var value = 1;
		for(i = 2; i <= n; i ++) {
			value *= i;
		}
		document.write(value);
	}
	else {
		document.write("Error!");
	}
```
### 斐波那契数列，输出 n 项
```
	// 斐波那契数列，输出 n 项
	var n = parseInt(window.prompt('input'));
	if(n > 0) {
		var j = 1;
		var k = 1;
		document.write(j + " " + k + " ");
		for(var i = 2; i < n; i ++) {
			if(i % 2 == 1) {
				j += k;
				document.write(j + " ");
			}
			else {
				k += j;
				document.write(k + " ");
			}
		}
	}
	else {
		document.write("Error!");
	}
```

```
	// 斐波那契数列，输出 n 项
	var n = parseInt(window.prompt('input'));
	if(n > 0) {
		var first = 1;
		var second = 1;
		if(n > 2) {
			var third;
			document.write(first + " " + second + " ");
			for(var i = 2; i < n; i ++) {
				third = first + second;
				first = second;
				second = third;
				document.write(third + " ");
			}
		}else {
			document.write(first);
		}
	}else {
		document.write("Error!");
	}
```
### 编写程序，输入一个正整数，输出时反向输出
```
	// 编写程序，输入一个正整数，输出时反向输出
	var n = parseInt(window.prompt('input'));
	if(n > 0) {
		var count = n + "";
		for(var i = 0; i < count.length; i ++) {
			var value = n % 10;
			n -= value;
			n /= 10;
			document.write(value);
		}
	}else {
		document.write("Error!");
	}
```
### 输入三个数字，打印出最大的
```
	// 输入三个数字，打印出最大的
	var first = parseInt(window.prompt('first number'));
	var second = parseInt(window.prompt('second number'));
	var third = parseInt(window.prompt('third number'));
	var max = first;
	if(first > second) {
		if(first > third) {
			max = first;
		}
		else {
			max = third;
		}
	}
	else {
		if(second > third) {
			mac = second;
		}
		else {
			max = third;
		}
	}
	document.write(max);
```
### 打印 n 以内的质数
```
	// 打印 n 以内的质数
	var n = parseInt(window.prompt('input a number'));
	var count = 0;
	for(var i = 2; i < n; i ++) {
		for(var j = 1; j <= Math.sqrt(i); j ++) {
			if(i % j == 0) {
				count ++;
			}
		}
		if(count == 1) {
			document.write(i + " ");
		}
		count = 0;
	}
```
### 写一个函数，功能是告知你所选定的小动物的叫声
```
	// 写一个函数，功能是告知你所选定的小动物的叫声
	function scream (animal) {
		switch(animal) {
			case "dog" :
				console.log("汪汪汪");
				break;
			case "cat" :
				console.log("喵喵喵");
				break;
		}
	}
	var n = String(window.prompt('input'));
	scream(n);
```
### 写一个函数，实现加法计数器
```
	// 写一个函数，实现加法计数器
	var add = function add() {
		var result = 0;
		for(var i = 0; i < arguments.length; i ++) {
			result += arguments[i];
		}
		console.log(result);
	}
	add(1, 2, 3, 100);
```
### 定义一组函数，输入数字，逆转并输出汉字形式
```
	// 定义一组函数，输入数字，逆转并输出汉字形式 changeover
	var changeover = function (n) {
		var changeoverChar = function(n) {
			switch(n) {
				case 1 : log("一"); break;
				case 2 : log("二"); break;
				case 3 : log("三"); break;
				case 4 : log("四"); break;
				case 5 : log("五"); break;
				case 6 : log("六"); break;
				case 7 : log("七"); break;
				case 8 : log("八"); break;
				case 9 : log("九"); break;
				case 0 : log("零"); break;
			}
		}
		var log = function(n) {
			console.log(n);
		}
		var write = function(n) {
			document.write(n);
		}
		var value = n;
		var count = value + "";
		var result = 0;
		if(value >= 0) {
			for(var i = 0; i < count.length; i ++) {
				result = value % 10;
				changeoverChar(result);
				value = (value - result) / 10;
			}
		}else {
			log("Error!");
		}
	}
	var n = parseInt(window.prompt('input'));
	changeover(n);
```

```
	// 定义一组函数，输入数字，逆转并输出汉字形式 changeover
	var changeover = function (n) {
		var transfer = function(target) {
			switch(target) {
				case "1" : return "一";
				case "2" : return "二";
				case "3" : return "三";
				case "4" : return "四";
				case "5" : return "五";
				case "6" : return "六";
				case "7" : return "七";
				case "8" : return "八";
				case "9" : return "九";
				case "0" : return "零";
			}
		}
		if(n >= 0) {
			var result = "";
			for(var i = n.length -1; i >= 0; i --) {
				result += transfer(n.charAt(i));
			}
			console.log(result);
		}else {
			log("Error!");
		}
	}
	var n = window.prompt('input');
	changeover(n);
```
### 写一个函数，实现 n 的阶乘
```
	// 写一个函数，实现 n 的阶乘 factorial
	var factorial = function(n) {
		// 阶乘亦可以递归方式定义：0!=1，n!=(n-1)!×n
		if(n >= 0) {
			var value = 1;
			for(i = 2; i <= n; i ++) {
				value *= i;
			}
			console.log(value);
		}else {
			console.log("Error!");
		}
	}
	var n = parseInt(window.prompt('input'));
	factorial(n);
```

```
	// 写一个函数，实现 n 的阶乘 factorial
	var factorial = function(n) {
		// 阶乘亦可以递归方式定义：0!=1，n!=(n-1)!×n recursion
		var recursion = function(n) {
			if(n == 0) {
				return 1;
			}
			return factorial(n - 1) * n;
		}
		if(n >= 0) {
			recursion(n);
		}else {
			console.log("Error!");
		}
	}
```
### 写一个函数，实现斐波那契数列
```
	// 写一个函数，实现斐波那契数列 Fibonacci sequence
	var fibonacciSequence = function (n) {
		if(n > 0) {
			var first = 1;
			var second = 1;
			var third;
			for(var i = 0; i < n; i ++) {
				if(i == 0) {
					console.log("第" + (i + 1) + "项: " + first);
				}else if(i == 1) {
					console.log("第" + (i + 1) + "项: " + second);
				}else {
					third = first + second;
					first = second;
					second = third;
					console.log("第" + (i + 1) + "项: " + third);
				}
			}
		}else {
			console.log("Eroor!");
		}
	}
	var n = parseInt(window.prompt('input'));
	fibonacciSequence(n);
```
### 要求输入一串低于 10 位的数字，输出这串数字的中文大写
```
	// 要求输入一串低于 10 位的数字，输出这串数字的中文大写
	var charTransfer = function(n) {
		var transfer = function(target) {
			switch(target) {
				case "0" : return "零";
				case "1" : return "壹";
				case "2" : return "贰";
				case "3" : return "叁";
				case "4" : return "肆";
				case "5" : return "伍";
				case "6" : return "陆";
				case "7" : return "柒";
				case "8" : return "捌";
				case "9" : return "玖";
			}
		}
		var add = function(value) {
			if(count > 5 && count < 10 || count == 1) {
				if(n.charAt(i) == "0") {

				}else {
					result += transfer(n.charAt(i)) + value;
				}
			}else if(count == 5) {
				if(n.charAt(i) == "0") {
					result += value;
				}else {
					result += transfer(n.charAt(i)) + value;
				}
			}else if(count > 1 && count < 5) {
				if(n.charAt(i) == "0") {
					if(n.charAt(i + 1) == "0") {

					}else {
						result += transfer(n.charAt(i));
					}
				}else {
					result += transfer(n.charAt(i)) + value;
				}
			}
			count --;
		}
		if(n.length < 10) {
			var result = "";
			var count = n.length;
			for(var i = 0; i < n.length; i ++) {
				if(count == 9) {
					add("亿");
				}else if(count == 8) {
					add("仟");
				}else if(count == 7) {
					add("佰");
				}else if(count == 6) {
					add("拾");
				}else if(count == 5) {
					add("万");
				}else if(count == 4) {
					add("仟");
				}else if(count == 3) {
					add("佰");
				}else if(count == 2) {
					add("拾");
				}else if(count == 1) {
					add("");
				}
			}
			console.log(result + "圆整");
		}else {
			console.log("Eroor!")
		}
	}
	var n = window.prompt('input');
	charTransfer(n);
```

