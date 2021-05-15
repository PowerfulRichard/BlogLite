# 数数小木块

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    墙角堆着一些小木块，每一层都有相同大小类似正方体，如下图所示：
  </p>
  
  <p>
    <img src="https://i2.wp.com/acm.webturing.com/JudgeOnline/upload/image/20171118/20171118182353_40758.jpg?w=688&#038;ssl=1" alt="" data-recalc-dims="1" />
  </p>
  
  <p>
    因为小木块建造得实在是太有规律了，你只要知道它的层数就可以计算所有小木块的数量了。 现在请你写个程序 给你一个层数<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>m</mi></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mi">m</span></span></span><span class="MJX_Assistive_MathML" role="presentation">m</span></span>，求出这个所有小木块的数量。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行是一个整数<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi><mo stretchy=&quot;false&quot;>(</mo><mi>N</mi><mo>&#x2264;</mo><mn>10</mn><mo stretchy=&quot;false&quot;>)</mo></math>"><span id="MathJax-Span-20" class="math"><span id="MathJax-Span-21" class="mrow"><span id="MathJax-Span-22" class="mi">N</span><span id="MathJax-Span-23" class="mo">(</span><span id="MathJax-Span-24" class="mi">N</span><span id="MathJax-Span-25" class="mo">≤</span><span id="MathJax-Span-26" class="mn">10</span><span id="MathJax-Span-27" class="mo">)</span></span></span></span>表示测试数据的组, 接下来的<span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>N</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">N</span></span>行 每行只有一个整数<span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>m</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">m</span></span> ，表示这个层数。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对应每个输入的层数有一个输出，表示这个小木块总数量，每个输出占一行
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;stdio.h&gt;

int a(int n){
    n = (1+n)*n/2;
    return n;
}

int main(){
    int n;
    scanf("%d", &n);
    for (int i = n; i&gt;=1; --i){
        int m, sum=0;
        scanf("%d", &m);
        for (int b = m; b&gt;=1; --b){
            sum += a(b);
        }
        printf("%d\n", sum);
    }

}</pre>

&nbsp;
