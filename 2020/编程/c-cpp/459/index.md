# 国王的魔镜

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    描述国王有一个魔镜，可以把任何接触镜面的东西变成原来的两倍——只是，因为是镜子嘛，增加的那部分是反的。
  </p>
  
  <p>
    比如一条项链，我们用AB来表示，不同的字母表示不同颜色的珍珠。如果把B端接触镜面的话，魔镜会把这条项链变为ABBA。如果再用一端接触的话，则会变成ABBAABBA（假定国王只用项链的某一端接触魔镜）。
  </p>
  
  <p>
    给定最终的项链，请编写程序输出国王没使用魔镜之前，最初的项链可能的最小长度。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行是一个整数N(N<=10)表示测试数据的组数） 每组测试数据占一行 只有一个字符串（长度小于100），由大写英文字母组成，表示最终的项链。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  每组测试数据的输出只有一个整数，表示小H没有使用魔法前，最初的项链可能的最小长度。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
bool ok(char* w) {
    int n = strlen(w);
    if (n &lt; 2 || n & 1)return false;
    char s[1000];
    strcpy(s, w);
    reverse(s, s + n);
    return strcmp(s, w) == 0;
}
int main() {
    int T; cin &gt;&gt; T;
    char w[1000];
    while (T--) {
        cin &gt;&gt; w;
        while (ok(w))w[strlen(w) / 2] = 0;
        cout &lt;&lt; strlen(w) &lt;&lt; endl;
    }
    return 0;
}
</pre>

&nbsp;
