# 结构体计算天数

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    定义一个包括年、月、日的结构体变量，读入年、月、日，计算该日在当年中是第几天。注意闰年问题。<br /> 请写一个函数days实现计算，将读入的结构体变量传递给days函数，计算后将答案返回给main函数进行输出。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    三个整数，分别表示年、月、日。保证输入是实际存在的日期，且年份在1000至3000之间（包含1000和3000）。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    输出该日期是一年中的第几天。<br /> 请注意行尾输出换行。
  </p>
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct date {
    int y, m, d;
    inline bool leap() {
        return y % 4 == 0 && y % 100 != 0 || y % 400 == 0;
    }
    inline int getMonthDay(int m) {
        if (m == 1 || m == 3 || m == 5 || m == 7 || m == 8 || m == 10 || m == 12)return 31;
        if (m == 4 || m == 6 || m == 9 || m == 11)return 30;
        if (leap())return 29;
        return 28;
    }
};
int days(date d) {
    int ret = d.d;
    for (int i = 1; i &lt; d.m; i++)
        ret += d.getMonthDay(i);
    return ret;
}
int main() {
    date d;
    cin &gt;&gt; d.y &gt;&gt; d.m &gt;&gt; d.d;
    cout &lt;&lt; days(d) &lt;&lt; endl;
    return 0;
}</pre>

&nbsp;
