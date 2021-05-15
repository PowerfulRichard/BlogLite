# 平方取中法

### 题目描述 {.page-header.text-muted}

平方取中法(midsquare method)是产生[0，1]均匀分布随机数的方法之一，亦称冯·诺伊曼取中法，最早由冯·诺伊曼(John von Neumann，1903-1957)提出的一种产生均匀<a href="https://baike.baidu.com/item/%E4%BC%AA%E9%9A%8F%E6%9C%BA%E6%95%B0/104358" target="_blank" rel="noopener">伪随机数</a>的方法。这里我们将这个算法稍作修改，产生下一个伪随机的正整数n  
不妨设置为 n  
（1）如果 n不足256 则+256  
（2）n表示成32位二进制（高位补0,），  
（3）舍去n的高16位  
（4）计算 n*n表示成32位二进制（高位补0,），  
（5）舍去高8位，低8位，获得一个16位二进制  
这个就是下一个随机数m

### 输入 {.content}

一个整数 n

### 输出 {.content}

<div class="content">
  输出用这个算法产生的下一个整数
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n;
    cin &gt;&gt; n;
    if (n &lt; 256)n += 256;
    n &lt;&lt;= 16;
    n &gt;&gt;= 16;
    n *= n;
    n &lt;&lt;= 8;
    n &gt;&gt;= 16;
    cout &lt;&lt; n &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
