### 当按下电源键   
cpu上电，芯片上的预设代码开始执行，加载引导程序 Bootloader 到ram中运行；  
Bootloader负责初始化硬件资源和加载 linux kernel，然后将控制权交给 linux kernel。    
linux kernel 得到控制权后，调用下列一系列函数：  
初始化内存分配  
初始化文件系统   
加载硬件驱动    
fork init进程，init进程会启动 ServiceManager 和 android的Zygote进程  
◆ [安卓进程模型图](../ImageFiles/launcher_001.png)  
讲到这，总结起来init进程主要做了几件事：   
◑ 创建一些文件夹并挂载设备；   
◑初始化和启动属性服务；  
◑ 启动ServiceManager为BinderDevice注册上下文管理者；   
◑ 解析init.rc配置文件并启动zygote进程；  

◆ 参考  
http://blog.csdn.net/mr_zhaojy/article/details/52776254    
http://blog.csdn.net/itachi85/article/details/54783506     
http://blog.csdn.net/hu3167343/article/details/38230271  
http://www.cnblogs.com/nokiaguy/archive/2013/04/14/3020774.html  
http://blog.jobbole.com/67931/  
http://blog.csdn.net/fu_kevin0606/article/details/53383031  
http://blog.csdn.net/sunao2002002/article/details/52454878  
http://blog.csdn.net/gaugamela/article/details/52133186  


