## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Aprilor/Apr.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Aprilor/Apr.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

## 前端学习笔记之 JavaScript

```
	// 计算 2 的 n 次幂，n 可输入，n 为自然数
	var n = parseInt(window.prompt('input'));
	if(n >= 0) {
		var value = 1;
		for(var i = 0; i < n; i++) {
			value *= 2;
		}
		document.write(value);
	}
	else {
		document.write("Error!");
	}
```
```
	// 计算 n 的阶乘，n 可输入
	var n = parseInt(window.prompt('input'));
	// 阶乘亦可以递归方式定义：0!=1，n!=(n-1)!×n
	if(n >= 0) {
		var value = 1;
		for(i = 2; i <= n; i++) {
			value *= i;
		}
		document.write(value);
	}
	else {
		document.write("Error!");
	}
```
```
	// 斐波那契数列，输出 n 项
	var n = parseInt(window.prompt('input'));
	if(n > 0) {
		var j = 1;
		var k = 1;
		document.write(j + " " + k + " ");
		for(var i = 2; i < n; i++) {
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

