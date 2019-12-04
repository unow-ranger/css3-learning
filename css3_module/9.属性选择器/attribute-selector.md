# 属性选择器

## 解释

**[attr]** 选择所有带有指定属性的元素

**[attr=value]** 选择所有属性名等于指定值的元素设置样式

**[attr～=value]** attr 中包含 value 且必须是完整单词

**[attr|=value]** attr 必须以 value 开始，必须是完整单词或带 -

**[attr*=value]** value 中包含 value 即可以

**[attr^=value]** attr 必须以 value 开始

**[attr$=value]** attr 必须以 value 结束

## 实现代码
```html
<!DOCTYPE html>
<html>
<head>
	<title>属性选择器</title>
	<link rel="stylesheet" type="text/css" href="../../style.css">
	<style>
        [name]{
            color:deeppink;
        }
        [name="p2"]{
            font-size:25px;
        }
    </style>
</head>
<body>
	<p name="p1">
        hello
    </p>
    <p name="p2">
        hello
    </p>
    <p>
        world
    </p>
</body>
</html>
```
