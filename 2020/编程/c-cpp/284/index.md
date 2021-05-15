# 梯形

## 题目描述 {.page-header.text-muted}

<div class="content">
  给出等腰梯形的上底、下底和高，要求计算该梯形的面积与周长。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入数据只有一行，每行依次出现三个数U、D、H，分别表示等腰梯形的上底、下底和高。（ 0 < U < D<100, 0 < H<100）
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出两行，第一行输出梯形的面积，第二行输出梯形的周长。（面积和周长均保留2位小数）
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    double u,d,h,s,c,t;
    cin&gt;&gt;u&gt;&gt;d&gt;&gt;h;
    t=sqrt(h*h+(((d-u)/2)*((d-u)/2)));
    s=(u+d)*h/2;
    c=u+d+2*t;
    printf("%.2lf\n%.2lf",s,c);
    return 0;
}</pre>

&nbsp;
