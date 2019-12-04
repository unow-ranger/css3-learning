# 目标伪类选择器

##  简介

目标伪类选择器 **:target** ,对页面中某个 target 元素指定样式，该样式只对用户点击了页面中的超链接并且跳转到 target 元素后起作用。



## 案例

```html
<!DOCTYPE html>
<html>
<head>
	<title>目标伪类选择器</title>
	<style>
		ul,ol,li {
			list-style: none;
		}
		a {
			text-decoration: none;
		}
		.chapter:target {
			background-color: skyblue;
		}
	</style>
</head>
<body>
	<h1>深入浅出css3</h1>
	<h2>目录列表</h2>
	<nav>
		<ul>
			<li>
				<a href="#p1">page1</a>
			</li>
			<li>
				<a href="#p2">page2</a>
			</li>
			<li>
				<a href="#p3">page3</a>
			</li>
			<li>
				<a href="#p4">page4</a>
			</li>
			<li>
				<a href="#p5">page5</a>
			</li>
		</ul>
	</nav>
	<hr>
	<h3 id="p1" class="chapter">page1</h3>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<h3 id="p2" class="chapter">page2</h3>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<h3 id="p3" class="chapter">page3</h3>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<h3 id="p4" class="chapter">page4</h3>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<h3 id="p5" class="chapter">page5</h3>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
	<p>hello world! hello world! hello world!</p>
</body>
</html>
```

