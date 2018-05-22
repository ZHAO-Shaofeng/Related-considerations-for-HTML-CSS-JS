## 开发注意事项

1、插件的版本是否统一；

2、全局样式用谁的；

3、样式表的结构是不是继承的写法，会不会互相干扰；

4、样式优先级如下：    
` 通用选择器 * < 元素(类型)选择器 < 类选择器 < 属性选择器 < 伪类 < ID 选择器 < 内联样式 `

5、团队协作下使用git了吗；

6、不同团队开发，在关于复用的组件以及全局的变量是否有进行沟通；

7、如非特殊情况，慎用!important，因为使用!important会扰乱原本层叠和权重产生正常的作用顺序，使后期维护带来麻烦；

## CSS常用
### 1、单行溢出省略号
```
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap;
```

### 2、多行溢出省略号 
```
overflow : hidden;
text-overflow: ellipsis;
display: -webkit-box;
-webkit-line-clamp: 2;
-webkit-box-orient: vertical;
```

### 3、placeholder样式
```
input::-webkit-input-placeholder{
  color:red;
}
input::-moz-placeholder{
  color:red;
}
input:-moz-placeholder{
  color:red;
}
input:-ms-input-placeholder{
  color:red;
}
 ```
 
 ### 4、渐变
*  从上到下
 ```
 background: -webkit-linear-gradient(red, blue);
 background: -o-linear-gradient(red, blue);
 background: -moz-linear-gradient(red, blue);
 background: linear-gradient(red, blue);
 ```
 
*  从左到右
 ```
 background: linear-gradient(to right, red , blue);
 ```
 
*  角度
 ```
 background: linear-gradient(to bottom right, red , blue);  /*左上角至右下角*/
 background: linear-gradient(180deg, red, blue);  /*指定角度*/
 ```
 
*  多个颜色
 ```
 background: linear-gradient(red, green, blue);
 ```
 
 ## HTML head
 ```
 <meta charset="UTF-8">
 <!-- 设置文档宽度、是否缩放 -->
 <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
 <!-- 优先使用IE最新版本和Chrome -->
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
<title></title>
<!-- 关键字 -->
<meta name="keywords" content="">
<!-- 描述 -->
<meta name="description" content="">
<!--[if lte IE 8]>
<p style="background:#000;text-align: center;color:#fff;font-size: 16px; line-height: 25px;">你的浏览器太老了，请到<a href="http://browsehappy.com" style="color:#ddd">这里</a>更新，以获取最佳的体验</p>
<![endif]-->
<!--[if lte IE 7]>
<p style="background:#000;text-align: center;color:#fff;font-size: 16px; line-height: 25px;">你的浏览器太老了，请到<a href="http://browsehappy.com" style="color:#ddd">这里</a>更新，以获取最佳的体验</p>
<![endif]-->
<!--[if lte IE 6]>
<p style="background:#000;text-align: center;color:#fff;font-size: 16px; line-height: 25px;">你的浏览器太老了，请到<a href="http://browsehappy.com" style="color:#ddd">这里</a>更新，以获取最佳的体验</p>
<![endif]-->
<!-- 360使用Google Chrome Frame -->
<meta name="renderer" content="webkit">
<!-- 百度禁止转码 -->
<meta http-equiv="Cache-Control" content="no-siteapp">
<!-- 定义网页搜索引擎索引方式 -->
<meta name="robots" content="index,follow">
<!-- ios设备 -->
<!-- 添加到主屏后的标题 -->
<meta name="apple-mobile-web-app-title" content="标题">
<!-- 是否启用WebApp全屏模式 -->
<meta content="yes" name="apple-mobile-web-app-capable">
<meta content="yes" name="apple-touch-fullscreen">
<!-- 设置状态栏的背景颜色 -->
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<!-- Android theme-color用来控制选项卡颜色。 -->
<meta name="theme-color" content="#747474">
<meta name="mobile-web-app-capable" content="yes">
<!-- 关闭chrome浏览器下翻译插件 -->
<meta name="google" value="notranslate" />
<!-- uc强制竖屏 -->
<meta name="screen-orientation" content="portrait">
<!-- QQ强制竖屏 -->
<meta name="x5-orientation" content="portrait">
<!-- UC强制全屏 -->
<meta name="full-screen" content="yes">
<!-- QQ强制全屏 -->
<meta name="x5-fullscreen" content="true">
<!-- UC应用模式 -->
<meta name="browsermode" content="application">
<!-- QQ应用模式 -->
<meta name="x5-page-mode" content="app">
  ```
