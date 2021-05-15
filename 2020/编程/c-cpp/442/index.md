# 简单编码

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    最近Kingly对编码很感兴趣，于是从网上找了一些编码原则来对字符串做实验。因为Kingly一直很忙，所以希望你这位编程高手来替他解决这个问题。下面是编码原则：（1） 如果访问到字符A，W，F就转化成I；（2） 如果访问到字符C，M，S就分别转化成L，o，v；（3） 如果访问到字符D，P，G，B就转化成e；（4） 如果访问到字符L，X就分别转化成Y，u；（5） 其他字符均保持不变；（6） 遇到END就结束！
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(void) {
    string a;
    int b, i;
    while (getline(cin, a)) {
        b = a.length();
        for (i = 0; i &lt; b; i++) {
            if (a[i] == 'E' && a[i + 1] == 'N' && a[i + 2] == 'D')return 0;
            else if (a[i] == 'A' || a[i] == 'W' || a[i] == 'F')cout &lt;&lt; "I";
            else if (a[i] == 'C')cout &lt;&lt; "L";
            else if (a[i] == 'M')cout &lt;&lt; "o";
            else if (a[i] == 'S')cout &lt;&lt; "v";
            else if (a[i] == 'D' || a[i] == 'P' || a[i] == 'G' || a[i] == 'B')cout &lt;&lt; "e";
            else if (a[i] == 'L')cout &lt;&lt; "Y";
            else if (a[i] == 'X')cout &lt;&lt; "u";
            else cout &lt;&lt; a[i];
        }cout &lt;&lt; endl;
    }
    return 0;
}</pre>

&nbsp;
