# 铺地毯[NOIP2011提高组]

<h2 class="lfe-h2" data-v-394f29d4="">题目描述</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

为了准备一个独特的颁奖典礼，组织者在会场的一片矩形区域（可看做是平面直角坐标系的第一象限）铺上一些矩形地毯。一共有 <span class="katex"><span class="katex-mathml">n</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span></span></span></span> 张地毯，编号从 <span class="katex"><span class="katex-mathml">1</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span></span></span></span> 到 <span class="katex"><span class="katex-mathml">n</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span></span></span></span>。现在将这些地毯按照编号从小到大的顺序平行于坐标轴先后铺设，后铺的地毯覆盖在前面已经铺好的地毯之上。

地毯铺设完成后，组织者想知道覆盖地面某个点的最上面的那张地毯的编号。注意：在矩形地毯边界和四个顶点上的点也算被地毯覆盖。</div> <h2 class="lfe-h2" data-v-394f29d4="">输入格式</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

输入共 <span class="katex"><span class="katex-mathml">n + 2</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span><span class="mbin">+</span></span><span class="base"><span class="mord">2</span></span></span></span> 行。

第一行，一个整数 <span class="katex"><span class="katex-mathml">n</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span></span></span></span>，表示总共有 <span class="katex"><span class="katex-mathml">n</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span></span></span></span> 张地毯。

接下来的 <span class="katex"><span class="katex-mathml">n</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span></span></span></span> 行中，第 <span class="katex"><span class="katex-mathml">i+1</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">i</span><span class="mbin">+</span></span><span class="base"><span class="mord">1</span></span></span></span> 行表示编号 <span class="katex"><span class="katex-mathml">i</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">i</span></span></span></span> 的地毯的信息，包含四个整数 <span class="katex"><span class="katex-mathml">a ,b ,g ,k</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">a</span><span class="mpunct">,</span><span class="mord mathnormal">b</span><span class="mpunct">,</span><span class="mord mathnormal">g</span><span class="mpunct">,</span><span class="mord mathnormal">k</span></span></span></span>，每两个整数之间用一个空格隔开，分别表示铺设地毯的左下角的坐标 <span class="katex"><span class="katex-mathml">(a, b)</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mopen">(</span><span class="mord mathnormal">a</span><span class="mpunct">,</span><span class="mord mathnormal">b</span><span class="mclose">)</span></span></span></span> 以及地毯在 <span class="katex"><span class="katex-mathml">x</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">x</span></span></span></span> 轴和 <span class="katex"><span class="katex-mathml">y</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">y</span></span></span></span> 轴方向的长度。

第 <span class="katex"><span class="katex-mathml">n + 2</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span><span class="mbin">+</span></span><span class="base"><span class="mord">2</span></span></span></span> 行包含两个整数 <span class="katex"><span class="katex-mathml">x</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">x</span></span></span></span> 和 <span class="katex"><span class="katex-mathml">y</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">y</span></span></span></span>，表示所求的地面的点的坐标 <span class="katex"><span class="katex-mathml">(x, y)</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mopen">(</span><span class="mord mathnormal">x</span><span class="mpunct">,</span><span class="mord mathnormal">y</span><span class="mclose">)</span></span></span></span>。</div> <h2 class="lfe-h2" data-v-394f29d4="">输出格式</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

输出共 <span class="katex"><span class="katex-mathml">1</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span></span></span></span> 行，一个整数，表示所求的地毯的编号；若此处没有被地毯覆盖则输出 `-1`。</div> <h2 class="lfe-h2" data-v-394f29d4="">输入输出样例</h2> <div class="sample-wrap sample" data-v-6ce8694a="" data-v-394f29d4=""> <div class="input" data-v-52f2d52f="" data-v-6ce8694a=""> 

<strong data-v-52f2d52f="">输入 #1</strong><pre data-v-52f2d52f="">3 1 0 2 3 0 2 3 3 2 1 3 3 2 2 </pre> </div> <div class="output" data-v-52f2d52f="" data-v-6ce8694a=""> 

<strong data-v-52f2d52f="">输出 #1</strong><pre data-v-52f2d52f="">3 </pre> </div> </div> <div class="sample-wrap sample" data-v-6ce8694a="" data-v-394f29d4=""> <div class="input" data-v-52f2d52f="" data-v-6ce8694a=""> 

