

### Java线程的状态

#### 线程可以有如下 6 种状态：

- New (新创建）

> 当用 new 操作符创建一个新线程时， 如 newThread(r)，该线程还没有开始运行。这意味
着它的状态是 new。当一个线程处于新创建状态时， 程序还没有开始运行线程中的代码。在
线程运行之前还有一些基础工作要做

- Runnable (可运行）

> 一旦调用 start 方法，线程处于 runnable 状态。一个可运行的线桿可能正在运行也可能没
有运行， 这取决于操作系统给线程提供运行的时间。（Java 的规范说明没有将它作为一个单独
状态。一个正在运行中的线程仍然处于可运行状态。）

- Blocked (被阻塞）

> 当一个线程试图获取一个内部的对象锁（而不是 javiutiUoncurrent 库中的锁，) 而该锁被其他线程持有， 则该线程进人阻塞状态

- Waiting (等待）

> 当线程等待另一个线程通知调度器一个条件时， 它自己进入等待状态。 在调用 Object.wait 方法或 Thread.join 方法， 或者是等待 java,util.concurrent 库中的 Lock 或 Condition 时，就会出现这种情况。实际上，被阻塞状态与等待状态是有很大不同的。

- Timed waiting (计时等待）

> 有几个方法有一个超时参数。调用它们导致线程进人计时等待（timed waiting) 状
态。这一状态将一直保持到超时期满或者接收到适当的通知。带有超时参数的方法有
Thread.sleep 和 Object.wait、 Thread.join、 Lock,tryLock 以及 Condition.await 的计时版

- Terminated (被终止）

> 线程因如下两个原因之一而被终止：

> 1、因为 run 方法正常退出而自然死亡。

> 2、因为一个没有捕获的异常终止了 run 方法而意外死亡。


#### 线程状态之间的转换


![线程状态之间的转换](https://github.com/vimx86/interview/blob/master/images/base/%E7%BA%BF%E7%A8%8B%E7%8A%B6%E6%80%81%E4%B9%8B%E9%97%B4%E7%9A%84%E8%BD%AC%E6%8D%A2.png?raw=true)










