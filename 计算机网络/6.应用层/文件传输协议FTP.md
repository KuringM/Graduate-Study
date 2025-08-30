# 文件传输协议FTP

- 文件传送协议FTP(File Transfer Protocol) -- 提供不同种类主机系统(硬、软件体系等都可以不同)之间的文件传输能力.
- 简单文件传送协议TFTP (Trivial File Transfer Protocol)

## FTP服务器和用户端

- FTP是基于客户/服务器(C/S)的协议.
- 用户通过一个客户机程序连接至在远程计算机上运行的服务器程序.
- 依照FTP协议提供服务, 进行文件传送的计算机就是 **FTP服务器**.
- 连接FTP服务器, 遵循FTP协议与服务器传送文件的电脑就是 **FTP客户端**.

## FTP工作原理

![[Pasted image 20250830183104.png]]

> FTP使用TCP实现可靠传输.

FTP传输模式

- 文本模式: ASCI模式, 以文本序列传输数据;
- 二进制模式: Binary模式, 以二进制序列传输数据.
