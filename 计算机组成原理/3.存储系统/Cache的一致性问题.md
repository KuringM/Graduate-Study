# Cache的一致性问题(Cache写策略)

## 写命中(Write Hit)

### 1. 写回法(write-back)

当CPU对Cache写命中时, 只修改Cache的内容, 而不立即写入主存, 只有当此块被换出时才写回主存.

> 减少了访存次数, 但存在数据不一致的隐患.

### 2. 全写法(写直通法, write-through)

当CPU对Cache写命中时, 必须把数据同时写入Cache和主存, 一般使用**写缓冲**(write buffer, SRAM实现的FIFO队列).

> 访存次数增加, 速度变慢, 但更能保证数据一致性.

使用写缓冲, CPU写的速度很快, 若写操作不频繁, 则效果很好.
若写操作很频繁, 可能会因为写缓冲饱和而发生阻塞.

## 写不命中

### 1. 写分配法(write-allocate)

当CPU对Cache写不命中时, 把主存中的块调入Cache, 在Cache中修改. 通常搭配写回法使用.

- 先将数据从内存中调入到cache中
- 再按回写法修改cach

### 2. 非写分配法(not-write-allocate)

当CPU对Cache写不命中时只写入主存, 不调入Cache. 搭配全写法使用.

- 直接去内存修改

> 只有"读"未命中时才调入Cache

## 多级Cache

![[Pasted image 20250819201108.png]]

现代计算机常采用多级Cache

- 离CPU越近的速度越快, 容量越小;
- 离CPU越远的速度越慢, 容量越大
