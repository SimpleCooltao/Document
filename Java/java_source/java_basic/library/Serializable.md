### Serializable  
当使用 ObjectInputStream、ObjectOutputStream时，需要使用标记接口 Serializable，标记接口的目的，是为了让其能转化成字节流保存起来，    
还能将本地的字节流再转成类对象，Serializable主要应用于数据持久化、网络流；  

◆ 相关注意事项  
序列化时，只对对象的状态进行保存，而不管对象的方法；  
当一个父类实现序列化，子类自动实现序列化，不需要显式实现Serializable接口；  
当一个对象的实例变量引用其他对象，序列化该对象时也把引用对象进行序列化；  
当某个字段被声明为transient后，默认序列化机制就会忽略该字段。  
序列化的作用就是为了不同jvm之间共享实例对象的一种解决方案；  
