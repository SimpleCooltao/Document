###  Android  

Jvm、Dalvik、Art和对比；  
如何保持应用的稳定性、低耗电；  
App启动流程，从点击桌面开始；  
Application 的 Context 和 Activity 的 Context；  

横竖屏切换的时候，Activity 各种情况下的生命周期；  
Fragment生命周期；  
Fragment状态保存；  
Fragment getActivity 为什么会 null；  
ViewPager使用细节，如何设置成每次只初始化当前的Fragment，其他的不初始化；  

SP是进程同步的吗?有什么方法做到同步；   

Handler机制及底层实现；  
handler实现机制（很多细节需要关注：如线程如何建立和退出消息循环等等）；  
Handler.postDelay 一定能收到吗？  
Service 的生命周期；  
BroadcastReceiver；  
Binder机制及底层实现；  
什么是AIDL 以及如何使用；  
BroadcastReceiver，LocalBroadcastReceiver 区别  



一张Bitmap所占内存以及内存占用的计算；  
ListView和RecyclerView区别  
既然RecyclerView在很多方面能取代ListView，Google为什么没把ListView划上一条过时的横线？  
```
答案： 可以沿着回收机制来回答。ListView采用的是RecyclerBin的回收机制在一些轻量级的List显示时效率更高  
```
你用过MD，你知道怎么定义一个Behavior吗？      https://www.jianshu.com/p/82d18b0d18f4  
AlertDialog,popupWindow,Activity区别；  


Serializable 和Parcelable 的区别；  

ArrayMap<Int, Int>  
SparseArray<Int>  
SparseBooleanArray  
SparseIntArray  
SparseLongArray  
LongSparseArray<Int>  

多线程断点续传原理；  
网络请求，怎么打包数据；  
OkHttp；
RxJava；  
Retrofit；  
Glide；  
EventBus；  
图片加载原理；  
Https请求慢的解决办法，DNS，携带数据，直接访问IP；  

热修复；  
插件化；  
组件化；  

1. IPC机制，Binder和匿名共享内存等
2. 四大组件启动，工作原理
3. View系统，绘制原理，事件分发
4. 动画框架，原理
5. 多线程机制，消息机制 AsyncTask，Thread/Handler
6. 系统启动过程，system_server启动过程
7. Window系统，Window创建过程
8. 资源管理系统，资源加载机制等


◆ 参考  
https://github.com/Blankj/AndroidOfferKiller  
https://github.com/JackyAndroid/AndroidInterview-Q-A  
https://github.com/francistao/LearningNotes  
https://github.com/leerduo/InterviewQuestion  
https://github.com/Mr-YangCheng/ForAndroidInterview  
http://www.jianshu.com/p/89f19d67b348  
https://github.com/suzeyu1992/repo  
https://www.jianshu.com/p/735be5ece9e8  
https://github.com/Freelander/Android_Data  
http://www.jianshu.com/nb/3450453  
https://github.com/LRH1993/android_interview  
https://juejin.im/post/59e54b9051882578cb511f00  
http://blog.csdn.net/axi295309066/article/details/51275470  
https://www.jianshu.com/p/b5ba11275a6d  
https://www.jianshu.com/p/dfa6d4caedad  
https://www.jianshu.com/p/3df3d2974234    
https://www.jianshu.com/p/a22450882af2  
https://www.jianshu.com/p/fb815eaf628f  
https://juejin.im/post/5aa721936fb9a028d4443d8b  
http://blog.csdn.net/qian520ao/article/details/79601179  
https://github.com/MindorksOpenSource/android-interview-questions  
https://www.jianshu.com/p/c70989bd5f29  
https://github.com/AweiLoveAndroid/CommonDevKnowledge  
https://github.com/guoxiaoxing/android-interview  
https://juejin.im/post/5b97ab465188255c865e030a  
https://juejin.im/post/5b8f15e26fb9a01a031b12d9  