# 求T(m)的值

<div class="content">
  <h2 class="page-header text-muted">
    题目描述
  </h2>
  
  <div class="content">
    <p>
      给定<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>m</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">m</span></span>根据以下公式计算<span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>T</mi><mo stretchy=&quot;false&quot;>(</mo><mi>m</mi><mo stretchy=&quot;false&quot;>)</mo></math>"><span id="MathJax-Span-50" class="math"><span id="MathJax-Span-51" class="mrow"><span id="MathJax-Span-52" class="mi">T</span><span id="MathJax-Span-53" class="mo">(</span><span id="MathJax-Span-54" class="mi">m</span><span id="MathJax-Span-55" class="mo">)</span></span></span></span>： <strong><span style="font-size: 1rem;">T(m)=1-(1/(2*2))-&#8230;.-(1/(m*m))</span></strong>
    </p>
    
    <h2 class="page-header text-muted">
      输入
    </h2>
    
    <div class="content">
      <p>
        整型变量m范围[2,1000]
      </p>
    </div>
    
    <h2 class="page-header text-muted">
      输出
    </h2>
    
    <div class="content">
      <p>
        计算<span id="MathJax-Element-11-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>T</mi><mo stretchy=&quot;false&quot;>(</mo><mi>m</mi><mo stretchy=&quot;false&quot;>)</mo></math>"><span id="MathJax-Span-89" class="math"><span id="MathJax-Span-90" class="mrow"><span id="MathJax-Span-91" class="mi">T</span><span id="MathJax-Span-92" class="mo">(</span><span id="MathJax-Span-93" class="mi">m</span><span id="MathJax-Span-94" class="mo">)</span></span></span></span>(保留六位小数)
      </p>
    </div>
  </div>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main(){
    int m,i=1;
    long double t,x,y;
    t=1;
    cin&gt;&gt;m;
    while(i&lt;m){
    	i=i+1;
        x=i*i;
        y=1/x;
        t=t-y;
    }
    printf("%.6Lf",t);
	return 0;
}</pre>

&nbsp;
