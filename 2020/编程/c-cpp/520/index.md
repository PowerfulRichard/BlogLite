# 尼科彻斯定理

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    验证尼科彻斯定理，即：任何一个正整数的立方都可以写成一串连续奇数的和。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    任一正整数
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    该数的立方分解为一串连续奇数的和
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int x;
    scanf("%d", &x);
    long long y = x * x * x;
    printf("%d*%d*%d=%lld=", x, x, x, y);
    y = x * x - x + 1;
    for (int i = 0; i &lt; x-1; i++) {
        cout &lt;&lt; y &lt;&lt; "+";
        y += 2;
    }
    cout &lt;&lt; y;
    return 0;
}</pre>

&nbsp;