<strong data-v-52f2d52f="">输入 #2</strong><pre data-v-52f2d52f="">3 1 0 2 3 0 2 3 3 2 1 3 3 4 5</pre> </div> <div class="output" data-v-52f2d52f="" data-v-6ce8694a=""> 

<strong data-v-52f2d52f="">输出 #2</strong><pre data-v-52f2d52f="">-1</pre> </div> </div> <h2 class="lfe-h3" data-v-394f29d4="">说明/提示</h2> <div class="marked" data-v-5a58a989="" data-v-394f29d4=""> 

【样例解释 1】

如下图，<span class="katex"><span class="katex-mathml">1</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span></span></span></span> 号地毯用实线表示，<span class="katex"><span class="katex-mathml">2</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">2</span></span></span></span> 号地毯用虚线表示，<span class="katex"><span class="katex-mathml">3</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">3</span></span></span></span> 号用双实线表示，覆盖点 <span class="katex"><span class="katex-mathml">(2,2)</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mopen">(</span><span class="mord">2</span><span class="mpunct">,</span><span class="mord">2</span><span class="mclose">)</span></span></span></span> 的最上面一张地毯是 <span class="katex"><span class="katex-mathml">3</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">3</span></span></span></span> 号地毯。

<img src="https://i1.wp.com/cdn.luogu.com.cn/upload/pic/100.png?w=688&#038;ssl=1" alt="" data-recalc-dims="1" /> 

【数据范围】

对于 <span class="katex"><span class="katex-mathml">30\%</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">3</span><span class="mord"></span><span class="mord">%</span></span></span></span> 的数据，有 <span class="katex"><span class="katex-mathml">n \le 2</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord mathnormal">n</span><span class="mrel">≤</span></span><span class="base"><span class="mord">2</span></span></span></span>。  
对于 <span class="katex"><span class="katex-mathml">50\%</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">5</span><span class="mord"></span><span class="mord">%</span></span></span></span> 的数据，<span class="katex"><span class="katex-mathml">0 \le a, b, g, k \le 100</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord"></span><span class="mrel">≤</span></span><span class="base"><span class="mord mathnormal">a</span><span class="mpunct">,</span><span class="mord mathnormal">b</span><span class="mpunct">,</span><span class="mord mathnormal">g</span><span class="mpunct">,</span><span class="mord mathnormal">k</span><span class="mrel">≤</span></span><span class="base"><span class="mord">1</span><span class="mord"></span><span class="mord"></span></span></span></span>。  
对于 <span class="katex"><span class="katex-mathml">100\%</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span><span class="mord"></span><span class="mord"></span><span class="mord">%</span></span></span></span> 的数据，有 <span class="katex"><span class="katex-mathml">0 \le n \le 10^4</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord"></span><span class="mrel">≤</span></span><span class="base"><span class="mord mathnormal">n</span><span class="mrel">≤</span></span><span class="base"><span class="mord">1</span><span class="mord"><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist"><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">4</span></span></span></span></span></span></span></span></span></span>, <span class="katex"><span class="katex-mathml">0 \le a, b, g, k \le {10}^5</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord"></span><span class="mrel">≤</span></span><span class="base"><span class="mord mathnormal">a</span><span class="mpunct">,</span><span class="mord mathnormal">b</span><span class="mpunct">,</span><span class="mord mathnormal">g</span><span class="mpunct">,</span><span class="mord mathnormal">k</span><span class="mrel">≤</span></span><span class="base"><span class="mord">10<span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist"><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">5</span></span></span></span></span></span></span></span></span></span>。

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct tanzi {
    int a, b, g, k;
};
int main() {
    int n;
    cin &gt;&gt; n;
    int i,x,y;
    tanzi m[10001];
    
    for (i = 1; i &lt;= n; i++) {
        cin &gt;&gt; m[i].a &gt;&gt; m[i].b &gt;&gt; m[i].g &gt;&gt; m[i].k;
    }
    cin &gt;&gt; x &gt;&gt; y;
    for (i = n; i &gt;0; i--) {
        if (x &gt;= m[i].a && x &lt;= m[i].a + m[i].g && y &gt;= m[i].b && y &lt;= m[i].b + m[i].k) {
            cout &lt;&lt; i;
            break;
        }
    }
    if (i == 0)cout &lt;&lt; "-1";
}</pre>

&nbsp;

noip2011 提高组 day1 第 <span class="katex"><span class="katex-mathml">1</span><span class="katex-html" aria-hidden="true"><span class="base"><span class="mord">1</span></span></span></span> 题。</div>
