### Semaphore  
Semaphore是一种基于计数的信号量。  
它可以设定一个阈值，基于此，多个线程竞争获取许可信号，做完自己的申请后归还，超过阈值后，线程申请许可信号将会被阻塞。  
Semaphore可以用来构建一些对象池，资源池之类的，比如数据库连接池，  
我们也可以创建计数为1的Semaphore，将其作为一种类似互斥锁的机制，这也叫二元信号量，表示两种互斥状态。  

◑ Semaphore(permits)  
创建一个 阈值 为permits 的信号量对象，只能有permits个线程同时访问；  
也就是说，允许permits个线程同时执行 acquire 和 release 之间的代码块；  
◑ acquire  
申请许可  
◑ release  
释放许可  