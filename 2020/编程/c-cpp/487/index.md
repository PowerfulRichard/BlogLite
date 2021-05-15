# 复数求和

## 题目描述 {.page-header.text-muted}

<p class="page-header text-muted">
  从键盘读入n个复数（实部和虚部都为整数）用链表存储，遍历链表求出n个复数的和并输出。
</p>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct Complex {
    int real;
    int image;
};
void input(Complex& c) {
    cin &gt;&gt; c.real &gt;&gt; c.image;
}
int main() {
    int n, x=0, y=0;
    Complex a, b,c;
    cin &gt;&gt; n;
    while (n--) {
        input(a);
        x = x + a.real;
        y = y + a.image;
    }
    cout &lt;&lt; x &lt;&lt; "+" &lt;&lt; y&lt;&lt;"i";
    return 0;
}</pre>

&nbsp;
