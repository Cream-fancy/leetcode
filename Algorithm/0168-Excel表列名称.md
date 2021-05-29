## 168. Excel表列名称

### 题目

给定一个正整数，返回它在 Excel 表中相对应的列名称。

例如，

```
    1 -> A
    2 -> B
    3 -> C
    ...
    26 -> Z
    27 -> AA
    28 -> AB 
    ...
```

**示例 1:**

```
输入: 1
输出: "A"
```

**示例 2:**

```
输入: 28
输出: "AB"
```

**示例 3:**

```
输入: 701
输出: "ZY"
```

### 题解

类似进制的思想，将 `1~26` 映射为 `0~25`，使得进制的计算更加方便。

```cpp
string convertToTitle(int columnNumber) {
  int cur=columnNumber-1;
  string s;
  while(cur/26){
    s.push_back('A'+cur%26);
    cur=cur/26-1;
  }
  s.push_back('A'+cur);
  reverse(s.begin(), s.end());
  return s;
}
```