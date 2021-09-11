## CFS
- [1]参考[进程管理笔记三、完全公平调度算法CFS](https://blog.csdn.net/XD_hebuters/article/details/79623130)
- [Linux CFS调度器](https://zhuanlan.zhihu.com/p/56430999)
- CFS:completely fair scheduler，完全公平调度器
- 公式如下：
$$
vruntime = 权重占比*\sum调度时间片长度=\frac{cpu.share_{default}}{cpu.share}*\sum runtime
$$
- 其中 $\textit{cpu.share}$ 就是 线程的权重，$cpu.share_{default} $ 就是nice 0的权重值，一般就是1024
- 一般是调度vruntime比较小的
- cfs 具体是用红黑树来进行调度
- 参考[1]可以推出一个调度周期内，vruntime的大小和进程的权重没有关系；或者说在一个周期内，vruntime的增长是一致的，那么vruntime的大小只取决于这个进程是不是之前就已经运行了多个周期了。所以，历史时间较短的进程有更多的可能被调用。
- 红黑树的实现源码：
  - 1[Linux内核——红黑树的C++实现(内含源码)](https://zhuanlan.zhihu.com/p/343673040)
  - 2[【红黑树】的详细实现(C++)附代码](https://zhuanlan.zhihu.com/p/348814281)