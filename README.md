###前言
***
欢迎你加入 bong 开放平台的大部落，对于每一位开发者我们都倍感珍贵。不需要掌握硬件知识和拥有专业设备，你就可以学习和运用通过传感器全时监测所获得前所未有的海量身体数据，开发出真正把虚拟带入现实的各种有趣应用，并且通过这些应用去改善你所关心的人们的生活。第三方应用将内嵌到 bong iOS 和 Android 软件中，每一位 bong 用户均可以访问到这些应用。

- **此文档适合无线应用和web应用查看**
- **无线应用**请查看[**android SDK 文档**] (https://github.com/Ginshell/bongSDK-android)和 [**iOS SDK 文档**](https://github.com/Ginshell/bongSDK-iOS)
- **如果你有一款硬件希望和bong支持的腕部设备进行互动，请查看[《bong第三方硬件设备接入》](https://github.com/Ginshell/bongOpenPlatform/blob/master/hardwaredevice.md)**
- 如果你对我们的开发文档**有疑惑**：[请向我们提问](https://github.com/Ginshell/bongOpenPlatform/issues/new)
- 提问前可以先**搜索你的问题**：[搜索已解决的问题](https://github.com/Ginshell/bongOpenPlatform/search?utf8=%E2%9C%93&q=%E8%BE%93%E5%85%A5%E4%BD%A0%E7%9A%84%E9%97%AE%E9%A2%98&type=Issues)

###加入开发者计划
Step 1: 提交申请 
任何对 bong 有兴趣的开发者都可以申请完全免费的开发者计划。点此立即[申请成为开发者](http://www.mikecrm.com/f.php?t=5FJFxc)。
**请注意：蓝牙数据同步功能只是为了不打开bong APP同步而设计的，返回的结果是bong云端算法的计算结果，与bong APP的数据一致。无法拿到bong的传感器原始数据!**

Step 2：审核
请耐心等待1-4个工作日。

Step 3：获得token
经过认证后，即可成为 bong 开放平台的开发者，获得授权开发者头衔，提前享受最新最火热的内测消息。我们更提供创意支持（用户投票的 [bong 原型菜园](http://openbong.lofter.com)），测试用户募集，用户调研，运营支持等全方位免费配套的服务，帮助你在快速成长的 bong 平台上获得成功。


###关于bong
bong 是世界上第一个能够全自动识别你的运动和睡眠状态的手环，只要佩戴在手腕上，无需手动切换识别状态。更重要的是，续航能力长达四周，省去频繁充电的烦恼，而且佩戴无感，不会有卡手的感觉。现在 bong 更进一步，通过开放接口与第三方应用开发者实现合作共赢，帮助你在可穿戴设备的第一波浪潮中抢得先机。

###bong无线开放平台
####[android SDK 文档](https://github.com/Ginshell/bongSDK-android)
####[iOS SDK 文档](https://github.com/Ginshell/bongSDK-iOS)

bong开放平台为无线应用（移动app）提供各种基础能力和服务，以让app开发者快速、低成本和bong互通：

1. 分享能力：获取Yes! 键 短触、长触事件，获取bong传感器数据。
2. 数据开放：通过sdk获取、驾驭海量数据。

###OAuth 2 认证
####授权原理图示
![](https://raw.githubusercontent.com/Ginshell/bongOpenPlatform/master/images/auth.png)

####OAuth 2文档和库
1. [OAuth 2](http://oauth.net/2/)

###授权过程
1. [需要向我们提交的资料](docs/signup.md)
2. [测试和正式环境的地址](docs/address.md)
3. [请求 request_token](docs/request_token.md)
4. [请求 access_token](docs/access_token.md)
5. [用 refresh_token 重新请求 access_token](docs/refresh_token.md)
6. [签名密钥](docs/signature.md)

###API说明
1. [名词说明](docs/api_term.md)
2. [天详细数据接口](docs/api_bongday.md)
3. [天综合数据接口](docs/api_sum.md)
4. [睡眠数据接口](docs/api_sleep.md)
5. [用户头像接口](docs/avatar.md)
6. [用户资料接口](docs/userinfo.md)
7. [推送消息接口](docs/notification.md)
8. [Yes! 键接口](docs/Yes.md)
9. [错误码说明](docs/error_desc.md)

###调测、账号注意事项
1. [测试环境]和[线上环境]的账号、数据完全独立，交叉登录则会报密码错误或未注册；开发者可到bong[开放平台]
下载测试环境的安装包，来自助注册测试账号并在测试环境使用、调测。**测试环境App下载：[iOS](http://fir.im/1os9/)、[Android](https://github.com/Ginshell/bongSDK-android/blob/master/bong_TEST_2_4_9_32.apk)**
2. 默认最初分配的AppID、AppKey等信息仅对测试环境生效，意味着只能在测试环境授权通过并调测，否则可能报授权失败。
3. 测试完成将要上线时请到[开放平台] 申请APP上线，用户即可使用，通过后线上环境即生效。

###开发环境
1. 测试环境：账号、数据与正式环境隔离，测试专用，线上用户看不到。
2. 预发环境：预发环境（GM）和线上环境账号、数据体系一致，预发环境测试通过后将发布线上。
3. 正式环境：线上用户使用的环境。


###用户界面规约
1. [用户界面规约 v0.1](docs/uig.md)

###接入流程
1. 提交应用。认证开发者需要提交的内容有：应用名称，重定向 URI，APP 主页，图标，应用说明（OAuth 2）。
2. 测试开发。提交审核通过后，我们会返回开发者测试环境的client_id、client_secret、sign_key等信息。另外我们会提供测试环境的测试账号以及bong的测试app，测试app中会展示开发者的测试应用，并可点击进入，帮助开发者调通整个流程。
3. 联调上线。第三方应用和 bong 开放平台的测试环境联调成功后，可以申请接入正式环境，申请接入时需要提供应用的使用文档，通过后正式发布到 bong app 内置的「我的应用」栏目中去。
4. 后期运营。我们目前会通过官方宣传渠道和应用内的「编辑推荐」的办法为有创意的应用提供持续的用户导入。

###什么样的应用将被拒绝
1. 暴露用户隐私 
2. 不符合国家有关法律法规
3. 广告或含有大量广告材料
4. 与宣传的功能不符或含有隐藏、虚假的功能
5. 界面粗糙，逻辑含有错误以及过于消耗手机电能
6. 载入速度过慢，导致界面崩溃
7. 推广不健康的生活方式
8. 内含错误的诊断信息
9. 与已上线的应用相似的应用

###什么样的应用将被下架
1. 滥用 API
2. 上线后的运营过程中出现了被拒绝应用中的任何一条的
3. 恶意记录、传播用户授权的信息

###运营支持
上线后，我们会持续对有创意有趣味的 app 进行运营上的支持和推广。
