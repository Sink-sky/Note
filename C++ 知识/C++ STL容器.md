# C++ STL容器 #

**参考文章:**

- [C++顺序性容器、关联性容器与容器适配器](https://www.cnblogs.com/dyllove98/p/3214898.html)
- [C++参考手册](https://zh.cppreference.com/w/cpp)

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
//链表结合 
//std::list::splice
splice();
L1.splice(L1,L2);//位置+结合后清空链表
```

## 关联式容器

**均采用红黑树(高效的平衡二叉搜索树)实现**

**set,map 无重复元素**

**multiset,multimap 可重复元素**

**unordered_set,unordered_map 哈希表(无序哈希)**

共有的一些函数

```c++
//相似的迭代方法(哈希表无反向迭代器)
begin();end();rbegin();rend();
//相似的插入方法
insert();
//相似的查找方法
find();
//相似的查空清空方法
empty();clear();erase();
//相似的大小查询方法
size();
//相似的查找键出现次数方法
count();
//第三个模板参数可以自定义排序规则,需要传入一个仿函数.
//bool operator()(const YouType & a,const YouType & b)
//C++对struct做了很大的扩充,以至于struct与class最大区别就只有访问控制了.
//map重载了[],可以用map[key]=value赋值,multimap无.
//哈希表可以修改哈希函数
//C++ std::hash仿函数
//std::size_t h1 = std::hash<std::string>{}(s.first_name);
//std::size_t operator()(S const& s)
```



## 容器适配器

**默认情况下,stack,queue采用deque实现,而priority_queue采用vector实现**

```c++
//容器适配器无clear()方法,因为底层是采用其他容器来实现.
//要clear一个容器适配器的最好方法就是与一个empty容器适配器swap
//stack可以修改实现实现更好性能
stack<int,vector<int>>;
//相似的增减方法
push();pop();
//相似的元素访问方法
front();back();
//相似判空方法
empty();
//相似大小方法
size();
//可以自定义优先队列的优先函数
template<
    class T,
    class Container = std::vector<T>,
    class Compare = std::less<typename Container::value_type>
> class priority_queue;
```


