### Charles抓包  
手机5.0以上通过数据线使用charles代理：
wifi设置代理：127.0.0.1：8888  
执行adb命令：  
adb reverse tcp:8888 tcp:8888  