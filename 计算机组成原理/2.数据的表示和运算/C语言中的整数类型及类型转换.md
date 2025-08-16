# C语言中的整数类型及类型转换

## 1. C语言中的整数数据类型

以补码形成储存

- 短整型(short , short int), 16位
- 整型(int), 32位
- 长整型(long, long int), 32位机中32位, 64位机中64位
  - 若不指定signed/unsigned , 则默认为有符号整型
- 字符型(char), 8位(默认无符号整型解释)

## 2. 强制类型转换

```c
void main(){
	short x=-4321; //short型占用2个字节
	unsigned short y=(unsigned short)x;
	int a=165537, b=-34991; //int型占用4个字节
	short c=(short)a, d=(short)b; //short型占用2个字节
	short x=-4321;
	int m=x;
	unsigned short n=(unsigned short)x;
	unsigned int p=n;
}

```

C 语言中定点整数是用"补码"存储的.

强制类型转换:

1. 无符号数与有符号数:不改变数据内容, 改变解释方式.
2. 长整数变短整数:高位截断, 保留低位.

---

- a: 0x000286a1
- c: 0x86a1 真值-31071
- b: 0xffff7751
- d: 0x7751 真值30545
- x: 1110 1111 0001 1111 ;0xef1f
- m: 1111 1111 1111 1111 1110 1111 0001 1111 ;0xffffef1f 真值-4321
- n: 1110 1111 0001 1111 ;0xef1f 真值61215
- p: 0000 0000 0000 0000 1110 1111 0001 1111; 0x0000ef1f 真值61215
