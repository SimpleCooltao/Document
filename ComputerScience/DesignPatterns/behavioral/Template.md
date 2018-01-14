### Template  
AbsTemplate抽象类，定义一套算法框架  
ConcreteImplA ConcreteImplB 具体实现类  
定义  
模板方法模式定义一个操作中的算法框架，将一些步骤延迟到子类中，使得子类可以不改变一个算法结构，子类可以重写算法中某些特定步骤。  

使用场景  
多个子类有公有的方法，并且逻辑基本相同时，复杂的算饭，将核心算法设计为模板方法，周边的相关细节功能由各个子类实现  
重构时，经常使用模板方法模式，将相同的代码抽取到父类中，然后通过钩子约束其行为  