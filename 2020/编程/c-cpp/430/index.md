# 求矩阵两对角线上的元素之和

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    求矩阵的两对角线上的元素之和
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    矩阵的行数N<br /> 和一个<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi><mo>&#x2217;</mo><mi>N</mi></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mi">N</span><span id="MathJax-Span-20" class="mo">∗</span><span id="MathJax-Span-21" class="mi">N</span></span></span></span>的整数矩阵<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><msub><mi>a</mi><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mi>i</mi><mo>,</mo><mi>j</mi></mrow></msub><mn>1</mn><mo>&#x2264;</mo><mi>N</mi><mo>&#x2264;</mo><mn>10</mn></math>"><span id="MathJax-Span-22" class="math"><span id="MathJax-Span-23" class="mrow"><span id="MathJax-Span-24" class="msubsup"><span id="MathJax-Span-25" class="mi">a</span><span id="MathJax-Span-26" class="texatom"><span id="MathJax-Span-27" class="mrow"><span id="MathJax-Span-28" class="mi">i</span><span id="MathJax-Span-29" class="mo">,</span><span id="MathJax-Span-30" class="mi">j</span></span></span></span><span id="MathJax-Span-31" class="mn">1</span><span id="MathJax-Span-32" class="mo">≤</span><span id="MathJax-Span-33" class="mi">N</span><span id="MathJax-Span-34" class="mo">≤</span><span id="MathJax-Span-35" class="mn">10</span></span></span></span>每一个元素都是整数，范围[-100,100]
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    所输矩阵的两对角线上的元素之和
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int a[100][100];
int n, x, y, sum = 0;
int main() {
    cin &gt;&gt; n;
    for (x = 0; x &lt; n; x++) {
        for (y = 0; y &lt; n; y++) {
            cin &gt;&gt; a[x][y];
        }
    }
    for (x = 0; x &lt; n; x++) {
        for (y = 0; y &lt; n; y++) {
            if (x + y == n - 1 || x == y) {
                sum += a[x][y];
            }
        }
    }
    cout &lt;&lt; sum;
    return 0;
}
</pre>

&nbsp;
