### 同步和异步的区别

同步是阻塞模式，异步是非阻塞模式。

同步 指同一个进程在执行某个请求的时候，若该请求需要一段时间才能返回信息，那么这个进程将会一直等待，知道收到返回信息才能继续执行下去；

异步 指进程不需要一直等下去，而是据需执行下面的操作，不管其他进程的状态，当有消息返回时，系统会通知进程进行处理，这样可以提高执行的效率。

---

### 请简述 __link__ 和 __@important__ 的区别.

+ link 是XHTML标签，除了加载CSS外，还可以定义RSS（真正简易联合，被设计用来展示选定的数据）等其他事务；@important 属于CSS范畴，只能加载CSS
+ link 引用CSS时，在页面加载时同时加载；@important 需要页面网页完全载入以后加载
+ link 是XHTML标签，无兼容问题；@important 是在CSS 2.1 提出的，低版本的浏览器不支持
+ link 支持使用JavaScript控制DOM去改变样式；@important 不支持
