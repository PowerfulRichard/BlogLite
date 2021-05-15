# Easy Fibonacci

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    定义<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>f</mi><mn>0</mn></msub><mo>=</mo><mn>0</mn></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="msubsup"><span id="MathJax-Span-20" class="mi">f</span><span id="MathJax-Span-21" class="mn"></span></span><span id="MathJax-Span-22" class="mo">=</span><span id="MathJax-Span-23" class="mn"></span></span></span></span>,<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>f</mi><mn>1</mn></msub><mo>=</mo><mn>1</mn></math>"><span id="MathJax-Span-24" class="math"><span id="MathJax-Span-25" class="mrow"><span id="MathJax-Span-26" class="msubsup"><span id="MathJax-Span-27" class="mi">f</span><span id="MathJax-Span-28" class="mn">1</span></span><span id="MathJax-Span-29" class="mo">=</span><span id="MathJax-Span-30" class="mn">1</span></span></span></span>
  </p>
  
  <p>
    对于<span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi><mo>&gt;=</mo><mn>2</mn></math>"><span id="MathJax-Span-31" class="math"><span id="MathJax-Span-32" class="mrow"><span id="MathJax-Span-33" class="mi">n</span><span id="MathJax-Span-34" class="mo">>=</span><span id="MathJax-Span-35" class="mn">2</span></span></span></span>定义
  </p>
  
  <div class="MathJax_Display">
    <span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: center; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot; display=&quot;block&quot;><msub><mi>f</mi><mi>n</mi></msub><mo>=</mo><mo stretchy=&quot;false&quot;>(</mo><msub><mi>f</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>n</mi><mo>&#x2212;</mo><mn>1</mn></mrow></msub><mo>+</mo><msub><mi>f</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>n</mi><mo>&#x2212;</mo><mn>2</mn></mrow></msub><mo stretchy=&quot;false&quot;>)</mo><mspace width=&quot;1em&quot; /><mi>mod</mi><mspace width=&quot;thinmathspace&quot; /><mspace width=&quot;thinmathspace&quot; /><mn>10</mn></math>"><span id="MathJax-Span-36" class="math"><span id="MathJax-Span-37" class="mrow"><span id="MathJax-Span-38" class="msubsup"><span id="MathJax-Span-39" class="mi">f</span><span id="MathJax-Span-40" class="mi">n</span></span><span id="MathJax-Span-41" class="mo">=</span><span id="MathJax-Span-42" class="mo">(</span><span id="MathJax-Span-43" class="msubsup"><span id="MathJax-Span-44" class="mi">f</span><span id="MathJax-Span-45" class="texatom"><span id="MathJax-Span-46" class="mrow"><span id="MathJax-Span-47" class="mi">n</span><span id="MathJax-Span-48" class="mo">−</span><span id="MathJax-Span-49" class="mn">1</span></span></span></span><span id="MathJax-Span-50" class="mo">+</span><span id="MathJax-Span-51" class="msubsup"><span id="MathJax-Span-52" class="mi">f</span><span id="MathJax-Span-53" class="texatom"><span id="MathJax-Span-54" class="mrow"><span id="MathJax-Span-55" class="mi">n</span><span id="MathJax-Span-56" class="mo">−</span><span id="MathJax-Span-57" class="mn">2</span></span></span></span><span id="MathJax-Span-58" class="mo">)</span><span id="MathJax-Span-59" class="TeXmathchoice"><span id="MathJax-Span-60" class="mspace"></span></span><span id="MathJax-Span-61" class="mi">mod</span><span id="MathJax-Span-62" class="mspace"></span><span id="MathJax-Span-63" class="mspace"></span><span id="MathJax-Span-64" class="mn">10</span></span></span></span>
  </div>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <span id="MathJax-Element-10-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>0</mn><mo>&#x2264;</mo><mi>k</mi><mo>&#x2264;</mo><msup><mn>10</mn><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mn>18</mn></mrow></msup></math>"><span id="MathJax-Span-65" class="math"><span id="MathJax-Span-66" class="mrow"><span id="MathJax-Span-67" class="mn"></span><span id="MathJax-Span-68" class="mo">≤</span><span id="MathJax-Span-69" class="mi">k</span><span id="MathJax-Span-70" class="mo">≤</span><span id="MathJax-Span-71" class="msubsup"><span id="MathJax-Span-72" class="mn">10</span><span id="MathJax-Span-73" class="texatom"><span id="MathJax-Span-74" class="mrow"><span id="MathJax-Span-75" class="mn">18</span></span></span></span></span></span></span>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <span class="md-expand">计算<span id="MathJax-Element-11-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>f</mi><mi>k</mi></msub></math>"><span id="MathJax-Span-76" class="math"><span id="MathJax-Span-77" class="mrow"><span id="MathJax-Span-78" class="msubsup"><span id="MathJax-Span-79" class="mi">f</span><span id="MathJax-Span-80" class="mi">k</span></span></span></span></span></span>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int a(long long n) {
    int arr[60] = { 0, 1, 1, 2, 3, 5, 8, 3, 1, 4,
                   5, 9, 4, 3, 7, 0, 7, 7, 4, 1,
                   5, 6, 1, 7, 8, 5, 3, 8, 1, 9,
                   0, 9, 9, 8, 7, 5, 2, 7, 9, 6,
                   5, 1, 6, 7, 3, 0, 3, 3, 6, 9,
                   5, 4, 9, 3, 2, 5, 7, 2, 9, 1 };
    return arr[n % 60];
}
int main() {
    long long n;
    while (scanf("%lld", &n) != EOF)
        printf("%d\n", a(n));
}</pre>

&nbsp;
