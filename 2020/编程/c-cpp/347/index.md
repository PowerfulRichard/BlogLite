# 最近平方数

## 题目描述 {.page-header.text-muted}

<div class="content">
  如果一个整数可以写成另一个整数的平方，则说它是一个完全平方数。比如<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>1</mn><mo>,</mo><mn>4</mn><mo>,</mo><mn>9</mn><mo>,</mo><mn>16</mn></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mn">1</span><span id="MathJax-Span-20" class="mo">,</span><span id="MathJax-Span-21" class="mn">4</span><span id="MathJax-Span-22" class="mo">,</span><span id="MathJax-Span-23" class="mn">9</span><span id="MathJax-Span-24" class="mo">,</span><span id="MathJax-Span-25" class="mn">16</span></span></span></span>是完全平方数。<br /> 输入一个整数，找到一个离它最近的完全平方数。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  仅有一组测式数据，输入一个整数<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span id="MathJax-Span-26" class="math"><span id="MathJax-Span-27" class="mrow"><span id="MathJax-Span-28" class="mi">N</span></span></span><span class="MJX_Assistive_MathML" role="presentation">N</span></span>,  <span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>0</mn><mo>&#x2264;</mo><mi>N</mi><mo>&#x2264;</mo><mn>100000</mn></math>"><span id="MathJax-Span-29" class="math"><span id="MathJax-Span-30" class="mrow"><span id="MathJax-Span-31" class="mn"></span><span id="MathJax-Span-32" class="mo">≤</span><span id="MathJax-Span-33" class="mi">N</span><span id="MathJax-Span-34" class="mo">≤</span><span id="MathJax-Span-35" class="mn">100000</span></span></span></span>。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出离它最近的完全平方数,如果<span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span id="MathJax-Span-36" class="math"><span id="MathJax-Span-37" class="mrow"><span id="MathJax-Span-38" class="mi">N</span></span></span></span>就是完全平方数，则输出<span id="MathJax-Element-10-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">N</span></span>。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n,a=1,b,c,nn;
    cin&gt;&gt;n;
    b=n;
    c=n;
    while(a*a!=b){
          while(a*a&lt;b){
            a++;
          }
          if(a*a!=b){
                a=1;
            b--;
          } 
    }
    while(a*a!=c){
          while(a*a&lt;c){
            a++;
          }
          if(a*a!=c){
            a=1;
            c++;
          } 
    }
    if((c-n)&gt;(n-b)){cout&lt;&lt;b;}
    else{cout&lt;&lt;c;}
    return 0;
}</pre>

&nbsp;
