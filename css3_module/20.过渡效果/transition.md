# Css3 过渡

## transition

### 解释

过渡可以为一个元素在不同状态之间切换的时候定义不同的过渡效果。

一般调用形式：

```css
transition: transition-property transition-duration transition-timing-function transition-delay
```

transition 的值：

- transition-property 设置要过渡的 css 属性名
- transition-duration 过渡花费时间，单位为秒 s
- transition-timing-function 设置过渡转换效果的曲线变化
- transition-delay 规定延迟多久开始，以 秒 或 毫秒 为单位



### 示例代码

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title>
<style> 
div
{
	width:100px;
	height:100px;
	background:red;
	transition:width 2s;
	-webkit-transition:width 2s; /* Safari */
}

div:hover
{
	width:300px;
}
</style>
</head>
<body>
<p><b>注意：</b>该实例无法在 Internet Explorer 9 及更早 IE 版本上工作。</p>

<div></div>

<p>鼠标移动到 div 元素上，查看过渡效果。</p>

</body>
</html>
```

## transition-timing-function

### 在线工具

<https://easings.net/>

<https://cubic-bezier.com/>

### 解释

transition-timing-function 是指定元素过渡变化的线性变化形式

值：

- linear 线性过渡，以相同速度开始一直到结束的过渡效果
- ease 平滑过渡，慢->快->慢
- ease-in 慢->快
- ease-out 快->慢
- ease-in-out 慢->快->慢
- cubic-bezier(n,n,n,n) 贝塞尔函数，n 的值为 0～1

### 案例代码

```html
<!DOCTYPE html>
<html>
<head>
<style> 
div
{
width:100px;
height:50px;
background:red;
color:white;
font-weight:bold;
transition:width 2s;
-moz-transition:width 2s; /* Firefox 4 */
-webkit-transition:width 2s; /* Safari and Chrome */
-o-transition:width 2s; /* Opera */
}

#div1 {transition-timing-function: linear;}
#div2 {transition-timing-function: ease;}
#div3 {transition-timing-function: ease-in;}
#div4 {transition-timing-function: ease-out;}
#div5 {transition-timing-function: ease-in-out;}

/* Firefox 4: */
#div1 {-moz-transition-timing-function: linear;}
#div2 {-moz-transition-timing-function: ease;}
#div3 {-moz-transition-timing-function: ease-in;}
#div4 {-moz-transition-timing-function: ease-out;}
#div5 {-moz-transition-timing-function: ease-in-out;}

/* Safari and Chrome: */
#div1 {-webkit-transition-timing-function: linear;}
#div2 {-webkit-transition-timing-function: ease;}
#div3 {-webkit-transition-timing-function: ease-in;}
#div4 {-webkit-transition-timing-function: ease-out;}
#div5 {-webkit-transition-timing-function: ease-in-out;}

/* Opera: */
#div1 {-o-transition-timing-function: linear;}
#div2 {-o-transition-timing-function: ease;}
#div3 {-o-transition-timing-function: ease-in;}
#div4 {-o-transition-timing-function: ease-out;}
#div5 {-o-transition-timing-function: ease-in-out;}

div:hover
{
width:300px;
}
</style>
</head>
<body>

<div id="div1" style="top:100px">linear</div>
<div id="div2" style="top:150px">ease</div>
<div id="div3" style="top:200px">ease-in</div>
<div id="div4" style="top:250px">ease-out</div>
<div id="div5" style="top:300px">ease-in-out</div>

<p>请把鼠标指针移动到红色的 div 元素上，就可以看到过渡效果。</p>

<p><b>注释：</b>本例在 Internet Explorer 中无效。</p>

<script type="text/javascript" src="https://s11.cnzz.com/z_stat.php?id=1257119077&web_id=1257119077"></script>
</body>
</html>
```

