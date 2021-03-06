Changelog
================

Version 1.1.1
-------------------
+ 修复微信支付 JS API 签名问题

Version 1.1.0
-------------------
+ 增加微信公众号第三方平台接口, 感谢 @hunter007 的贡献

Version 1.0.5
--------------------
+ 修复 Python 3 下解密消息报 TypeError 的 bug

Version 1.0.4
---------------------
+ 摇一摇周边接口 bug 修复
+ 更新自动重试的 error codes
+ ``WeChatClient._request`` 方法在解析 JSON 失败时返回原始 Response 对象

Version 1.0.3
---------------------
+ 群发消息增加上传图片接口
+ 修复下载永久素材接口错误

Version 1.0.2
---------------------
+ ``WeChatClient`` 初始化性能提升（Python 2.7+）
+ ``WeChatClient`` 数据乱码问题解决
+ Session storage ``get`` 方法增加可选默认值参数

Version 1.0.1
---------------------
+ 修复微信支付接口中文乱码问题
+ 微信支付订单查询接口 ``client_ip`` 参数可选，并修复了一些问题
+ 增加微信连 Wi-Fi 接口
+ 摇一摇周边接口增加 ``get_apply_status`` 接口
+ 摇一摇周边 ``add_material`` 接口增加 ``media_type`` 可选参数

Version 1.0.0
---------------------
+ 增加 Session 机制，目前只用来存储 access_token 等，支持 Redis, Memcached, 内存和 Shove 等存储 backend.
+ 增加微信门店接口
+ 增加摇一摇周边事件，添加页面接口增加 ``page_url`` 参数
+ reraise ``requests.RequestException`` 为 ``WeChatClientException``
+ 修复继承 ``WeChatClient`` 导致不能正常工作的问题
+ 企业号增加素材管理接口
+ 企业号增加 JS SDK API
+ 企业号增加 ``user_id`` 和 ``openid`` 互相转换接口
+ 企业号增加 OAuth 授权接口

Version 0.9.1
---------------------
+ 群发预览接口支持对指定微信号发送预览
+ 增加微信支付现金红包接口
+ 增加微信支付代金券接口
+ 增加微信支付企业付款接口
+ 增加微信支付公众号支付接口

Version 0.9.0
---------------------

+ 代码层面 API Endpoint 从实例属性变为类属性，在实例化后依然会和对应的实例绑定。此更改对库使用者而言是透明的。
+ `WeChatClient` 原有的 `_get` 和 `_post` 更名 `get` 和 `post`, 以前的接口依然保留。对于 wechatpy 没有实现的接口，可以使用 `get` 和 `post` 自行实现。

Version 0.8.7
--------------------

+ 修复多客服接口多个问题

Version 0.8.7
------------------

+ 修复群发视频上传视频证书验证不通过的问题
+ 增加了删除分组接口
+ 增加了发送卡券消息接口
+ 增加了群发卡券消息接口

Version 0.8.6
-------------------

+ 修复了图文消息图文数量一直递增的问题
+ 从此版本开始不再支持 Python 3.2（cryptography 不支持，PyCrypto 应该还可以）
+ 从此版本开始 Travis CI 上增加了 Python nightly build（Python 3.5-dev） 的测试

Version 0.8.5
-------------------

+ WeChatOAuth 增加 qrconnect_url 属性
+ 被动响应消息增加 create_time 属性（通过解析 time 时间戳获得的 datetime.datetime 对象）
+ 增加了模板消息设置行业接口
+ 增加了模板消息获取模板 ID 接口

Version 0.8.4
--------------------

+ 修复了 WeChatOAuth 编码问题
+ 修复了企业号更新部门接口 parentid 参数错误问题
+ 企业号创建部门接口增加 order 和 id 可选参数

Version 0.8.3
--------------------

+ 群发消息接口增加 is_to_all 参数
+ 群发消息接口支持预览（增加 preview 参数）
+ 修复了群发消息的一个 bug
+ 素材管理接口增加获取素材数量 API

Version 0.8.2
---------------------

+ 修复 WeChatClient access_token 过期自动重试的一个 bug
+ 增加摇一摇周边接口
+ 增加设备功能接口

Version 0.8.1
---------------------

+ 增加获取菜单配置接口
+ 增加获取自动回复规则接口
+ 更新客服消息接口，支持使用特定客服账号发送消息
+ 修复 OAuth 验证接口错误

Version 0.8.0
---------------------

+ 消息加解密兼容 cryptography 和 PyCrypto 库
+ 企业号增加异步任务接口
+ 增加小视频消息类型

Version 0.7.6
---------------------

+ 增加 JSSDK 接口
+ 增加语义理解接口
+ 增加素材管理接口
+ 增加客服会话管理接口
+ 企业号增加 agent 管理接口
