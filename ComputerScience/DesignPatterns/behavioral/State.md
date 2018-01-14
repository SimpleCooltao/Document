### 状态模式 
● Context（环境类）  
环境类又称为上下文类，它是拥有多种状态的对象。由于环境类的状态存在多样性且在不同状态下对象的行为有所不同，因此将状态独立出去形成单独的状态类。  
在环境类中维护一个抽象状态类State的实例，这个实例定义当前状态，在具体实现时，它是一个State子类的对象。  
● State（抽象状态类）  
它用于定义一个接口以封装与环境类的一个特定状态相关的行为，在抽象状态类中声明了各种不同状态对应的方法，  
而在其子类中实现类这些方法，由于不同状态下对象的行为可能不同，因此在不同子类中方法的实现可能存在不同，相同的方法可以写在抽象状态类中。  
● ConcreteState（具体状态类）  
它是抽象状态类的子类，每一个子类实现一个与环境类的一个状态相关的行为，每一个具体状态类对应环境的一个具体状态，不同的具体状态类其行为有所不同。  
◆ 定义  
当一个对象的内在状态改变时允许改变其行为，对象看起来似乎修改了它的类；  
◆ 使用场景  
一个对象的行为取决于它的状态，并且它必须在运行时根据状态改变它的行为，代码中包含大量与对象状态相关的条件语句  
◆ 总结
状态模式与策略模式的结构几乎是一样的，但是状态模式的行为是平行的，不可替换的；策略模式的行为是彼此独立的，是可以相互替换的。  
◆ 优点：
State模式将所有与一个特定状态相关的行为都放入一个具体状态对象中，提供了一个更好的方法来组织与特定状态相关的代码，  
将繁琐的状态判断换成结构清晰的状态类族，在避免代码膨胀的同时也保证了可扩展性与可维护性。  
◆ 缺点：  
State模式的使用必然会增加系统类和对象的个数  

◆ 状态模式 与 策略模式  
代码写起来，是比较类似，但是两者的建模思想，迥然不同；  
策略模式做的是，一个策略对应一个算法；例如优惠政策；
状态模式做的是，一种状态对应一个业务； 例如 OA审批， 到组长那里， 组长会进行处理，标记更新状态；再到经理那里，经理处理，标记更新状态；以此迭代下去。。。   
状态的迁移是由内部决定，策略的选择是由外部决定；  