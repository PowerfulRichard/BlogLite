# 最左边一位数

## 题目描述 {.page-header.text-muted}

<div class="content">
  对于给定的正整数N，输出N^N的最左边一位数。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入包含多组测试数据。输入的第一行是一个整数T，代表测试组数。随后输入T组测试数据，每组测试数据包含一个正整数N ( 1< = N< = 1,000,000,000 ）.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对于每组测试数据，输出N^N次方的最左边一位数。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n, t;
    scanf("%d", &t);
    while (t--) {
        scanf("%d", &n);
        double x = n * log10((double)n);
        x -= (long long)x;
        x = (int)pow(10, x);
        printf("%.0lf\n", x);
    }
}</pre>

&nbsp;
