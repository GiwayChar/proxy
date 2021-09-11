## CFS
- 参考[进程管理笔记三、完全公平调度算法CFS](https://blog.csdn.net/XD_hebuters/article/details/79623130)
- [Linux CFS调度器](https://zhuanlan.zhihu.com/p/56430999)
- CFS:completely fair scheduler，完全公平调度器
- 公式如下：
$$
vruntime = 权重占比*\sum调度时间片长度=\frac{cpu.share_{default}}{cpu.share}*\sum runtime
$$
- 其中 $\textit{cpu.share}$ 就是 线程的权重，$cpu.share_{default} $ 就是nice 0的权重值，一般就是1024
- 一般是调度vruntime比较小的
- cfs 具体使用红黑树来进行调度