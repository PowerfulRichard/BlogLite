# 结构体输入与输出

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    编写两个函数input和print，分别用来输入5个学生的数据记录和打印这5个学生的记录。对于每一个学生，其记录包含了学号、名字、3门课程的成绩共5项。用主函数分别调用input和print函数进行输入和输出。<br /> 要求使用结构体数组实现，结构体中包括了每个学生的5项记录。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    共有5行，每行包含了一个学生的学号（整数）、名字（长度不超过19的无空格字符串）和3门课程的成绩（0至100之间的整数），用空格隔开。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    与输入格式相同，每行输出一个学生的所有记录。<br /> 请注意行尾输出换行。
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
    while (cin &gt;&gt; info.num &gt;&gt; info.name &gt;&gt; info.g1 &gt;&gt; info.g2 &gt;&gt; info.g3) {
        cout &lt;&lt; info.num &lt;&lt; " " &lt;&lt; info.name &lt;&lt; " " &lt;&lt; info.g1 &lt;&lt; " " &lt;&lt; info.g2 &lt;&lt; " " &lt;&lt; info.g3 &lt;&lt; endl;
    }
    return 0;
}</pre>

&nbsp;
