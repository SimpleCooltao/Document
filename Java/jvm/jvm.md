###### JVM相关知识

> 内存划分

[程序计数器（PC）](memory/Memory_PC.md)  
[Java虚拟机栈](memory/Memory_Stack.md)  
Java虚拟机栈，通常意义上说就是 Java方法的栈帧；  
栈帧包括：局部变量表、操作数栈、动态链接、方法出口信息；  
[本地方法栈](memory/Memory_Native_Stack.md)  
[Java堆（Heap）](memory/Memory_Heap.md)    
[方法区（Method Area）](memory/Memory_MethodArea.md)  
[直接内存](memory/Memory_DirectMemory.md)  




> 类与对象 

[对象的创建](Class_CreateObject.md)  
[对象的内存布局](Class_ObjectInfo.md)  
[对象的访问定位](Class_ObjectAccessLocation.md)  
[Class类文件结构](class_file_structure/ClassFileStructure.md)    
[类加载的生命周期](class_load_lifecye/ClassLoadLifecye.md)  
[类加载器ClassLoader，与双亲委派模型](class_loader/ClassLoader.md)      




> 内存回收

[堆内存，年代划分](memory/Memory_Generation.md)  ：  年轻代、年老代、持久代    
[什么情况下触发垃圾回收](GC/GC_Trigger.md)  
[JVM怎么判断对象是否已死](GC/GC_ClassLifecycle.md)  
[判断对象是否存活与“引用”有关](GC/GC_Reference.md)   
[垃圾收集算法](GC/GC_Garbage_Collector.md)   



> Java内存模型

[Java内存模型（JMM）](jvm_library/jmm_basic_concept.md)  
[volatile 关键字](jvm_library/volatile.md)  





> 参考
- http://www.importnew.com/17770.html
- http://www.cnblogs.com/dingyingsi/p/3760447.html
- http://www.cnblogs.com/dingyingsi/p/3760730.html
- https://github.com/LRH1993/android_interview/blob/master/java/virtual-machine/Garbage-Collector.md

- 深入理解java虚拟机第三版