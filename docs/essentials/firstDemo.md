## 第一个Demo项目

本篇文章将手把手教你，开发一个最简单的demo示例。在做本Demo之前，您需要有些许`Javascript`及`HTML`的开发基础。

> 如您还未注册成为`Forface`开发者，请[点这里](https://account.fa-part.com)进行注册

##### step.1 安装或引用核心库

Forface唯一官方指定的资源路径URL如下：

```html
<link href="https://www.fa-part.com/forface-libs/forface3dViewer/style.css" rel="stylesheet" />
<script src="https://www.fa-part.com/forface-libs/forface3dViewer/viewer3D.min.js"></script>
```

> 为方便开发者快速入门，建议初学者使用如上两条官方提供的URL资源。如您需要本地化部署，请联系我们 0755-21004731


#### step.2 添加一个用来呈现3D的`<div>`标签

在您的`HTML`页面中，添加一个`<div>`标签用来呈现渲染3D模型视窗，并给定一个唯一`id`属性，同时指定`width`，`height`属性manpang

```html
<div id="forface-container-div" style="width:100%; height: 100vh;"></div>
```

#### step.3 初始化`Forface3DViewer`实例

最后一步写`Javascript`代码，初始化`Forface3Dviewer`，即可实现3D模型的web端展示预览

```js
// 初始化
Forface3dViewer.Init('forface-container-div', {
    // 必须的
    appId: 'CA884D4537B75AE8382185723DCEC918',
    secretKey: 'F9C5AD37257632619B2F889AE77EECB0'
}).then(function(){
    // 加载模型
    Forface3dViewer.viewer.loadModel('FC65B7B5C67180B04F461E2CC414EB41')
})
```

代码解析

`Forface3dViewer.Init()` 为初始化静态方法，只要引用了Forface的Js库，即可使用该方法进行初始化

`appId`及`secretKey` 为Forface系列产品必须提供的，获取appId及secretKey的方式可看[前序准备及开发环境](./essentials/env)

`Forface3dViewer.viewer.loadModel()` 为加载模型的方法，该方法提供需要提供`ModelKey`，ModelKey的获取方式可查看[上传3D模型](./essentials/upload)

> 关于Forface3dViewer更多的接口Api使用方法可查看[Forface Js API开发文档](https://www.fa-part.com/manual/jsdoc/)


## 完整的Demo代码

最后赠送给大家一套完整Demo代码，可作为开发测试用

>如您已经拥有`appId`及`secretKey`，同时也拥有相应的`modelKey`，替换代码中的值即可立即看到效果

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<title>Forface 3D Viewer - Example</title>
		<meta charset="utf-8">
        <meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0">
        <link href="https://www.fa-part.com/forface-libs/forface3dViewer/style.css" rel="stylesheet" />
	</head>
	<body style="margin: 0">
        <div id="forface-container-div" style="width:100%; height: 100vh;"></div>
        <script src="https://www.fa-part.com/forface-libs/forface3dViewer/viewer3D.min.js"></script>
        <script>
        // 初始化
        Forface3dViewer.Init('forface-container-div', {
            // 必须的
            appId: 'CA884D4537B75AE8382185723DCEC918',
            secretKey: 'F9C5AD37257632619B2F889AE77EECB0'
        }).then(function(){
            // 加载模型
            Forface3dViewer.viewer.loadModel('FC65B7B5C67180B04F461E2CC414EB41')
        })
        </script>
	</body>
</html>
```

如一切正常，在浏览器访问该页面可看到如下下过！恭喜您，成功开发出自己的`第一个3D Demo应用`

<img src="./img/3d-demo.png">

> 注意：上面的页面需要`以web服务的形式访问`方可正常浏览。直接在本地以本地文件的形式`双击是无法正常浏览的`

> 快速搭建一个web服务可使用[nginx快速搭建前端web服务](./faq/webserver)，也可使用[node.js快速搭建前端web服务](./faq/webserver)