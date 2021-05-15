# 最优找零2

## 题目描述 {.page-header.text-muted}

<div class="content">
  假设货币有1,2,4,5,10五种硬币，每种数量都无限多，现在给出金额n(1<=n<=1000000)，求出最少的硬币数量
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  现在给出金额n(1<=n<=1000000）
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  最少的硬币数量
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n;
    cin &gt;&gt; n;
    int a[n + 1] = { 0 };
    int data[6] = { 0, 1, 2, 4, 5, 10 };
    for (int i = 1; i &lt;= n; i++)
        a[i] = i;
    for (int i = 1; i &lt;= n; i++)
        for (int j = 1; j &lt;= 5; j++)if (data[j] &lt;= i)a[i] = min(a[i], a[i - data[j]] + 1);
    cout &lt;&lt; a[n] &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
