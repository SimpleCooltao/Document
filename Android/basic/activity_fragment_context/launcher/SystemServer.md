### SystemServer 进程  
在 ZygoteInit.main()方法里 调用 forkSystemServer 方法 fork 了 SystemServer；  
SystemServer一个进程，是由zygote进程fork出来的。系统里面重要的服务都是在这个进程里面开启的，比如   
ActivityManagerService、PackageManagerService、WindowManagerService、DisplayManagerService等等。  
最后调用Looper.loop(); 进行消息循环，后续会处理相关消息；  
◆ SystemServer在启动时做了如下工作：   
◐ 启动Binder线程池，这样就可以与其他进程进行通信。   
◐ 创建SystemServiceManager用于对系统的服务进行创建、启动和生命周期管理。   
◐ 启动各种系统服务。  


> 参考  

http://blog.csdn.net/qq_23547831/article/details/51105171    
http://blog.csdn.net/itachi85/article/details/55053356  
http://liuwangshu.cn/framework/booting/3-syetemserver.html  


