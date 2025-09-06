# 二叉排序树(BST)

## 二叉排序树的定义

二叉排序树, 又称二叉查找树(**BST**, Binary Search Tree),

一棵二叉树或者是空二叉树, 或者是具有如下性质的二叉树:

- 左子树上所有结点的关键字均小于根结点的关键字;
- 右子树上所有结点的关键字均大于根结点的关键字;
- 左子树和右子树又各是一棵二叉排序树.

`左子树结点值 < 根结点值 < 右子树结点值`

- ==进行中序遍历, 可以得到一个递增的有序序列==
- 二叉排序树可用于元素的有序组织、搜索

## 二叉排序树的查找

- 若树非空, 目标值与根结点的值比较:
  - 若相等, 则查找成功;
  - 若小于根结点, 则在左子树上查找, 否则在右子树上查找.
- 查找成功, 返回结点指针;查找失败返回NULL

```c
// 二叉排序树结点
typedef struct BSTNode {
  int key;
  struct BSTNode *lchild, *rchild;
} BSTNode, *BSTree;

// 在二叉排序树中查找值为 key 的结点 (非递归实现) // 最坏空间复杂度O(1)
BSTNode *BST_Search(BSTreeT, int key) {
  while (T != NULL && key != T->key) { // 若树空或等于根结点值, 则结束循环
    if (key < T->key)                  // 小于, 则在左子树上查找
      T = T->lchild;
    else // 大于, 则在右子树上查找
      T = T->rchild;
  }
  return T;
}

// 在二叉排序树中查找值为 key 的结点(递归实现) //最坏空间复杂度O(h)
BSTNode *BSTSearch(BSTree T, int key) {
  if (T == NULL)
    return NULL; // 查找失败
  if (key == T->key)
    return T; // 查找成功
  else if (key < T->key)
    return BSTSearch(T->lchild, key); // 在左子树中找
  else
    return BSTSearch(T->rchild, key); // 在右子树中找
}
```

### 查找效率分析

- 查找长度 -- 在查找运算中, 需要对比关键字的次数称为查找长度, 反映了查找操作时间复杂度.
- 平均查找长度= $O(\log_2 n)$
- 若树高h, 找到最下层的一个结点需要对比 h 次
- 最好情况: n个结点的二叉树最小高度为 $\lfloor  \log_2 n\rfloor+1$. -- $ASL=O(\log_2 n)$
- 最坏情况: 每个结点只有一个分支, 树高h=结点数n. -- $ASL=O(n)$

![[Pasted image 20250904064327.png]]

> 平衡二叉树. 树上任一结点的左子树和右子树的深度之差不超过1. <BR>
> n个结点的二叉树最小高度为 $\lfloor \log_2 n \rfloor+1$(完全二叉树)而平衡二叉树高度与完全二叉树同等数量级.

![[Pasted image 20250904065304.png]]

## 二叉排序树的插入

- 若原二叉排序树为空, 则直接插入结点; 否则,
  - 若关键字k小于根结点值, 则插入到左子树,
  - 若关键字k大于根结点值, 则插入到右子树

```c
// 在二叉排序树插入关键字为K的新结点(递归实现) //最坏空间复杂度O(h)
int BST_Insert(BSTree &T, int k) {
  if (T == NULL) { // 原树为空, 新插入的结点为根结点
    T = (BSTree)malloc(sizeof(BSTNode));
    T->key = k;
    T->child = T->rchild = NULL;
    return 1; // 返回1, 插入成功
  }

  else if (k == T->key) // 树中存在相同关键字的结点, 插入失败
    return 0;
  else if (k < T->key) // 插入到T的左子树
    return BST_Insert(T->| child, k);
  else // 插入到T的右子树
    return BST_Insert(T->rchild, k);
}

// 在二叉排序树插入关键字为K的新结点(非递归实现)
// TODO:Nomething<2025 / 09 / 04, Kuring>
```

### 二叉排序树的构造

```c
// 按照 str[] 中的关键字序列建立二叉排序树
void Creat_BST(BSTree &T, int str[l, int n){
  T = NULL; // 初始时T为空树
  int i = 0;
  while (i < n) { // 依次将每个关键字插入到二叉排序树中
    BST_Insert(T, str[i]);
    i++;
  }
}
```

- 不同的关键字序列可能得到同款二叉排序树, 也可能得到不同款二叉排序树

## 二叉排序树的删除

先搜索找到目标结点:

1. 若被删除结点z是叶结点, 则直接删除, 不会破坏二叉排序树的性质.
2. 若结点z只有一棵左子树或右子树, 则让z的子树成为z父结点的子树, 替代z的位置.
3. ==若结点z有左、右两棵子树, 则令z的直接后继(或直接前驱)替代z, 然后从二叉排序树中删去这个直接后继(或直接前驱), 这样就转换成了第一或第二种情况==.
   - 对z的右子树进行中序遍历, 可以得到一个递增的**有序序列**, 用z的直接后继(或直接前驱)替代z, 在删除前驱(后继)结点
     - **z的后继(后继线索)**: z的右子树中最左下结点(该节点一定没有左子树)
     - **z的前驱(前继线索)**: z的左子树中最右下结点(该节点一定没有右子树)
   - 能产生两种新树

```c
- TODO:Nomething<2025 / 09 / 04, Kuring> -
```
