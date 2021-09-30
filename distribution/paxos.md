

non-Byzantine  无拜占将军的错      

    一般地，把出现故障( crash 或 fail-stop，即不响应)但不会伪造信息的情况称为“非拜占庭错误”( non-byzantine fault)或“故障错误”( Crash Fault);      
    伪造信息恶意响应的情况称为“拜占庭错误”( Byzantine Fault)，对应节点为拜占庭节点。      
    处理非拜占庭错误的算法有：paxos、raft和其变种；        
    处理拜占庭错误算法有：pbft、pow算法；      
2.1 系统假定
一般常见的分布式系统运行模型的假定：

 A0.1 Processors operate at arbitrary speed

 A0.2 Processors may experience failures

 A0.3 Processors with stable storage may re-join the protocol after failures

 A0.4 Processors do not collude, lie, or otherwise attempt to subvert the protocol. That is, Byzantine failures don't occur

 A0.5 Processors can send messages to any other processor

 A0.6 Messages are sent asynchronously and may take arbitrarily long to deliver

 A0.7 Messages may be lost, reordered, or duplicated

 A0.8 Messages are delivered without corruption. That is, Byzantine failures don't occur

  -- https://en.wikipedia.org/wiki/Paxos_(computer_science)#Assumptions

我们将上面陈述中的假定A0.7替换为A0.9即得到本文中所默认的系统假定

 A0.9 Messages may be lost, reordered, but will never be duplicated

