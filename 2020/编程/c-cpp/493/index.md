# 谁拿了最多奖学金？

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    某校的惯例是在每学期的期末考试之后发放奖学金。发放的奖学金共有五种，获取的条件各自不同：
  </p>
  
  <p>
    1) 院士奖学金，每人8000元，期末平均成绩高于80分（>80），并且在本学期内发表1篇或1篇以上论文的学生均可获得；
  </p>
  
  <p>
    2) 五四奖学金，每人4000元，期末平均成绩高于85分（>85），并且班级评议成绩高于80分（>80）的学生均可获得；
  </p>
  
  <p>
    3) 成绩优秀奖，每人2000元，期末平均成绩高于90分（>90）的学生均可获得；
  </p>
  
  <p>
    4) 西部奖学金，每人1000元，期末平均成绩高于85分（>85）的西部省份学生均可获得；
  </p>
  
  <p>
    5) 班级贡献奖，每人850元，班级评议成绩高于80分（>80）的学生干部均可获得；
  </p>
  
  <p>
    只要符合条件就可以得奖，每项奖学金的获奖人数没有限制，每名学生也可以同时获得多项奖学金。例如姚林的期末平均成绩是87分，班级评议成绩82分，同时他还是一位学生干部，那么他可以同时获得五四奖学金和班级贡献奖，奖金总数是4850元。
  </p>
  
  <p>
    现在给出若干学生的相关数据，请计算哪些同学获得的奖金总数最高（假设总有同学能满足获得奖学金的条件）。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  输入的第一行是一个整数N（1 <= N <= 100），表示学生的总数。接下来的N行每行是一位学生的数据，从左向右依次是姓名，期末平均成绩，班级评议成绩，是否是学生干部，是否是西部省份学生，以及发表的论文数。姓名是由大小写英文字母组成的长度不超过20的字符串（不含空格）；期末平均成绩和班级评议成绩都是0到100之间的整数（包括0和100）；是否是学生干部和是否是西部省份学生分别用一个字符表示，Y表示是，N表示不是；发表的论文数是0到10的整数（包括0和10）。每两个相邻数据项之间用一个空格分隔。
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  输出包括三行，第一行是获得最多奖金的学生的姓名，第二行是这名学生获得的奖金总数。如果有两位或两位以上的学生获得的奖金最多，输出他们之中在输入文件中出现最早的学生的姓名。第三行是这N个学生获得的奖学金的总数。
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
struct people{
    char name[20],leader, western;
    short int end, comment, paper;
};
void input(people& c) {
    cin &gt;&gt; c.name &gt;&gt; c.end &gt;&gt; c.comment &gt;&gt; c.leader &gt;&gt; c.western &gt;&gt; c.paper;
}
int main() {
    short int n; people x, y; int all = 0, max=0, sch;
    cin &gt;&gt; n;
    while (n--) {
        input(x);
        sch = 0;
        if (x.end &gt; 80 && x.paper &gt; 0) {
            sch = 8000;
            all = all + 8000;
        }//院士
        if (x.end &gt; 85 && x.comment &gt; 80) {
            sch = sch + 4000;
            all = all + 4000;
        }//54
        if (x.end &gt; 90) {
            sch = sch + 2000;
            all = all +2000;
        }//优秀
        if (x.end &gt; 85 && x.western == 'Y') {
            sch = sch + 1000;
            all = all + 1000;
        }//西部
        if (x.comment &gt; 80 && x.leader == 'Y') {
            sch = sch + 850;
            all = all + 850;
        }//班干
        if (sch &gt; max) {
            max = sch;
            y = x;
        }
    }
    cout &lt;&lt; y.name &lt;&lt; endl &lt;&lt; max &lt;&lt; endl &lt;&lt; all;
    return 0;
}</pre>

&nbsp;
