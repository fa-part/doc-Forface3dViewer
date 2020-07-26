## 上传3D模型并生成预览

基于Forface 3D Viewer开发一款3D展示应用前，您需要有3D模型。Forface 3D Viewer提供的云端`3D模型管理`服务，可以统一管理您需要展示的各种格式的3D模型。

Forface 3D Viewer Js库只需提供一个3D模型的`modelKey`，即可自动完成模型的加载、渲染、展示等。使用Forface 3D Viewer的云端3D模型管理服务可最大化的减轻您的开发量，节省成本，让你集中精力开发核心业务。

#### step.1 上传一个3D模型

上传3D模型到Forface 3D Viewer的云端`3D模型管理`后，方可通过Forface 3D Viewer提供的Js库加载该模型。上传过程如下：


首先，登录到[Forface账户中心](https://account.fa-part.com)->进入`产品中心`->[拥有的产品](https://account.fa-part.com/zh/myProducts/)，展开`3D预览器`，点击`进入管理`进入`3D预览器`管理页面如下图:

<img src="./img/manager.png">

然后，进入[我拥有的模型](https://account.fa-part.com/zh/myProducts/)，点击`上传模型`，开始上传模型。

Forface 3D Viewer支持的3D模型格式覆盖了FA行业的主流格式，支持的格式见[介绍](./essentials/introduction)。3D模型上传好后，如下所示:

<img src="./img/myModels.png">

#### step.2 转换生成预览

模型上传完毕后，需要自动构建生成预览后，放可在`Forface 3D Viewer`中正常预览模型。点击`配置`->`生成预览`，按提示确认转换生成预览

>每个新上传的3D模型都需要转换生成3D预览后，方可在线预览3D模型，Forface 3D Viewer才能正常加载。转换生成预览是需要支付若干`云币`的，新用户默认赠送100个云币，这些云币足够您进行开发测试用的。

>云币用完后，是需要充值的，没有云币请[点这里进行充值](https://account.fa-part.com/zh/cloudAccount/topUp)

<img src="./img/change.png">

模型转换需要一点时间。根据模型大小复杂度，转换的时间会不一样，模型转换结束后，会邮件通知到您的注册邮箱。

<img src="./img/success.png">

点击转换完成的模型，在线预览3D模型

<img src="./img/3d_preview.png">

#### step.3 获取`ModelKey`


模型转换结束后，您就可以根据模型的`modelKey`，通过`Forface 3D Viewer` Js库加载该模型了。

获取模型`modelKey`的方法有两种

<img src="./img/view_modelKey.png">

第一种，查看指定模型的`modelKey`；点击模型列表中的`复制Icon`按钮，可快速复制`modelKey`，复制成功提示如下：

<img src="./img/copy_modelkey.png">

第二种，可通过批量导出您拥有的所有可用的3D模型的`modelKey`列表；点击左上角的`导出ModelKey`按钮，可下载excel文件格式的`modelKey`列表

<img src="./img/export.png">