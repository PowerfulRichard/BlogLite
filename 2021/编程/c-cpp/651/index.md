# 公约数和公倍数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    小明被一个问题给难住了，现在需要你帮帮忙。问题是：给出两个整数，求出它们的最大公约数和最小公倍数。
  </p>
  
  <p>
    特别的我们规定
  </p>
  
  <p>
    如果x!=0  gcd(x,0)=gcd(0,x)=x,lcm(x,0)=lcm(0,x)=0
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行输入一个大于0的整数n(n<=20)，示有n组测试数据随后的n行输入两个不同时为0的非负整数i,j(i,j小于32767)。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出每组测试数据的最大公约数和最小公倍数
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a, b, d;
    cin &gt;&gt; d;
    while (d--) {
        cin &gt;&gt; a &gt;&gt; b;
        int c = __gcd(a, b);
        cout &lt;&lt; c &lt;&lt; " " &lt;&lt; a * b / c &lt;&lt; endl;
    }
}</pre>

&nbsp;
