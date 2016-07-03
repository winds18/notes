# 前端开发问题小记

##让360浏览器自动使用极速内核解析页面
让360等国内双核浏览器默认使用Chromium内核(极速模式)，需要通过在网页头部添加以下Meta标签来控制
```html
<!--360浏览器-->
<meta name="renderer" content="webkit">
<!--其他双核浏览器-->
<meta name="force-rendering" content="webkit">
<!--如果安装了GCF，则使用GCF来渲染页面，如果没有安装GCF，则使用最高版本的IE内核进行渲染。-->
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"/>
```
<font color="red">`注意：标签的顺序是不可以变的，否则360浏览器不会成功切换到极速的内核。`</font><br>
`第三个标签里的 X-UA-Compatible 是IE8的专用标记,用来指定IE8浏览器去模拟某个特定版本的IE浏览器的渲染方式(如IE6)，以此来解决部分兼容问题。`
