# 结义兄弟

## 题目描述 {.page-header.text-muted}

<div class="content">
  现在有一群同学都想结成异姓兄弟，规定按照年龄大小来从大到小排序。你来搜集这些同学的信息：姓名和对应的出生年月日。且他们不存在同年同月同日生的情况，你来帮助他们排个序。
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入第一行有一个整数N(0< N < 1000)表示N个同学。<br /> 接下来有N行，且每行都有一个字符串（全为小写字母且长度小于30)和3个整数 ，分别表示姓名、年、月、日。<br /> 所有同学的年龄均为1900年以后的。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  请按从大到小的顺序输出所有同学的姓名。<br /> 假设不存在同年同月同日生的同学。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct Person {
    char name[100];
    int y, m, d;
};
const int maxn = 1000 + 10;
Person p[maxn];
int n;
bool cmp(Person a, Person b) {
    if (a.y != b.y)return a.y &lt; b.y;
    if (a.m != b.m)return a.m &lt; b.m;
    return a.d &lt; b.d;
}
int main() {
    cin &gt;&gt; n;
    for (int i = 0; i &lt; n; i++)cin &gt;&gt; p[i].name &gt;&gt; p[i].y &gt;&gt; p[i].m &gt;&gt; p[i].d;
    sort(p, p + n, cmp);
    for (int i = 0; i &lt; n; i++)cout &lt;&lt; p[i].name &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
