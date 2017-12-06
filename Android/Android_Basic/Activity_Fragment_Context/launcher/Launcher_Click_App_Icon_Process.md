#### 点击Launcher中，App的图标后，发生了什么  

#### 启动流程：  
①点击桌面App图标，Launcher进程采用Binder IPC向system_server进程发起startActivity请求；  
②system_server进程接收到请求后，向zygote进程发送创建进程的请求；  
③Zygote进程fork出新的子进程，即App进程；  
④App进程，通过Binder IPC向sytem_server进程发起attachApplication请求；  
⑤system_server进程在收到请求后，进行一系列准备工作后，再通过binder IPC向App进程发送scheduleLaunchActivity请求；  
⑥App进程的binder线程（ApplicationThread）在收到请求后，通过handler向主线程发送LAUNCH_ACTIVITY消息；  
⑦主线程在收到Message后，通过发射机制创建目标Activity，并回调Activity.onCreate()等方法。  
⑧到此，App便正式启动，开始进入Activity生命周期，执行完onCreate/onStart/onResume方法，UI渲染结束后便可以看到App的主界面。  
上面的一些列步骤简单介绍了一个APP启动到主页面显示的过程，可能这些流程中的一些术语看的有些懵，什么是Launcher，什么是zygote，什么是applicationThread.....  

> 参考  
- https://github.com/LRH1993/android_interview/blob/master/android/advance/app-launch.md