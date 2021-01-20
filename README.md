## bidataval 项目自动生成  

##### 1.项目Clone下来后，默认使用local-profile运行项目，可直接运行Application.java看项目效果，local中的配置仅为Demo，后续需要根据自己的业务重新配置  

##### 2.项目启动后，可通过访问以下URL来测试组件集成
> 测试连接数据库：http://localhost:8080/demo/test/database  
> 测试连接Redis：http://localhost:8080/demo/test/redis  
> 测试集成missconf：http://localhost:8080/demo/test/missconf  
> 测试集成MQ：http://localhost:8080/demo/test/mq  (访问后会发MQ消息，与此同时DemoConsumer会消费MQ，通过控制台日志可以看出)  

##### 3.因为是demo原因，local配置中的logback-extend.xml只起到示例作用，其他profile下的logback-extend.xml默认没有内容，需要根据项目情况自己配置。
> misslog的logback-extend.xml配置可参考：http://wiki.missfresh.net/pages/viewpage.action?pageId=51323932

##### 4.可以通过使用单元测试DemoTest，查看各组件集成效果

##### 5.部署到dev、test、pre、prod等环境前，请修改对应的profile下的配置文件，确保连接正确环境（配置中${required.xxx}都是需要手动修改的配置）
> 关于如何通过max发布到开发、测试环境，参考下面#关于如何接入自动部署#

## 关于如何接入自动部署（开发/测试环境）
##### 1.在项目接入Max自动部署系统之前，请先确保项目在应用中心已创建appCode
> 参考链接：http://taotie.missfresh.net/home

##### 2.接入Max
> 通过脚手架创建的项目，默认在Max中


## 关于如何接入自动部署（预发/生产环境）

## 参考文档
##### 日志组件接入手册
> http://wiki.missfresh.net/pages/viewpage.action?pageId=37343589  

##### 限流降级接入手册
> http://wiki.missfresh.net/pages/viewpage.action?pageId=37351764  

##### 主商城Dubbo Provider端口记录（测试环境端口隔离）
> http://wiki.missfresh.net/pages/viewpage.action?pageId=4917593