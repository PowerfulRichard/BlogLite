# 不要11

## 题目描述 {.page-header.text-muted}

<div class="content">
  长度为n但是不含11的字符串(只含01构成)有多少？（允许有前导0)
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  一个正整数长度n(1<=n<=1000)
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  所有不含有11的字符串的总数由于数值很大，请输出对与1000000007取模的结果
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n;
    cin &gt;&gt; n;
    long long a[1001][2];
    memset(a, 0, sizeof(a));
    a[1][0] = 1;
    a[1][1] = 1;
    for (int i = 2; i &lt;= n; i++) {
        a[i][0] = (a[i - 1][0] + a[i - 1][1]) % 1000000007;
        a[i][1] = a[i - 1][0] % 1000000007;
    }
    cout &lt;&lt; (a[n][0] + a[n][1]) % 1000000007 &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
