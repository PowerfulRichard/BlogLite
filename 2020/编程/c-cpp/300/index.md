# The Sum Problem数列求和（代码简化）

## 题目描述 {.page-header.text-muted}

<div class="content">
  Hey, welcome to ahstu oj.<br /> In this problem, your task is to calculate SUM(n) = 1 + 2 + 3 + &#8230; + n.
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  The input will consist of a series of integers n, one integer per line.
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  For each case, output SUM(n) in one line. You may assume the result will be in the range of 32-bit signed integer.
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
int main(){
    int n;
    while(scanf("%d",&n)!=EOF){cout&lt;&lt;(1+n)*n/2&lt;&lt;endl;}
    return 0;
}</pre>

&nbsp;
