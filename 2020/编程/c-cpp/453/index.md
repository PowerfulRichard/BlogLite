# 字母大小写转换

## 题目描述 {.page-header.text-muted}

<div class="content">
  现在给出了一个只包含大小写字母的字符串，不含空格和换行，要求把其中的大写换成小写，小写换成大写，然后输出互换后的字符串。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行只有一个整数m（m<=10),表示测试数据组数。<br /> 接下来的m行，每行有一个字符串（长度不超过100）。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出互换后的字符串，每组输出占一行。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int n, i, j;
    cin &gt;&gt; n;
    string a;
    while (n--) {
        cin &gt;&gt; a;
        j = a.length();
        for (i = 0; i &lt; j; i++) {
            if (a[i] &gt;= 'a' && a[i] &lt;= 'z')a[i] = a[i] - 32;
            else a[i] += 32;
        }
        cout &lt;&lt; a &lt;&lt; endl;
    }
    return 0;
}</pre>

&nbsp;
