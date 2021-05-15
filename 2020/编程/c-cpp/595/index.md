# 连续和

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    对一个给定的自然数M，求出所有的连续的自然数段（连续个数大于1），这些连续的自然数段中的全部数之和为M。<br /> 例子：1998+1999+2000+2001+2002 = 10000，所以从1998到2002的一个自然数段为M=10000的一个解。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    包含一个整数的单独一行给出M的值（10 <= M <= 2,000,000）
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    每行两个自然数，给出一个满足条件的连续自然数段中的第一个数和最后一个数，两数之间用一个空格隔开，所有输出行的第一个按从小到大的升序排列，对于给定的输入数据，保证至少有一个解。
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    int m, k1, k2;
    cin &gt;&gt; m;
    for (k1 = sqrt(m * 2); k1 &gt; 1; k1--)
        if (2 * m % k1 == 0 && (k1 + 2 * m / k1) % 2 == 1) {
            k2 = 2 * m / k1;
            cout &lt;&lt; (k2 - k1 + 1) / 2 &lt;&lt; " " &lt;&lt; (k2 + k1 + 1) / 2 - 1 &lt;&lt; endl;
        }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
