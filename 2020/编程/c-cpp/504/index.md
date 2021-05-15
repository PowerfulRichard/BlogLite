# 精挑细选

## 题目描述 {.page-header.text-muted}

<div class="content">
  小王是公司的仓库管理员，一天，他接到了这样一个任务：从仓库中找出一根钢管。这听起来不算什么，但是这根钢管的要求可真是让他犯难了，要求如下： 1、 这根钢管一定要是仓库中最长的； 2、 这根钢管一定要是最长的钢管中最细的； 3、 这根钢管一定要是符合前两条的钢管中编码最大的（每根钢管都有一个互不相同的编码，越大表示生产日期越近）。 相关的资料到是有，可是，手工从几百份钢管材料中选出符合要求的那根…… 要不，还是请你编写个程序来帮他解决这个问题吧。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行是一个整数N(N<=10)表示测试数据的组数） 每组测试数据的第一行 有一个整数m(m<=1000)，表示仓库中所有钢管的数量， 之后m行，每行三个整数，分别表示一根钢管的长度（以毫米为单位）、直径（以毫米为单位）和编码（一个9位整数）。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  对应每组测试数据的输出只有一个9位整数，表示选出的那根钢管的编码， 每个输出占一行
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct Pipe {
    int length, diameter, number;
};
void input(Pipe& p) {
    cin &gt;&gt; p.length &gt;&gt; p.diameter &gt;&gt; p.number;
}
Pipe pipes[1000];
int n;
bool cmp(Pipe a, Pipe b) {
    if (a.length != b.length)return a.length &gt; b.length;
    if (a.diameter != b.diameter)return a.diameter &lt; b.diameter;
    return a.number &gt; b.number;
}
int main() {
    int T;
    cin &gt;&gt; T;
    while (T--) {
        cin &gt;&gt; n;
        for (int i = 0; i &lt; n; ++i)input(pipes[i]);
        sort(pipes, pipes + n, cmp);
        cout &lt;&lt; pipes[0].number &lt;&lt; endl;
    }
    return 0;
}
</pre>

&nbsp;
