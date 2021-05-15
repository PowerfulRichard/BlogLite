# 韩信点兵

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    相传韩信才智过人，从不直接清点自己的军队的个数，只要让士兵先后以三人一排，五人一排，七人一排，变换队形，而他每次只掠一眼队伍的排尾人数就知道总人数了，输入三个非负整数,a,b,c表示每种队形排尾的人数，(a < 3, b < 5,c < 7)输出总人数的最小值（或报告无解）,已知总人数不超过100，不少于10人
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    ，输入三个非负整数,a,b,c表示每种队形排尾的人数，(a < 3, b < 5,c < 7)
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输出总人数的最小值（或报告无解）
  </p>
  
  <blockquote>
    <p>
      注：需使用<strong><em>中国剩余定理</em></strong>
    </p>
  </blockquote>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int a,b,c,t;
    while(scanf("%d %d %d",&a,&b,&c)!=EOF){
        t=a*70+21*b+c*15;
        while(t&gt;105){
            t=t-105;
        }
        if(t&gt;100){
            cout&lt;&lt;"No answer"&lt;&lt;endl;
        }
        else{
            cout&lt;&lt;t&lt;&lt;endl;
        }
        t=0;
    }
    
    return 0;
}</pre>

&nbsp;
