## 171. Excel表列序号

### 题目

给定一个Excel表格中的列名称，返回其相应的列序号。

例如，

```
    A -> 1
    B -> 2
    C -> 3
    ...
    Z -> 26
    AA -> 27
    AB -> 28 
    ...
```

**示例 1:**

```
输入: "A"
输出: 1
```

**示例 2:**

```
输入: "AB"
输出: 28
```

**示例 3:**

```
输入: "ZY"
输出: 701
```

### 题解

```cpp
int titleToNumber(string columnTitle) {
  int sz=columnTitle.size();
  long long res=0;
  for(int i=0; i<sz; ++i){
    res=res*26+columnTitle[i]-'A'+1;
  }
  return res;
}
```