# aabb问题

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
        输出所有形如<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>a</mi><mi>a</mi><mi>b</mi><mi>b</mi></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mi">a</span><span id="MathJax-Span-20" class="mi">a</span><span id="MathJax-Span-21" class="mi">b</span><span id="MathJax-Span-22" class="mi">b</span></span></span></span>的四位完全平方数，每一个一行
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    无
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输出所有形如<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>a</mi><mi>a</mi><mi>b</mi><mi>b</mi></math>"><span id="MathJax-Span-23" class="math"><span id="MathJax-Span-24" class="mrow"><span id="MathJax-Span-25" class="mi">a</span><span id="MathJax-Span-26" class="mi">a</span><span id="MathJax-Span-27" class="mi">b</span><span id="MathJax-Span-28" class="mi">b</span></span></span></span>的四位完全平方数，每一个一行
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    int a=1000;
    while(a&lt;10000)
    {
        for(int i=33;i*i&lt;=a;i++)
        {
            if(i*i==a) 
            if(a%10==a/10%10&&a/100%10==a/1000)
            cout&lt;&lt;a&lt;&lt;endl;
        } 
        a++;
    }
    return 0;       
}</pre>
  
  <p>
    &nbsp;
  </p>
</div>
