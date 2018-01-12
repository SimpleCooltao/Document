### 对象引用 

♬ 强引用  
通常我们使用new操作符创建一个对象时所返回的引用即为强引用  
♬ 软引用  
若一个对象只能通过软引用到达，那么这个对象在内存不足时会被回收，  
♬ 弱引用  
若一个对象只能通过弱引用到达，那么它就会被回收（即使内存充足），   
♬ 虚引用  
虚引用是Java中最“弱”的引用，通过它甚至无法获取被引用的对象，它存在的唯一作用就是当它指向的对象回收时，
它本身会被加入到引用队列中，这样我们可以知道它指向的对象何时被销毁。

◆ 强引用  
通常我们通过new来创建一个新对象时返回的引用就是一个强引用，若一个对象通过一系列强引用可到达，它就是强可达的，那么它就不被回收  


◆ 弱引用  
弱引用对象的存在不会阻止它所指向的对象被垃圾回收器回收。  
假设垃圾收集器在某个时间点决定一个对象是弱可达的，也就是说当前指向它的全都是弱引用，  
这时垃圾收集器会清除所有指向该对象的弱引用，然后把这个弱可达对象标记为可终结(finalizable)的，这样它随后就会被回收。  
与此同时或稍后，垃圾收集器会把那些刚清除的弱引用放入创建弱引用对象时所指定的引用队列(Reference Queue)中。  
