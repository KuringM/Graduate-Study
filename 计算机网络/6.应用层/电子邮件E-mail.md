# 电子邮件E-mail

## E-mail的信息格式

![[Pasted image 20250830183326.png]]

## E-mail的组成结构

![[Pasted image 20250830183701.png]]

### 发送、接受过程

![[Pasted image 20250830183745.png]]

## 简单邮件传送协议SMTP( Simple Mail Transfer Protocol )

- SMTP规定了在两个相互通信的SMTP进程之间应如何交换信息.
- 负责发送邮件的SMTP进程就是SMTP客户, 负责接收邮件的进程就是SMTP服务器.
- SMTP规定了14条命令(几个字母)和21种应答信息(三位数字代码+简单文字说明).

SMTP通信的三个阶段: 建立连接->邮件传送->连接释放

> 采用TCP连接, 端口号25, 使用C/S模型

![[Pasted image 20250830185104.png]]

### 通用因特网邮件扩充MIME(Multipurpose Internet Mail Extensions)

SMTP的缺点:

1. SMTP不能传送可执行文件或者其他二进制对象.
2. SMTP仅限于传送7位ASCII码, 不能传送其他非英语国家的文字.
3. SMTP服务器会拒绝超过一定长度的邮件.

![[Pasted image 20250830185234.png]]

- 使电子邮件系统可以支持声音、图像、视频、多种国家语言等等.
- 使得传输内容丰富多彩

## 邮局协议POP3(Post Office Protocol)

> 采用TCP连接, 端口号110, 使用C/S模型

![[Pasted image 20250830185454.png]]

## 因特网报文存取协议IMAP(Internet Mail Access Protocal)

![[Pasted image 20250830185728.png]]

## 基于万维网的电子邮件

![[Pasted image 20250830185816.png]]

