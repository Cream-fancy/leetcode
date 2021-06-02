## 412. Fizz Buzz

### 题目

写一个程序，输出从 1 到 *n* 数字的字符串表示。

1. 如果 *n* 是3的倍数，输出 "Fizz"；
2. 如果 *n* 是5的倍数，输出 "Buzz"；
3. 如果 *n* 同时是3和5的倍数，输出 "FizzBuzz"。

**示例：**

```
n = 15,

返回:
[
    "1",
    "2",
    "Fizz",
    "4",
    "Buzz",
    "Fizz",
    "7",
    "8",
    "Fizz",
    "Buzz",
    "11",
    "Fizz",
    "13",
    "14",
    "FizzBuzz"
]
```

### 题解

```cpp
vector<string> fizzBuzz(int n) {
  vector<string> v;
  int f3, f5;
  for(int i=1; i<=n; ++i){
    f3=!(i%3), f5=!(i%5);
    if(f3 && f5) v.push_back("FizzBuzz");
    else if(f3) v.push_back("Fizz");
    else if(f5) v.push_back("Buzz");
    else v.push_back(to_string(i));
  }
  return v;
}
```