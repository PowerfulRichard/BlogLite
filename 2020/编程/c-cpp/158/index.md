# 调和级数

## 题目描述 {.page-header.text-muted}

<div class="content">
  输入正整数n 输出H（n）=1+1/2+1/3+&#8230;.+1/n的值，保留3位有效数字
</div>

## 输入 {.content}

<div class="content">
  输入正整数n (n <10^6)
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出H（n）=1+1/2+1/3+&#8230;.+1/n的值，保留3位有效数字
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#define _CRT_SECURE_NO_WARNINGS
#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    int n, i = 1;
    long double h = 0,x,y;
    while (scanf("%d", &n) != EOF) {
        while (i &lt;= n) {
            long double ii = (int)i;    //将整形i转换为浮点型ii
            h = h +(1/ii);              //不同类型数据之间不能计算！
            i = i + 1;
        }
        printf("%.3Lf\n", h);
        h = 0; i = 1;
    }
    return 0;
}</pre>

&nbsp;
