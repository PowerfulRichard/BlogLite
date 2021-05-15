# 选择排序（蓝桥杯）

## 题目描述 {.page-header.text-muted}

<div class="content">
  排序，顾名思义，是将若干个元素按其大小关系排出一个顺序。形式化描述如下：有n个元素a[1]，a[2]，…，a[n]，从小到大排序就是将它们排成一个新顺序a[i[1]]< a[i[2]]< …< a[i[n]]<br /> i[k]为这个新顺序。<br /> 选择排序的思想极其简单，每一步都把一个最小元素放到前面，如果有多个相等的最小元素，选择排位较考前的放到当前头部。还是那个例子：{3  1  5  4  2}：<br /> 第一步将1放到开头（第一个位置），也就是交换3和1，即swap(a[0],a[1])得到{1  3  5  4  2}<br /> 第二步将2放到第二个位置，也就是交换3和2，即swap(a[1],a[4])得到{1  2  5  4  3}<br /> 第三步将3放到第三个位置，也就是交换5和3，即swap(a[2],a[4])得到{1  2  3  4  5}<br /> 第四步将4放到第四个位置，也就是交换4和4，即swap(a[3],a[3])得到{1  2  3  4  5}<br /> 第五步将5放到第五个位置，也就是交换5和5，即swap(a[4],a[4])得到{1  2  3  4  5}<br /> 输入n个整数，输出选择排序的全过程。<br /> 要求使用递归实现
</div>

## 输入 {.page-header.text-muted}

<div class="content">
  第一行一个正整数n，表示元素个数<br /> 第二行为n个整数，以空格隔开
</div>

## 输出 {.page-header.text-muted}

<div class="content">
  共n行，每行输出第n步选择时交换哪两个位置的下标，以及交换得到的序列，格式:<br /> swap(a[i],a[j]):a[0]  …  a[n-1]<br /> i和j为所交换元素的下标，下标从0开始，最初元素顺序按输入顺序。另外请保证i< =j<br /> a[0]…a[n-1]为交换后的序列，元素间以一个空格隔开
</div>

<pre class="EnlighterJSRAW" data-enlighter-language="generic">#include&lt;bits/stdc++.h&gt;
using namespace std;
int n;
void sorts(int* a, int b)
{
    if (b == n)
        return;
    int min = a[b];
    int t = b;
    for (int i = b + 1; i &lt; n; ++i)
    {
        if (min &gt; a[i])
        {
            min = a[i];
            t = i;
        }
    }
    int x = a[b];
    a[b] = a[t];
    a[t] = x;
    printf("swap(a[%d], a[%d]):%d", b, t, a[0]);
    for (int i = 1; i &lt; n; ++i)
        printf(" %d", a[i]);
    printf("\n");
    sorts(a, b + 1);
}

int main()
{
    int a[105] = { 0 };
    cin &gt;&gt; n;
    for(int i = 0; i &lt; n; ++i)cin &gt;&gt; a[i];
    sorts(a, 0);
    return 0;
}</pre>

&nbsp;
