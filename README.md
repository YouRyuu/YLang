# 高性能在线聊天服务器实现
## 此项目源于我在阅读Linux网络编程相关书籍时产生的想法:如何实现一个类似于qq的聊天软件?由此一步步开始了这个项目的开发.
参考书籍:UNP1, APUE, Linux多线程服务器编程  
## 项目中使用到的技术
* 非阻塞IO
* IO多路复用(epoll)
* Reactor模式(one loop per thread)