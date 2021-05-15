# 求（超大）数字的第一位

## 题目描述 {.page-header.text-muted}

<div class="content">
  输入一个整数<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mi">n</span></span></span></span>（<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>1</mn><mo>&#x2264;</mo><mi>n</mi><mo>&#x2264;</mo><msup><mn>2</mn><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mn>63</mn></mrow></msup><mo>&#x2212;</mo><mn>1</mn></math>"><span id="MathJax-Span-20" class="math"><span id="MathJax-Span-21" class="mrow"><span id="MathJax-Span-22" class="mn">1</span><span id="MathJax-Span-23" class="mo">≤</span><span id="MathJax-Span-24" class="mi">n</span><span id="MathJax-Span-25" class="mo">≤</span><span id="MathJax-Span-26" class="msubsup"><span id="MathJax-Span-27" class="mn">2</span><sup><span id="MathJax-Span-28" class="texatom"><span id="MathJax-Span-29" class="mrow"><span id="MathJax-Span-30" class="mn">63</span></span></span></sup></span><span id="MathJax-Span-31" class="mo">−</span><span id="MathJax-Span-32" class="mn">1</span></span></span></span>），你的任务是算出<span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi></math>"><span id="MathJax-Span-33" class="math"><span id="MathJax-Span-34" class="mrow"><span id="MathJax-Span-35" class="mi">n</span></span></span><span class="MJX_Assistive_MathML" role="presentation">n</span></span>最高位
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    多组输入，第一个是整数<span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span id="MathJax-Span-36" class="math"><span id="MathJax-Span-37" class="mrow"><span id="MathJax-Span-38" class="mi">N</span></span></span></span>代表有<span id="MathJax-Element-10-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span id="MathJax-Span-39" class="math"><span id="MathJax-Span-40" class="mrow"><span id="MathJax-Span-41" class="mi">N</span></span></span></span>个数，
  </p>
  
  <p>
    后面有<span id="MathJax-Element-11-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span id="MathJax-Span-42" class="math"><span id="MathJax-Span-43" class="mrow"><span id="MathJax-Span-44" class="mi">N</span></span></span></span>个整数<span id="MathJax-Element-12-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>m</mi></math>"><span id="MathJax-Span-45" class="math"><span id="MathJax-Span-46" class="mrow"><span id="MathJax-Span-47" class="mi">m</span></span></span></span>
  </p>
  
  <p>
    对每一个<span id="MathJax-Element-13-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>m</mi></math>"><span id="MathJax-Span-48" class="math"><span id="MathJax-Span-49" class="mrow"><span id="MathJax-Span-50" class="mi">m</span></span></span></span>输出最高一位
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    对每一个<span id="MathJax-Element-14-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>m</mi></math>"><span id="MathJax-Span-51" class="math"><span id="MathJax-Span-52" class="mrow"><span id="MathJax-Span-53" class="mi">m</span></span></span></span>输出最高一位
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    char n[20];
    int x,i;
    cin&gt;&gt;i;
    while(i--){
    scanf("%s",n);
    cout&lt;&lt;n[0]&lt;&lt;endl;
    }
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
