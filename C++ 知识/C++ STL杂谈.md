# C++ string #
可随机访问的容器一般都不需迭代器访问
```c++
//子串
substr();
//插入
insert();
//删除
erase();
//替换
//添加一个范围替换子串
replace();
//尾部添加
append();
//赋值
assign();
//查找 找不到返回string::npos
find();rfind();
//查找第一个在args的字符位置
find_first_of(args);
//查找最后一个在args的字符位置
find_last_of(args);
//查找第一个不在args的字符位置
find_first_not_of(args);
//查找最后一个不在args的字符位置
find_last_not_of(args);
//比较 相等返回0
compare();
//类型转换 sto...()
//to_string MinGw下报错
```

## C++ pair

```c++
make_pair();
```



## C++ tuple

类模板 `std::tuple` 是固定大小的异类值汇集。它是`std::pair`的推广。

```C++
make_tuple();
```

