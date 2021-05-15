# 区间质数统计

## 题目描述 {.page-header.text-muted}

<div class="content">
  计算 区间<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mo stretchy=&quot;false&quot;>[</mo><mi>a</mi><mo>,</mo><mi>b</mi><mo stretchy=&quot;false&quot;>]</mo></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mo">[</span><span id="MathJax-Span-20" class="mi">a</span><span id="MathJax-Span-21" class="mo">,</span><span id="MathJax-Span-22" class="mi">b</span><span id="MathJax-Span-23" class="mo">]</span></span></span></span>的所有质数个数（<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>1</mn><mo>&#x2264;</mo><mi>a</mi><mo>&#x003C;</mo><mi>b</mi><mo>&#x2264;</mo><mn>1000000</mn></math>"><span id="MathJax-Span-24" class="math"><span id="MathJax-Span-25" class="mrow"><span id="MathJax-Span-26" class="mn">1</span><span id="MathJax-Span-27" class="mo">≤</span><span id="MathJax-Span-28" class="mi">a</span><span id="MathJax-Span-29" class="mo"><</span><span id="MathJax-Span-30" class="mi">b</span><span id="MathJax-Span-31" class="mo">≤</span><span id="MathJax-Span-32" class="mn">1000000）</span></span></span></span>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  两个整数 <span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>a</mi></math>"><span id="MathJax-Span-33" class="math"><span id="MathJax-Span-34" class="mrow"><span id="MathJax-Span-35" class="mi"><span style="font-size: 14px; white-space: nowrap;">a,</span>，</span></span></span></span><span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>b</mi></math>"><span id="MathJax-Span-36" class="math"><span id="MathJax-Span-37" class="mrow"><span id="MathJax-Span-38" class="mi">b</span></span></span></span>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  区间<span id="MathJax-Element-10-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mo stretchy=&quot;false&quot;>[</mo><mi>a</mi><mo>,</mo><mi>b</mi><mo stretchy=&quot;false&quot;>]</mo></math>"><span id="MathJax-Span-39" class="math"><span id="MathJax-Span-40" class="mrow"><span id="MathJax-Span-41" class="mo">[</span><span id="MathJax-Span-42" class="mi">a</span><span id="MathJax-Span-43" class="mo">,</span><span id="MathJax-Span-44" class="mi">b</span><span id="MathJax-Span-45" class="mo">]</span></span></span></span>的所有质数个数
</div>

<div>
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
    int a, b;
    cin &gt;&gt; a &gt;&gt; b;
    int i, j;
    int count = 0;
    for (i = a; i &lt;= b; i++) {
        for (j = 2; j &lt; i; j++) {
            if (i % j == 0)break;
        }
        if (j == i) {
            count++;
        }
    }
    cout &lt;&lt; count &lt;&lt; endl;
    return 0;
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
