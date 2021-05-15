# 阶乘之和

## 题目描述 {.page-header.text-muted}

<div class="content">
  给你一个非负数整数n，判断n是不是一些数（这些数不允许重复使用，且为正数）的阶乘之和，如9=1！+2!+3!，如果是，则输出Yes，否则输出No；
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行有一个整数0<m<100,表示有m组测试数据；<br /> 每组测试数据有一个正整数n<1000000;
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  如果符合条件，输出Yes，否则输出No;
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    int a[10], i, m, t, s = 1;
    a[0] = 0;
    for (i = 1; i &lt;= 9; ++i) {
        s *= i;
        a[i] = s;
    }
    scanf("%d", &t);
    while (t--) {
        scanf("%d", &m);
        for (i = 9; i &gt;= 1; --i)
        {
            if (m &gt;= a[i])
                m -= a[i];
            if (!m)
                break;
        }
        if (!m)printf("Yes\n");
        else printf("No\n");
    }
    return 0;
}</pre>

&nbsp;
