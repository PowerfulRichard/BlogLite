# a/b+c/d

### 题目描述

给你2个分数，求他们的和，并要求和为最简形式。

### 输入

输入首先包含一个正整数T（T<=1000），表示有T组测试数据，然后是T行数据，每行包含四个正整数a,b,c,d（0<a,b,c,d<1000），表示两个分数a/b 和 c/d。

### 输出

对于每组测试数据，输出两个整数e和f，表示a/b + c/d的最简化结果是e/f，每组输出占一行。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int gcd(int a, int b) {
    if (b == 0)return a;
    else return gcd(b, a%b);
}
int main() {
    int n,a,b,c,d;
    cin &gt;&gt;n;
    while (n--) {
        cin &gt;&gt; a &gt;&gt; b &gt;&gt; c &gt;&gt; d;
        int x,y;
        x = a * d + b * c;
        y = b * d;
        int z = gcd(x,y);
        cout &lt;&lt; x/z &lt;&lt; " " &lt;&lt; y/z &lt;&lt; endl;
    }
    return 0;
}</pre>

&nbsp;
