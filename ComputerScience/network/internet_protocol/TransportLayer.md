### Transport Layer  
运输层主要为两台主机上的应用程序提供端到端的通信。  
在 TCP - IP协议族中，有两个互不相同的传输协议： TCP（传输控制协议）和 UDP（用户数据报协议）。  
TCP为两台主机提供高可靠性的数据通信。  
它所做的工作包括把应用程序交给它的数据分成合适的小块交给下面的网络层，确认接收到的分组，设置发送最后确认分组的超时时钟等。  
由于运输层提供了高可靠性的端到端的通信，因此应用层可以忽略所有这些细节。
UDP则为应用层提供一种非常简单的服务。它只是把称作数据报的分组从一台主机发送到另一台主机，但并不保证该数据报能到达另一端。  
任何必需的可靠性必须由应用层来提供。  

TCP、UDP    

