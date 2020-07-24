## 前序准备

#### 成为Forface开发者

使用Forface系列产品，您需要先前往Forface开放平台[注册成为Forface开发者](https://account.fa-part.com)。注册成功后，在`产品中心`->`拥有的产品`下默认会有个`3D预览器`产品。展开该产品，点击`进入管理`，进入您的3D预览器管理页面，在这里，您可以管理您的所有的3D模型。

> 新注册的用户将免费赠送100个云币，用于平台上的各种消费，如：模型在线转换



#### 获取Access许可凭据

注册成功成为Forface开发者后，可在`我的应用`->`所有的Apps`中，创建一个App,如下图：

<img src="./img/create_app.png">

创建成功后，打开新创的`App`，可以查看`AppId`及`SecretKey`，如下图：

<img src="./img/app.png">

有了`AppId`及`SecretKey`后，您就可以愉快地进行Forface 3D Viewer二次开发了

## 开发环境

#### ES5(Javascript)下开发

只需在html页面的`<head>`中引入`Forface 3D Viewer`的Javascript库即可立即开始二次开发

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<title>Forface Test Demo- Example</title>
		<meta charset="utf-8">
        <meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0">
        <link href="http://www.fa-part.com/forface-libs/forface3dViewer-lib/style.css" rel="stylesheet" />
        <script src="http://www.fa-part.com/forface-libs/forface3dViewer-lib/viewer3D.min.js"></script>
	</head>
	<body style="margin: 0">
        <div id="forface-div" style="width:100%; height: 100vh;"></div>
	</body>
</html>
```

> 注意：为确保您的`Forface 3D Viewer` JS库是最新版本，建议您直接引用我们官方提供的Js库资源路径。

#### Forface Javascript Lib 唯一官方资源路径

使用`Forface 3D Viewer`必须引用两条资源，如下所示。为提升页面响应速度`<script>`资源可放在`<body>`标签内。

```html
<link href="http://www.fa-part.com/forface-libs/forface3dViewer-lib/style.css" rel="stylesheet" />
<script src="http://www.fa-part.com/forface-libs/forface3dViewer-lib/viewer3D.min.js"></script>
```

>注意：如需要离线部署您的项目，可联系我司单独提供解决方案