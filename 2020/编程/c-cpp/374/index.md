# Fibonacci数列前20项(斐波那契数列)

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    Fibonacci数列的特点：第1,2个数为1,1。从第3个数开始，概述是前面两个数之和。即： <img src="https://i1.wp.com/acm.webturing.com/JudgeOnline/upload/pimg2310_1.jpg?w=688&#038;ssl=1" alt="" data-recalc-dims="1" />
  </p>
  
  <p>
    要求输出Fibonacci数列的前20个数。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  无
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  Fibonacci数列的前20个数，每个数占一行。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int f[20]={1,1};
    for(int n=2;n&lt;20;n++){
        f[n]=f[n-1]+f[n-2];
    }
    for(int i=0;i&lt;20;i++){
        cout&lt;&lt;f[i]&lt;&lt;endl;
    }
    return 0;
}</pre>

&nbsp;
