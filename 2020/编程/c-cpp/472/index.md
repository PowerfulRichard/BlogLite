# 结构体计算学生成绩平均值

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    有10个学生，每个学生的数据包括学号、姓名、3门课程的成绩。读入这10个学生的数据，要求输出3门课程的总平均成绩，以及个人平均分最高的学生的数据（包括学号、姓名、3门课程成绩、平均分数）。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    共有10行，每行包含了一个学生的学号（整数）、名字（长度不超过19的无空格字符串）和3门课程的成绩（0至100之间的整数），用空格隔开。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    第一行包含了3个实数，分别表示3门课程的总平均成绩，保留2位小数，每个数之后输出一个空格。<br /> 第二行输出个人平均分最高的学生的数据，与输入数据格式相同。如果有多位个人平均分最高的学生，输出按照输入顺序第一个最高分的学生数据。<br /> 请注意行尾输出换行。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct {
    int num;
    string name;
    int g1;int g2; int g3;
}info;
int main() {
    double x1=0, x2=0, x3=0, p, q = 0;
    string j;
    int n = 10,i,k,l,m;
    while (n--){cin &gt;&gt; info.num &gt;&gt; info.name &gt;&gt; info.g1 &gt;&gt; info.g2 &gt;&gt; info.g3;
        x1 = x1 + info.g1; x2 = x2 + info.g2; x3 = x3 + info.g3;
        p = info.g1 + info.g2 + info.g3;
        if (p &gt; q) {
            q = p;
            i = info.num; j = info.name; k = info.g1; l = info.g2; m = info.g3;
        }
        }
    cout &lt;&lt; fixed &lt;&lt; setprecision(2) &lt;&lt; (x1 / 10)&lt;&lt;" " &lt;&lt; (x2 / 10)&lt;&lt;" " &lt;&lt; (x3 / 10) &lt;&lt; endl;
    cout &lt;&lt; i&lt;&lt;" "&lt;&lt;j&lt;&lt;" "&lt;&lt;k&lt;&lt;" "&lt;&lt;l&lt;&lt;" "&lt;&lt;m&lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
