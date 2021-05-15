# 计算双阶乘

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    定义$N$的双阶乘:
  </p>
  
  <p>
    <span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi><mo>!</mo><mo>!</mo><mo>=</mo><mi>N</mi><mo>&#x2217;</mo><mo stretchy=&quot;false&quot;>(</mo><mi>N</mi><mo>&#x2212;</mo><mn>2</mn><mo stretchy=&quot;false&quot;>)</mo><mo>&#x2217;</mo><mo stretchy=&quot;false&quot;>(</mo><mi>N</mi><mo>&#x2212;</mo><mn>4</mn><mo stretchy=&quot;false&quot;>)</mo><mo>&#x2217;</mo><mo>.</mo><mo>.</mo><mo>.</mo><mo>.</mo><mi>i</mi></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mi">N</span><span id="MathJax-Span-20" class="mo">!</span><span id="MathJax-Span-21" class="mo">!</span><span id="MathJax-Span-22" class="mo">=</span><span id="MathJax-Span-23" class="mi">N</span><span id="MathJax-Span-24" class="mo">∗</span><span id="MathJax-Span-25" class="mo">(</span><span id="MathJax-Span-26" class="mi">N</span><span id="MathJax-Span-27" class="mo">−</span><span id="MathJax-Span-28" class="mn">2</span><span id="MathJax-Span-29" class="mo">)</span><span id="MathJax-Span-30" class="mo">∗</span><span id="MathJax-Span-31" class="mo">(</span><span id="MathJax-Span-32" class="mi">N</span><span id="MathJax-Span-33" class="mo">−</span><span id="MathJax-Span-34" class="mn">4</span><span id="MathJax-Span-35" class="mo">)</span><span id="MathJax-Span-36" class="mo">∗</span><span id="MathJax-Span-37" class="mo">.</span><span id="MathJax-Span-38" class="mo">.</span><span id="MathJax-Span-39" class="mo">.</span><span id="MathJax-Span-40" class="mo">.</span><span id="MathJax-Span-41" class="mi">i</span></span></span></span>（$i=1<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>o</mi><mi>r</mi></math>"><span id="MathJax-Span-42" class="math"><span id="MathJax-Span-43" class="mrow"><span id="MathJax-Span-44" class="mi">o</span><span id="MathJax-Span-45" class="mi">r</span></span></span></span>i=2$）
  </p>
  
  <p>
    比如<span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>5</mn><mo>!</mo><mo>!</mo><mo>=</mo><mn>5</mn><mo>&#x2217;</mo><mn>3</mn><mo>&#x2217;</mo><mn>1</mn><mo>=</mo><mn>15</mn></math>"><span id="MathJax-Span-46" class="math"><span id="MathJax-Span-47" class="mrow"><span id="MathJax-Span-48" class="mn">5</span><span id="MathJax-Span-49" class="mo">!</span><span id="MathJax-Span-50" class="mo">!</span><span id="MathJax-Span-51" class="mo">=</span><span id="MathJax-Span-52" class="mn">5</span><span id="MathJax-Span-53" class="mo">∗</span><span id="MathJax-Span-54" class="mn">3</span><span id="MathJax-Span-55" class="mo">∗</span><span id="MathJax-Span-56" class="mn">1</span><span id="MathJax-Span-57" class="mo">=</span><span id="MathJax-Span-58" class="mn">15</span></span></span></span>
  </p>
  
  <p>
    而<span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>6</mn><mo>!</mo><mo>!</mo><mo>=</mo><mn>6</mn><mo>&#x2217;</mo><mn>4</mn><mo>&#x2217;</mo><mn>2</mn><mo>=</mo><mn>48</mn></math>"><span id="MathJax-Span-59" class="math"><span id="MathJax-Span-60" class="mrow"><span id="MathJax-Span-61" class="mn">6</span><span id="MathJax-Span-62" class="mo">!</span><span id="MathJax-Span-63" class="mo">!</span><span id="MathJax-Span-64" class="mo">=</span><span id="MathJax-Span-65" class="mn">6</span><span id="MathJax-Span-66" class="mo">∗</span><span id="MathJax-Span-67" class="mn">4</span><span id="MathJax-Span-68" class="mo">∗</span><span id="MathJax-Span-69" class="mn">2</span><span id="MathJax-Span-70" class="mo">=</span><span id="MathJax-Span-71" class="mn">48</span></span></span></span>
  </p>
  
  <p>
    特别的我们定义<span id="MathJax-Element-10-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>0</mn><mo>!</mo><mo>!</mo><mo>=</mo><mn>1</mn><mo>!</mo><mo>!</mo><mo>=</mo><mn>1</mn></math>"><span id="MathJax-Span-72" class="math"><span id="MathJax-Span-73" class="mrow"><span id="MathJax-Span-74" class="mn"></span><span id="MathJax-Span-75" class="mo">!</span><span id="MathJax-Span-76" class="mo">!</span><span id="MathJax-Span-77" class="mo">=</span><span id="MathJax-Span-78" class="mn">1!!=1</span></span></span></span>
  </p>
  
  <p>
    给定<span id="MathJax-Element-11-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span id="MathJax-Span-83" class="math"><span id="MathJax-Span-84" class="mrow"><span id="MathJax-Span-85" class="mi">N</span></span></span><span class="MJX_Assistive_MathML" role="presentation">N</span></span>你的任务是计算出<span id="MathJax-Element-12-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi><mo>!</mo><mo>!</mo></math>"><span id="MathJax-Span-86" class="math"><span id="MathJax-Span-87" class="mrow"><span id="MathJax-Span-88" class="mi">N</span><span id="MathJax-Span-89" class="mo">!</span><span id="MathJax-Span-90" class="mo">!</span></span></span><span class="MJX_Assistive_MathML" role="presentation">N!!</span></span>(你可以假设答案不超过int 范围）
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  多组输入，每行一个整数<span id="MathJax-Element-13-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span id="MathJax-Span-91" class="math"><span id="MathJax-Span-92" class="mrow"><span id="MathJax-Span-93" class="mi">N</span></span></span><span class="MJX_Assistive_MathML" role="presentation">N</span></span>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  你的任务是计算出<span id="MathJax-Element-14-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi><mo>!</mo><mo>!</mo></math>"><span id="MathJax-Span-94" class="math"><span id="MathJax-Span-95" class="mrow"><span id="MathJax-Span-96" class="mi">N</span><span id="MathJax-Span-97" class="mo">!</span><span id="MathJax-Span-98" class="mo">!</span></span></span><span class="MJX_Assistive_MathML" role="presentation">N!!</span></span>(你可以假设答案不超过int 范围）
</div>

> <div>
>   注：需要分奇偶分别计算
> </div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int n,s,x;
    while(scanf("%d",&n)!=EOF){
        s=n;
        if(n%2==0){
            while(n&gt;2){
                x=n-2;
                s=s*x;
                n=x;
            }
            cout&lt;&lt;s&lt;&lt;endl;}
        else{
            while(n&gt;1){
                x=n-2;
                s=s*x;
                n=x;
            }
            cout&lt;&lt;s&lt;&lt;endl;}
    }
    return 0;
}</pre>

&nbsp;
