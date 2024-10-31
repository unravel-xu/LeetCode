# 3 列表
## 3-F 循环节
* 由选择排序引入
## 3-G 插入排序
## 3-H 归并排序
## 3-I 逆序对
	统计逆序对个数
## 3-J 游标
* data：记录数据链头
* free：记录空闲链头
# 4 栈和队列
## 4-B 递归相关
### 4-B3 消除递归
* 递归函数的空间复杂度：
	* 主要取决于最大递归深度
	* 而非递归实例总数
### 4-B4 尾递归
* 容易改写为迭代形式（例如 goto 模拟递归返回）
* 空间复杂度可能会有渐进改进
* 时间复杂度可能有常系数改进
## 4-C 进制转换
* 栈：迭代版
* 递归版
## 4-D 括号匹配
* 消除一对紧邻的左右括号，不影响全局的匹配判断
* 顺序扫描，遇到左括号进栈，遇到右括号出栈
## 4-E 栈混洗
* 栈混洗总数：$$SP(n) = \sum^{n}_{k=1}SP(k-1)\cdot SP(n-k)=\frac{(2n)!}{n!(n+1)!}$$
* 禁形："312"
* n 个元素的栈混洗=n 对括号的匹配
## 4-F 中缀表达式
## 4-G 逆波兰表达式
### 4-G1 求值

| 24  |
| --- |
| 8   |
| 2   |
2 8 24 - + = (8 - 24) + 2 **栈底减（除）栈顶**
### 4-G2 转换
* 手工转化
后缀转中缀
![](Images/Pasted%20image%2020241031095536.png)
中缀转后缀
    加括号，运算符代替右括号，清除左括号
![](Images/Pasted%20image%2020241031095747.png)
* 自动转化
	中缀表达式求值算法附带完成
## 4-H 队列
* 基于向量派生
* 基于列表派生
## 4-J 双栈当队
![|475](Images/1857360-20220714210806132-1672496540.gif)
栈 B 为空时，需先将栈 A 元素转入 B 中，再对栈 B 做 pop
![|475](Images/1857360-20220714210806248-927348673.gif)
## 4-K Steap + Queap
Steap = Stack + Heap = push + pop + getmax
![](Images/Pasted%20image%2020241031110246.png)
* getmax()：return P.top(); // O(1)
* pop()：P.pop(); return S.pop();  //O(1)
* push(): P.push(max(elem, P.top())); S.push(elem);

Queap = Queue + Heap = enqueue + dequeue + getMax
![](Images/Pasted%20image%2020241031112344.png)
* getmax()：return P.front();  // O(1)
* dequeue()：P.dequeue();  return Q.dequeue();  // O(1)
* enqueue()：![|400](Images/Pasted%20image%2020241031113153.png)
  最坏情况需要 O(n)
## 4-L 直方图内最大矩形
[[912 DSA复习笔记##04-L 直方图内最大矩形]]
# 5 二叉树