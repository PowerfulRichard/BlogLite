# 最大公约数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    写一个函数，求两个整数的最大公约数。通过主函数调用这个函数，并输出结果。
  </p>
  
  <p>
    两个整数通过键盘输入。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  空格分隔的2个整数
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输入两数的最大公约数，单独占一行。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#define _CRT_SECURE_NO_WARNINGS
#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a, b, i=1, t=0;
    cin &gt;&gt; a &gt;&gt; b;
    while (i &lt;= a || i &lt;= b) {
        if (a % i == 0 && b % i == 0) {
            t = i;
        }
        i++;
    }
    cout &lt;&lt; t &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
