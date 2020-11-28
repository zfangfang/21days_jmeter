## jmeter 21 天打卡学习

#### Day01: 熟悉jmeter官网

#### Day02: jmeter安装

#### Day03: jmeter启动
&nbsp;&nbsp; 1. 熟悉菜单栏和功能栏的作用
&nbsp;&nbsp; 2. 文件 ->模板 ->新建web模板计划，系统提供的计划里包含哪些组件？

#### Day04: 请求百度网址并查看响应
&nbsp;&nbsp; 1. 新建测试计划 ->线程组 ->取样器http请求 ->添加监听器查看结果树 
&nbsp;&nbsp; 2. http请求协议:http, 服务器或ip: www.baidu.com
&nbsp;&nbsp; 3. 启动运行，查看结果树

#### Day05: 请求百度网址并查看响应两条接口测试
&nbsp;&nbsp;  1. 新建测试计划 ->线程组 ->取样器http请求 （添加两个） 
&nbsp;&nbsp;  2. 线程组 ->添加监听器 查看结果树&断言结果 
&nbsp;&nbsp;  3. 两个http请求协议：http, 服务器或ip: www.baidu.com 
&nbsp;&nbsp;  4. 第一个http请求：添加 ->断言->响应断言；配置：测试字段为“响应文本”，模式匹配规则为“字符串”，测试模式为“百度一下” 
&nbsp;&nbsp;  5. 第二个http请求：添加 ->断言->响应断言；配置：测试字段为“响应文本”，模式匹配规则为“字符串”，测试模式为“百度二下” 
&nbsp;&nbsp;  6. 启动运行，查看结果树 

#### Day06: 配置元件之HTTP头信息+cookie管理器
&nbsp;&nbsp;  1. 新建测试计划 ->线程组 ->取样器http请求 ->添加监听器查看结果树 
&nbsp;&nbsp;  2. http请求协议：http, 服务器或ip: www.baidu.com 
&nbsp;&nbsp;  3. 启动运行，查看结果树，可以看到请求的request headers头部字段中没有Content-Type字段 
&nbsp;&nbsp;  4. http请求：添加 ->配置元件 ->HTTP信息头管理器 
&nbsp;&nbsp;  5. 在HTTP头信息管理器中添加信息头：名称”Content-Type“，值”application/json“ 
&nbsp;&nbsp;  6. 启动运行，查看结果树，可以看到请求的request headers头部字段中有Content-Type:application/json 

#### Day07: httpbin.org_get
&nbsp;&nbsp;  0. 网址: http://httpbin.org/ 
&nbsp;&nbsp;  1. 新建测试计划 ->线程组 ->取样器http请求 ->添加监听器查看结果树 
&nbsp;&nbsp;  2. http请求协议：http, 服务器或ip: httpbin.org，请求方法GET,路径/get 
&nbsp;&nbsp;  3. 若填参数：名称get，值IDO（response body中会返回响应的请求参数"args":{"get":"IDO"}） 
&nbsp;&nbsp;  4. 若填消息体数据：IDO（response body中会返回content-length:3） 
&nbsp;&nbsp;  5. 启动运行，查看结果树 

#### Day08: httpbin.org_get_put_delete
&nbsp;&nbsp; 操作方法同Day07, 分别测试请求方法GET/PUT/DELETE,路径/get, /put, /delete 。   (curl 发送http请求:https://www.cnblogs.com/alfred0311/p/7988648.html) 

#### Day09: httpbin.org_post提交表单和json
&nbsp;&nbsp;  0. 提交表单和json区别：https://www.cnblogs.com/star12111/p/13160383.html； https://zhuanlan.zhihu.com/p/102032020 
&nbsp;&nbsp;  1. 新建测试计划 ->线程组 ->取样器http请求 ->添加监听器查看结果树 
&nbsp;&nbsp;  2. http请求协议：http, 服务器或ip: httpbin.org，请求方法GET,路径/get 
&nbsp;&nbsp;  3. 若是提交表单：参数部分填名称get，值IDO；或 http请求消息体：IDO 
&nbsp;&nbsp;  4. 若是提交json：消息体数据填{”post“:"123"} 
&nbsp;&nbsp;  5. 启动运行，查看结果树 

#### Day10: 线程用户之setUp_tearDown
&nbsp;&nbsp; 1. setUp线程组可以用于测试准备，比如用它来创建测试用户等
&nbsp;&nbsp; 2. teardown线程组可以用于测试清理工作，比如删除测试用户等
&nbsp;&nbsp; 3. 与普通线程组区别在于，setUp线程在普通线程执行前自动触发执行；而tearDown线程组在主线程结束后执行

#### Day11: 配置元件之CSV数据文件配置
&nbsp;&nbsp; 参考：https://www.jianshu.com/p/c5ff791e5352

#### Day12: 逻辑控制器之循环控制器
&nbsp;&nbsp; 参考：https://www.jianshu.com/p/53335b2ff9be

#### Day13: 逻辑控制器之if控制器和简单控制器
&nbsp;&nbsp; 参考：https://www.jianshu.com/p/9e3838cfb220

#### Day14: 监听器之察看结果树+断言结果+聚合报告+图形结果+用表格察看结果
&nbsp;&nbsp; 参考 https://www.jianshu.com/p/c81806d82142
&nbsp;&nbsp; 把响应中的unicode编码转中文：https://blog.csdn.net/yyj0880/article/details/90475506
&nbsp;&nbsp; 添加后置处理器也不行，还需将jmeter.properties中默认编码设置为utf-8: sampleresult.default.encoding=utf-8
