# ASCII码给字母排序

## 题目描述 {.page-header.text-muted}

<div class="content">
  输入三个字符（可以重复）后，按各字符的ASCII码从小到大的顺序输出这三个字符。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行输入一个数N,表示有N组测试数据。后面的N行输入多组数据，每组输入数据都是占一行，有三个字符组成，之间无空格。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对于每组输入数据，输出一行，字符中间用一个空格分开。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n;
    cin &gt;&gt; n;
    const char* a[3],*b;
    string t, x, y, z;
    while (n--) {
        cin &gt;&gt; t;
        x = t[0]; y = t[1]; z = t[2];
        a[0] = x.c_str(); a[1] = y.c_str(); a[2] = z.c_str();
        if (strcmp(a[0], a[1]) &gt; 0) {
            b = a[0];
            a[0] = a[1];
            a[1] = b;
        }
        if (strcmp(a[0], a[2]) &gt; 0) {
            b = a[0];
            a[0] = a[2];
            a[2] = b;
        }
        if (strcmp(a[1], a[2]) &gt; 0) {
            b = a[1];
            a[1] = a[2];
            a[2] = b;
        }
        cout &lt;&lt; a[0] &lt;&lt; " " &lt;&lt; a[1] &lt;&lt; " " &lt;&lt; a[2] &lt;&lt; endl;
    }
    return 0;
}</pre>

&nbsp;
