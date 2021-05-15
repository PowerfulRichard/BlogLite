# 电子表A+B

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    A+B非常经典，同学们也非常喜欢，这不老师也给大家出一个A+B的问题：设电子表格式为24小时制的 HH:MM:SS
  </p>
  
  <p>
    输入一个电子表上的时间A,经过时间B后，电子表上显示的时间是多少呢？
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    多组输入
  </p>
  
  <p>
    每一行为一组测试数据包含六个整数 表示两个时间数据A B格式为时分秒
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  每组数据输出A时刻开始B时间段后所对应的时间
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct times{
    int h, m, s,hh,mm,ss;
};
void input(times& c) {
    cin &gt;&gt;c.m &gt;&gt; c.s &gt;&gt; c.hh &gt;&gt; c.mm &gt;&gt; c.ss;
}
int main() {
    times x;
    int h,a,b,c;
    while (cin &gt;&gt; h) {
        input(x);
        a = h + x.hh; b = x.m + x.mm; c = x.s + x.ss;
        while (c &gt;= 60) { b = b + 1; c = c - 60; }
        while (b &gt;= 60) { a = a + 1; b = b - 60; }
        while (a &gt;=24) { a = a - 24; }
        printf("%02d:%02d:%02d\n", a, b, c);
    }
    return 0;
}</pre>

&nbsp;
