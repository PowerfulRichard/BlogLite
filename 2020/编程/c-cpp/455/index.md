# 回文串

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    回文串是从左到右或者从右到左读起来都一样的字符串，试编程判别一个字符串是否为回文串。是则输出Y，不是则输出N
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    多组输入,每组输入一个不含有空格的字符串。题目保证串长度 不超过255.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    判别输入的字符串是否为回文串，是输出&#8221;Y&#8221;,否则输出&#8221;N&#8221;。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    char s[255 + 10], t[255 + 10];
    while (cin &gt;&gt; s) {
        strcpy(t, s);
        reverse(t, t + strlen(t));
        if (strcmp(s, t) == 0)cout &lt;&lt; "Y" &lt;&lt; endl;
        else cout &lt;&lt; "N" &lt;&lt; endl;
    }
    return 0;
}
</pre>

&nbsp;
