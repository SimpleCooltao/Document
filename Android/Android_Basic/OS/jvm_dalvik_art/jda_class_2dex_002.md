#### Dalvik可执行文件体积更小  

class文件中包含多个不同的方法签名，如果A类文件引用B类文件中的方法，方法签名也会被复制到A类文件中，  
在虚拟机加载类的连接阶段将会使用该签名链接到B类的对应方法，也就是说，多个不同的类会同时包含相同的方法签名，  
同样地，大量的字符串常量在多个类文件中也被重复使用，这些冗余信息会直接增加文件的体积，  
而JVM在把描述类的数据从class文件加载到内存时，需要对数据进行校验、转换解析和初始化，最终才形成可以被虚拟机直接使用的JAVA类型，  
因为大量的冗余信息，会严重影响虚拟机解析文件的效率。为了减小执行文件的体积，安卓使用Dalvik虚拟机，  
SDK中有个dx工具负责将JAVA字节码转换为Dalvik字节码，  dx工具对JAVA类文件重新排列，将所有JAVA类文件中的常量池分解，消除其中的冗余信息，  
重新组合形成一个常量池，所有的类文件共享同一个常量池，使得相同的字符串、常量在DEX文件中只出现一次，从而减小了文件的体积。  
