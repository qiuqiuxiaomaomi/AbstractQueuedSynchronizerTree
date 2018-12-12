# AbstractQueuedSynchronizerTree
AbstractQueuedSynchronizer技术研究


![](https://i.imgur.com/c00Hobh.png)

<pre>
AQS：
       AQS提供了一种实现阻塞和一些列依赖FIFO等待队列同步器的框架；

       AQS为一系列同步器依赖于一个单独的原子变量state的同步器提供了一个非常有用的基础。子类
    必须定义改变state是如何获取或释放的。

       AQS中对state的操作是原子的，且不能被继承。所有的同步机制的实现均依赖对变量的原子操作
    。AQS并不实现任何借口，他提供了一些可以被具体实现类直接调用的一些原子操作方法来重写相应
    的同步逻辑。AQS同时提供了互斥模式exclusive和共享模式shared两种不同的同步逻辑。

    state：(原子操作)
         getState();
         setState();
         compareAndSetState(); （unsafe类中的方法）

    acquire(int)；
    tryAcquire(int)；
    addWaiter(Node)；
    enq(node)；
    acquireQueued(Node, int)；
    release(int)；
</pre>