# 近似计算PI

## 题目描述 {.page-header.text-muted}

<div class="content">
  计算pi/4=1-1/3+1/5-1/7+&#8230;.+1/n，
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  n
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  根据该算式计算的pi的值（精确6位有效数字）
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    double pi=0,i,n;
    while(scanf("%lf",&n)!=EOF){
        i=3;
        while(i&lt;=n){
            pi=pi+(1/i);
            i=i+4;
        }
        i=5;
        while(i&lt;=n){
            pi=pi-(1/i);
            i=i+4;
        }
        printf("%lf\n",(1-pi)*4);
        pi=0;
    }
    return 0;
}</pre>

&nbsp;
