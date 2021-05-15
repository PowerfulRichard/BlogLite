# 自由落体问题

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    一个球从<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>100</mn></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mn">100</span></span></span></span>米高度自由落下,每次落地后反跳回原来高度的一半,再落下,再反弹.求它在第<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">N</span></span>次落地时共经过多少米?
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    反弹的次数N范围[2,1000]
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    小球经过的路程(保留四位小数)
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n;
    double s=100,x=100;
    cin&gt;&gt;n;
    for(;n&gt;1;n=n-1){
        x=x/2;
        s=s+2*x;
    }
    printf("%.4lf",s);
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>

&nbsp;
