# 字母小写转大写

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    读入一些字符串，将其中的小写字母转成大写字母（其他字符不变）。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    输入为多行，每行为一个字符串，字符串只由字母和数字组成，长度不超过80。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    对于每行输入，输出转换后的字符串。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    string a;
    int b, i;
    while (cin &gt;&gt; a) {
        b = a.length();
        for (i = 0; i &lt; b; i++) {
            if (a[i] &gt;= 'a' && a[i] &lt;= 'z') {
                a[i] = a[i] - 32;
            }
        }
        cout &lt;&lt; a &lt;&lt; endl;
    }

    return 0;
}</pre>

&nbsp;
