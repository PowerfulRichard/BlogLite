# 区间质数统计（加强版）

## 题目描述 {.page-header.text-muted}

<div class="content">
    给定区间<span id="MathJax-Element-6-Frame" class="MathJax" style="box-sizing: border-box; font-size: 14px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mo stretchy=&quot;false&quot;>[</mo><mi>L</mi><mo>,</mo><mi>R</mi><mo stretchy=&quot;false&quot;>]</mo></math>"><span id="MathJax-Span-17" class="math"><span id="MathJax-Span-18" class="mrow"><span id="MathJax-Span-19" class="mo">[</span><span id="MathJax-Span-20" class="mi">L</span><span id="MathJax-Span-21" class="mo">,</span><span id="MathJax-Span-22" class="mi">R</span><span id="MathJax-Span-23" class="mo">]</span></span></span></span> ，  请计算区间中素数的个数。 其中<span id="MathJax-Element-7-Frame" class="MathJax" style="box-sizing: border-box; font-size: 13.3333px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>2</mn><mo>&#x2264;</mo><mi>L</mi><mo>&#x2264;</mo><mi>R</mi><mo>&#x2264;</mo><mn>2</mn><mo>&#x00D7;</mo><msup><mn>10</mn><mn>9</mn></msup></math>"><span id="MathJax-Span-24" class="math"><span id="MathJax-Span-25" class="mrow"><span id="MathJax-Span-26" class="mn" style="font-size: 13.3333px; white-space: nowrap;">2</span><span id="MathJax-Span-27" class="mo" style="font-size: 13.3333px; white-space: nowrap;">≤</span><span id="MathJax-Span-28" class="mi" style="font-size: 13.3333px; white-space: nowrap;">L</span><span id="MathJax-Span-29" class="mo" style="font-size: 13.3333px; white-space: nowrap;">≤</span><span id="MathJax-Span-30" class="mi" style="font-size: 13.3333px; white-space: nowrap;">R</span><span id="MathJax-Span-31" class="mo" style="font-size: 13.3333px; white-space: nowrap;">≤</span><span id="MathJax-Span-32" class="mn" style="font-size: 13.3333px; white-space: nowrap;">2</span><span id="MathJax-Span-33" class="mo" style="font-size: 13.3333px; white-space: nowrap;">×</span><span id="MathJax-Span-34" class="msubsup"><span id="MathJax-Span-35" class="mn" style="font-size: 13.3333px; white-space: nowrap;">10</span><span id="MathJax-Span-36" class="mn"><span style="font-size: 13.3333px; white-space: nowrap;">9</span>，</span></span></span></span></span><span id="MathJax-Element-8-Frame" class="MathJax" style="box-sizing: border-box; font-size: 13.3333px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>R</mi><mo>&#x2212;</mo><mi>L</mi><mo>&#x2264;</mo><mn>1000000</mn></math>"><span id="MathJax-Span-37" class="math"><span id="MathJax-Span-38" class="mrow"><span id="MathJax-Span-39" class="mi">R</span><span id="MathJax-Span-40" class="mo">−</span><span id="MathJax-Span-41" class="mi">L</span><span id="MathJax-Span-42" class="mo">≤</span><span id="MathJax-Span-43" class="mn">1000000</span></span></span></span>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  两个数<span id="MathJax-Element-9-Frame" class="MathJax" style="box-sizing: border-box; font-size: 13.3333px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>L</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">L</span></span>和<span id="MathJax-Element-10-Frame" class="MathJax" style="box-sizing: border-box; font-size: 13.3333px; display: inline; font-style: normal; font-weight: normal; line-height: normal; text-indent: 0px; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; overflow-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0px; min-height: 0px; border: 0px; padding: 0px; margin: 0px; position: relative;" tabindex="0" role="presentation" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>R</mi></math>"><span class="MJX_Assistive_MathML" role="presentation">R</span></span>。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  一行，区间中素数的个数。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
#define maxn 1000010
int pri[10000];
typedef long long LL;
bool a[maxn];
int Eratosthenes_Sieve(int n, int pri[]) {
    for (int i = 2; i * i &lt;= n; i++)
        if (a[i] == 0)
            for (int j = i &lt;&lt; 1; j &lt;= n; j += i)
                a[j] = 1;
    int cnt = 0;
    for (int i = 2; i &lt;= n; i++)
        if (!a[i])
            pri[cnt++] = i;
    return cnt;
}
int main() {
    int cnt = Eratosthenes_Sieve(50000, pri);
    LL L, R;
    scanf("%lld %lld", &L, &R);
    memset(a, 0, sizeof(a));
    for (int i = 0; i &lt; cnt; i++)
        for (LL j = max(2ll, (L - 1) / pri[i] + 1) * pri[i]; j &lt;= R; j += pri[i])
            a[j - L] = 1;
    int ans = 0;
    for (LL i = L; i &lt;= R; i++)
        if (a[i - L] == 0)
            ans++;
    printf("%d", ans);
    return 0;
}</pre>

&nbsp;
