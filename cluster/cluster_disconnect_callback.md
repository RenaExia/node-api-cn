<!-- YAML
added: v0.7.7
-->

* `callback` {Function} 当所有工作进程都断开连接并且所有句柄都关闭的时候调用。

在 `cluster.workers` 的每个工作进程中调用 `.disconnect()`。

当所有工作进程断开连接后，所有内部句柄将会关闭，这个时候如果没有等待事件的话，运行主进程优雅地关闭。

这个方法可以选择添加一个回调参数，当结束时会调用这个回调函数。

这个方法只能由主进程调用。
