# 尺寸单位和颜色单位



## 尺寸单位

浏览器默认 font-size 为 16px

font-size: 100%; 实际上等价于 font-size:16px;

font-size: 200%; 实际上等价于 font-size: 32px;

### 解释

1. **em** 相对于父元素的尺寸设置倍数，当父元素尺寸为 20px ；子元素尺寸为 2em，即等价于 父元素尺寸*2，随父元素改变而改变
2. **%** 相对于根元素的尺寸大小而变化
3. **rem** 相对于根元素设置倍数

### 代码展示

```html
<!DOCTYPE html>
<html>
<head>
	<title>尺寸单位</title>
	<style type="text/css">
		.default{
			font-size: 16px;
		}
		.percent{
			font-size: 200%;
		}

		.parent-em {
			font-size:40px;
		}
		.parent-em>span{
			font-size: 2em;
		}
		.parent-rem {
			font-size: 40px;
		}
		.parent-rem>span{
			font-size: 2rem;
		}
	</style>
</head>
<body>
	<h1>尺寸单位</h1>
	<span style="color:red;">默认</span>
	<p>hello world</p>
	<p class="default">
		this is browser default-size
	</p>
	<hr/>
	<span style="color:red;">%</span>
	<p class="percent">
		this is browser percent-size
	</p>

	<hr/>
	<span style="color:red;">em</span>
	<p class="parent-em">
		hello <span> james </span>
	</p>
	<hr/>
	<span style="color:red;">rem</span>
	<p class="parent-rem">
		hello <span> james </span>
	</p>
</body>
</html>
```



## 颜色单位

几个颜色设计网站

[WEB安全色板](https://www.bootcss.com/p/websafecolors/)

[colordrop.io](https://colordrop.io/)

[rehabcenter.marketing](https://www.rehabcenter.marketing/tintui/)

### 解释

1. 指定颜色关键字，如 color:red;

2. 指定十六进制，如color:#ff0000;

3. 使用三原色，rgb(0-255,0-255,0-255)

4. 使用三原色加透明度，rgba(0-255,0-255,0-255,0-1)，最后一项为透明度

5. **transparent** 透明

6. **currentColor ** 使用父元素的颜色

7. **opacity** 指定透明度

8. **hsl** 和 rgb 一样，都是工业界颜色标准，

   色调h：0～360，饱和度 s：0%～100%，亮度 l：0%～100%

9. **hsla** 在 hsl 基础上多了第 4 个值，为透明度 0～1
### 代码展示

```html
<!DOCTYPE html>
<html>
<head>
	<title>颜色单位</title>
	<style type="text/css">
		.keyword {
			color:deeppink;
		}
		.hex {
			color:#ff0000;
		}
		.rgb{
			color:rgb(123,23,12);
		}
		.rgba{
			color:rgba(250,0,0,.2);
		}
		.rgb-p{
			color:rgb(150%,0%,0%);
		}
		.rgba-p{
			color:rgba(150%,0%,0%,.2);
		}
		.transparent{
			border: 1px solid deeppink;
			border-top: transparent;
		}
		.currentColor{
			color: red;
			margin: 2px;
		}
		.currentColor span{
			border: 2px solid currentColor;
		}
		.container>div{
			display: inline-block;
			width: 100px;
			height: 100px;
			background-color: deeppink;
		}
		div.opacity100{
			opacity: 1; 
		}
		div.opacity90{
			opacity: .9; 
		}
		div.opacity80{
			opacity: .8; 
		}
		div.opacity70{
			opacity: .7; 
		}
		div.opacity60{
			opacity: .6; 
		}
		div.opacity50{
			opacity: .5; 
		}
		div.opacity40{
			opacity: .4; 
		}
		div.opacity30{
			opacity: .3; 
		}
		div.opacity20{
			opacity: .2; 
		}
		div.opacity10{
			opacity: .1; 
		}
	</style>
</head>
<body>
	<h1>颜色单位</h1>
	<p class="keyword">关键字</p>
	<hr/>
	<p class="hex">十六进制</p>
	<hr/>
	<p class="rgb">RGB</p>
	<hr/>
	<p class="rgba">RGB 透明色</p>
	<hr/>
	<p class="rgb-p">RGB|百分比</p>
	<hr/>
	<p class="rgba-p">RGB 透明色|百分比</p>
	<hr/>
	<p class="transparent">border-top透明</p>
	<p class="currentColor">使用当前父元素的元素<span>currentColor</span></p>
	<h1>opacity</h1>
	<div class="container">
		<div class="opacity100">opacity100</div>
		<div class="opacity90">opacity90</div>
		<div class="opacity80">opacity80</div>
		<div class="opacity70">opacity70</div>
		<div class="opacity60">opacity60</div>
		<div class="opacity50">opacity50</div>
		<div class="opacity40">opacity40</div>
		<div class="opacity30">opacity30</div>
		<div class="opacity20">opacity20</div>
		<div class="opacity10">opacity10</div>
	</div>
</body>
</html>
```

