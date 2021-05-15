# 给老师发工资

## 题目描述 {.page-header.text-muted}

<div class="content">
  <p>
    作为安科大的老师，最盼望的日子就是每月的9号了，因为这一天是发工资的日子，养家糊口就靠它了，呵呵<br /> 但是对于学校财务处的工作人员来说，这一天则是很忙碌的一天，财务处的小胡老师最近就在考虑一个问题：如果每个老师的工资额都知道，最少需要准备多少张人民币，才能在给每位老师发工资的时候都不用老师找零呢？<br /> 这里假设老师的工资都是正整数，单位元，人民币一共有100元、50元、20元、10元、5元、2元和1元七种。
  </p>
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  <p>
    输入数据包含多个测试实例，每个测试实例的第一行是一个整数n（n<100），表示老师的人数，然后是n个老师的工资。<br /> n=0表示输入的结束，不做处理。
  </p>
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  <p>
    对于每个测试实例输出一个整数x,表示至少需要准备的人民币张数。每个输出占一行。
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="cpp">#include&lt;bits/stdc++.h&gt;
using namespace std;
int main() {
        const int cur[7] = { 100,50,20,10,5,2,1 };
        int teacher[100];
        int num;
        while (cin &gt;&gt; num)
        {
            if (num != 0)
            {
                int sum = 0;
                for (int i = 0; i &lt; num; i++)
                    cin &gt;&gt; teacher[i];
                for (int j = 0; j &lt; num; j++)
                {
                    for (int k = 0; k &lt; 7; k++)
                    {
                        sum += teacher[j] / cur[k];
                        teacher[j] %= cur[k];
                    }
                }
                cout &lt;&lt; sum &lt;&lt; endl;
            }
            else
                break;
        }
    }</pre>
  
  <p>
    &nbsp;
  </p>
</div>
