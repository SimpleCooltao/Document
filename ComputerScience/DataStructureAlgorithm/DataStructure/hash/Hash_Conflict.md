###### 解决冲突

在Java中，数组的大小是固定的，而且不能扩展；  
如果需要对哈希表扩容，就需要新建一个较大的数组，然后把老数组的元素，全部放入新数组中；  
哈希表是要根据数组的大小，计算每个元素对应的哈希值，所以，老数组元素放入新数组时，需要逐个迭代  由新的哈希值确认新的数组下标【重新哈希化】；   

开放地址法的表达式  

![开放地址法的表达式](ImageFiles/hash_conflict_001.png)  


> 开放地址法 之 线性探测法

假设遇到了冲突，会向右找到下一个为空的单元格，只要哈希表足够大，就一定能找下一个单元格，可能花费的时间比较大；  
会导致相同hash值的元素挨在一起，其他hash值对应的槽被占用等问题；  

其中 i = 0,1,2...M-1  
di = 1, 2, 3 ... k


> 开放地址法 之 平方探测法

其中 i = 0, 1, 2 ... M-1  
di = 1^2, - 1^2, 2^2, - 2^2,  ... k^2, - k^2

> 开放地址法 之 伪随机再散列

di = 伪随机数
  
> 再哈希法、双哈希法
  
当 p = h(k)出现冲突时，以p为基础， p1 = h(p)  
当 p1 = h(p)出现冲突时，以p1为基础， p2 = h(p1)  
以此类推...   
虽然不容易发生聚集，但是 增加计算时间；  

> 建立公共溢出区

将哈希表分为基本表和溢出表两部分，凡是和基本表发生冲突的元素，一律填入溢出表



> 链地址法

在java8中HashMap在put元素时，遇到hash相同，但是equals是false时，也就是遇到哈希冲突的时候，采用链地址法；   
在[关于哈希表的基本知识](Hash_Node.md)中，我们知道哈希表存放的箱子呢，是有指针元素的，在遇到冲突的时候，  
会把新的元素放在下一指针的节点上，构成简单链表，如果单一哈希值下的冲突较多，  
[详见HashMap相关知识](../../../../Java/java_source/java_collection/HashMap/HashMap.md)
- 可以对哈希表扩容 ：    
同样的，老数组中的每个箱子会 重新经过哈希函数，算出新的索引值，放在数组的对应位置；  
- 也可以将哈希值对应的链表树化，变成红黑树；

- 与开放定址法相比，拉链法有如下几个优点：  
①拉链法处理冲突简单，且聚集现象；    
②由于拉链法中各链表上的结点空间是动态申请的，故它更适合于造表前无法确定表长的情况；  
③开放定址法为减少冲突，要求装载因子较小，故当装载因子较大时会浪费很多空间。  
而拉链法中可取α≥1，且结点较大时，拉链法中增加的指针域可忽略不计，因此节省空间；  
④在用拉链法构造的散列表中，删除结点的操作易于实现。只要简单地删去链表上相应的结点即可。  

- 拉链法的缺点  
指针需要额外的空间，故当结点规模较小时，开放定址法较为节省空间，而若将节省的指针空间用来扩大散列表的规模，  
可使装填因子变小，这又减少了开放定址法中的冲突，从而提高平均查找速度。  




