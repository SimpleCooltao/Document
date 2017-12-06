#### 稳定性、低功耗  

● 异常处理，尽量保障应用不会出现crash；  
● 大一点的对象，array、list、map，在不用的时候，需要及时clear；  
● 广播、EventBus之类的，也要及时解除注册；  
● 对于循环动画，在onStop 或者 onPause 暂停，GPU不断刷新视图也是很耗电的；  
● Application、Activity 启动的时候，不能有过多的操作，如果需要耗时操作，要用多线程处理；  
● 最好不要静态持有Activity，或者有 较长生命周期的对象，不要持有较短生命周期的对象引用，会造成内存泄漏；  
● 对于Bitmap或者本地的Drawable，最好先压缩处理在展示，或者用Glide等开源框架做处理；  
● 循环语句里面，不要重复造对象的引用，字符串拼接最好要使用StringBuild；  
● HashMap、ArrayList 初始化时，最好预估计其容量，扩容也是比较耗时的；  