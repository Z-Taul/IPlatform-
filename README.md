# IPlatform
基于WEB的个人接口计费管理平台，基于这个接口管理平台，可以接上需要进行计费管理的的其他服务（通过http调用，微服务化），比如java服务，或是python服务、node express服务，这里已一个识别服务为例，适合二次开发
# 环境
* JDK1.8
* SpringBoot 2.6.3
* MySql Server 5.7.39
* Redis 5.0.10
* 前端包括vue2、webpack5、elementUI等
# 项目优势
* 支持以一个用户一个secret形式对需要进行进行管理的接口服务进行统计、计费
* 支持用户端的多线程并发请求
* 线程数可控，可以配置constant/ServerConfigConstants/MAX_DISCERN_CONCURRENT参数控制同时处理的并发线程
* 数据灵活化，所有可能会变动的数据（比如页面的配置显示信息）都存于数据库中，与运行的应用程序解耦，灵活配置，比如前端打开获取通知信息、导航栏文字显示内容等
* 记录用户调用ip，采用redis缓存热点数据及用户的异常行为，通过配置，若达到一定条件，则认为用户存在大量无效请求，为防止服务器资源滥用，熔断拒绝服务，待达到一定时间或用户可疑消除则恢复正常
* 搭配前端友好用户数据展示、记录页面
* 可以容易地根据更多需求在这个基础上进行扩展
* 更多功能等待你的发现
