# 查找最大元素

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">对于输入的每个字符串，查找其中的最大字母，在该字母后面插入字符串“(max)”。</span>
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">输入数据包括多个测试实例，每个实例由一行长度不超过100的字符串组成，字符串仅由大小写字母及数字构成</span>
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">对于每个测试实例输出一行字符串，输出的结果是插入字符串“(max)”后的结果，如果存在多个最大的字母，就在每一个最大字母后面都插入&#8221;(max)&#8221;。</span>
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    char s[100 + 10];
    while (cin &gt;&gt; s) {
        for (char* p = s; *p; ++p) {
            char m = *max_element(s, s + strlen(s));
            cout &lt;&lt; *p;
            if (*p == m)cout &lt;&lt; "(max)";
        }
        cout &lt;&lt; endl;
    }
    return 0;
}
</pre>

<div class="content">
  <p>
    &nbsp;
  </p>
</div>
