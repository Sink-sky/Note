# C++ STL算法

## heap 堆

**最大堆,最小堆**

基于想有一种数据结构,能方便的进行插入,同时又能方便的访问到最值的情况.

```
//都是一个迭代器范围再加上一个可选的比较仿函数
make_heap();
push_heap();
//只能pop极值
pop_heap();
//利用堆,进行堆排序.使堆变为一个有序序列.
sort_heap();
```

## 不修改序列的操作

```c++
all_of();any_of();none_of();
for_each();
count();count_if();
mismatch();
find();find_if();find_if_not();find_end();
search();search_n();
```



## 修改序列的操作

```C++
fill();
remove();remove_if();
replace();replace_if();
swap();swap_ranges();
reverse();
unique();
```



## 划分操作

```C++
partition();
```



## 二分操作

```C++
lower_bound();
upper_bound();
binary_search();
equal_range();
```



## 集合操作

```C++
merge();
includes();
set_difference();
set_intersection();
set_symmetric_dofference();
set_union();
```



## 最大最小操作

```c++
max();min();
max_element();min_element();
```



## 排列操作

```C++
is_permutation();
next_permutation();
prev_permutation();
```
