# 哥德巴赫猜想

## 题目描述 {.page-header.text-muted}

<div class="content">
  著名的哥德巴赫猜想可以陈述为：任何一个不小于6的偶数一定可以拆成两个质数的和。如6=3+3,8=5+3等，你的任务是将一个大于6的偶数n拆成两个最接近的质数p,q,满足p+q=n.
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入包含多组测试数据。每组数据包含1个偶数n（n在6到1000000之间包含边界）。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对于每组测试数据，输出两个质数p,q(p<=q)满足p+q=n。</p> 
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int P[1000000] = {
    0
};
void Prime_list() {
    P[0] = P[1] = 1;
    for (int i = 2; i &lt; 1000000; i++) {
        for (int j = i * 2; j &lt; 1000000; j += i) {
            P[j] = 1;
        }
    }
}
int main() {
    int n;
    int i, cache;
    Prime_list();
    while (cin &gt;&gt; n) {
        for (i = 2; i &lt;= n / 2; i++) {
            if (P[i] == 0 && P[n - i] == 0) {
                cache = i;
            }
        }
        cout &lt;&lt; cache &lt;&lt; " " &lt;&lt; n - cache &lt;&lt; endl;
    }
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
