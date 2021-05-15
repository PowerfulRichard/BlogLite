# Tom数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    正整数的各位数字之和称为Tom数。求输入<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">n</span></span>, <span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi><mo>&#x2264;</mo><msup><mn>2</mn><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mn>31</mn></mrow></msup><mo>&#x2212;</mo><mn>1</mn></math>"><span class="MJX_Assistive_MathML" role="presentation">n≤2<sup>31</sup>−1</span></span>的Tom数!
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    每行一个整数<span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">n</span></span> ,<span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 15px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>n</mi><mo>&#x2264;</mo><msup><mn>2</mn><mrow class=&quot;MJX-TeXAtom-ORD&quot;><mn>31</mn></mrow></msup><mo>&#x2212;</mo><mn>1</mn></math>"><span class="MJX_Assistive_MathML" role="presentation">n≤2<sup>31</sup>−1</span></span>.
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    每行一个输出,对应该数的各位数之和.
  </p>
</div>

方法一

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{
    int n;
    char s[1001];
    while(scanf("%s",&s)!=EOF)
    {
        int a=0;
        n=strlen(s);
        for(int i=0; i&lt;n; i++)
        {
            a+=(s[i]-‘0‘);
        }
        printf("%d\n",a);
    }
    return 0;
}</pre>

&nbsp;

方法二：优化版

<pre class="EnlighterJSRAW" data-enlighter-language="c">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main()
{  
    char a[11];
    while(gets(a)!=NULL){
        int i,sum=0;
        for(i=0;i&lt;strlen(a);i++)
            sum+=a[i]-'0';        //将字母转换成数字
        printf("%d\n",sum);
    }
    return 0;
}</pre>

&nbsp;
