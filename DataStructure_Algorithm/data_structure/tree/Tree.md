### 二叉树

每个节点，最多 有2个节点的树，叫二叉树；  
#### 二叉查找树、二叉搜索树、二叉排序树（BST）

二叉查找树，每个节点的数值，都大于其左节点的数值，小于其右节点的数值；

#### [平衡二叉树（AVL树）](Tree_AVL.md)

AVL树是根据它的发明者G. M. Adelson-Velskii和E. M. Landis命名的。它是一种特殊的二叉搜索树。  
AVL树要求: 任一节点的左子树深度和右子树深度相差不超过1；  
AVL树的特性让二叉搜索树的节点实现平衡(balance)：节点相对均匀分布，而不是偏向某一侧。  
因此，AVL树的搜索算法复杂度是log(n)的量级。  

[哈夫曼树、最优二叉树](HuffmanTree.md)    

给定n个权值作为n个叶子结点，构造一棵二叉树，若带权路径长度达到最小，称这样的二叉树为最优二叉树，也称为哈夫曼树(Huffman Tree)。  
哈夫曼树是带权路径长度最短的树，权值较大的结点离根较近。    


#### [红黑树](RedBlackTree/RedBlackTree.md) 
 
B+树    

B-树    

Trie树    


前缀树或字典树，读音 /ˈtraɪ/ ；原意 retrieval

#### 参考 
http://www.cnblogs.com/vamei/archive/2013/03/21/2964092.html  
http://www.cnblogs.com/skywang12345/p/3577479.html  
http://www.cnblogs.com/QG-whz/p/5167238.html  