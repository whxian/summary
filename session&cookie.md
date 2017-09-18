# session & cookie #
___

在网站开发中，对于存储和记忆有cookie和session两种方式，对于前端开发工程师来说，使用session的情况并不多，大多数前端前端开发工程师可能更了解cookie，然而，熟悉后端的前端程序员也了解session，session是服务器端的存储信息机制。

### 区别： ###

1. cookie是将数据存放在客户端内存或者硬盘中，而session是将数据存放在服务器的硬盘中。

2. cookie有数量和大小的限制，但个cookie一般不超过4k，超过这个大小则会无法存储；cookie在存储的数量上也有限制，大部分浏览器都限制一个站点最多保存20个cookie。session却没有限制。

3. 从性能方面来考虑，我们应该选择cookie，因为session会在一段时间内保存在服务器上，当访问量较大时，会损耗服务器的性能。

4. 当对cookie设置了时间限制，那么，客户端会根据cookie里面设置的时间是否删除此记录。对于session而言，关闭浏览器就意味着此次访问的结束，session保存的记录也随之消失。

### 安全性： ###

1. 二者的安全性有区别，如果安全性相同，则二者就失去了同时存在的必要性了。

2. session的sessionID是放在cookie里，要想功破session的话，第一要功破cookie。功破cookie后，你要得到 sessionID,sessionID是要有人登录，或者启动session_start才会有，你不知道什么时候会有人登录

3. 第二，sessionID是加密的，第二次session_start的时候，前一次的sessionID就失效了，session过期时sessionid也会失效，想在短时间内功破加了密的 sessionID很难。session是针对某一次通信而言，会话结束session也就随着消失了，而真正的cookie存在于客户端硬盘上的一个文本文件，显然session是更安全的。

对于前端开发者而言，我们大多数使用的cookie，在前端开发中，我们只要游刃有余的使用cookie存储数据就可以了，不必考虑到session存储。
