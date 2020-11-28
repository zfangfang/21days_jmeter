><u>Jmeter 是一款使用Java开发的，开源免费的，测试工具， 主要用来做功能测试和性能测试（压力测试/负载测试）。</u>

1. 官网 : *https://jmeter.apache.org/*

2. 最新版本号：5.3

3. UX 变化：新增 **Darklaf** 主题

4. 启动方式：
    > a. GUI 启动：主要用于编写，调试脚本
    > b. CLI 模式（NON GUI）：命令行启动，用于压力测试。使用Jmeter的GUI界面进行大并发量的性能测试时，界面容易卡死，无法继续进行性能测试

    * **方式1：** jmeter.bat（windows）/ jmeter.sh(linux)
    运行JMeter
    * **方式2：** jmeterw.cmd
     在没有Windows Shell控制台的情况下运行JMeter（默认情况下处于GUI模式）
    * **方式3：** jmeter-n.cmd
    在其上放置一个JMX文件以运行CLI模式测试
    * **方式4：** jmeter-n-r.cmd
    在其上放置一个JMX文件以远程运行CLI模式测试
    * **方式5：** jmeter-t.cmd
    在其上放置一个JMX文件以在GUI模式下加载它
    * **方式6：** jmeter-server.bat
    在服务器模式下启动JMeter
    * **方式7：** mirror-server.cmd
    在CLI模式下运行JMeter Mirror Server
    * **shutdown.cmd**
    运行Shutdown客户端以正常停止CLI模式实例
    * **stoptest.cmd**
    运行Shutdown客户端以突然停止CLI模式实例
    
    
```
jmeter 命令行启动参数：
-h 帮助 -> 打印出有用的信息并退出
-n 非 GUI 模式 -> 在非 GUI 模式下运行 JMeter
-t 测试文件 -> 要运行的 JMeter 测试脚本文件
-l 日志文件 -> 记录结果的文件
-r 远程执行 -> 启动远程服务
-H 代理主机 -> 设置 JMeter 使用的代理主机
-P 代理端口 -> 设置 JMeter 使用的代理主机的端口号
```