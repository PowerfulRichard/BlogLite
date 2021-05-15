# 考试排名

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">C++编程考试使用的实时提交系统，具有即时获得成绩排名的特点。它的功能是怎么实现的呢？<br /> 我们做好了题目的解答，提交之后，要么“AC”，要么错误，不管怎样错法，总是给你记上一笔，表明你曾经有过一次错误提交，因而当你一旦提交该题 “AC”后，就要与你算一算帐了，总共该题错误提交了几回。虽然你在题数上，大步地跃上了一个台阶，但是在耗时上要摊上你共花去的时间。特别是，曾经有过 的错误提交，每次都要摊上一定的单位时间分。这样一来，你在做出的题数上，可能领先别人很多，但是，在做出同样题数的人群中，你可能会在耗时上处于排名的 劣势。<br /> 例如：某次考试一共8题（A，B，C，D，E，F，G，H），每个人做的题都在对应的题号下有个数量标记，负数表示该学生在该题上有过的错误提交 次数，但到现在还没有AC，正数表示AC所耗的时间，如果正数a跟上一对括号，里面有个整数b，那就表示该学生提交该题AC了，耗去了时间a，同时，曾经 错误提交了b次，因此对于下述输入数据：<br /> name A B C D E F G H<br /> Smith -1 -16 8 0 0 120 39 0<br /> John 116 -2 11 0 0 82 55(1) 0<br /> Jose 72(3) 126 10 -3 0 47 21(2) -2<br /> Bush 0 -1 -8 0 0 0 0 0<br /> Alice -2 67(2) 13 -1 0 133 79(1) -1<br /> Bob 0 0 57(5) 0 0 168 -7 0<br /> 若每次错误提交的罚分为20分，则其排名从高到低应该是这样的：<br /> Jose 5 376<br /> John 4 284<br /> Alice 4 352<br /> Smith 3 167<br /> Bob 2 325<br /> Bush 0 0</span>
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">输入数据的第一行是考试题数n（1≤n≤12）以及单位罚分数 m（10≤m≤20），每行数据描述一个学生的用户名（不多于10个字符的字串）以及对所有n道题的答题现状，其描述采用问题描述中的数量标记的格式，见 上面的表格，提交次数总是小于100，AC所耗时间总是小于1000。</span>
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    <span style="font-family: Times New Roman; font-size: medium;">将这些学生的考试现状，输出一个实时排名。实时排名显然先按AC题数的多 少排，多的在前，再按时间分的多少排，少的在前，如果凑巧前两者都相等，则按名字的字典序排，小的在前。每个学生占一行，输出名字（10个字符宽），做出 的题数（2个字符宽，右对齐）和时间分（4个字符宽，右对齐）。名字、题数和时间分相互之间有一个空格。</span>
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int cnt, litter;
//cnt为需要计算的题数，litter为惩罚时间
struct pupil {
    string name;
    int ac_t;
    //ac的题目数量
    int time;
    //题目的时间
}
tmp;
int total_ac = 0, total_time = 0;
struct rule {
    bool operator()(const pupil& s1, const pupil& s2) {
        if (s1.ac_t != s2.ac_t) {
            return s1.ac_t &gt; s2.ac_t;
        }
        else if (s1.time != s2.time) {
            return s1.time &lt; s2.time;
        }
        else {
            return s1.name &lt; s2.name;
        }
    }
};
set &lt; pupil, rule &gt; s;
void process(string a) {
    stringstream ssp(a);
    int num;
    ssp &gt;&gt; num;
    if (num &gt; 0) {
        ++total_ac;
        int i = a.size() - 1;
        int cnt_n = 0;
        if (a[i] == ')') {
            --i;
            for (int p = 1; a[i] != '('; --i, p *= 10) {
                cnt_n += a[i] * p - '0';
            }
        }
        total_time += (cnt_n * litter + num);
    }
    return;
}
void input() {
    string st;
    while (getline(cin, st)) {
        if (st == "") {
            return;
        }
        stringstream ss(st);
        ss &gt;&gt; tmp.name;
        total_ac = 0;
        total_time = 0;
        for (int i = 1; i &lt;= cnt; ++i) {
            string a;
            ss &gt;&gt; a;
            process(a);
        }
        tmp.time = total_time;
        tmp.ac_t = total_ac;
        s.insert(tmp);
    }
    return;
}
void output() {
    set &lt; pupil, rule &gt;::iterator i = s.begin();
    for (; i != s.end(); ++i) {
        cout &lt;&lt; std::left &lt;&lt; setw(10) &lt;&lt; (*i).name &lt;&lt; " " &lt;&lt; std::right &lt;&lt; setw(2) &lt;&lt; (*i).ac_t &lt;&lt; " " &lt;&lt; std::right &lt;&lt; setw(4) &lt;&lt; (*i).time &lt;&lt; endl;
    }
    return;
}
int main() {
    string absorb;
    cin &gt;&gt; cnt &gt;&gt; litter;
    getline(cin, absorb);
    input();
    output();
    return 0;
}</pre>

&nbsp;
