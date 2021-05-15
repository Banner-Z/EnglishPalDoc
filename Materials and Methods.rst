Materials and Methods
======================

**model-level dependency** 主要使用 *snakefood* 分析
（因为snakefood需要python2的环境，所以我选择在Ubuntu的服务器上进行，使用putty连接服务器），
通过snakefood得到的代码生成依赖图。

**class/function-level dependency** 则通过手动的分析
（我直接在 *GitHub* 的库中完成了这一任务，同时参考了GitHub统计的每个类和函数的定义/调用情况）。

为了理清依赖关系，我按照文件顺序，一一分析其内部所有类和函数的 *被调用情况* ，并记录其对应的依赖图，
所以，在这些图中，当前这个文件中的类/函数（除了没有被依赖的）总是处在依赖图的底层，我期待在这种图里得到一些启发。

同时，我将部分文件合在一起分析，比如pickle_idea1.py和pickle_idea2.py，WordFreq.py和wordfreqCMD.py。
因为这样比较合理。

此外，分析需要，我仔细 *阅读和比较了少部分的函数* 。
对于除此之外的函数，我大致理解了其作用，并且认为其完美地完成了他的任务。

最后，我生成了一张总的类/函数依赖图并作了进一步的观察和分析。