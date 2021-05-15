# 分！分！分! 学生的命根

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    大家都知道，考研包括初试和复试，院校根据初试成绩和复试成绩综合决定是否录取你，具体的计算总成绩的方案是(初试总成绩)*0.6+(复试成绩)*0.4.这不Pmathticol还没玩够，又要开始准备万恶的复试了。不仅如此，对各科也还都有要求，所以院校会划定各科成绩线要求以及总分要求，只有过了各个单科分数线且总分足够才有资格进入复试。另外若是复试分数(满分为100分)不及格，则也不被录取。假定录取名额没有限制，只要符合上述条件的就被录取。我们知道初试科目包括数学，英语，政治，专业课。给定n个同学的各科成绩和复试成绩(假设每位同学都有复试成绩)，以及报考院校的各个单科分数线和总分线。要你求最后被录取的名单以及他们的相关信息。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    只有一组测试数据，<br /> 第一行是报考院校的单科要求(英语，政治，数学，专业)和总分要求<br /> 接下来包括n名同学(10<=n<=200),每行的格式如下：<br /> 姓名 英语 政治 数学 专业 复试成绩
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出被录取的同学信息(姓名 初试成绩 复试成绩 总成绩 复试序号)，并按照最终成绩从高到低排序。成绩相同的，按照名字字母顺序先后排序。所有的数据都用double型输入，最后结果初试和复试成绩四舍五入为整数输出，总成绩保留1位小数。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct stu {
    string s;
    double a, b, c, d, e, f, g;
}k[50];
bool q(stu A, stu B) {
    if (A.g != B.g) {
        return A.g &gt; B.g;
    }
    else {
        return A.s &lt; A.s;
    }
}
int x, y, z, r, p, j, i = 0, t = 1;
int main() {
    for (cin &gt;&gt; x &gt;&gt; y &gt;&gt; z &gt;&gt; r &gt;&gt; p; cin &gt;&gt; k[i].s &gt;&gt; k[i].a &gt;&gt; k[i].b &gt;&gt; k[i].c &gt;&gt; k[i].d &gt;&gt; k[i].e;)
    {
        k[i].f = k[i].a + k[i].b + k[i].c + k[i].d, k[i].g = k[i].f * 0.6 + k[i].e * 0.4;
        if (k[i].a &gt;= x && k[i].b &gt;= y && k[i].c &gt;= z && k[i].d &gt;= r && k[i].f &gt;= p)i++;
        sort(k, k + i, q);
    }
    for (j = 0; j &lt; i; j++)
        cout &lt;&lt; k[j].s.c_str() &lt;&lt; fixed &lt;&lt; setprecision(0) &lt;&lt; " " &lt;&lt; setprecision(0) &lt;&lt; k[j].f &lt;&lt; " " &lt;&lt; setprecision(0) &lt;&lt; k[j].e &lt;&lt; " " &lt;&lt; setprecision(1) &lt;&lt; k[j].g &lt;&lt; " " &lt;&lt; t++ &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
