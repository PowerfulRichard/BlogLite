# 输入输出（字符串）

## 题目描述 {.page-header.text-muted}

<div class="content">
  小时候唐巧住在农村老家，老家的山很高，每次无聊的时候，他都会对着山大声说话，这个时候，山也会对他“说”同样的话（回声）。现在唐巧虽然已经长大了，但是还是常常想起儿时的故事，他想：如果可以再体会一下儿时的那种感觉多好呀!<br /> 请你编程完成模拟回声的程序。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入数据有多行，每行为一个字符串（字符串只由字母组成），字符串最长为15。以EOF结束。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对于每行输入，输出同样的内容。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    char a[15];
    while (scanf("%s",&a)!=EOF) {
        printf("%s\n",a);
    }
    return 0;
}</pre>

&nbsp;
