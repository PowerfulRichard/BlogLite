# 小明A+B

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">小明今年3岁了, 现在他已经能够认识100以内的非负整数, 并且能够进行100以内的非负整数的加法计算. 对于大于等于100的整数, 小明仅保留该数的最后两位进行计算, 如果计算结果大于等于100, 那么小明也仅保留计算结果的最后两位. 例如, 对于小明来说: 1) 1234和34是相等的 2) 35+80=15 给定非负整数A和B, 你的任务是代表小明计算出A+B的值.</span>
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">输入数据的第一行为一个正整数T, 表示测试数据的组数. 然后是T组测试数据. 每组测试数据包含两个非负整数A和B(A和B均在int型可表示的范围内).</span>
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">对于每组测试数据, 输出小明A+B的结果.</span>
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a,b,t,s;
    cin&gt;&gt;t;
    while(scanf("%d %d",&a,&b)!=EOF){
        s=a+b;
        s=s%100;
        cout&lt;&lt;s&lt;&lt;endl;
    }
    return 0;
}</pre>

&nbsp;
