gso
===
这是一个用NodeJs编写的Google搜索服务，原理是拿着用户的关键词去Google服务器搜索，然后将返回的结果响应给用户。

安装：

`git clone https://github.com/lenbo-ma/gso.git`

`cd gso`

`npm install`


Run:

` ./bin/run`

或使用[forever](https://github.com/nodejitsu/forever)启动(推荐在生产环境中使用forever管理)

`forever start -e err.log -o output.log ./bin/run`

或使用[pm2](https://github.com/Unitech/pm2)启动

`pm2 start ./bin/run -i max`

最近新增:

1. 增加“相关搜索”功能；
2. opensearch, 支持Firefox,Chrome设置为默认搜索引擎；
3. 简单的敏感词检测，否则连接会被qiang重置；
4. html代码压缩，使用html-minifier模块进行压缩已渲染好的html代码；
5. headroom功能(当页面向下滚动时，搜索区消失，当页面向上滚动时，搜索区又出现了。个人觉得这个体验对小屏幕笔记本及pad比较好，尤其是手机终端); 

todo：

1. 响应式设计(终端对象：桌面，平板)，字体优化，并且为手机创建专门的页面(因交互方式和桌面端差别较大);
2. 实现https功能(关键词加密);
3. 增加在线代理功能(代理搜索结果中出现的部分被屏蔽的网站)；

[可用服务列表](https://github.com/lenbo-ma/gso/wiki/%E5%8F%AF%E7%94%A8%E6%9C%8D%E5%8A%A1%E5%88%97%E8%A1%A8)
