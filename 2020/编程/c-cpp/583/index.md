# 快速计算斐波那契数列（Fibonacci数列）

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    输入一个正整数n，求Fibonacci数列的第n个数。Fibonacci数列的特点：第1,2个数为1,1。从第3个数开始，概述是前面两个数之和。即：
  </p>
  
  <p>
    <img src="https://i2.wp.com/acm.webturing.com/JudgeOnline/upload/pimg2278_1.jpg?w=688&#038;ssl=1" alt="" data-recalc-dims="1" />要求输入的正整数n不超过50.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  一个不超过50的正整数
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  Fibonacci数列的第n个数，末尾输出换行。
</div>

<div>
</div>

<div>
  <em>递归法（使用数组记录已经算过的斐波那契数）</em>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
uint64_t Fibonacci(unsigned char n)
{
    static uint64_t fib[256] = { 0, 1 };
    if (n == 0) return 0;
    if (fib[n] != 0) return fib[n];
    fib[n] = Fibonacci(n - 1) + Fibonacci(n - 2);
    return fib[n];
}
int main() {
    int n;
    cin &gt;&gt; n;
    cout &lt;&lt; Fibonacci(n);
}</pre>

_递推法_

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    long long sum = 1, pre_sum = 0, cre_sum;
    int i;
    scanf("%d", &i);
    while (--i){
        cre_sum = sum;
        sum += pre_sum;
        pre_sum = cre_sum;
    }
    printf("%lld\n", sum);
    return 0;
}</pre>

&nbsp;
