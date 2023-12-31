# Assignment 2

实现一个基于char数组的string类，不允许使用c和c++的string库

接口命名可参考[std::string](https://en.cppreference.com/w/cpp/string)

## Basic

### Constructor/Destructor

- [ ] 默认构造函数
- [ ] 构造空字符串并预留指定大小空间
- [ ] 根据字面量构造
- [ ] 复制构造
- [ ] 移动构造

### Operator overload

- [ ] 复制赋值运算符
- [ ] 移动赋值运算符
- [ ] operator+
- [ ] operator[]

### Member function

> 具体功能看cpp reference

- [ ] size()
- [ ] resize()
- [ ] capacity()
- [ ] insert(pos,str)

### Friend function

- [ ] operator<<(std::ostream, String)
- [ ] operator>>(std::istream, String)

## Optional

> 选做,感兴趣用空可以做,可能佷耗时

- [ ] RAII: 实现类似shared_ptr的引用计数进行非拷贝的字符串复制(不要用shared_ptr来实现)
- [ ] Random access iterator [link](https://en.cppreference.com/w/cpp/named_req/RandomAccessIterator): 实现`begin(),end(),rbegin(),rend()` 成员函数，支持`std::sort`等算法 (~~相当于vector<char>了~~)

## Hits

- 使用std::memcpy进行拷贝
- 不考虑处理用户的脑瘫行为(如对返回的data进行delete等等)
- 对nullptr执行delete不会报错(无任何效果)
