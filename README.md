# XMall




### 单体版获取
- 单体XMall系统 非分布式 可跑在1g1核服务器上
- 获取方式：进入商城登陆后随意测试支付商品 填写捐赠信息 支付成功后将自动发至您填写的邮箱

### 前台页面为基于Vue的独立项目 

- 微信小程序APP 
    
![](https://i.loli.net/2018/07/21/5b52e1de385e7.png)
    
![](https://i.loli.net/2018/07/21/5b52e274d2085.png)
    
- - 

### 基于SOA架构的分布式购物电商商城
- [x] 后台管理系统：管理商品、订单、类目、商品规格属性、用户、权限、系统统计、系统日志以及前台内容等功能
- [x] 前台系统：用户可以在前台系统中进行注册、登录、浏览商品、首页、下单等操作
- [x] 会员系统：用户可以在该系统中查询已下的订单、管理订单、我的优惠券等信息
- [x] 订单系统：提供下单、查询订单、修改订单状态、定时处理订单
- [x] 搜索系统：提供商品的搜索功能
- [x] 单点登录系统：为多个系统之间提供用户登录凭证以及查询登录用户的信息

### v1.1更新日志(需更新前后台代码及SQL)
- [x] 更新Dubbo(2.6.1)、ES(6.2.3)等依赖版本 
- [x] 取消ES需在页面中配置及跨域问题，ES默认配置集群名改为原elasticsearch
- [x] 修复后台统计热卖商品SQL错误，xmall-front-web模块支持SpringMVC文件上传配置
- [x] 修改金额字段类型优化SQL与备注
- [x] 优化后台页面 修复用户修改BUG 优化批量删除 优化商品分类添加
- [x] 重构首页，后台可配置，包括3D轮播图
- [x] 后台新增缓存管理功能菜单 完成订单打印发货等功能，实现快递管理
- [x] 增添订单统计报表
- [x] 修复前后端分离极验验证码session存储问题
- [x] 实现ES IK分词插件扩展词典库管理
- [x] 增添限流
- [x] 2018.7.22 取消快速搜索接口需前端配置 发送邮件端口改为465
- [x] 2018.7.24 修复添加分类BUG
- [x] 2018.7.27 首页导航栏可后台配置
- 注：SKU设计预计将在开源小程序后台实现
- [极验验证码移除文档](https://github.com/Exrick/xmall/wiki/%E6%9E%81%E9%AA%8C%E7%A7%BB%E9%99%A4%E6%96%87%E6%A1%A3)

![](https://i.loli.net/2018/07/22/5b5460eb23cb9.jpg "登录界面")

![](https://i.loli.net/2018/07/22/5b5461099039e.jpg "后台首页")

![](https://i.loli.net/2018/07/22/5b546125886ca.jpg "商品管理")

![](https://i.loli.net/2018/07/22/5b54613bc866f.jpg "管理员编辑")

![](https://i.loli.net/2018/07/22/5b54615b95788.jpg "前台首页")

![](https://i.loli.net/2018/07/22/5b5461756b2b0.jpg "ES分词搜索")

### 项目架构及功能模块图

![](https://i.loli.net/2018/07/22/5b5461926969b.png)

![](https://i.loli.net/2018/07/22/5b5461aa2fdee.jpg)

![](https://i.loli.net/2018/07/22/5b5461c54cb55.jpg)

### 前端所用技术
- 后台页面
    - 感谢 [H-ui](http://www.h-ui.net/)、[FlatLab](https://github.com/Exrick/xmall/blob/master/study/FlatLab.md) 提供静态页面支持
    - [Ztree](http://www.treejs.cn/v3/main.php#_zTreeInfo)：jQuery树插件
    - [DataTables](http://www.datatables.club/)：jQuery表格插件
    - [Layer](http://layer.layui.com/)：web弹层组件
    - [Distpicker](https://github.com/fengyuanchen/distpicker)：中国省市区地址三级联动插件
    - [KindEditor](https://github.com/kindsoft/kindeditor)：富文本编辑器 简洁方便 没UEditor那么多坑
    - [WebUploader](http://fex.baidu.com/webuploader/getting-started.html)：百度文件上传插件
    - [HighCharts](http://www.hcharts.cn/)：图表库
    - [不蒜子](http://busuanzi.ibruce.info/)：极简网页计数器
- 前台页面
    - 详情请跳转至 [xmall-front](https://github.com/Exrick/xmall-front) 项目仓库
    - 感谢 [yucccc](https://github.com/yucccc) 的开源 [vue-mall](https://github.com/yucccc/vue-mall) 项目提供前端页面及框架支持
    - Vue2 + Vuex + Vue Router + Element UI + ES6 + webpack + axios + Node.js
    
### 后端所用技术
##### 各框架依赖版本皆使用目前最新版本 可进入xmall-parent中 [pom.xml](https://github.com/Exrick/xmall/blob/master/xmall-parent/pom.xml) 查看
- Spring
- [SpringMVC](https://github.com/Exrick/xmall/blob/master/study/SpringMVC.md)
- MyBatis
- [Dubbo](https://github.com/Exrick/xmall/blob/master/study/Dubbo.md)
- [ZooKeeper](https://github.com/Exrick/xmall/blob/master/study/Zookeeper.md)
- MySQL
- Mycat：数据库分库分表中间件
- [Redis](https://github.com/Exrick/xmall/blob/master/study/Redis.md)：缓存
- [Elasticsearch](https://github.com/Exrick/xmall/blob/master/study/Elasticsearch.md)：基于Lucene分布式搜索引擎
- [ActiveMQ](https://github.com/Exrick/xmall/blob/master/study/ActiveMQ.md)：消息队列
- [Druid](http://druid.io/)：阿里高性能数据库连接池
- Shiro：安全框架
- [Swagger2](https://github.com/Exrick/xmall/blob/master/study/Swagger2.md)：Api文档生成
- Docker
- [Nginx](https://github.com/Exrick/xmall/blob/master/study/Nginx.md)
- Tomcat
- [Maven](https://github.com/Exrick/xmall/blob/master/study/Maven.md)
- 第三方SDK
    - [七牛云文件存储服务](https://developer.qiniu.com/kodo/sdk/1239/java)
    - ~~[极验Test-button人机验证码](http://www.geetest.com/Test-button.html)~~ 因其收费见[极验验证码移除文档](https://github.com/Exrick/xmall/wiki/%E6%9E%81%E9%AA%8C%E7%A7%BB%E9%99%A4%E6%96%87%E6%A1%A3)
- 第三方插件
    - [hotjar](https://github.com/Exrick/xmall/blob/master/study/hotjar.md)：一体化分析和反馈
    - [搜狐畅言评论插件](http://changyan.kuaizhan.com/)
- 第三方接口
    - [Mob全国天气预报接口](http://api.mob.com/#/apiwiki/weather)：需注册账号创建应用后申请填入AppKey
- 其它开发工具
    - Jenkins：持续集成
    - ~~[JRebel](https://github.com/Exrick/xmall/blob/master/study/JRebel.md)：开发热部署~~ 现已无法免费使用
    - [阿里JAVA开发规约插件](https://github.com/alibaba/p3c)

### 文件说明
- `xmall` 文件夹提供部分依赖与sql文件
    - xmall.sql：数据库文件
    - dubbo.xsd：需手动配置避免报错
    - redis-3.0.0.gem：Redis集群搭建所需Ruby库
- `generatorSqlmapCustom` 文件夹为 [Mybatis Generator](http://www.mybatis.org/generator/) 逆向生成工具，且已配置好maven插件
### 本地开发运行部署
- 下载zip直接解压或安装git后执行克隆命令 `git clone https://github.com/Exrick/xmall.git`
- 安装各中间件并启动：[ZooKeeper](https://github.com/Exrick/xmall/blob/master/study/Zookeeper.md)、[Redis](https://github.com/Exrick/xmall/blob/master/study/Redis.md)、[ActiveMQ](https://github.com/Exrick/xmall/blob/master/study/ActiveMQ.md)、[Elasticsearch](https://github.com/Exrick/xmall/blob/master/study/Elasticsearch.md)
- 修改各配置文件相应依赖IP配置(默认本地127.0.0.1)，以及七牛云、极验配置、天气接口在 `xmall-common - utils` 中找到修改，XPay邮箱配置在 `manager-service与sso-service` 中
- [Maven安装和在IDEA中配置](https://github.com/Exrick/xmall/blob/master/study/Maven.md)
- 使用IDEA([破解/免费注册](http://idea.lanyus.com/)) `File-Open` 直接打开xmall项目，点击右下角 `Import Changes` 等待安装完依赖即可
- MySQL数据库新建 `xmall` 数据库，运行sql文件，注意在有 `db.properties` 的模块中修改你的数据库连接配置
- 按照依赖顺序分别在每个模块文件夹根目录执行 `mvn install` 命令
- 项目需运行除 `xmall-parent` `xmall-common` 以外其它所有6个服务，且都已配置好Tomcat插件, 执行命令 `mvn tomcat7:run` 或在IDEA中使用插件(`View - Tool Buttons - 右侧菜单Maven Projects - tomcat7 - tomcat7:run`)运行即可，当然可自行配置
- 后端管理系统默认端口8888 http://localhost:8888 管理员账密admin|123456
- 前端项目接口默认端口7777 前台页面请启动基于Vue的 [xmall-front](https://github.com/Exrick/xmall-front) 项目，并修改其接口配置
### 相关技术点说明
- ES-IK分词插件词典库扩展
    - 详见 [elasticsearch-analysis-ik插件作者项目README说明](https://github.com/medcl/elasticsearch-analysis-ik)
    - 本项目中扩展接口和禁用词接口分别为 `http:localhost:8888/getDictList` 和 `http:localhost:8888/getStopDictList`，将以上2个接口配置进IK插件扩展配置文件{conf}/analysis-ik/config/IKAnalyzer.cfg.xml 或者 {plugins}/elasticsearch-analysis-ik-*/config/IKAnalyzer.cfg.xml中即可，示例：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
    <properties>
        <comment>IK Analyzer 扩展配置</comment>
        <!--用户可以在这里配置远程扩展字典 -->
        <entry key="remote_ext_dict">http:localhost:8888/getDictList</entry>
        <!--用户可以在这里配置远程扩展停止词字典-->
        <entry key="remote_ext_stopwords">http:localhost:8888/getStopDictList</entry>
    </properties>
    ```
- 限流
    - `xmall-front-web` 中已配置限流，配置文件 `resource.properties` 中可配置全局限流，示例：

        ```properties
        #启用全局限流
        xmall.rateLimit.enable=true
        #每1秒内
        xmall.rateLimit.timeout=1000
        #限制10个请求
        xmall.rateLimit.limit=10
        ```
    - 指定方法限流注解
        ```java
        @RateLimiter(limit = 1, timeout = 5000)
        ```
    - 支持多维度IP、uid等限流 详见代码
- 



