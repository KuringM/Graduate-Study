# KMP算法的进一步优化

优化**next数组**, 使用**nextval数组**

|     序号     |  1  |  2  |   3   |  4  |   5   |  6  |
| :----------: | :-: | :-: | :---: | :-: | :---: | :-: |
|    模式串    |  a  |  b  |   a   |  a  |   b   |  c  |
|  `next[j]`   |  0  |  1  |   1   |  2  |   2   |  3  |
| `nextval[j]` |  0  |  1  | ==0== |  2  | ==1== |  3  |

```c
int Index_KMP(SString S, SString T,int nextval[]){
	int i=1, j=1;

	//继续比较后继字符
	while(i <= S.length && j <= T.length){
		if (j == 0 || S.ch[i] == T.ch[j]){
			++i;
			++j;
		else
			j=next[j]; //模式串向右移动
	}

	if(j>T.length)
		return i -  T.length;
	else
		return 0; //匹配成功
}
```

## 求 "nextval数组" (手算)

手算解题: 先求next数组,再由next数组求nextval数组.

```c
nextval[1]=0;
for (int j = 2; j <= T.length; j++)
	if (T.ch[next[j]] == T.ch[j])
		nextval[j] = nextval[next [j]];
	else
		nextval[j] = next [j];
{
```

例如: 模式串 T = "ababaa"

|     序号     |  1  |  2  |   3   |   4   |   5   |  6  |
| :----------: | :-: | :-: | :---: | :---: | :---: | :-: |
|    模式串    |  a  |  b  |   a   |   b   |   a   |  a  |
|  `next[j]`   |  0  |  1  |   1   |   2   |   3   |  4  |
| `nextval[j]` |  0  |  1  | ==0== | ==1== | ==0== |  4  |

例如: 模式串 T = "aaaab"

|     序号     |  1  |  2  |  3  |  4  |  5  |
| :----------: | :-: | :-: | :-: | :-: | :-: |
|    模式串    |  a  |  a  |  a  |  a  |  b  |
|  `next[j]`   |  0  |  1  |  2  |  3  |  4  |
| `nextval[j]` |  0  |  0  |  0  |  0  |  4  |
