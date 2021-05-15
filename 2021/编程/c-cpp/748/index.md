# 计数问题[NOIP2013普及组]

<h2 class="lfe-h2" data-v-394f29d4="">题目描述</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

试计算在区间 <span class="katex"><span class="katex-mathml">1</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span></span></span></span> 到 <span class="katex"><span class="katex-mathml">n</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span></span></span></span>的所有整数中，数字<span class="katex"><span class="katex-mathml">x(0 ≤ x ≤ 9)</span></span>共出现了多少次？例如，在 <span class="katex"><span class="katex-mathml">1</span></span>到<span class="katex"><span class="katex-mathml">1</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span></span></span></span>中，即在 <span class="katex"><span class="katex-mathml">1,2,3,4,5,6,7,8,9,10,11</span></span> 中，数字 <span class="katex"><span class="katex-mathml">1</span></span> 出现了 <span class="katex"><span class="katex-mathml">4</span></span> 次。</div> <h2 class="lfe-h2" data-v-394f29d4="">输入格式</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

<span class="katex"><span class="katex-mathml">2</span></span>个整数<span class="katex"><span class="katex-mathml">n,x</span></span>，之间用一个空格隔开。</div> <h2 class="lfe-h2" data-v-394f29d4="">输出格式</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

<span class="katex"><span class="katex-mathml">1</span></span>个整数，表示<span class="katex"><span class="katex-mathml">x</span></span>出现的次数。</div> <h2 class="lfe-h2" data-v-394f29d4="">输入输出样例</h2> <div class="sample-wrap sample" data-v-6ce8694a="" data-v-394f29d4=""> <div class="input" data-v-52f2d52f="" data-v-6ce8694a=""> 

<strong data-v-52f2d52f="">输入 #1</strong><button class="copy-btn lfe-form-sz-middle" type="button" data-v-370e72e2="" data-v-52f2d52f="">复制</button><pre data-v-52f2d52f="">11 1</pre> </div> <div class="output" data-v-52f2d52f="" data-v-6ce8694a=""> 

<strong data-v-52f2d52f="">输出 #1</strong><button class="copy-btn lfe-form-sz-middle" type="button" data-v-370e72e2="" data-v-52f2d52f="">复制</button><pre data-v-52f2d52f="">4</pre> </div> </div> <h2 class="lfe-h3" data-v-394f29d4="">说明/提示</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

对于 <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span><span class="mord"></span><span class="mord">%</span></span></span></span>的数据，<span class="katex"><span class="katex-mathml">1≤ n ≤ 1,000,000   0 ≤ x ≤ 9</span></span>

&nbsp;</div> 

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int num(int n,int x){
    int z=0;
    if (n &lt; 10) {
        if (n == x)z+=1;
        else z+=0;
    }
    else if (n &lt; 100) {
        if (n / 10 == x)z += 1;
        if (n % 10 == x)z += 1;
        else z += 0;
        
    }
    else if (n &lt; 1000) {
        if (n / 100 == x)z += 1;
        if (n % 10 == x)z += 1;
        if (n / 10 % 10 == x)z += 1;
        else z += 0;
    }
    else if (n &lt; 10000) {
        if (n / 1000 == x)z += 1;
        if (n % 10 == x)z += 1;
        if (n / 10 % 10 == x)z += 1;
        if (n / 100 % 10 == x)z += 1;
        else z += 0;
    }
    else if (n &lt; 100000) {
        if (n / 10000 == x)z += 1;
        if (n % 10 == x)z += 1;
        if (n / 10 % 10 == x)z += 1;
        if (n / 100 % 10 == x)z += 1;
        if (n / 1000 % 10 == x)z += 1;
        else z += 0;
    }
    else if (n &lt; 1000000) {
        if (n / 100000 == x)z += 1;
        if (n % 10 == x)z += 1;
        if (n / 10 % 10 == x)z += 1;
        if (n / 100 % 10 == x)z += 1;
        if (n / 1000 % 10 == x)z += 1;
        if (n / 10000 % 10 == x)z += 1;
        else z += 0;
    }
    else if (n &lt; 10000000) {
        if (n / 1000000 == x)z += 1;
        if (n % 10 == x)z += 1;
        if (n / 10 % 10 == x)z += 1;
        if (n / 100 % 10 == x)z += 1;
        if (n / 1000 % 10 == x)z += 1;
        if (n / 10000 % 10 == x)z += 1;
        if (n / 100000 % 10 == x)z += 1;
        else z += 0;
    }
    return z;
}
int main() {
    int n,x,i=0;
    cin &gt;&gt; n &gt;&gt; x;
    for (int j = 1; j &lt;= n; j++) {
        i += num(j, x);
    }
    cout &lt;&lt; i;
}</pre>

&nbsp;
