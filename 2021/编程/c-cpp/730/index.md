# 陶陶摘苹果[NOIP2005]

<h2 class="lfe-h2" data-v-394f29d4="">题目描述</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

陶陶家的院子里有一棵苹果树，每到秋天树上就会结出 <span class="katex"><span class="katex-mathml">10</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span></span></span></span> 个苹果。苹果成熟的时候，陶陶就会跑去摘苹果。陶陶有个 <span class="katex"><span class="katex-mathml">30</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">3</span><span class="mord"></span></span></span></span> 厘米高的板凳，当她不能直接用手摘到苹果的时候，就会踩到板凳上再试试。

现在已知 <span class="katex"><span class="katex-mathml">10</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span></span></span></span> 个苹果到地面的高度，以及陶陶把手伸直的时候能够达到的最大高度，请帮陶陶算一下她能够摘到的苹果的数目。假设她碰到苹果，苹果就会掉下来。</div> <h2 class="lfe-h2" data-v-394f29d4="">输入格式</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

输入包括两行数据。第一行包含 <span class="katex"><span class="katex-mathml">10</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span></span></span></span> 个 <span class="katex"><span class="katex-mathml">100</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span><span class="mord"></span></span></span></span> 到 <span class="katex"><span class="katex-mathml">200</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">2</span><span class="mord"></span><span class="mord"></span></span></span></span> 之间（包括 <span class="katex"><span class="katex-mathml">100</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span><span class="mord"></span></span></span></span> 和 <span class="katex"><span class="katex-mathml">200</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">2</span><span class="mord"></span><span class="mord"></span></span></span></span> ）的整数（以厘米为单位）分别表示 <span class="katex"><span class="katex-mathml">10</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span></span></span></span> 个苹果到地面的高度，两个相邻的整数之间用一个空格隔开。第二行只包括一个 <span class="katex"><span class="katex-mathml">100</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span><span class="mord"></span></span></span></span> 到 <span class="katex"><span class="katex-mathml">120</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord">2</span><span class="mord"></span></span></span></span> 之间（包含 <span class="katex"><span class="katex-mathml">100</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span><span class="mord"></span></span></span></span> 和 <span class="katex"><span class="katex-mathml">120</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord">2</span><span class="mord"></span></span></span></span> ）的整数（以厘米为单位），表示陶陶把手伸直的时候能够达到的最大高度。</div> <h2 class="lfe-h2" data-v-394f29d4="">输出格式</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

输出包括一行，这一行只包含一个整数，表示陶陶能够摘到的苹果的数目。</div> 

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int a[15];
int main() {
    int b, B, A, c = 0;
    for (int i = 1; i &lt;= 10; i++)cin &gt;&gt; a[i];
    cin &gt;&gt; b;
    B = b + 30;
    for (int i = 1; i &lt;= 10; i++)if (a[i] &lt;= B)c++;
    cout &lt;&lt; c;
    return 0;
}</pre>

&nbsp;
