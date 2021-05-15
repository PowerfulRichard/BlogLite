# Computation – Min, Max and Sum

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Min, Max and Sum
  </p>
  
  <p>
    Write a program which reads a sequence of n integers ai(i=1,2,&#8230;n), and prints the minimum value, maximum value and sum of the sequence.
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  In the first line, an integer n is given. In the next line, n integers ai are given in a line.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  Print the minimum value, maximum value and sum in a line. Put a single space between the values.
</div>

> <div>
>   注：还应该比较max或min与新赋值i的大小
> </div>

<div>
  <pre class="EnlighterJSRAW" data-enlighter-language="c">#define _CRT_SECURE_NO_WARNINGS
#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a, n, i, max, min, sum, t;
    scanf("%d %d", &n, &a);
    sum = a;
    max = a; min = a;
    while (n &gt; 1) {
        scanf("%d", &i);
        sum = sum + i;
        if (a &lt;= i) {
            if (max &lt; i) {
                max = i;
            }
            if (min &gt; a) {
                min = a;
            }
        }
        else {
            if (max &lt; a) {
                max = a;
            }
            if (min &gt; i) {
                min = i;
            }
        }
        n = n - 1;
    }
    cout &lt;&lt; min &lt;&lt; " " &lt;&lt; max &lt;&lt; " " &lt;&lt; sum &lt;&lt; endl;
    return 0;
}</pre>
</div>

<div>
  <p>
    &nbsp;
  </p>
</div>

<div>
  <p>
    &nbsp;
  </p>
</div>

<div id="gtx-trans" style="position: absolute; left: 13px; top: 335.969px;">
  <div class="gtx-trans-icon">
  </div>
</div>
