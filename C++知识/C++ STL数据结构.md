# C++ STL数据结构 #

**参考文章:**

- [C++顺序性容器、关联性容器与容器适配器](https://www.cnblogs.com/dyllove98/p/3214898.html)

-----

## 概述

**顺序性容器**
*vector,deque,list*
物理与逻辑上线性排放,线性结构.

**关联式容器**
*set,map,multiset,multimap*
kv,树状结构.

**容器适配器**
*stack,queue,priority_queue*
包装了容器,发生了接口转换,是容器的容器.



## 顺序性容器

**vector 向量** 连续内存块

**deque 双向队列** 多个连续内存块

**list 双向链表** 分开的元素内存块

共有的一些函数

```c++
//相似的构造方法
list<int> (3,5);//三个节点为5
//相似的重分配方法
assign();
//相似的迭代方法
begin();end();rbegin();rend();
//相似的取值方法
front();end();
//相似的前后增删方法(vector只有后增删)
push_back();pop_back();
push_front();pop_front();
//相似的插入方法
insert();
//相似的查空清空方法
empty();clear();erase();
//相似的大小查询方法
size();resize();
//vector,deque支持随机访问
```

## 关联式容器



## 容器适配器

**默认情况下,stack,queue采用deque实现,而priority_queue采用vector实现**

## list 双向链表 ##
```c++
//构造函数
list<int>(5);//五节点0
list<int>(3,2);//三节点2
//assign() 分配值
assign(3,2);//分配三节点2
//迭代器
begin();end();rbegin();rend();
//取值
front();back();
//前后增删
push_front();pop_front();push_back();pop_back();
//删除
erase();remove();
remove_if();
//大小 
size();
//判空 
empty();
//清空
clear();
//插入元素
insert();
//删除相邻重复元素 
qnique();
//反转链表
reverse();
//合并两个有序链表 
merge(L2);
//链表结合 
splice();
L1.splice(L1,L2);//位置+结合后清空链表
//排序 sort()
```