# 求组合数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    组合数Cnr(n,r)=n!/r!/(n-r)!,虽然组合数的计算简单但也不乏有些陷阱，这主要是因为语言中的数据类型在表示范围上是有限的。更何况还有中间结果溢出的现象，所以千万要小心。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    输入数据不超过100多组测试用例，每一行有两个整数M与N，你可以假设结果不会超过64位有符号整数，每对整数M和N满足0=＜m, n≤28，以EOF结束。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输出该组合数。每个组合数换行。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#define _CRT_SECURE_NO_WARNINGS
#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    double m, n, nn;
    long double s = 1;
    while (scanf("%lf %lf", &m, &n) != EOF) {
        nn = n;
        while (nn--) {
            s = s * m;
            m--;
        }
        nn = 1;
        while (n &gt;= nn) {
            s = s / nn;
            nn++;
        }
        printf("%.0Lf\n", s);
        s = 1;
    }
    return 0;
}</pre>

&nbsp;
