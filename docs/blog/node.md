
* node适用于I/O密集型，不适合于CPU密集型
* 帮助实践轮询的libuv库V8不是一个线程

* 并不是所有都用一部任务好，遵循一个公式： s=  (Ws+Wp)/(Ws+Wp/p)     ws表示同步任务，Wp表示异步任务，p表示处理器的数量

* libuv在linux下是   custom  threadpool
* libuv在windows下是  iocp

* node代码单线程，可以通过引入cluster模块，实现主从进程

* node垃圾回收机制：分代式回收机制（新生代，老生代）

* 新生代采用 scavenge算法 ： from to 交换
* 老生代采用 标记清除（mark-swap），移动清除（mark-compact）

* node测试工具 node-inspector
    