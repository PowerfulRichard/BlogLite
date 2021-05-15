# First Blood

## 题目描述 {.page-header.text-muted}

<div class="content">
  盖伦是个小学一年级的学生，在一次数学课的时候，老师给他们出了一个难题：<br /> 老师给了一个正整数 n，需要在不大于n的范围内选择三个正整数(可以是相同的)，使它们三个的最小公倍数尽可能的大。盖伦很想第一个解决这个问题，你能帮助盖伦拿到“first blood”吗？
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  首先是一个正整数T，表示有T组测试数据<br /> 每组测试数据是一个正整数n(1<=n<=10^6)
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对于每组测试数据，输出最大的最小公倍数，每个输出单独占一行</p> 
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a;
    cin &gt;&gt; a;
    long long n;
    while (a--) {
        cin &gt;&gt; n;
        if (n &gt;= 1 && n &lt;= 2) { cout &lt;&lt; n &lt;&lt; endl; continue; }
        cout &lt;&lt; (n % 2 ? n * (n - 1) * (n - 2) : n % 3 ? n * (n - 1) * (n - 3) : (n - 1) * (n - 2) * (n - 3)) &lt;&lt; endl;
    }
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
